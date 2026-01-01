![ACRLauncher](https://github.com/user-attachments/assets/dd6469ec-30e1-4e86-ba09-492454094b7f)

## 🛠️ Summary of Fixes and Improvements

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

- **Manual Path Selection**  
  Allows browsing and selecting `acr.exe` if installed in a custom location.

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


