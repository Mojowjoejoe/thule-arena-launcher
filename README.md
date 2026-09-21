# Thule Arena launcher

[Download the launcher](https://github.com/Mojowjoejoe/thule-arena-launcher/releases/latest/download/ThuleArena-Launcher.zip)

Extract the complete ZIP, then run StartThuleArena.exe. Keep a shortcut to that file. It checks signed launcher updates on opening and preserves your settings. The game remains invite-only; downloading the launcher does not grant a game account.

This repository contains only signed update metadata. Executable downloads are stored in Releases. No game client, game-server source, database, account data or private signing keys are distributed here.

## Update feeds

- Launcher: https://raw.githubusercontent.com/Mojowjoejoe/thule-arena-launcher/main/launcher
- Game content: https://raw.githubusercontent.com/Mojowjoejoe/thule-arena-launcher/main/updates

## Release process

Build a new launcher version, upload its executable to a versioned GitHub Release, and sign the launcher manifest referencing that asset. Push the verified manifest.json and manifest.sig together to launcher/ on main. Players receive that signed release on their next launcher start. A source-code push alone is not a published update. Never commit private signing keys.

Launcher signatures and SHA-256 hashes are verified before execution. The installer preserves a previous working version for startup recovery. The executable is not Windows Authenticode signed.
