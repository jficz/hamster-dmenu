# hamster-dmenu
Use Hamster with dmenu and friends!

Usage:

- Type `--` to stop current task.
- Type `/` to launch Hamster GUI
- Type `<task>[@<category>] [start time [stop time]]` to create a new task
- Select a task from list to start it

Basically whatever you type to the prompt will be verbatim given to
Hamster cli so check `hamster --help` for more details.

Requirements: hamster, <dmenu | fuzzel | wofi | rofi | bemenu | ...>

Default config path: `~/.config/hamster-dmenu/hamster-dmenu.conf`

First run will create a default config. If Wayland is detected, `fuzzel --dmenu`
is set as the menu app, otherwise `dmenu` is used.

The menu command can be fully customized in the config.

Author recommends using [fuzzel](https://codeberg.org/dnkl/fuzzel/) as it
leverages fuzzy matching and allows putting selected text to prompt
without executing it right away (by pressing C-Tab), allowing for better
command customization (such as start and stop times, etc., see above).

Any arguments given to this script are passed to the the menu program.

