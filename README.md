## Fresh machine install

If you already have a dotfiles repo using `chezmoi` on GitHub at
https://github.com/$GITHUB_USERNAME/dotfiles then you can install `chezmoi`
and your dotfiles with the single command (e.g. on Debian):

    $ sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply $GITHUB_USERNAME

Later on to apply changes just run:

    $ chezmoi update -v

### Add files locally

If you want to add files to your dotfiles repo without changing your local environement (e.g. macOS) then you can do so with the following commands:

```sh
# Go to the local clone.
cd ~/repos/dotfiles

# Add files from a specific directory.
chezmoi -S "$PWD" -D "$HOME/repos/home_linux" add "$HOME/repos/home_linux/.profile"
```