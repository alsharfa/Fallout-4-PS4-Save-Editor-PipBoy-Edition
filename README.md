# Fallout 4 PS4 Save Editor PipBoy edition

A Pip-Boy-style editor for **decrypted Fallout 4 PS4 `SAVEDATA.DAT`** files.

This repository is intentionally clean and contains only:

- `Fallout_4_PS4_Save_Editor_PipBoy_Edition.pyw` — the complete editor with its runtime files, item database and artwork embedded inside it.
- `README.md` — usage, features and third-party notices.

## Features

- Player name, Level, XP, HP, AP and Carry Weight editing.
- SPECIAL editing and the 70 vanilla SPECIAL perk groups.
- Real inventory quantity editing.
- Category-specific add buttons for Weapons, Apparel, Aid, Misc, Junk, Mods and Ammo.
- Weapon add/change/remove workflow by name — no manual FormID entry.
- Weapon and apparel OMOD / legendary editing, including adding a legendary effect to a clean item.
- **Two Shot Gauss Rifle** workflow.
- One-click **BEST GEAR** preset with a modded Two Shot Gauss Rifle, ammo and Heavy Polymer Combat Armor.
- General stored statistics, global workshop statistics and verified quest stage/objective editing.
- Undo/Redo, pending-change review, structural validation and automatic backups.
- Background Open / Validate / Save operations and optimized inventory/OMOD search.

## Run

1. Install **Python 3.10 or newer** for Windows with Tcl/Tk enabled.
2. Optional but recommended for image previews: `py -m pip install Pillow`.
3. Double-click `Fallout_4_PS4_Save_Editor_PipBoy_Edition.pyw`.
4. Open a **decrypted** PS4 `SAVEDATA.DAT`.
5. Make edits, use **VALIDATE**, then **SAVE EDITED**.
6. Re-sign/re-encrypt the edited save with your normal PS4 save tool before importing it to the console.

The single `.pyw` file extracts its embedded runtime to a versioned local cache automatically. No source folders, item database files, assets, test folders or build scripts need to sit beside the editor.

## Important notes

- The editor only writes save structures it can verify and reparse.
- Workshop values currently exposed by the editor are stored **global workshop/stat counters**, not a claim to represent every live per-settlement resource field.
- PS4 encryption/signing is not performed by this editor.
- Structural tests have been run against the supplied decrypted saves, but real-console acceptance still depends on correct PS4 re-sign/re-encryption and the game's own loader.

## Third-party notices

The low-level Fallout 4 save structure parser/writer embedded in the editor is adapted from the MIT-licensed **pub-struct/fo4-save-cleaner** project:

https://github.com/pub-struct/fo4-save-cleaner

MIT License

Copyright (c) the fo4-save-cleaner contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Save-format and record-layout decisions were also cross-checked against public technical references from **xEdit/TES5Edit**, **FallrimTools**, and **F4SE**. Vanilla perk record identifiers were cross-checked against public Fallout 4 data from `urazovm/falloutlab.com`. Their source code/binaries are not bundled as separate third-party packages in this repository.
