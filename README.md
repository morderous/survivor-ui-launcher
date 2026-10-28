# Azeroth SurvivorUI Launcher (beta)

> **The launcher is back in [morderous/survivor-ui](https://github.com/morderous/survivor-ui)**, its source in [`installer/`](https://github.com/morderous/survivor-ui/tree/main/installer). Download it from [Survivor UI's latest release](https://github.com/morderous/survivor-ui/releases/latest). This repository's last release, 1.6.1, takes the launchers that looked here (1.5.7 to 1.6.0) back there by themselves; nothing new comes here.

A launcher for [Azeroth Survivors](https://wow.aethus.pl), a game by Aethus; the launcher by morderous. It plays the game, keeps it current, and installs and updates [Survivor UI](https://github.com/morderous/survivor-ui) and Survivor Plates, its interface addons, and more addons from a list morderous checked. It also backs up your save, shows your statistics and keeps your Run History.

## Install

1. Download `SurvivorUI-Installer.zip` from this repository's [Releases](../../releases/latest), unzip it and open `SurvivorInstaller.exe`.
   Windows may say "Windows protected your PC" (the program is new and not signed): click "More info", then "Run anyway".
2. No game yet? Click **Get the game**. Have it already? The launcher finds it by itself, or click **Find game...** and pick `AzerothSurvivors.exe`.
3. In the **Addons** tab, Survivor UI is first (recommended): click **Install**, then **Play** in the Play tab.

It updates itself from this repository's releases: leave "Update the launcher by itself" ticked. Survivor UI's own updates still come from [morderous/survivor-ui](https://github.com/morderous/survivor-ui).

`README.txt`, in the zip, tells every tab and setting.

## Build

`build.bat` builds `SurvivorInstaller.exe` with the C# compiler that comes with Windows (.NET Framework 4.8). Nothing to download.

## Mirrors

`mirrors.json` lists the mirrors Get the game offers beside Aethus' own servers (name, url, size, sha256, and a login where one is asked). The launcher reads it from this repository as it gets the game, so a mirror is added or changed here without a new launcher; it uses the ones built in when the file is out of reach. A mirror's package is taken only with the size and sha256 Aethus gave.

## More addons

`addons.json` lists the addons the Addons tab offers under Survivor UI, the ones morderous checked: each one's name, author, repository, its release's zip (its name, or a pattern with `*` for a version in the name), the author's sha256 list where there is one, its folders and a few words. The launcher installs each from its author's own latest release (or a `tag` pinned there), only the addon's own folder and its kinds of files, never a program, never over Survivor UI's folders. An addon is added or changed here without a new launcher; the ones built in serve when the file is out of reach.

## Changes

### 1.6.1, 2026-10-28

- **Back in Survivor UI's repository**: it updates itself from [morderous/survivor-ui](https://github.com/morderous/survivor-ui)'s releases again, and reads its lists (`addons.json`, `mirrors.json`) from its `installer/` folder. Nothing else changes from 1.6.0.

### 1.6.0, 2026-10-28

- **The Addons tab**: Survivor UI and Survivor Plates first, recommended (the release, the beta, What's new, each on or off), the Survivor UI tab folded into it; then the addons from `addons.json` (ASBuilder, Azerloot, AZSSpellMeter, KeijinUI, SurvivorsDragonUi), each from its author's latest release, checked by its size and its author's sha256 where there is one; then the ones put in by hand.
- **Install, Update all, Uninstall, On or off**: only an addon's own folder and kinds of files come in; Uninstall sends it to the Recycle Bin, its settings kept. Installed, Not installed or Outdated in the list; an addon off greyed.
- **The game's AddOns folder** and Check folder and move if necessary on the Play tab.
- **Credits and feedback** under every tab: Azeroth Survivors by Aethus, the launcher by morderous, and Feedback on Discord.

### 1.5.8, 2026-10-28

- **Get the game from the mirrors too**: the game's package also comes from the mirrors the game's Discord gave (thanks to Meexa and Leo), beside Aethus' own servers. Each is timed first and offered in a list with its speed, the fastest picked; or a package you downloaded already (.rar).
- **Checked before it is used**: a mirror's package only with the size and sha256 Aethus gave.
- **A broken download goes on where it stopped**, on a source that allows it, up to five breaks.
- **Try another source**: while it downloads, the Play button goes on with the next source; and a source that would finish three times later than another, for ten seconds in a row, is left for it by itself.

### 1.5.7, 2026-10-28

- Updates itself from this repository's releases. Survivor UI's updates still come from morderous/survivor-ui. Nothing else changes from 1.5.6.

## What it touches

Only the SurvivorUI and SurvivorPlates folders inside the game's AddOns folder and the game's list of addons. It also touches your folders when you ask it to move them, the game's own files when it gets or updates the game for you, and your save and settings when you ask it to back them up or restore one. It reads your save and Survivor UI's settings for Statistics and Run History, and never writes them. Its own settings are in `%APPDATA%\SurvivorUIInstaller`.

## Credits

- Art: Wenrexa's ["UI RPG Game Interface"](https://wenrexa.itch.io/werdanta03), Creative Commons Zero, with thanks (`art/CREDITS.txt`).
- The title's font: Cinzel Decorative, under the SIL Open Font License (`OFL-CinzelDecorative.txt`).

## License

GPL-3.0 (`LICENSE`). Azeroth Survivors and its data are Aethus'; this launcher only gets them from his servers, with his ok.
