# wo - Workspace Navigator

A simple zsh plugin for quickly navigating between project directories.

## What it does

`wo` (short for "work-on" or "workspace") lets you quickly jump to project directories without typing full paths. It searches configured target directories for matching subdirectories and changes to them.

## Usage

List all available projects:
```zsh
wo
```

Navigate to a project:
```zsh
wo myproject
```

The plugin supports:
- Case-insensitive matching
- Tab completion for all available projects
- Multiple target directories (configurable in `wo.plugin.zsh`)

## Installation

### Using Antigen

Add to your `.antigenrc`:
```zsh
antigen bundle aroberts/wo-zsh-plugin
```

### Using Oh-My-Zsh

Clone this repository into `~/.oh-my-zsh/custom/plugins/wo`:
```zsh
git clone https://github.com/aroberts/wo-zsh-plugin ~/.oh-my-zsh/custom/plugins/wo
```

Then add `wo` to your plugins array in `.zshrc`:
```zsh
plugins=(... wo)
```

### Manual Installation

1. Clone this repository
2. Add the plugin directory to your `fpath` in `.zshrc`:
   ```zsh
   fpath=(/path/to/wo-zsh-plugin $fpath)
   ```
3. Source the plugin:
   ```zsh
   source /path/to/wo-zsh-plugin/wo.plugin.zsh
   ```

## Configuration

By default, `wo` searches for projects in `$HOME/Source`. To customize the search paths, edit `wo.plugin.zsh` and modify the `targets` array:

```zsh
targets=("$HOME/Source" "$HOME/Projects" "/path/to/other/workspace")
```

## License

MIT
