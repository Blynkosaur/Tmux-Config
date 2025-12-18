# Tmux Configuration

A personalized tmux configuration with vim-style keybindings, enhanced navigation, and useful plugins for a productive terminal workflow.

## Features

### Key Bindings

- **Prefix Key**: `Ctrl-f` (instead of default `Ctrl-b`)
- **Window Splitting**:
  - `Prefix + i` - Split window horizontally
  - `Prefix + ;` - Split window vertically
- **Window Navigation**:
  - `Prefix + n` - Next window
- **Pane Resizing** (repeatable with `-r` flag):
  - `Prefix + h` - Resize pane left
  - `Prefix + j` - Resize pane down
  - `Prefix + k` - Resize pane up
  - `Prefix + l` - Resize pane right
- **Pane Management**:
  - `Prefix + m` - Maximize/minimize pane (zoom toggle)
- **Reload Config**:
  - `Prefix + r` - Reload tmux configuration

### Vim Integration

- **Copy Mode**: Uses vi keybindings (`set-window-option -g mode-keys vi`)
- **Selection**: `v` to begin selection, `y` to copy selection
- **Vim-Tmux Navigator**: Seamless navigation between vim and tmux panes

### Mouse Support

- Mouse mode enabled for easier pane selection and resizing

### Plugins

This configuration uses [TPM (Tmux Plugin Manager)](https://github.com/tmux-plugins/tpm) and includes:

1. **[vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)**
   - Seamless navigation between vim splits and tmux panes using `Ctrl-h/j/k/l`

2. **[tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect)**
   - Save and restore tmux sessions
   - Captures pane contents for full session restoration

3. **[tmux-continuum](https://github.com/tmux-plugins/tmux-continuum)**
   - Automatic session saving and restoration
   - Restores sessions automatically on tmux server start

## Installation

1. **Clone this repository**:
   ```bash
   git clone https://github.com/yourusername/Tmux-Config.git ~/.tmux-config
   ```

2. **Create a symlink** (or copy) to your home directory:
   ```bash
   ln -s ~/.tmux-config/tmux.conf ~/.tmux.conf
   ```
   Or if you prefer `.tmux.conf`:
   ```bash
   ln -s ~/.tmux-config/.tmux.conf ~/.tmux.conf
   ```

3. **Install TPM** (Tmux Plugin Manager):
   ```bash
   git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
   ```

4. **Start tmux** and install plugins:
   ```bash
   tmux
   ```
   Then press `Prefix + I` (capital I) to install plugins.

## Usage

### Basic Commands

- Start a new session: `tmux`
- Attach to existing session: `tmux attach`
- List sessions: `tmux ls`
- Detach from session: `Prefix + d`

### Session Management with Plugins

- **Save session manually**: `Prefix + Ctrl-s`
- **Restore session**: `Prefix + Ctrl-r`
- Sessions are automatically saved and restored with tmux-continuum

## Customization

To customize this configuration:

1. Edit `tmux.conf` or `.tmux.conf` in this repository
2. Reload the configuration with `Prefix + r` (no need to restart tmux)

## Requirements

- tmux 2.1 or higher
- Git (for TPM and plugins)

## License

This configuration is provided as-is. Feel free to use and modify for your own needs.
