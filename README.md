<p align="center">
  <img src="docs/images/banner.png" alt="NB Multiplayer" width="100%">
</p>

<p align="center">
  <b>Play <i>Banjo-Kazooie: Nuts &amp; Bolts</i> with your friends again: online, in co-op, and with mods.</b><br>
  One app that runs the game, connects you through Steam (no port forwarding, no accounts, no servers to rent) and
  manages your mods: the game's own Xbox LIVE races and sports, single-player Showdown Town together, a mod library
  with tick-box tweaks, and your NB Studio projects.
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

- [What it does](#what-it-does)
- [What you need](#what-you-need)
- [Install](#install)
- [First start](#first-start)
- [Hosting a room](#hosting-a-room)
- [Joining a room](#joining-a-room)
- [In the game](#in-the-game)
- [Showdown Town co-op (preview)](#showdown-town-co-op-preview)
- [Snowy Showdown Town](#snowy-showdown-town)
- [Mods, editions and tweaks](#mods-editions-and-tweaks)
- [Projects and NB Studio](#projects-and-nb-studio)
- [Updates](#updates)
- [Troubleshooting](#troubleshooting)
- [How it works](#how-it-works)
- [Building from source](#building-from-source)
- [Credits and legal](#credits-and-legal)

---

## What it does

| | |
|---|---|
| 🏁 **Online matches** | The game's own Xbox LIVE parties, races, sports and team games, up to 4 players. Friends land in the host's party automatically. |
| 🏘️ **Showdown Town co-op** *(preview)* | Play the single-player game together: see each other in town, build and change vehicles at the same time, and fight: weapon hits break parts off the other player's vehicle. |
| 🔧 **Mods & editions** | A mod library with categories (maps, vehicle parts, gameplay, visuals, sounds, tweaks, co-op) and tick-box tweaks such as *Unlimited parts* or *All parts unlocked*. Tick mods, build an edition, play it alone or host it. Mods that change the same world are combined asset by asset. Friends get missing mods from the host when they join. |
| 📁 **Your modded game** | Modded your game folder by hand in the past? **Add a modded game folder** turns it into a mod you can combine with others and play in co-op. |
| ❄️ **Snowy Showdown Town** | The first official map mod: Showdown Town under snow, with falling snow everywhere, holly and red-and-green bunting, and winter light and skies for every time of day. Combines with co-op. |
| ⚙️ **ULTRA Parts** | A bundled vehicle-parts mod: ULTRA Engine, Fuel, Ammo and Wheels, Plane Hull, Tiki and Fusion Reactor in Mumbo's Motors. |
| 🗂️ **Projects** | Your [NB Studio](https://github.com/weighta/NB-Studio-Banjo-Kazooie-Nuts-and-Bolts-World-Editor-) projects: NB Multiplayer installs and updates the editor, opens projects in it and turns them into mods. |
| 💾 **All-unlocked save** | Skip the intro: start every game with everything unlocked (your own save is kept aside). |
| 🌐 **Steam connection** | Rooms through Steam's relay network: share a room code, nothing to configure. Home network and direct internet work too. |
| ⬆️ **Updates** | NB Multiplayer updates itself from this repository's releases (it asks first). |

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
`xenia`, `patches` and `saves` folders belong together.

**3.** Run **`NBMultiplayer.exe`**. If Windows says *"Windows protected your PC"*, click **More info → Run anyway**
(the app is not code-signed). It offers to create a desktop shortcut.

## First start

The **Play** page tells you what's missing. Open **Settings**:

<p align="center"><img src="docs/images/02-app-settings.png" alt="Settings" width="85%"></p>

1. **Player name**: letters and digits, up to 15 characters. It becomes your in-game profile name.
2. **Game folder**: click **Browse...** and choose the folder that contains `default.xex` and `Bundle`.
   NB Multiplayer only reads it; it never changes your game files.
3. *(Optional)* **Start every game with the all-unlocked save**: no intro, every world, Act, vehicle and part unlocked
   (see [Showdown Town co-op](#showdown-town-co-op-preview)).

Your profile and saves are stored in `%LOCALAPPDATA%\NB-Multiplayer` (Settings → *Open data folder*), separate from any
other Xenia you use.

## Hosting a room

One player hosts; everyone else joins. On the **Play** page, first pick the **edition** to play (*Vanilla* or one you
built under [Mods & editions](#mods-editions-and-tweaks)); **Play solo** plays it on your own without a room.

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

**2.** NB Multiplayer connects (through Steam for `NBS-` codes), switches to the host's
[edition](#mods-editions-and-tweaks) (building it, and getting any mod you lack from the host, when you don't have it
yet), checks that your game files match the host's and starts the game. If something differs it tells you exactly what
(for example *"vehicle parts library: 2 files"*).

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
* **The same time of day for everyone**: the host picks *Random, Morning, Midday, Afternoon* or *Night* in the co-op
  room panel, and every player's Showdown Town loads with it (a change applies the next time the town loads).
* **ULTRA Parts**: **Add co-op + ULTRA Parts** adds the ULTRA Engine, Fuel, Ammo and Wheels, the Plane Hull, the Tiki and
  the Fusion Reactor to Mumbo's Motors for everyone in the room. Showdown Town itself stays as it is.

<p align="center"><img src="docs/images/16-coop-town.png" alt="Co-op in Showdown Town" width="100%"></p>
<p align="center"><i>The host's game: their own trolley (left) and the friend's trolley (right), moving wherever the friend drives in their own game.</i></p>

<p align="center">
  <img src="docs/images/22-coop-laser-hit.png" alt="Laser hit on the other player" width="49%">
  <img src="docs/images/23-coop-parts-off.png" alt="Parts broken off" width="49%">
</p>
<p align="center"><i>Fighting: a laser hit on the friend's trolley (left) is applied in the friend's own game, where parts of their vehicle break off (right).</i></p>

<p align="center">
  <img src="docs/images/21-coop-weapons.png" alt="Every weapon in Mumbo's Motors" width="49%">
  <img src="docs/images/20-coop-ultra-parts.png" alt="ULTRA engine in Mumbo's Motors" width="49%">
</p>
<p align="center"><i>Mumbo's Motors in the co-op edition: every part unlocked, including every weapon (left), and the ULTRA parts (right).</i></p>

**1.** **Mods & editions** → **Add co-op edition** (or **Add co-op + ULTRA Parts**). Friends who join get the same edition
automatically. (If you have the co-op edition of an older NB Multiplayer, the button says **Update co-op edition**.)

**2.** Host: on the **Play** page choose the edition **Showdown Town Co-op**, then **Start hosting** (Steam recommended).
Friends join with the room code as usual. The room panel lists everyone who is synced and how many players each game shows:

<p align="center"><img src="docs/images/17-coop-room.png" alt="Co-op room" width="85%"></p>

**3.** In the game: **SINGLE PLAYER** → load your save, or start a new game and play until you reach Showdown Town.
No save yet, or want everything unlocked? **Settings > Start every game with the all-unlocked save**: **RESUME SAVED GAME**
then goes straight to Showdown Town with every world, Act, vehicle and part unlocked (your own save is set aside and comes
back when you turn the option off).
As soon as two players are in town, each sees the other.

> **Preview limits:** players on foot are not shown yet (when someone gets out, their trolley waits where they left it), everyone appears in the standard trolley (not their own
> vehicle design), ramming and spikes only hurt in each player's own game (the bump itself happens in both), and crates, Acts and story progress are not shared yet.

## Snowy Showdown Town

<p align="center"><img src="docs/images/24-snowy-night.jpg" alt="Snowy Showdown Town at night" width="100%"></p>

**Snowy Showdown Town** ships with NB Multiplayer as an official mod (*Maps & worlds*). Tick it under
[Mods & editions](#mods-editions-and-tweaks) and build an edition, alone or together with **Showdown Town Co-op**,
**ULTRA Parts** and any tweaks:

* **Snow everywhere**: deep snow on the streets, squares and hills, snow-dusted cobbles and jigsaw paving with snow
  packed into the gaps, snow-covered roofs, frosted trees and benches.
* **Christmas**: red-and-green bunting across the streets, holly garlands with red berries on the walls, and a snowy
  painted backdrop in the theatre.
* **Falling snow** all over town: the snowfall follows the camera, so it snows wherever you drive or walk.
* **Winter light, fog and skies** for every time of day: a pale morning, a grey-white snowy midday, a lilac dusk and a
  starry blue night, with the far hills fading into winter mist.

<p align="center"><img src="docs/images/25-snowy-times-of-day.jpg" alt="Morning, midday, dusk and night" width="100%"></p>
<p align="center"><i>Mumbo's Motors in the morning, at midday, at dusk and at night.</i></p>

<p align="center"><img src="docs/images/26-snowy-before-after.jpg" alt="Original and snowy" width="100%"></p>
<p align="center"><img src="docs/images/31-snowy-before-after-night.jpg" alt="Original and snowy at night" width="100%"></p>
<p align="center"><i>The original town (left) and Snowy Showdown Town (right), at midday and at night.</i></p>

<p align="center">
  <img src="docs/images/27-snowy-vista.jpg" alt="Snowy rooftops and hills" width="49%">
  <img src="docs/images/30-snowy-clocktower-night.jpg" alt="The clock tower on a snowy night" width="49%">
</p>

<p align="center"><img src="docs/images/28-snowy-coop.jpg" alt="Snowy Showdown Town in co-op" width="85%"></p>
<p align="center"><i>Snowy Showdown Town + Co-op: the friend's trolley (ahead) drives through your snowy town.</i></p>

The mod was made the way many players mod: by changing a copy of the game folder by hand, then turning it into a mod
with **Add a modded game folder** / NB Studio's **Create Patch from a Modified Game Folder**. Its build script and the
research behind the snow, light and fog are in the
[NB Studio repository](https://github.com/weighta/NB-Studio-Banjo-Kazooie-Nuts-and-Bolts-World-Editor-) (`snow/`).

## Mods, editions and tweaks

**Mods** change the game: new maps, vehicle parts, gameplay, looks, and small **tweaks**. Every mod has a category
(*Maps & worlds, Vehicle parts, Gameplay & scripts, Textures & visuals, Sounds & music, Tweaks, Co-op & multiplayer*)
shown as a badge and used as a filter. An **edition** is your game with the mods you ticked, like a mod profile: tick
mods, press **Build an edition**, then host it or play it alone with **Play solo** on the Play page.

<p align="center"><img src="docs/images/13-app-editions.png" alt="Mods and editions" width="85%"></p>

<p align="center"><img src="docs/images/19-app-mods.png" alt="Mod library" width="85%"></p>
<p align="center"><i>The mod library: category filters, badges, built-in tweaks and the build bar for the ticked mods.</i></p>

* **Built-in tweaks**: the game-executable mods researched for NB Studio are tick boxes: *Unlimited parts (2000),
  Bigger world edge, No world-edge reset, Bigger garage, Longer draw distance, Change vehicles in town, Breakable town
  vehicles, Jumping AI vehicles, All parts unlocked, Developer main menu* and more. They combine with each other and
  with any mod.
* **Add a mod (.nbpatch)**: mods made with
  [NB Studio](https://github.com/weighta/NB-Studio-Banjo-Kazooie-Nuts-and-Bolts-World-Editor-) (or by friends) go into
  your mod library.
* **Add a modded game folder**: a game folder you changed by hand (replaced bundles or textures, a hex-edited
  `default.xex`) becomes a mod. NB Multiplayer compares it with the original game (it knows the size and SHA-256 of
  every original file), takes the differences against a clean copy (your game folder, or one you choose), recognises
  known executable tweaks by name and picks the category for you. If your game folder *is* the modded one, it offers
  to use the clean copy as your game folder from now on, so your changes become a mod you can tick, combine and share.

<p align="center"><img src="docs/images/29-app-modded-folder.png" alt="Add a modded game folder" width="85%"></p>
* **Change mods** on an edition ticks its mods so you can add or remove some and rebuild it.
* **Rooms share mods**: everyone in a room plays the host's edition. A friend who lacks one of its mods gets it from
  the host's room when they join (through Steam too) and NB Multiplayer builds the same edition for them.
* Editions are built next to NB Multiplayer; unchanged game files are linked, not copied, and your own game folder is
  never modified.
* **Mods combine asset by asset**: when two mods change the same game file, each mod's changed assets (textures,
  models, markers, scripts, vehicle parts) are taken from that mod. Only two mods changing the *same asset* differently
  is a conflict, and NB Multiplayer names it (for example *"Mod A" and "Mod B" both change
  aid_marker_banjox_showdowntown_main*). Tweaks always combine.
* **Co-op is a layer**: Showdown Town Co-op adds its puppet trolleys as world edits that are replayed on top of the
  other mods, so co-op works on any Showdown Town: vanilla, snowy, or your own.
* The Mods page shows the newest version of each mod; older versions stay available for editions that use them.
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
| Co-op: I can't see my friend in town | Both of you must play the co-op edition (the room panel shows *Co-op (2 players)*) and be in Showdown Town; players on foot are not shown yet, so get into a vehicle. |
| Co-op: pressing X warps instead of firing | You are on a warp pad or at a world door: drive off it first. |
| "These mods change the same things" | Two ticked mods change the same asset (the message names it), for example two mods that both edit the town's markers. Untick one of them. |
| A friend on NB Multiplayer 1.5 or older sees no puppets | Co-op 1.2 needs NB Multiplayer 1.6: everyone in the room should update (About & updates). |
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
* **Showdown Town co-op** runs each player's own single-player game. NB Multiplayer reads each player's vehicle 30 times
  a second and drives a stand-in vehicle (a "puppet" trolley of the co-op edition) to the same place in the other
  games. A small executable mod logs weapon hits on puppets instead of applying them; NB Multiplayer sends them to that
  player's game, where the game's own damage code applies them (so parts break off naturally).
* **Mods** are `.nbpatch` files: differences against the original game files, no game data. An edition applies a list
  of mods (its recipe) to a linked copy of your game; executable mods of several mods are merged into one `default.xex`.
  Files that several mods change are merged asset by asset first; mods can also carry **world edits** (instructions
  such as "copy this vehicle into the town" or "add this AI route"), replayed after every mod's files.
* **Modded folders** are compared with a list of the size and SHA-256 of every original game file (shipped with the
  app, no game data); the clean copy only provides the original bytes of the changed files.

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
