# magic-tuner-update
## [Download Magic Tuner](https://play.google.com/store/apps/details?id=com.levv.gametuner&pcampaignid=web_share)

This repository contains update metadata and resources for **Magic Tuner**.  
It is used by the application to check the latest version and fetch update notes.

### Purpose
- Hosts update metadata  
- Stores version information for the in-app update checker  
- Provides public access to lightweight update resources  
- Keeps a clean changelog for each release  

### Notes
- This repository does **not** include the Magic Tuner application source code  
- Only update-related data is stored here
___________________________________________________________________________________
## Addon Modules (Experimental)

Magic Tuner includes an **Addon Module system** that allows power-users to extend or modify
runtime behavior using custom scripts.  
An Addon is packaged as a `.zip` file containing optional components such as:

- `install.sh` — installation routine executed by the user  
- `customize/*` — silent scripts automatically applied when Magic Tuner starts  
- `uninstall/uninstall.sh` — optional removal script  
- `info.sh` — metadata descriptor (ID, name, version, author, description)

### Auto-Run Behavior
When the application enters the foreground, Magic Tuner scans all installed addons and executes
their `customize` scripts (`global.sh`, `system.sh`, `secure.sh`, `props.sh`) in silent mode.
This enables persistent tweaks without user interaction.

### Purpose of the Addon System
- Provide modular, user-controlled extensions  
- Allow advanced system-level tuning via controlled scripts  
- Enable per-device or per-game customization  
- Maintain isolation from the core application logic  

Addon Modules are optional and targeted at advanced users who require deeper control of Android system parameters.
