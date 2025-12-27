# NinjaFind

Cross-platform file search with a clean GUI. One codebase, runs natively on Windows and Linux. Built for developers who need to find files quickly without leaving their workflow.

**Tested on:** Windows 11, Ubuntu, Linux Mint, Debian

## Why NinjaFind?

Windows Search is slow and unreliable. Everything requires indexing. Command-line tools are powerful but context-switching breaks flow. NinjaFind gives you:

- Instant file search without indexing
- Content search inside files (text and regex)
- A GUI that stays out of your way
- Folder exclusions for `node_modules`, `.git`, and other noise

## Features

### Search
- **Fast file search** - No indexing required, searches on demand
- **Content search** - Find text inside files with regex support
- **Pattern matching** - Wildcards and glob patterns
- **Size and date filters** - Narrow results by file attributes
- **Extension filter** - Search only specific file types

### Smart Defaults
- **Skipped folders** - Auto-excludes `.git`, `node_modules`, `__pycache__`, `venv`
- **Binary detection** - Skips binary files in content search
- **Hidden files** - Toggle visibility in settings

### File Operations
- **Open file** - Default application or specific program
- **Open containing folder** - Jump to file location
- **Copy path** - Full path to clipboard
- **Copy MD5** - Quick file hash for verification
- **Rename/Delete** - File management without leaving the app

### Truly Cross-Platform
- **Single codebase** - Same Python files run on Windows and Linux
- **Native look** - Uses Qt, feels native on both platforms
- **Platform-aware** - Auto-detects OS for file operations and config paths
- **Tested extensively** - Windows 11, Ubuntu, Linux Mint, Debian

### Quality of Life
- **Dark mode** - Easy on the eyes (qdarkstyle)
- **Search history** - Autocomplete from previous searches
- **Column reordering** - Customize the results view

## Quick Start

### Requirements
- Python 3.6+
- PySide6 6.9.x
- qdarkstyle

```bash
pip install "PySide6>=6.9.0,<6.10.0" qdarkstyle
```

### Run Anywhere

The same Python file works on both platforms:

```bash
# Universal (works on both)
python zgsearch_znn_gui_main.py
```

### Windows
```cmd
zrunwin11.bat
```
Or double-click `zrunwin11.pyw` (no console window)

### Linux (Ubuntu, Mint, Debian)
```bash
./zrunlinux.sh
```

Both launchers auto-install missing dependencies if needed.

## Screenshots

| Search Results | Content Search | Settings |
|----------------|----------------|----------|
| File list with size, date, location | Text matches highlighted in context | Configure exclusions and appearance |

## Configuration

Settings stored in:
- Windows: `config_gsearch.json` (app directory)
- Linux: `~/.config/gsearch/config_gsearch.json`

### Skipped Folders

Edit via Settings or add to config:
```json
{
  "search": {
    "skipped_folders": [".git", "node_modules", "__pycache__", "venv", ".venv"],
    "enable_skipped_folders": true
  }
}
```

## Performance Tips

- Use extension filters to narrow search scope
- Add frequently-ignored folders to skip list
- Content search is fastest on text files under 10MB

## Author

**Takashi Kyoto** - [GitHub](https://github.com/TakashiSeven) | [YouTube](https://youtube.com/@TakashiKyoto)

## License

MIT License - See [LICENSE](LICENSE) for details.
