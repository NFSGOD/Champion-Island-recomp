# 🏮 Google Doodle Champion Island Games — Local Edition & Launcher

Play the complete **Google Doodle Champion Island Games** locally on your computer with offline asset serving, bug fixes, on-the-fly splash screen switching, a multi-save manager, and a native desktop launcher.

On 26 July 2021, Google released [the "Champion Island Games" Doodle](https://www.google.com/doodles/doodle-champion-island-games-july-26) celebrating the Tokyo Olympics, created in partnership with anime studio [STUDIO4°C](http://www.studio4c.co.jp/).

---

## ✨ Features & Enhancements

- **Standalone Native Launcher (`Google Doodle Champion Island.exe`)**:
  - Built-in lightweight HTTP server — **no Python or external runtimes required** on Windows.
  - Desktop control panel to launch either in your default browser or as a clean, borderless **standalone desktop app window** (`--app`).
  - **One-Click Stop Server**: Automatically terminates standalone game windows, cuts off sound, and closes active browser tabs with no lingering processes.
- **🎨 On-the-Fly Splash Screen Switcher**:
  - Switch between all **9 seasonal & sport opening screens** instantly from the top toolbar or launcher gallery:
    1. *Opening Ceremony* (Centered Play Button)
    2. *Archery — Yoichi*
    3. *Climbing — Fukuro*
    4. *Marathon — Kijimuna*
    5. *Rugby — The Oni*
    6. *Skateboarding — Tanuki*
    7. *Artistic Swimming — Princess Otohime*
    8. *Table Tennis — Tengu*
    9. *Closing Ceremony* (Festival Fireworks Finale)
  - Optional **"Randomize on Startup"** setting.
- **💾 Multiple Save Slots Manager**:
  - Create, load, overwrite, rename, export, and import multiple save profiles.
  - Inspect save stats at a glance (chosen team, Sacred Scrolls progress `0/7`–`7/7`, and trophy icons).
  - Includes a one-click **"100% Champion Slot"** preset to explore the island with all 7 Sacred Scrolls unlocked.
- **🔇 Audio Echo & Multi-Instance Protection**:
  - Fixed double-instantiation bugs and added a live multi-instance guard. If a new game tab or window is launched, older instances automatically pause their audio so you never get echoing sound.
- **⌨️ Fixed Controls & Custom Key Remapping**:
  - Keyboard focus issues resolved — `WASD`, Arrow keys, `Space`, `Enter`, `Z`, `Escape`, and `Backspace` work reliably without requiring manual canvas clicks.
  - Custom key remappings made in the in-game Controls menu persist across reloads.
- **🔤 Clean Fonts & Text Style Switching**:
  - Embedded local `PixelMplus10` retro pixel font (no external Google font dependency).
  - Toggle between **Retro Pixel** and **Modern Sans-Serif** in real time.
- **⚡ Instant Scene Warp**:
  - Warp directly to the Island Overworld, any of the 7 minigames, or the animated anime cutscenes.
- **🌐 Quick Links**:
  - Direct links to the official [Google Doodle Champion Island Games](https://doodles.google/doodle/doodle-champion-island-games-begin/) and archive pages.
  - Local scoreboard persistence (`scores.json` and `saves.json`).

---

## 🚀 How to Play

### Option 1: Native Windows Executable (Recommended — No Python Needed)
Double-click:
```text
Google Doodle Champion Island.exe
```
This opens the desktop launcher window where you can choose:
- **▶ Launch in Default Browser**: Opens the game in your favorite web browser (`http://localhost:8000`).
- **🖥️ Launch in Standalone App Window**: Opens the game in a borderless window like a native desktop app.
- **⏻ Stop Server & Exit**: Cleanly shuts down the server and closes all running game windows.

### Option 2: Batch Launcher (Python)
If you prefer running via Python:
1. Double-click `Google Doodle Champion Island.bat` or run:
   ```bash
   python run_server.py
   ```
2. Your default web browser will automatically open to `http://localhost:8000`.

---

## 🎮 Controls

| Action | Primary Keys | Secondary / Controller |
| :--- | :--- | :--- |
| **Move** | `W`, `A`, `S`, `D` | `Arrow Keys` / D-Pad |
| **Action / Confirm** | `Spacebar` / `Enter` | `Z` / Gamepad Button A |
| **Menu / Cancel** | `Escape` / `Backspace` | `X` / Gamepad Button B |
| **Open In-Game Launcher** | `F1` / Top Bar Button | — |

---

## 🛠️ Recompiling the Native Launcher (Optional)

The native executable is compiled using the Windows built-in C# compiler (`csc.exe`):
```powershell
& "C:\Windows\Microsoft.NET\Framework64\v4.0.30319\csc.exe" /nologo /target:winexe /optimize+ /out:"Google Doodle Champion Island.exe" /win32icon:"favicon.ico" /r:System.dll /r:System.Drawing.dll /r:System.Windows.Forms.dll /r:System.Management.dll "LauncherApp.cs"
```

---

## ⚖️ Credits & Copyright

- All game art, music, character designs, animations, and source code are owned and copyrighted by **[Google LLC](https://google.com)** and **[STUDIO4°C](http://www.studio4c.co.jp/)**.
- Original doodle preserved and made locally playable based on assets archived by [potherca-blog](https://github.com/potherca-blog).
