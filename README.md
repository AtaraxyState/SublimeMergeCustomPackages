# Sublime Merge Stash Plugin

A Sublime Merge plugin that adds convenient stash functionality through context menus and command palette.

## Features

- **Right-click to stash files** in the summary view
- **Right-click to stash hunks** in the diff view
- **Interactive hunk stashing** - choose exactly which hunks to stash
- **Command palette integration** for quick stashing
- **Multiple file types supported** - works with modified, untracked, and staged files

## Installation

1. **Find your Sublime Merge packages directory:**
   - Windows: `%APPDATA%\Sublime Merge\Packages\User`
   - macOS: `~/Library/Application Support/Sublime Merge/Packages/User`
   - Linux: `~/.config/sublime-merge/Packages/User`

2. **Copy all `.sublime-menu` and `.sublime-commands` files** from this repository into that directory

3. **Restart Sublime Merge** to load the new menus

## Usage

### File Stashing
- **Right-click any file** in the Files tab → **"Stash File"**
- Works with modified, untracked, and staged files

### Hunk Stashing
- **Right-click in any diff content** → **"Stash Hunk (Interactive)"**
- Git will show each hunk and let you choose which ones to stash
- Type `y` for yes, `n` for no, `q` to finish

### Command Palette
Press `Ctrl+P` (or `Cmd+P` on macOS) and type:
- **"Git: Stash All Changes"** - Quick stash of all changes
- **"Git: Stash Hunks (Interactive)"** - Interactive hunk selection
- **"Git: Stash Including Untracked"** - Stash including untracked files
- **"Git: Stash Staged Changes Only"** - Stash only staged changes

### Menu Access
Go to **Repository** → **Stash All Changes** or **Stash Including Untracked**

## Files Included

- `Modified File.sublime-menu` - Context menu for modified files
- `Untracked File.sublime-menu` - Context menu for untracked files  
- `Index File.sublime-menu` - Context menu for staged files
- `Diff Context.sublime-menu` - Context menu for diff content (includes hunk stashing)
- `Hunk.sublime-menu` - Context menu for hunk headers
- `File.sublime-menu` - Context menu for file headers
- `Default.sublime-commands` - Command palette entries
- `Main.sublime-menu` - Main menu integration

## Git Commands Used

The plugin uses these Git commands:
- `git stash push $path` - Stash specific file
- `git stash push --patch $path` - Interactive hunk stashing
- `git stash push --include-untracked` - Stash including untracked files
- `git stash push --staged` - Stash only staged changes

## Contributing

Feel free to submit issues and pull requests!

## License

MIT License - see LICENSE file for details 