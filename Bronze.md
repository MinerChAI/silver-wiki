## Subcommands
### `init`
This subcommand outputs shell script to be evaluated by your shell on startup. Bronze tries to detect your shell with the `SHELL` environment variable, but the `SHELL` environment variable is not necessarily the currently used shell, but the default shell for the user, so it's recommended to explicitly set the `SHELL` variable.

### `print`
This subcommand shouldn't be called by the user, but by the code `init` generates. It outputs the prompt.

## Environment variables
### `BRONZE`
This variable is an array of every module, in order, you want in your prompt. The elements in this array have three fields separated by colons. The first field is the module name, the second is the background color of the segment, and the third is the foreground color.

For example, if you wanted the `dir` module with black text on a blue background, the element would be `dir:blue:black`.

### `BRONZE_SEPARATOR`
This variable is the separator between segments. The default value is `\ue0b0`.

Example with `\ue0b4`:<br/>
![](e0b4.png)

Example with `\ue0bc`:<br/>
![](e0bc.png)

### `BRONZE_THIN_SEPARATOR`
![](thin-separator.png)

This variable is the thin separator between segments of the same background color. The default value is `\ue0b1`.

### `BRONZE_ICONS`
This variable is a preset of every icon. Valid values are `nerd`, `unicode`, or `ascii`. It defaults to `nerd`. For more information, see [Icons](Icons).

## Example configurations
`~/.bashrc`/`~/.zshrc`:
```sh
export SHELL=$0
BRONZE=(status:black:white shortdir:blue:black git:green:black cmdtime:magenta:black)
eval "$(bronze init)"
```

`~/.config/fish/config.fish`:
```fish
set -x SHELL fish
set BRONZE status:black:white shortdir:blue:black git:green:black cmdtime:magenta:black
eval (bronze init)
```
