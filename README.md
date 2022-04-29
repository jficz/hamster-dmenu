# hamster-dmenu
Use Hamster wit dmenu and friends!

Usage:

- Type `-` to stop current task.
- Type `/` to launch Hamster GUI
- Type `<task>[@<category>] [start time [stop time]]` to create a new task
- Select a task from list to start it

Basically whatever you type to the prompt will be verbatim given to
Hamster cli so check `hamster --help` for more details.

Requirements: hamster, <dmenu | wofi | rofi | bemenu | ...>

Default config path: `~/.config/hamster-dmenu/hamster-dmenu.conf`

First run will create a default config. If Wayland is detected, `wofi --dmenu`
is set as the menu app, otherwise `dmenu` is used.

The menu command can be fully customized in the config.

Author recommends using `bemenu` as it allows putting selected text to prompt
without executing it right away (by pressing Shift-Tab), allowing for better
command customization (such as start and stop times, etc., see above)

```bash
menu="bemenu -i -l10 -W0.4"
```

Any arguments given to this script are passed to the the menu program.

