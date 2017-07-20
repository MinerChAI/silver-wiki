# `dir`
![](dir.png)

This module displays the current working directory. If you are in your home directory, it is replaced with a home icon.

## Environment variables
### `BRONZE_DIR_ALIASES`
This variable defines icon aliases for directories. For example, if you wanted to replace `~/go/src` with `\ue627`, the value would be `$HOME/go/src:\ue627`. Multiple aliases can be separated with colons.

### `BRONZE_DIR_LENGTH`
This variable defines the maximum amount of unicode characters that are allowed in the directory. The last directory is not affected.

Example with a value of `1`:<br/>
![](shortdir.png)
