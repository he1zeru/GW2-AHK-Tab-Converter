# GW2 AHK → Tab Converter

**Convert AutoHotkey `.ahk` Numpad macros into human-readable sight-reading tab notation for Guild Wars 2 input.**

**Version:** v0.28  
**Author:** Haze  
**Contact:** Discord - bitchazel *  Guild Wars 2 User ID - hazey.4901

**Repository:** https://github.com/he1zeru/GW2-AHK-Tab-Converter

---

## Summary

This desktop GUI application parses AutoHotkey `.ahk` macro files (found on http://gw2mb.com/ or created from midi with online converters such as https://rosebud.ai/p/e3fd739c-47e2-4204-b16c-ebd8f535f816) and converts them into tab notation used for instrumental reading for Guild Wars 2. It supports single-file and batch conversion, chunking for long files, configurable thresholds for chord detection and line breaks, token-aware wrapping, dark/light themes, presets, and other completely useless extra nonsense.

---

## Key features

- **Octave-aware formatting** - lower `[n]`, middle `n`, upper `(n)` notation.
- **Chord detection** with configurable millisecond threshold.
- **Chunked conversion** to protect the UI when processing long macros.
- **Presets** - save/load conversion profiles.
- **GUI autosave** - Theme and Window UI size changes persist across sessions.
- **Batch Convert** - process multiple `.ahk` files in one operation.

---

## Quick start

1. Run the app (`python "GW2 AHK to Tab Converter.py"`) or use the provided `exe` file.
2. On first run choose a destination root when prompted (or set it in Settings).
   - This creates `GW2 AHK Inputs/`, `GW2 Tab Outputs/`, `Presets/`, and `README.md`.
3. Optionally place and store `.ahk` files into `GW2 AHK Inputs/`.
4. Use **Open AHK File** to load a file and click **Convert**.
5. Use **Copy Output** or **Export TXT** to save or share results.
6. *Optionally fiddle around with the Chord Threshold until you get something that looks decent enough if the chord indicator marks (/) are incorrect. I can't be perfect every time lol.

---

## Presets

- Save control settings (chord threshold, chunk size, linebreak threshold, themes,, etc.) as reusable JSON presets.
- Presets are stored in the `Presets/` folder inside the chosen destination root (makes sharing easier).

---

## Files and folders created by the app

- `settings.json` - limited-autosave configuration (dark_mode, sash fraction, dest_root, etc).
- `GW2 AHK Inputs/` - suggested folder to place source `.ahk` files.
- `GW2 Tab Outputs/` - converted `.txt` files are written here.
- `Presets/` - JSON files for saved presets.

---

## Troubleshooting

- If the app saves to an unexpected location, open **Settings → Change Destination Folder**.
- If conversion stalls, reduce the **Chunk Size** (minutes) or use **Batch Convert** with chunking enabled.

---


