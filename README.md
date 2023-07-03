# My dotfiles
### Setup a new machine
#### Quick start
```bash
$ sh -c "$(curl -fsLS get.chezmoi.io)" --init --apply $GITHUB_USERNAME
$ source ~/.profile
```
#### More cautious approach
```bash
$ sh -c "$(curl -fsLS get.chezmoi.io)" $GITHUB_USERNAME
$ source ~/.profile
$ chezmoi --init
$ chezmoi --diff
$ chezmoi --apply
@ source ~/.profile
```

