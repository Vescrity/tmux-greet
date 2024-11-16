# tmux-greet

Launch tui-greet in tmux.

## Why tmux

Just a simple way to make me change the brightness of my screen and run some commands.

## Start

- Arch: copy the PKGBUILD and makepkg
- Others: place the `tmux-greet` to your `bin` and `tmux-greet-startup` to your /etc

```TOML
#/etc/greetd/config.toml
[default_session]
command = "tmux-greet"
```
