# File-Organizer
🗂️ Smart File Organizer — Automatically sort files into categorized folders using rule-based + AI content detection. Features real-time folder monitoring, dark-themed GUI, and Windows startup integration.


## Features

| Feature | Description |
|---|---|
| **130+ file types** | Automatic classification by extension |
| **AI classification** | MIME/magic-byte detection for unknown extensions |
| **Real-time monitoring** | Watchdog-based background folder watcher |
| **Debounce logic** | Waits for downloads to finish before sorting |
| **Duplicate handling** | Auto-renames `file (1).ext`, `file (2).ext` |
| **Modern GUI** | Dark-themed Tkinter interface with live log |
| **Auto-startup** | Register to run on Windows boot |
| **CLI mode** | Headless watcher or one-shot batch organize |

---

## Quick Start

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Launch the GUI

```bash
python main.py
```

### 3. Or use CLI mode

```bash
# Watch a folder in the background
python main.py --watch "C:\Users\you\Downloads"

# One-shot: organize all files now and exit
python main.py --organize "C:\Users\you\Downloads"
```

---

## File Categories

| Category | Extensions |
|---|---|
| **Images** | jpg, jpeg, png, gif, bmp, svg, webp, ico, tiff, heic, raw |
| **Documents** | pdf, doc, docx, xls, xlsx, ppt, pptx, txt, rtf, csv, md, epub |
| **Videos** | mp4, avi, mkv, mov, wmv, flv, webm, m4v, 3gp |
| **Music** | mp3, wav, flac, aac, ogg, wma, m4a, opus |
| **Archives** | zip, rar, 7z, tar, gz, bz2, xz, iso |
| **Code** | py, js, ts, html, css, java, c, cpp, go, rs, dart, json, yaml, sql |
| **Programs** | exe, msi, dmg, deb, rpm, apk |
| **Design** | psd, ai, sketch, fig, xd |
| **Fonts** | ttf, otf, woff, woff2 |
| **Others** | Anything not recognized above |

---

## Project Structure

```
File Organizer/
├── main.py          # Entry point (GUI or CLI)
├── config.py        # Extension rules & settings
├── classifier.py    # Rule-based + AI classification
├── organizer.py     # File-moving logic
├── watcher.py       # Background folder monitor
├── gui.py           # Tkinter GUI
├── startup.py       # Windows auto-startup
├── requirements.txt # Dependencies
└── README.md        # This file
```

---

## Configuration

Edit `config.py` to:
- Add/remove file extension mappings
- Change the default watch folder
- Adjust the debounce delay
- Modify ignored file prefixes/extensions
