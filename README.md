## Fresh machine install

If you already have a dotfiles repo using chezmoi on GitHub at
https://github.com/$GITHUB_USERNAME/dotfiles then you can install chezmoi
and your dotfiles with the single command (e.g. on Debian):

```sh
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply $GITHUB_USERNAME
```

### Add files locally (without changing local setup, e.g. on macOS)

```sh
cd ~/repos/dotfiles

# Add files from a Linux-home snapshot directory.
chezmoi -S "$PWD" -D "$HOME/repos/home_linux" add "$HOME/repos/home_linux/.profile"

# Check status against that same destination.
chezmoi -S "$PWD" -D "$HOME/repos/home_linux" status
```