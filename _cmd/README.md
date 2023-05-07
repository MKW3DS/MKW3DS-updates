# Update & Installer Info tools

## mkInstallInfo

This tool is a one-shot program that, under normal conditions, does not output anything. It creates `installInfo.txt` for the MKT7 installers to install the mod.

## updateInfo

This tool uses the `hashes.txt` to try auto-create update info.

Usage: `updateInfo.py [arg1]`

Argument 1 can be: `new`, `check`,  `update`, `revert`

**Flaw:** All files must be unique, even dummy files must not have identical file contents.

---

## hashes.txt

This file contains the file names and their SHA-256 hashes.

It's used by the [`updateInfo`](#updateinfo) tool.

Another use case is a PC installer utility, whereas it can make extended integrity checks and redownload any broken files.