# 🟦 TeamsAlive v1.1

**Stay active. Stay seen. Stay sane.**

TeamsAlive is a lightweight, open-source utility designed for remote workers who need to step away from their desks without their status flipping to "Away." It works with **Microsoft Teams, Slack, Zoom,** and any other application that tracks your idle time.

---

## ✨ Why TeamsAlive?

* **Take a real break:** Step away to grab a coffee or clear your head before the next task without being "status-shamed."
* **Relentless work ethic:** Impress your boss with your unwavering availability, even when you're focusing on off-screen tasks.
* **Privacy First:** * 🛡️ **100% Open Source:** Inspect the code yourself.
    * 🚫 **No Viruses:** Built with clean Python libraries.
    * 📭 **No Telemetry:** No tracking, no data collection, no background pings.
* **Invisible Operation:** Nudges your mouse by 1px and back every 60 seconds. It won't interrupt your typing, clicking, or gaming.

---

## 👤 For end users — no Python needed

Check Releases in https://github.com/philippo-source/teams-alive/releases

### Windows
1. Double-click **`TeamsAlive-Setup.exe`**
2. Follow the wizard (Next → Install → Finish)
3. TeamsAlive launches automatically ✅

### macOS
1. Double-click **`TeamsAlive-1.0-macOS.dmg`**
2. Drag **TeamsAlive** into the **Applications** folder
3. **First launch only:** right-click the app → **Open** (to pass Gatekeeper)
4. When prompted, go to:
   **System Settings → Privacy & Security → Accessibility**
   → click **+** and add TeamsAlive *(needed to move the mouse)*
5. Launch TeamsAlive from Applications ✅

---

## 🛠 For developers — build from source

### Prerequisites (build machine only)
- Python 3.9+  (python.org)
- The build scripts install everything else automatically

### Windows — build EXE + installer

```bat
build_windows.bat
```

Outputs:
- `dist\TeamsAliveWin.exe` — portable single file, no install needed
- `TeamsAlive-Setup.exe` — full setup wizard (requires NSIS)

### macOS — build .app + DMG

```bash
chmod +x build_macos.sh && ./build_macos.sh
```

Outputs:
- `dist/TeamsAlive.app` — self-contained app bundle
- `TeamsAlive-1.0-macOS.dmg` — drag-and-drop disk image

### Run directly from Python

```bash
pip install -r requirements.txt
python teams_alive.py
```

---

## ⚙️ Configuration

```python
INTERVAL = 60   # seconds between nudges  (top of teams_alive.py)
```

---

## 📁 File overview

| File | Purpose |
|------|---------|
| `teams_alive.py` | Main application |
| `requirements.txt` | Python dependencies |
| `build_windows.bat` | One-click Windows build |
| `build_macos.sh` | One-click macOS build |
| `teams_alive.spec` | PyInstaller config |
| `installer.nsi` | NSIS installer script |

---

## 📄 License — MIT
