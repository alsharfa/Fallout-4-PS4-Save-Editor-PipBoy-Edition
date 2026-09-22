# Fallout 4 PS4 Save Editor PipBoy edition

A Pip-Boy-style editor for **decrypted Fallout 4 PS4 `SAVEDATA.DAT`** files.

This repository package contains only:

- `Fallout_4_PS4_Save_Editor_PipBoy_Edition.pyw` — the complete editor with runtime files, item database and artwork embedded inside it.
- `README.md` — usage, features and third-party notices.

## v4.1 — linked Level + XP fix

Level and XP are no longer treated as unrelated fields.

Fallout 4 stores player progression in several places. v4.1 keeps them synchronized when you edit either **LEVEL** or **TOTAL XP**:

- the save-header level;
- the persistent PlayerCharacter (`NPC_:00000007`) level override;
- the PlayerRef total-XP actor value;
- the header's current level-progress XP;
- the XP required for the next level.

`LEVEL XP` and `NEXT XP` are now calculated automatically instead of being independently editable.

The Fallout 4 level curve used by the editor is:

- XP needed from level `L` to `L+1`: `75 × L + 125`;
- total XP at the beginning of level `L`: `200 × (L-1) + 75 × (L-1) × (L-2) / 2`.

The editor stores total XP with the same 32-bit float precision used by the save format.

## Other features

- Player name, linked Level/XP, persistent HP, AP and Carry Weight editing.
- One-click **UNLIMITED PLAYER HEALTH** preset (`999,999,999`).
- One-click **UNLIMITED PLAYER CARRY** preset (`999,999,999`).
- Companion detection and companion carry overrides.
- SPECIAL editing and the 70 vanilla SPECIAL perk groups.
- Real inventory quantity editing.
- Category-specific add buttons for Weapons, Apparel, Aid, Misc, Junk, Mods and Ammo.
- Weapon add/change/remove workflow by name — no manual FormID entry.
- Weapon and apparel OMOD / legendary editing.
- **Two Shot Gauss Rifle** workflow.
- One-click **BEST GEAR** preset.
- Stored statistics, global workshop statistics and verified quest stage/objective editing.
- Undo/Redo, pending-change review, structural validation and automatic backups.

## Run

1. Install **Python 3.10 or newer** for Windows with Tcl/Tk enabled.
2. Optional for image previews: `py -m pip install Pillow`.
3. Double-click `Fallout_4_PS4_Save_Editor_PipBoy_Edition.pyw`.
4. Open a **decrypted** PS4 `SAVEDATA.DAT`.
5. Open **STAT > STATUS**.
6. Change either **LEVEL** or **TOTAL XP**. The editor synchronizes the other progression fields when you press **QUEUE STATUS** or save.
7. Make any other edits, use **VALIDATE**, then **SAVE EDITED**.
8. Re-sign/re-encrypt the edited save with your normal PS4 save tool before importing it to the console.

## Important notes

- Keep an untouched backup of the original save.
- The editor only writes structures it can verify and reparse.
- PS4 container encryption/signing is not performed by this editor.
- `999,999,999` cannot be represented exactly as a 32-bit float; the saved/read-back value may display as `1,000,000,000`. This is normal.

## Third-party notices

The low-level Fallout 4 save structure parser/writer embedded in the editor is adapted from the MIT-licensed **pub-struct/fo4-save-cleaner** project:

https://github.com/pub-struct/fo4-save-cleaner

MIT License

Copyright (c) the fo4-save-cleaner contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE.