# TMUX Keybindings and Commands

This repository contains a collection of essential **tmux** keybindings and commands that can help improve your terminal workflow. The commands are organized to manage sessions, windows, panes, and various tmux functionalities.

## Keybindings and Commands

### Session Management
- `tmux` => Start a new tmux session
- `tmux new -s session_name` => Start a new named session
- `ctrl+a, d` => Detach from the current tmux session
- `tmux a` => Reattach to the most recent session
- `tmux ls` => List all tmux sessions
- `tmux a -t 0` => Reattach to the first session (sessions are indexed from 0)
- `tmux kill-session` => Kill the most recent session
- `tmux kill-session -t session_name` => Kill the targeted session by name
- `tmux kill-server` => Kill all tmux sessions, windows, and panes
- `tmux new -t session_name` => Create a new named session and window

### Window Management
- `ctrl+a, c` => Create a new window
- `ctrl+a, ,` => Rename the current window
- `ctrl+a, w` => Show a list of windows
- `ctrl+a, x` => Kill the current window
- `ctrl+a, &` => Kill all windows
- `ctrl+a, index_no_window` => Move to the window at the specified index
- `ctrl+a, n` => Move to the next window
- `ctrl+a, p` => Move to the previous window

### Pane Management
- `ctrl+a, %` => Split the current pane horizontally
- `ctrl+a, "` => Split the current pane vertically
- `ctrl+a, (h/j/k/l)` => Resize the current pane
- `ctrl+a, q` => Show the numbers of all panes
- `ctrl+a, q, number_of_pane` => Switch to a specific pane by number
- `ctrl(h/j/k/l)` => Move between panes using arrow keys
- `ctrl+a, alt` => Resize panes faster
- `ctrl+a, alt, 1/2/3/4/5` => Resize the current pane
- `ctrl+a, m` => Maximize the current pane

### Copy Mode
- `ctrl+a, [` => Enter copy mode
- `ctrl+c` => Exit copy mode
- `ctrl+a, h/j/k/l` => Move in copy mode using the arrow keys

### Miscellaneous
- `ctrl+a, I` => Install a package through the package manager
- `ctrl+a, r` => Refresh tmux (reload the `.config` file)

### Navigation in Copy Mode
- `ctrl+a, [` => Enter copy mode
- `ctrl+a, h/j/k/l` => Move between text in copy mode
- `ctrl+c` => Exit copy mode

---

## Installation

To use these keybindings, you can add the necessary tmux configuration to your `~/.tmux.conf` file or load them interactively in your tmux sessions.

Here is a basic example of how to add custom keybindings to `~/.tmux.conf`:

```bash
# Example tmux keymap configuration
bind c new-window  # Bind 'c' to create a new window
bind % split-window -h  # Bind '%' to split the window horizontally
bind '"' split-window -v  # Bind '"' to split the window vertically
