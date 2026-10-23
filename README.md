# Fallout 4 PS4 Save Editor

## Latest local package: v5.0.34

**v5.0.34 — Safety & Phased Upgrades**

This project provides a Windows-focused Python save editor for supported **Fallout 4 PS4** save data. The v5.0.34 launcher is a self-contained `.pyw` file. **It does not decrypt, encrypt, or sign PS4 saves.**

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
