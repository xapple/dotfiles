To add files locally:

    $ cd ~/repos/dotfiles
    $ chezmoi apply -S "$PWD"
    $ chezmoi -S "$PWD" add ~/repos/home_linux/.profile

If you already have a dotfiles repo using `chezmoi` on GitHub at https://github.com/$GITHUB_USERNAME/dotfiles then you can install chezmoi and your dotfiles with the single command:

    $ sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply $GITHUB_USERNAME