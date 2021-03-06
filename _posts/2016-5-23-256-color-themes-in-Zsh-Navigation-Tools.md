---
layout: post
title: 256-color themes in Zsh Navigation Tools
---

[Zsh Navigation Tools](https://github.com/psprint/zsh-navigation-tools)
support color themes that can be tried out by
pressing `Ctrl-T` (next theme) and `Ctrl-G` (previous theme). They
are configured via `themes` variable (array) in
`~/.config/znt/n-list.conf`:

```zsh
# Combinations of colors to try out with Ctrl-T and Ctrl-G
# The last number is the bold option, 0 or 1
local -a themes
themes=( "white/black/0" "white/black/1" "green/black/0"
         "green/black/1" "white/blue/0" "white/blue/1"
         "magenta/black/0" "magenta/black/1" )
```

Other way to configure is utilizing `ZNT`'s integration with `zshrc` and
setting variable `znt_list_themes` there:

```zsh
znt_list_themes=( "green/black/1" "black/white/1" )
```

### More colors

Next version of Zsh (assumed to be `5.3`) will provide support for 256
colors for `zcurses`, a module used by `Zsh Navigation Tools`. This
means that `ZNT` will be able to use those colors. Following
configuration can be used (i.e. set in `~/.config/znt/n-list.conf`) to
make use of the functionality:

```zsh
themes=( "white/17/0" "10/17/1" "white/24/1" "white/22/0"
         "white/22/1" "white/25/0" "white/25/1" "white/59/0"
         "white/59/1" "white/60/0" "white/60/1" "white/61/0"
         "white/61/1" "black/65/0" "black/244/0" )
```

You can also set the `themes` array via `zshrc`, via `znt_list_themes`
variable.

View on [asciinema](https://asciinema.org/a/46477). You can resize the video by pressing `Ctrl-+` or `Cmd-+`.

<script type="text/javascript" src="https://asciinema.org/a/46477.js" id="asciicast-46477" async></script>
