# `cmdtime`
![](cmdtime.png)

This module displays the time it took the last command to complete. This module is not available on Bash.

## Environment Variables
### `BRONZE_CMDTIME_THRESHOLD`
The minimum duration of time to show the segment. For example, with the value of `1s`, if the command took 500ms, the segment would not show, but if the command took 1s or more, the segment would show.
