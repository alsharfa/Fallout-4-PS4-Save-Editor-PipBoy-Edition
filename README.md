# Fallout 4 PS4 Save Editor

## Latest local package: v5.0.34

**v5.0.34 — Safety & Phased Upgrades**

This project provides a Windows-focused Python save editor for supported **Fallout 4 PS4** save data. The v5.0.34 launcher is a self-contained `.pyw` file. **It does not decrypt, encrypt, or sign PS4 saves.**

> **Distribution status:** v5.0.34 was packaged as `Fallout_4_PS4_Save_Editor_v5.0.34.zip`, but the ZIP has not yet been uploaded to this GitHub repository. The older v4.9.4 GitHub release linked below remains the published release until a newer release is posted.

### Running v5.0.34 on Windows

1. Obtain the v5.0.34 ZIP from the project maintainer and extract it.
2. Install Python 3 on Windows, with `tkinter` support.
3. Open `Fallout_4_PS4_Save_Editor_v5.0.34.pyw` (or run `py Fallout_4_PS4_Save_Editor_v5.0.34.pyw` from Command Prompt for troubleshooting).
4. Keep an untouched backup of each save, and work only on a save file in a format supported by the editor.
5. Review queued changes, use the editor's save action, and test the result in-game before replacing your working save.

### Important limitations

- Encrypted or signed PlayStation save files must be prepared with a **separate, compatible save-decryption/signing workflow**, where applicable.
- Never overwrite your only working save. An edited file passing structural validation does not guarantee in-game compatibility.
- Item, companion, settler, power-armor and quest-editing options may depend on save data, enabled plugins and verified record support.

### Validation performed on the v5.0.34 archive

- ZIP archive integrity and byte-for-byte extraction verified.
- Python launcher syntax successfully parsed.
- Full Windows GUI execution and in-game loading **have not been verified** by these checks.

---

## Previous published release and historical notes

### Previously published version

**v4.9.4 — Power Armor / Settler Inventory Bugfix**

Latest release package:

