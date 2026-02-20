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
#sudo ln -s ~/.local/kitty.app/bin/kitty /usr/bin/kitty
# symlink kitten
#sudo ln -s ~/.local/kitty.app/bin/kitten /usr/bin/kitten
# kitty icon entry button to show in menu/dock
#sudo cp /home/ubuntu/.local/kitty.app/share/applications/* /usr/share/applications/
# kitty icon for its entry menu/dock
#sudo cp /home/ubuntu/.local/kitty.app/share/icons/hicolor/scalable/apps/kitty.svg /usr/share/icons/

# Create symbolic links to add kitty and kitten to PATH (assuming ~/.local/bin is in
# your system-wide PATH)
ln -sf ~/.local/kitty.app/bin/kitty ~/.local/kitty.app/bin/kitten ~/.local/bin/
# Place the kitty.desktop file somewhere it can be found by the OS
cp ~/.local/kitty.app/share/applications/kitty.desktop ~/.local/share/applications/
# If you want to open text files and images in kitty via your file manager also add the kitty-open.desktop file
cp ~/.local/kitty.app/share/applications/kitty-open.desktop ~/.local/share/applications/
# Update the paths to the kitty and its icon in the kitty desktop file(s)
sed -i "s|Icon=kitty|Icon=$(readlink -f ~)/.local/kitty.app/share/icons/hicolor/256x256/apps/kitty.png|g" ~/.local/share/applications/kitty*.desktop
sed -i "s|Exec=kitty|Exec=$(readlink -f ~)/.local/kitty.app/bin/kitty|g" ~/.local/share/applications/kitty*.desktop
# Make xdg-terminal-exec (and hence desktop environments that support it use kitty)
echo 'kitty.desktop' > ~/.config/xdg-terminals.list

# copy xterm-kitty to systemwide terminfo
sudo cp ~/.local/kitty.app/share/terminfo/x/xterm-kitty /usr/share/terminfo/x/
# or for user only
cp ~/.local/kitty.app/share/terminfo/x/xterm-kitty ~/.terminfo/x/
```

## my other configs

- kitty config (this repo)
- [nvim config](https://github.com/abanoubha/nvim)
- [vim config](https://github.com/abanoubha/vim-config)
- fish shell config (currently private)
- [ghostty terminal config](https://github.com/abanoubha/ghostty)

