<p align="center">
  <img src="docs/images/banner.png" alt="NB Multiplayer" width="100%">
</p>

<p align="center">
  <b>Play <i>Banjo-Kazooie: Nuts &amp; Bolts</i> online with your friends again.</b><br>
  The game's own Xbox LIVE multiplayer (parties, races, sports, team games) running in an emulator, connected
  through Steam: no port forwarding, no accounts, no servers to rent. Plus a mod library with tick-box tweaks,
  Showdown Town co-op, and your NB Studio projects in one place.
</p>

<p align="center">
  <a href="../../releases/latest"><img alt="Download" src="https://img.shields.io/badge/download-latest%20release-f5a623?style=for-the-badge"></a>
</p>

<p align="center">
  <img src="docs/images/12-game-same-race.png" alt="Two players in the same race" width="100%">
  <br><i>Two PCs, one race: the host (left) and a friend (right) in the same Jiggosseum Speedway match.</i>
</p>

---

## Contents

- [What you need](#what-you-need)
- [Install](#install)
- [First start](#first-start)
- [Hosting a room](#hosting-a-room)
- [Joining a room](#joining-a-room)
- [In the game](#in-the-game)
- [Showdown Town co-op (preview)](#showdown-town-co-op-preview)
- [Mods, editions and tweaks](#mods-editions-and-tweaks)
- [Projects and NB Studio](#projects-and-nb-studio)
- [Updates](#updates)
- [Troubleshooting](#troubleshooting)
- [How it works](#how-it-works)
- [Building from source](#building-from-source)
- [Credits and legal](#credits-and-legal)

---

## What you need

| | |
|---|---|
| 🎮 **The game** | Your own copy of *Banjo-Kazooie: Nuts & Bolts* (Xbox 360), **extracted to a folder**: the folder with `default.xex` and the `Bundle` folder. Everyone in a room must have the same version. |
| 💻 **A PC** | Windows 10 or 11 (64-bit) that runs the Xenia emulator (a DirectX 12 graphics card). |
| 🟦 **Steam** | Running and logged in, for the recommended "through Steam" connection. Any free Steam account works; you don't need to be Steam friends. |
| 🕹️ **A controller** | Xbox controllers work as they are; PlayStation 4/5 controllers work too (see [Troubleshooting](#troubleshooting)). |

Up to 4 players per room.

## Install

**1.** Download **`NB-Multiplayer-x.y.z.zip`** from the [latest release](../../releases/latest).

**2.** Right-click the zip → **Properties** → tick **Unblock** → **OK**, then extract it anywhere
(for example `Documents\NB-Multiplayer`). Keep the folder together: `NBMultiplayer.exe`, `steam_api64.dll` and the
`xenia` folder belong together.

**3.** Run **`NBMultiplayer.exe`**. If Windows says *"Windows protected your PC"*, click **More info → Run anyway**
(the app is not code-signed). It offers to create a desktop shortcut.

## First start

The **Play** page tells you what's missing. Open **Settings**:

<p align="center"><img src="docs/images/02-app-settings.png" alt="Settings" width="85%"></p>

1. **Player name**: letters and digits, up to 15 characters. It becomes your in-game profile name.
2. **Game folder**: click **Browse...** and choose the folder that contains `default.xex` and `Bundle`.
   NB Multiplayer only reads it; it never changes your game files.

Your profile and saves are stored in `%LOCALAPPDATA%\NB-Multiplayer` (Settings → *Open data folder*), separate from any
other Xenia you use.

## Hosting a room

One player hosts; everyone else joins. On the **Play** page:

<p align="center"><img src="docs/images/01-app-play.png" alt="Play page" width="85%"></p>

**1.** Under *Where are your friends?* choose:

| Option | When | Setup |
|---|---|---|
| **Anywhere, through Steam** *(recommended)* | Friends anywhere in the world | Nothing: Steam's relay network connects you. Steam must be running on every PC. |
| **On my home network** | Everyone on the same Wi-Fi/LAN | Nothing. |
| **Over the internet** | Without Steam | Forward **TCP 36000** and **UDP 36001** in your router to your PC, and allow NB Multiplayer through your firewall. *Test from the internet* checks it. |

**2.** Click **Start hosting**. NB Multiplayer checks your game files (the first time takes a few minutes), opens the
room and shows the **room code**, already copied to your clipboard:

<p align="center"><img src="docs/images/03-app-hosting.png" alt="Hosting" width="85%"></p>

**3.** Send the room code to your friends (Discord, Steam chat...). The game starts by itself; the *room* panel at the
bottom lists everyone who connects.

> Keep NB Multiplayer open while you play: it runs the room. *Close room* ends it.

## Joining a room

**1.** Paste the room code into **Room code or address** and click **Join**.

<p align="center"><img src="docs/images/04-app-joining.png" alt="Joining" width="85%"></p>

**2.** NB Multiplayer connects (through Steam for `NBS-` codes), checks that your game files match the host's, switches
to the host's [edition](#editions-and-mods) if you have it, and starts the game. If something differs it tells you
exactly what (for example *"vehicle parts library: 2 files"*).

## In the game

**1.** At the house menu go right to **MULTIPLAYER** and choose **Xbox LIVE**.

<p align="center"><img src="docs/images/05-game-multiplayer.png" alt="Multiplayer menu" width="75%"></p>

**2.** The very first time, the game asks *"Save game doesn't exist, start a new game?"*: choose **Yes**. You go straight
to the Xbox LIVE lobby.

<p align="center"><img src="docs/images/06-game-new-save.png" alt="New save prompt" width="75%"></p>

**3.** **Host:** set **MATCH CHOICE** to **"Play a game with my party"**. Friends who open Xbox LIVE are added to your
party automatically, within a few seconds. A notice appears on screen: *"Joining ...'s party"*.

<p align="center">
  <img src="docs/images/07-game-party-host.png" alt="Host party" width="49%">
  <img src="docs/images/08-game-party-friend.png" alt="Friend party" width="49%">
</p>
<p align="center"><i>The same party seen by the host (left) and the friend (right). Only the host can start.</i></p>

> ⚠️ Don't press **B** on the party screen: it means *Leave party*.

**4.** **Host:** under **CHOSEN GAME** pick a race or a sport (**RB** switches between races and sports), then **START**
and confirm.

<p align="center">
  <img src="docs/images/09-game-pick-game.png" alt="Pick a game" width="49%">
  <img src="docs/images/10-game-start.png" alt="Start the match" width="49%">
</p>

**5.** Everyone loads into the match, picks a vehicle (or keeps the default) and plays.

<p align="center"><img src="docs/images/11-game-loading.png" alt="Vehicle choice" width="75%"></p>

## Showdown Town co-op (preview)

Play the **single-player game together**. Everyone plays their own save; NB Multiplayer shows the other players in your
Showdown Town as a trolley with Banjo at the wheel, steered 30 times a second to where they really are. You can bump into
each other, town vehicles break apart, and *Change Vehicle* / *Build Vehicle* work anywhere in town.

* **Every vehicle part is unlocked** in the co-op edition, whatever each player's save has: build endlessly in Mumbo's
  Motors, each player in their own garage, at the same time.
* **Fight each other**: weapon hits on the other player's trolley (lasers, egg guns, explosions) are sent to their game
  and applied there by the game itself, so their vehicle takes the damage and parts break off and fall into the street.
* **ULTRA Parts**: **Add co-op + ULTRA Parts** adds the ULTRA Engine, Fuel, Ammo and Wheels, the Plane Hull, the Tiki and
  the Fusion Reactor to Mumbo's Motors for everyone in the room. Showdown Town itself stays as it is.

<p align="center"><img src="docs/images/16-coop-town.png" alt="Co-op in Showdown Town" width="100%"></p>
<p align="center"><i>The host's game: their own trolley (left) and the friend's trolley (right), moving wherever the friend drives in their own game.</i></p>

**1.** **Mods & editions** → **Add co-op edition** (or **Add co-op + ULTRA Parts**). Friends who join get the same edition
automatically. (If you have the co-op edition of an older NB Multiplayer, the button says **Update co-op edition**.)

**2.** Host: on the **Play** page choose the edition **Showdown Town Co-op**, then **Start hosting** (Steam recommended).
Friends join with the room code as usual. The room panel lists everyone who is synced:

<p align="center"><img src="docs/images/17-coop-room.png" alt="Co-op room" width="85%"></p>

**3.** In the game: **SINGLE PLAYER** → load your save, or start a new game and play until you reach Showdown Town.
As soon as two players are in town, each sees the other.

> **Preview limits:** players on foot are not shown yet (when someone gets out, their trolley waits where they left it), everyone appears in the standard trolley (not their own
> vehicle design), ramming and spikes only hurt in each player's own game (the bump itself happens in both), and crates, Acts and story progress are not shared yet. Each player has their own time of day.

## Mods, editions and tweaks

**Mods** change the game: new maps, vehicle parts, gameplay, looks, and small **tweaks**. Every mod has a category
(*Maps & worlds, Vehicle parts, Gameplay & scripts, Textures & visuals, Sounds & music, Tweaks, Co-op & multiplayer*)
shown as a badge and used as a filter. An **edition** is your game with the mods you ticked, like a mod profile: tick
mods, press **Build an edition**, then host it or play it alone with **Play solo** on the Play page.

<p align="center"><img src="docs/images/13-app-editions.png" alt="Mods and editions" width="85%"></p>

* **Built-in tweaks**: the game-executable mods researched for NB Studio are tick boxes: *Unlimited parts (2000),
  Bigger world edge, No world-edge reset, Bigger garage, Longer draw distance, Change vehicles in town, Breakable town
  vehicles, Jumping AI vehicles, All parts unlocked, Developer main menu* and more. They combine with each other and
  with any mod.
* **Add a mod (.nbpatch)**: mods made with
  [NB Studio](https://github.com/weighta/NB-Studio-Banjo-Kazooie-Nuts-and-Bolts-World-Editor-) (or by friends) go into
  your mod library.
* **Change mods** on an edition ticks its mods so you can add or remove some and rebuild it.
* **Rooms share mods**: everyone in a room plays the host's edition. A friend who lacks one of its mods gets it from
  the host's room when they join (through Steam too) and NB Multiplayer builds the same edition for them.
* Editions are built next to NB Multiplayer; unchanged game files are linked, not copied, and your own game folder is
  never modified.
* **For now** mods can be combined when they change different game files (tweaks always combine). Mods that edit the
  same world, such as two Showdown Town overhauls, are shown as conflicting; merging them is planned.
* A **mod depot** (browse and download community mods, share your own) is in development.

## Projects and NB Studio

The **Projects** page lists your NB Studio projects (NB Studio adds every project you open). **Get NB Studio** downloads
the editor from GitHub and keeps it up to date; **Open in NB Studio** opens a project in it; **Play** runs the project
with its executable tweaks; **Make a mod** turns it into a mod for your library, with a name, version, category and
description, and saves the `.nbpatch` file to share in the project's `mods` folder. **New project** makes a copy of
your game for NB Studio to edit.

<p align="center"><img src="docs/images/18-app-projects.png" alt="Projects" width="85%"></p>

## Updates

NB Multiplayer checks this repository's releases when it starts (you can turn that off in Settings). When a new version
is out, a banner offers **Update now**, **What's new**, **Later** or **Skip this version**. Updating keeps your settings,
profile, saves and editions.

<p align="center"><img src="docs/images/15-update-banner.png" alt="Update banner" width="85%"></p>

<p align="center"><img src="docs/images/14-app-about.png" alt="About and updates" width="75%"></p>

## Troubleshooting

| Problem | Fix |
|---|---|
| *"Steam is not available"* | Start Steam and log in, then try again. Steam shows you as playing **"Spacewar"**: that's Valve's public test app that NB Multiplayer uses for its connections. |
| *"Could not reach the host through Steam"* | Check the code; the host's NB Multiplayer must be open with the room started, and Steam running on both PCs. |
| Friend can't join on *home network / internet* | Something blocks incoming connections on the host: Windows Firewall, Portmaster, or an antivirus firewall must allow **NBMultiplayer.exe**. For internet play the router must forward TCP 36000 and UDP 36001. The hosting page shows a warning when this PC refuses connections. |
| *"Your game files differ from the host's"* | Use the same game version and the same edition. The message lists which kind of files differ. |
| Friend stays in their own party | Make sure the host is already in the Xbox LIVE lobby; the friend can back out to the house menu and open Xbox LIVE again. |
| PlayStation controller acts twice / as two players | DS4Windows or Steam's PlayStation support is also active: close them, or enable *Hide DS4 Controller* in DS4Windows. |
| A player drops back to their own party while a match loads | Rare; start the match again. |
| Something else | Send `%LOCALAPPDATA%\NB-Multiplayer\data\xenia.log` and `steam.log` from both PCs with an [issue](../../issues). |

## How it works

```
 Friend's PC                                    Host's PC
 ┌──────────────────────────┐   Steam relay    ┌──────────────────────────────┐
 │ Xenia (NB build)         │  ◄────────────►  │ NB Multiplayer               │
 │  game's Xbox LIVE code   │  (or direct      │  room server  (TCP 36000)    │
 │      │ localhost         │   TCP/UDP)       │  game relay   (UDP 36001)    │
 │ NB Multiplayer (tunnel)  │                  │ Xenia (NB build) ─ the game  │
 └──────────────────────────┘                  └──────────────────────────────┘
```

* The game runs in an **NB build of Xenia Canary netplay** (by AdrianCassar), which emulates Xbox LIVE against a
  server. NB Multiplayer **is** that server: a small in-memory implementation of the Xenia web services API running on
  the host's PC (sessions, players, QoS, friends).
* **Game traffic** (the game's own peer-to-peer packets) goes through a relay on the host: every player gets a virtual
  address (`10.77.0.N`), and per-session security associations are emulated (`10.78.x.y`). Getting these right is what
  makes Nuts & Bolts parties and matches stay together (see [xenia/](xenia)).
* **Steam**: joiners run a local tunnel (`127.0.0.1:36000/36001`) that carries everything over a Steam Networking
  Sockets connection (Steam Datagram Relay) to the host's NB Multiplayer, so nobody opens ports.
* **Room codes**: `NB-...` codes contain the host's IP address and port, `NBS-...` codes the host's Steam ID; both end
  with a fingerprint of the host's game files (SHA-256 of `default.xex` and every bundle) so mismatches are caught early.
* **Party joining** is automatic: the NB Xenia build befriends everyone in the room and accepts the host's invite as
  soon as you open Xbox LIVE.

## Building from source

* **The app** (`NBMultiplayer.exe`) is built from `src/NB.Multiplayer` in the
  [NB Studio repository](https://github.com/weighta/NB-Studio-Banjo-Kazooie-Nuts-and-Bolts-World-Editor-)
  (it shares NB.Core, the room server and the patch code):
  `dotnet publish src/NB.Multiplayer -c Release -r win-x64 --self-contained -p:PublishSingleFile=true`.
* **The Xenia build**: apply [`xenia/nb-xenia-netplay.patch`](xenia/nb-xenia-netplay.patch) to
  AdrianCassar/xenia-canary `netplay_canary_experimental` at commit `6dbaa1f`; see [xenia/README.md](xenia/README.md).

## Credits and legal

* NB Multiplayer by **weighta**. MIT license ([LICENSE](LICENSE)).
* [Xenia](https://github.com/xenia-project/xenia) / [Xenia Canary](https://github.com/xenia-canary/xenia-canary) and
  the [netplay fork by AdrianCassar](https://github.com/AdrianCassar/xenia-canary) (BSD license, included as
  `xenia/LICENSE-xenia.txt` in the release).
* Steam networking through [Facepunch.Steamworks](https://github.com/Facepunch/Facepunch.Steamworks) (MIT) and Valve's
  Steamworks API (`steam_api64.dll`, redistributable).
* *Banjo-Kazooie: Nuts & Bolts* is © Microsoft and Rare. Unofficial fan project, not affiliated with or endorsed by them,
  Valve or the Xenia project. No game files are included; you need your own copy of the game.
