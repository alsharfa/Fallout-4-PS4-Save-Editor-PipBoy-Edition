# Fallout 4 PS4 Save Editor

## Current version

**v4.7.8**

## Features

- Player name editing.
- Linked **Level + XP** editing with automatic progression synchronization.
- Persistent **Player Health**, **AP**, and **Carry Weight** editing.
- **Max Health**, **Rapid Health Regen**, and **Max Carry Weight** save-field presets.
- **Fusion Core** quantity preset.
- Companion detection and carry-weight overrides.
- SPECIAL stat editing and all 70 vanilla SPECIAL perk groups.
- Real inventory quantity editing.
- Add items from the built-in database with a selectable amount.
- Database categories for Weapons, Apparel, Power Armor, Aid, Misc, Junk, Mods and Ammo.
- Expanded apparel database support, including armor, clothing, outfits, headwear and other wearable ARMO records.
- Power Armor database support, including Hellfire and X-02 records when their required plugins are present.
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

## v4.7.8 changes

- Added a dedicated **KEYS** inventory category.
- Added **ADD ALL JUNK** with a configurable Amount field.
- Added **SET EXISTING JUNK** to set the quantity of junk already present.
- Added **ADD ALL KEYS** with a configurable Amount field.
- Added **SET EXISTING KEYS** to set the quantity of keys already present.
- Bulk Add All operations only insert missing items instead of overwriting existing stacks.
- DLC/plugin validation and duplicate-safe inventory handling remain enabled.

## v4.7.7 fixes

- Replaced the ambiguous unsaved-edits Yes/No prompt with explicit **Save / Discard / Cancel** behavior.
- Cancel now keeps the current editor session open.
- Save must complete successfully before the editor continues with the pending action.
- Renamed **UNLIMITED ALL DETECTED** to **UNLIMITED ALL VERIFIED** for companion carry editing.
- Companion actor-value tables that are not verified are explicitly skipped/read-only.
- Companion carry operations now report how many verified companions were modified and how many were skipped.

## v4.7.6 changes

- Added the improved **Armor & Weapon Upgrades** interface.
- Added human-readable upgrade categories instead of requiring users to work directly with raw OMOD records.
- Added Legendary / Armor / Weapon upgrade filtering.
- Added suggested-for-current-item filtering.
- Added clearer Add Selected Upgrade and Replace Slot workflows.
- Retains the v4.7.5 Best Non-Power Armor preset and expanded v4.7.4 apparel database.

## v4.7.5 changes

- Added one-click **BEST NON-POWER ARMOR**.
- Added an **Amount** field controlling how many copies of each applicable piece are queued.
- Uses a Marine Armor loadout when Far Harbor is available.
- Falls back to Heavy Combat Armor when Far Harbor is unavailable.

## v4.7.4 changes

- Expanded the apparel picker to expose all ARMO records available in the editor item database.
- Includes supported vanilla, DLC and available Creation Club apparel records.

## v4.7.3 changes

- Added a dedicated **POWER ARMOR** database category.
- Added Hellfire and X-02 power-armor records with plugin-presence checks.

## v4.7.2 changes

- Added right-click clipboard menus to editable fields.
- Added right-click row copying in inventory/table views.
- Improved the item database picker with user-selectable quantities.
- Added double-click and Enter-key shortcuts for adding database items.

## v4.7.1 fixes

- Renamed the application to **Fallout 4 PS4 Save Editor**.
- Corrected Health, Health Regen and Carry Weight save-field handling to use the supplied save-code search locations.
- Corrected post-write verification so it validates the same fields that are modified.
- Improved the default editor window sizing and UI text.