[Download Fallout_4_PS4_Save_Editor_v4.9.4.zip](https://github.com/alsharfa/Fallout-4-PS4-Save-Editor-PipBoy-Edition/releases/download/v4.9.4/Fallout_4_PS4_Save_Editor_v4.9.4.zip)

## v4.9.4 bug fixes

- Fixed **Power Armor Condition %** edits so they are saved correctly even when condition is the only pending edit.
- Power Armor condition changes now participate in **Undo / Redo / Discard Pending**.
- Power Armor condition changes now appear in the pending-change review before saving.
- Fixed pending-state tracking for **Settler Inventory** add, remove and copy operations.
- Settler inventory changes now participate correctly in **Undo / Redo / Discard Pending**.
- Settler inventory changes now appear in the pending-change review.
- Individual settler/NPC inventories remain isolated: additions and removals apply only to the selected settler.
- Right-click settler inventory supports **Remove Item from Settler**.
- Right-click settler list supports **Copy All Inventory** and **Paste Inventory to This Settler** while leaving the source settler unchanged.
- Power Armor details include verified frame-installed torso detection, condition display/editing, installed mods and supported maximum lining workflows.
- Unsupported Power Armor stat/OMOD combinations are not guessed or written.

## Features

- Player name editing.
- Linked **Level + XP** editing with automatic progression synchronization.
- Persistent **Player Health**, **AP**, and **Carry Weight** editing.
- **Max Health**, **Rapid Health Regen**, and **Max Carry Weight** save-field presets.
- **Fusion Core** quantity preset.
- Companion detection and carry-weight overrides.
- Individual **Settler / NPC Inventory** editing with per-settler add/remove and full-inventory copy/paste.
- SPECIAL stat editing and all 70 vanilla SPECIAL perk groups.
- Real inventory quantity editing.
- Add items from the built-in database with a selectable amount.
- Database categories for Weapons, Apparel, Power Armor, Aid, Misc, Junk, Keys, Mods and Ammo.
- Expanded apparel database support, including armor, clothing, outfits, headwear and other wearable ARMO records.
- Power Armor database support, including Hellfire and X-02 records when their required plugins are present.
- **Power Armor Details** with torso detection, condition editing and supported maximum lining operations.
- One-click **BEST NON-POWER ARMOR** preset with an Amount field.
- Far Harbor-aware Marine Armor preset with Heavy Combat Armor fallback.
- Right-click **Copy / Paste / Select All** support for editable fields.
- Right-click **Copy Row** support for inventory/table rows.
- Double-click and Enter-key shortcuts for adding database items.
- Weapon add, change and remove workflow by name.
- Human-readable **Armor & Weapon Upgrades** interface.
- Upgrade filtering for **Legendary**, **Armor upgrades**, and **Weapon upgrades**.
- Suggested-upgrades filtering for the selected item.
- **Add Selected Upgrade** and **Replace Slot** controls.
- Weapon and apparel OMOD editing.
- Legendary effect editing.
- **Two Shot Gauss Rifle** workflow.
- One-click **BEST GEAR** preset.
- Stored statistics and global workshop statistics editing.
- Verified quest stage and objective editing.
- Undo / Redo, pending-change review, structural save validation, and automatic backups.

## Safety / save handling

- The editor queues supported edits before writing.
- Use **SAVE EDITED** to commit pending changes.
- Structural validation is performed before the edited save is accepted.
- Automatic backups are retained.
- The editor avoids guessing unsupported record layouts or Power Armor modifications.

## Older changes

### v4.7.8

- Added a dedicated **KEYS** inventory category.
- Added **ADD ALL JUNK** with a configurable Amount field.
- Added **SET EXISTING JUNK** to set the quantity of junk already present.
- Added **ADD ALL KEYS** with a configurable Amount field.
- Added **SET EXISTING KEYS** to set the quantity of keys already present.
- Bulk Add All operations only insert missing items instead of overwriting existing stacks.
- DLC/plugin validation and duplicate-safe inventory handling remain enabled.

### v4.7.7

- Replaced the ambiguous unsaved-edits Yes/No prompt with explicit **Save / Discard / Cancel** behavior.
- Cancel keeps the current editor session open.
- Save must complete successfully before the editor continues with the pending action.
- Renamed **UNLIMITED ALL DETECTED** to **UNLIMITED ALL VERIFIED** for companion carry editing.
- Companion actor-value tables that are not verified are explicitly skipped/read-only.

### v4.7.6

- Added the improved **Armor & Weapon Upgrades** interface.
- Added human-readable upgrade categories instead of requiring raw OMOD records.
- Added Legendary / Armor / Weapon upgrade filtering.
- Added suggested-for-current-item filtering.
- Added clearer Add Selected Upgrade and Replace Slot workflows.

### v4.7.5

- Added one-click **BEST NON-POWER ARMOR**.
- Added an **Amount** field controlling how many copies of each applicable piece are queued.
- Uses a Marine Armor loadout when Far Harbor is available.
- Falls back to Heavy Combat Armor when Far Harbor is unavailable.

### v4.7.4

- Expanded the apparel picker to expose all ARMO records available in the editor item database.
- Includes supported vanilla, DLC and available Creation Club apparel records.

### v4.7.3

- Added a dedicated **POWER ARMOR** database category.
- Added Hellfire and X-02 power-armor records with plugin-presence checks.

### v4.7.2

- Added right-click clipboard menus to editable fields.
- Added right-click row copying in inventory/table views.
- Improved the item database picker with user-selectable quantities.
- Added double-click and Enter-key shortcuts for adding database items.

### v4.7.1

- Renamed the application to **Fallout 4 PS4 Save Editor**.
- Corrected Health, Health Regen and Carry Weight save-field handling.
- Corrected post-write verification so it validates the same fields that are modified.
- Improved the default editor window sizing and UI text.
