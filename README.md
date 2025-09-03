# GW2 AHK → Tab Converter

**Convert AutoHotkey `.ahk` Numpad macros into human-readable sight-reading tab notation for Guild Wars 2 input.**

**Version:** v0.28  
**Author:** Haze  
**Contact:** Discord - bitchazel *  Guild Wars 2 - hazey.4901

**Repository:** https://github.com/he1zeru/GW2-AHK-Tab-Converter

---

## Summary

This desktop GUI application parses AutoHotkey `.ahk` macro files (commonly produced by MIDI→AHK conversion tools that send Numpad keys) and converts them into compact, readable text-based tab notation suitable for Guild Wars 2-style input. It supports single-file and batch conversion, chunking for long files, configurable thresholds for chord detection and line breaks, token-aware wrapping, dark/light themes, presets, and progress reporting.

---

## Key features

- **Octave-aware formatting** — lower `[n]`, middle `n`, upper `(n)` notation.
- **Chord detection** with configurable millisecond threshold.
- **Chunked conversion** to protect the UI when processing long macros.
- **Token-aware wrapping** (wraps lines on space-separated tokens).
- **Presets** — save/load conversion control profiles.
- **Limited autosave** — dark mode and UI sash position persist across sessions.
- **Bottom message margin & history** — status messages, progress, and event history.
- **Batch Convert** — process multiple `.ahk` files in one operation.

---

## Quick start

1. Run the app (`python "GW2 AHK to Tab Converter.py"`) or use the provided `exe`.
2. On first run choose a destination root when prompted (or set it in Settings).
   - This creates `GW2 AHK Inputs/`, `GW2 Tab Outputs/`, `Presets/`, and `README.md`.
3. Place `.ahk` files into `GW2 AHK Inputs/`.
4. Use **Open AHK File** to load a file and click **Convert**.
5. Use **Copy Output** or **Export TXT** to save or share results.

---

## Presets

- Save control settings (chord threshold, chunk size, linebreak threshold, etc.) as reusable JSON presets.
- Presets are stored in the `Presets/` folder inside the chosen destination root (makes sharing easier).

---

## Files and folders created by the app

- `settings.json` — limited-autosave configuration (dark_mode, sash fraction, dest_root, etc).
- `GW2 AHK Inputs/` — suggested folder to place source `.ahk` files.
- `GW2 Tab Outputs/` — converted `.txt` files are written here.
- `Presets/` — JSON files for saved presets.

---

## Troubleshooting

- If the app saves to an unexpected location, open **Settings → Change Destination Folder**.
- If conversion stalls, reduce the **Chunk Size** (minutes) or use **Batch Convert** with chunking enabled.

---


