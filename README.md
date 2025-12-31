![ACRLauncher](https://github.com/user-attachments/assets/dd6469ec-30e1-4e86-ba09-492454094b7f)

# ACRLauncher v0.0.2.5

## 🛠️ Fixed argument validation error with error code 2 (file not found)

A custom-built, feature-rich standalone launcher designed for the Early Access version of **Assetto Corsa Rally**.  
This tool provides advanced configuration options, VR management, and troubleshooting utilities that are not available in the standard game launcher.

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

