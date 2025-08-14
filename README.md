# Ghost Key Blocker

A cross-platform tool to **detect and disable ghost key presses** on your keyboard.

```
   ____ _               _     _  __ _   _     
  / ___| |__   ___  ___| |_  | |/ /| |_| |__  
 | |  _| '_ \ / _ \/ __| __| | ' / | __| '_ \ 
 | |_| | | | |  __/\__ \ |_  | . \ | |_| | | |
  \____|_| |_|\___||___/\__| |_|
```

**Developed by HERO RITIK**  
**Instagram: @haker_attitude42**

## ✨ Features
- Works on **Linux (X11)** and **Windows**
- Choose which **key** to control (e.g., `d`, `space`, `enter`)
- **Auto-detects ghost presses** and disables the key (default: 20 presses in 2s)
- Manual **Disable / Enable** options
- Lightweight, no admin service needed

> ⚠️ Linux support requires **X11** and `xmodmap`. Wayland sessions are not supported.

## 📦 Installation

### Common
```bash
pip install -r requirements.txt
```

### Linux (Kali/Ubuntu etc.)
```bash
sudo apt update
sudo apt install -y x11-xserver-utils  # provides xmodmap
python3 ghost_key_blocker.py
```

### Windows
```cmd
pip install -r requirements.txt
python ghost_key_blocker.py
```

#### Build EXE (Windows)
```cmd
pip install pyinstaller
pyinstaller --onefile ghost_key_blocker.py
dist\ghost_key_blocker.exe
```

## 🚀 Usage
1. Run the tool
2. Enter the **key** you want to control (e.g., `d` or `space`)
3. Choose:
   - **1** → Start auto-detect (disables when ghosting detected)
   - **2** → Disable now
   - **3** → Enable now
   - **4** → Change key

## 🔧 Notes & Tips
- On Linux, the tool uses `xmodmap` to map the key to `NoSymbol` and back.
- On Windows, it uses the `keyboard` library to block/unblock the key.
- If your login/lock screen shows ghost presses, this tool will only act **after login**.

## 📝 License
MIT — see `LICENSE`

---

**Credits**  
Developed by **HERO RITIK**  
Instagram: **@haker_attitude42**