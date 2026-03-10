# Killoxs ExifTool Stamper

> A modern Windows desktop app to batch-apply custom copyright metadata to images using ExifTool.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square&logo=windows)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![ExifTool](https://img.shields.io/badge/Powered%20by-ExifTool-orange?style=flat-square)

---

## What it does

Killoxs ExifTool Stamper lets you select any folder and batch-stamp all your images with your custom copyright and ownership metadata in one click. It strips existing EXIF/IPTC/XMP/Photoshop metadata and writes your own — recursively across all subfolders.

Built for photographers, digital artists, and content creators who want to protect and brand their work.

---

## Features

- Browse any folder and apply metadata recursively
- Clears existing EXIF, IPTC, XMP, and Photoshop metadata before writing
- All metadata fields editable directly in the UI before running
- Live scrolling output log with color-coded results
- Runs in a background thread — UI never freezes
- Overwrites originals in place (no duplicate files)
- Safe for JPEG, PNG, TIFF, PSD, WEBP and most image formats

---

## Metadata written

| Tag | Default Value |
|-----|---------------|
| Creator | 
| Artist |
| Rights | 
| Copyright | 
| Credit |
| Source | 
| WebStatement | 
| Email | 
| Software | 
| XMP-dc:Rights | 

All values are editable in the UI — the defaults above are just starting points.

---

## Download

Go to the [**Releases**](../../releases) page and download the latest `KilloxsExifStamper.exe`.

No Python installation required. No ExifTool installation required. Just run the EXE.

---

## Build it yourself

### Requirements

- Python 3.10+
- `exiftool.exe` + `exiftool_files\` folder from [exiftool.org](https://exiftool.org)

### Steps

1. Clone the repo
   ```
   git clone https://github.com/killoxs/image-copyright-stamper.git
   cd to folder
   ```

2. Download ExifTool for Windows from [exiftool.org](https://exiftool.org)
   - Unzip it
   - Rename `exiftool-k.exe` to `exiftool.exe`
   - Place `exiftool.exe` and the `exiftool_files\` folder in the repo root

3. Run the build script
   ```
   build.bat
   ```

4. Your EXE will be at `dist\KilloxsExifStamper.exe`

### Run without building

```
pip install customtkinter
py killoxs_exif.py
```

Requires `exiftool.exe` and `exiftool_files\` in the same folder as the script.

---

## Project structure

```
killoxs-exif-stamper/
├── killoxs_exif.py       # Main app
├── build.bat             # One-click EXE builder
└── README.md
```

> `exiftool.exe` and `exiftool_files\` are not included in the repo.
> Download them separately from [exiftool.org](https://exiftool.org).

---

## Tech stack

- [Python 3](https://python.org)
- [customtkinter](https://github.com/TomSchimansky/CustomTkinter) — modern dark UI
- [ExifTool by Phil Harvey](https://exiftool.org) — metadata engine
- [PyInstaller](https://pyinstaller.org) — EXE packaging

---

## License

GPL

---

## Author

**Seif Abroud** — [killoxs.com](https://killoxs.com) · hello@killoxs.com
