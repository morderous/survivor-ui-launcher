# Azeroth SurvivorUI Launcher (beta)

A launcher for [Azeroth Survivors](https://wow.aethus.pl), a game by Aethus. It plays the game, keeps it current, and installs and updates [Survivor UI](https://github.com/morderous/survivor-ui) and Survivor Plates, its interface addons. It also backs up your save, shows your statistics and keeps your Run History.

## Install

1. Download `SurvivorUI-Installer.zip` from this repository's [Releases](../../releases/latest), unzip it and open `SurvivorInstaller.exe`.
   Windows may say "Windows protected your PC" (the program is new and not signed): click "More info", then "Run anyway".
2. No game yet? Click **Get the game**. Have it already? The launcher finds it by itself, or click **Find game...** and pick `AzerothSurvivors.exe`.
3. In the **Survivor UI** tab, click the gold **Install** button, then **Play**.

It updates itself from this repository's releases: leave "Update the launcher by itself" ticked. Survivor UI's own updates still come from [morderous/survivor-ui](https://github.com/morderous/survivor-ui).

`README.txt`, in the zip, tells every tab and setting.

## Build

`build.bat` builds `SurvivorInstaller.exe` with the C# compiler that comes with Windows (.NET Framework 4.8). Nothing to download.

## What it touches

Only the SurvivorUI and SurvivorPlates folders inside the game's AddOns folder and the game's list of addons. It also touches your folders when you ask it to move them, the game's own files when it gets or updates the game for you, and your save and settings when you ask it to back them up or restore one. It reads your save and Survivor UI's settings for Statistics and Run History, and never writes them. Its own settings are in `%APPDATA%\SurvivorUIInstaller`.

## Credits

- Art: Wenrexa's ["UI RPG Game Interface"](https://wenrexa.itch.io/werdanta03), Creative Commons Zero, with thanks (`art/CREDITS.txt`).
- The title's font: Cinzel Decorative, under the SIL Open Font License (`OFL-CinzelDecorative.txt`).

## License

GPL-3.0 (`LICENSE`). Azeroth Survivors and its data are Aethus'; this launcher only gets them from his servers, with his ok.
