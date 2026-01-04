![ACRLauncher_CPU](https://github.com/user-attachments/assets/8ebc6447-0ec4-4502-81ad-162913dbcb27)

![ACRLauncher](https://github.com/user-attachments/assets/277342fc-2d60-46ab-b36e-c5c77c45b60d)

## What's New in v0.0.5.2

### 🧠 CPU Affinity (No-SMT)
Specific fix for Affinity block (Works perfectly if launched in ACRLauncher.exe executable).
In the **Play** tab, under Priority, a new checkbox appears: **"Affinity: Physical Cores Only"**.  
This disables HyperThreading for the game (uses only even-numbered cores: 0, 2, 4...) to reduce micro‑stuttering.

### 🔄 Save Backup & Restore
In the **Advanced** tab, there's now a panel to create `.zip` backups of your save files and restore them with a single click.

### 🚀 Game Booster
In the **Advanced** tab, you can enable the Booster.  
A text box lets you list processes to close automatically when launching the game (e.g., `chrome`, `teams`, `edge`).

### 📝 Configuration Editor
A **"Edit .INI"** button now opens the `GameUserSettings.ini` file directly in Notepad for quick manual tweaks.

### 🔍 Update Checker (Preparation)
On startup, the tool checks whether a newer version is available.  
It's currently pointed to a placeholder link, but the update-checking logic is fully implemented.

### 🧩 CPU Priority
- Fixed the incorrect functioning of the high priority of the acr.exe process.
- Now, in the list of active Windows processes, you will see the acr.exe process using high CPU priority.

### ✔️ Simplified Platform Menu
- Removed unnecessary options.
- The system now works in **Auto-Detect** mode.
- If the game is not found, a popup appears prompting the user to download it, automatically opening the browser.

---

### 🚀 Advanced Non-Blocking Scan
- Improved the **Find-Game** function.
- The search now covers many more standard paths:
  - Drives: `C:\`, `D:\`, `E:\`, `F:\`
  - Common Steam / Epic directories
- Added `[System.Windows.Forms.Application]::DoEvents()` to prevent the window from freezing or turning white during the scan.

---

### 📁 Corrected Paths
- Updated the configuration/cache path:

---

### 🧩 CPU Priority Crash Fix
- The crash (“process terminated”) occurred because:
- The initial launcher process often closes immediately to start the actual game.
- The launcher attempted to set CPU priority while the process was still initializing.
- Added a **HasExited** check and dedicated error handling to prevent the script from crashing.

---

## 🚀 Key Features

### 🎮 Game Management
- **Multi-Platform Support**  
  Automatically detects game installations on Steam and Epic Games.

- **Dynamic UI**  
  Automatically extracts and displays the official game icon inside the launcher.

- **Smart Process Check**  
  Prevents accidental double-launching by detecting if the game is already running.

---

### 👓 VR & Display Options
- **VR Selector**  
  Easily switch between:
  - Standard Monitor  
  - SteamVR (OpenVR)  
  - Oculus VR  
  …without manually editing command lines.

- **Video Flags**  
  - Force DirectX 11: `-dx11`  
  - Windowed Mode: `-windowed`

---

### ⚡ Performance & Tweaks
- **CPU Priority Boost**  
  Optional “High Priority” mode that forces Windows to prioritize the game process, reducing micro-stutters and input lag.

- **Custom Arguments**  
  Dedicated text field for advanced users to inject custom launch parameters.

---

### 🛠️ Troubleshooting & Maintenance
- **ReShade Manager**  
  One-click toggle to safely enable/disable ReShade by renaming `dxgi.dll` (no file deletion). Perfect for debugging crashes.

- **Panic Button (Cache Cleaner)**  
  Instantly wipes temporary configuration files (`.ini`) in `%LOCALAPPDATA%`.  
  Useful for fixing:
  - Fatal Errors  
  - Corrupted video settings  
  …without reinstalling the game.

---

### ⚙️ Quality of Life
- **Configuration Persistence**  
  Automatically saves all preferences (paths, VR mode, flags, language) to a JSON file.

- **Bilingual Support**  
  Real-time language switching between English and Italian.

- **Quick Links**  
  Direct buttons to open:
  - Game Logs folder  
  - Mods folder  
  - Official website

- **Auto-Close**  
  Option to automatically close the launcher once the game starts.

---

## 📥 How to Use
1. Download the executable.  
2. Place it anywhere on your PC (no installation required).  
3. Run the launcher.  
4. If the game is not detected automatically, use **Browse** to locate `acr.exe`.  
5. Click **START ENGINE**.

---

## 📝 Requirements
- Windows 10 / 11  
- .NET Framework 4.5+ (included in most Windows systems)  
- Assetto Corsa Rally (Early Access)
