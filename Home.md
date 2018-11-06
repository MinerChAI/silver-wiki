## Subcommands
### `init`
This subcommand outputs shell script to be evaluated by your shell on startup. Silver detects your shell with the [`SILVER_SHELL`](#silver_shell) environment variable.

### `print`
This subcommand shouldn't be called by the user, but by the code `init` generates. It outputs the prompt.

## Environment variables
Every following variable with the exception of `$SILVER` must be exported by the shell.

### `SILVER`
This variable is an array of every module, in order, you want in your prompt. The elements in this array have three fields separated by colons. The first field is the module name, the second is the background color of the segment, and the third is the foreground color.

For example, if you wanted the `dir` module with black text on a blue background, the element would be `dir:blue:black`.

### `SILVER_SHELL`
This variable tells silver what shell you are using. The supported shells are Bash, Zsh, and fish.

### `SILVER_SEPARATOR`
This variable is the separator between segments. The default value is `\ue0b0`.

Example with `\ue0b4`:<br/>
![](e0b4.png)

Example with `\ue0bc`:<br/>
![](e0bc.png)

### `SILVER_THIN_SEPARATOR`
![](thin-separator.png)

This variable is the thin separator between segments of the same background color. The default value is `\ue0b1`.

### `SILVER_ICONS`
This variable is a preset of every icon. Valid values are `nerd`, `unicode`, or `ascii`. It defaults to `nerd`. For more information, see [Icons](#icons).

## Modules
* [OS](OS)
* [Status](Status)
* [User](User)
* [Directory](Directory)
* [Git](Git)
* [Command Time](Command-Time)
* [Time](Time)
* [Environment Variable](Environment-Variable)
* [virtualenv](virtualenv)

## Icons
Every icon is completely customizable through environment variables.

There are three presets for icons (which can be set through [`SILVER_ICONS`](#silver_icons)):
* `nerd` uses icons from [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts)
* `unicode` uses Unicode (mostly emojis)
* `ascii` uses only ASCII

The default preset is `nerd`, but each individual icon can be set with environment variables. The environment variables to set is `SILVER_ICON_[icon name]`. For example, if you wanted to set the `failed` icon to "&#x2717;", you would set the environment variable `SILVER_ICON_FAILED` to `\u2717`.

Every icon name can be found on the appropriate module wiki page.

## Example configurations
`~/.bashrc`/`~/.zshrc`:
```sh
export SILVER_SHELL=$0
SILVER=(status:black:white dir:blue:black git:green:black cmdtime:magenta:black)
eval "$(silver init)"
```

`~/.config/fish/config.fish`:
```fish
set -x SILVER_SHELL fish
set SILVER status:black:white dir:blue:black git:green:black cmdtime:magenta:black
eval (silver init)
```
