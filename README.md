# kitty terminal config

my config for kitty terminal

> [!NOTE]
> This config is opinionated and created by Abanoub Hanna, for Abanoub Hanna. You can use it as you like.

## config

- dark theme named "Builtin Tango Dark"
- titlebar background color set to black
- set font family to "JetBrains Mono"
- set font size to 18.0
- set fish shell as interactive login shell
- some performance optimizations
- key mappings

## How I install it ?

```sh
# install/upgrade kitty
curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin

# symlink kitty
sudo ln -s ~/.local/kitty.app/bin/kitty /usr/bin/kitty

# symlink kitten
sudo ln -s ~/.local/kitty.app/bin/kitten /usr/bin/kitten

# kitty icon entry button to show in menu/dock
sudo cp /home/ubuntu/.local/kitty.app/share/applications/* /usr/share/applications/

# kitty icon for its entry menu/dock
sudo cp /home/ubuntu/.local/kitty.app/share/icons/hicolor/scalable/apps/kitty.svg /usr/share/icons/
```

## my other configs

- kitty config (this repo)
- [nvim config](https://github.com/abanoubha/nvim)
- [vim config](https://github.com/abanoubha/vim-config)
- fish shell config (currently private)
- [ghostty terminal config](https://github.com/abanoubha/ghostty)

