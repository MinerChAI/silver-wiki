Every icon is completely customizable through environment variables.

There are three presets for icons:
* `nerd` uses icons from [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts)
* `unicode` uses Unicode (mostly emojis)
* `ascii` uses only ASCII

The default preset is `nerd`, but each individual icon can be set with environment variables. The environment variables to set is `BRONZE_ICON_[icon name]`. For example, if you wanted to set the `failed` icon to "&#x2717;", you would set the environment variable `BRONZE_ICON_FAILED` to `\u2717`.

Every icon name can be found on the appropriate module wiki page.
