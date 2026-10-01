# NB build of Xenia Canary netplay

NB Multiplayer runs the game in a modified build of
[AdrianCassar/xenia-canary](https://github.com/AdrianCassar/xenia-canary), branch `netplay_canary_experimental`,
commit `6dbaa1f` ("[XSession] Removed results buffer size check"). The changes are in
[`nb-xenia-netplay.patch`](nb-xenia-netplay.patch) (Xenia is BSD-licensed; the changes are released under the same
license).

## What the patch changes

| Area | Files | Change |
|---|---|---|
| NB room network | `kernel/nb_overlay.*`, `kernel/xsocket.*`, `kernel/XLiveAPI.cpp` | Every instance gets a virtual address `10.77.0.N` from the room server (`/whoami`, `X-NB-Instance` header); game UDP to virtual addresses is wrapped in a 24-byte header (source/destination address and port, session key) and sent through the room's relay. Several instances can share one PC. Cvars `nb_overlay`, `nb_instance`, `nb_relay`. |
| Security associations | `kernel/xam/xam_net.cc` | A console gives each (peer, session key) pair its own IN_ADDR; upstream returned one per peer. Nuts & Bolts keeps peers in the party lobby and the match session at once and dropped them when the two collided. Associations are now synthetic addresses `10.78.x.y`, and `XNetInAddrToXnAddr` returns the right key. |
| Room watch | `kernel/nb_overlay.cc`, `kernel/xsession.cc` | Polls the room server's `/nb/room`: befriends every player in the room, shows on-screen notices, and accepts the host's party invite when this player opens Xbox LIVE (cvars `nb_auto_join`, `nb_room_code`). Control port `nb_control_port` (`JOIN <xuid>`, `FRIEND <xuid>`, `PING`) for tools. |
| Heartbeat | `kernel/xam/user_tracker.cc` | With the NB network, one missed 10-second heartbeat (a PC busy loading a level) no longer drops the player from Xbox LIVE; three in a row do. |
| Profiles | `kernel/xam/profile_manager.*`, `emulator.cc` | `nb_create_profile=<name>`: creates a Live-enabled profile on first start and signs in the existing one later. |
| Virtual gamepad | `hid/nbremote/*`, `app/xenia_main.cc` | `nb_remote_input_port`: a UDP-driven gamepad used for automated testing (off by default). |
| Diagnostics | `kernel/xam/xam_msg.cc` | Logs the guest call chain of XSession create/delete/join/leave messages. |

## Building

1. Clone the netplay fork with submodules and check out the base commit:
   ```bash
   git clone --recursive https://github.com/AdrianCassar/xenia-canary.git -b netplay_canary_experimental
   cd xenia-canary
   git checkout 6dbaa1f
   git submodule update --init --recursive
   ```
2. Apply the patch: `git apply path/to/nb-xenia-netplay.patch`
3. Build as described in the fork's README (Windows: Visual Studio 2022, CMake, the Vulkan SDK), target `xenia-app`,
   Release configuration.
4. Ship `xenia_canary_netplay.exe` with the Visual C++ 2015-2022 x64 runtime DLLs, in the `xenia` folder next to
   `NBMultiplayer.exe`.
