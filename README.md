<h1 align="center">Magic Tuner</h1>

  ![magictuner](https://github.com/user-attachments/assets/1cc27f23-6f84-449c-99a6-afe218144339)

## <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Google_Play_Store_badge_EN.svg/120px-Google_Play_Store_badge_EN.svg.png" width="60"> [Download Magic Tuner](https://play.google.com/store/apps/details?id=com.levv.gametuner&pcampaignid=web_share)

## Magic Tuner Updates
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


## Game API
Game API in Magic Tuner enables the system-level Game Manager available on Android 10 and newer devices.  
When supported by the device, Game Manager can be activated to apply per-game performance profiles without affecting other apps.

Magic Tuner extends this capability by allowing custom control over:
- Rendering behavior  
- Target FPS  
- Downscaling level  

All changes are applied per game and do not modify global system settings.  
This approach ensures that users can freely adjust performance preferences without risk, without system instability, and without affecting non-gaming apps.


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


## Credits
- **Magic Tuner Lead Developer** – [Levv](https://www.youtube.com/c/BANGLEvV)  
- **Core Contributor** – [User Sabun](https://www.youtube.com/channel/UCHepqylvjYSUcoxwu75uCmg/join)  
- **Android API Documentation** – [Android Developers](https://developer.android.com)  
- **Root Environment Provider** – [Magisk (topjohnwu)](https://github.com/topjohnwu/Magisk)  
- **Shizuku Service Provider** – [RikkaApps / Shizuku](https://shizuku.rikka.app/)  


## License
Magic Tuner is proprietary software.  
All rights reserved © 2023 Levv.

Redistribution, modification, reverse engineering, or commercial use of this software — including its modules, scripts, assets, logic, or runtime components — is strictly prohibited without explicit written permission.

## Third-Party Attribution
Android API documentation © [Google](https://developer.android.com)  
Magisk root environment © [topjohnwu](https://github.com/topjohnwu/Magisk)  
Shizuku service © [RikkaApps](https://shizuku.rikka.app/)


**Note:** This project is closed-source. Documentation only.
