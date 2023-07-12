# My dotfiles

### Setup a new machine

#### Quick start

```bash
$ scp -r $SOURCE_HOST:~/.password-store ~/.
$ scp $SOURCE_HOST:~/ake_gpg_private.key ~/.
$ gpg --import ~/ake_gpg_private.key
$ sh -c "$(curl -fsLS get.chezmoi.io)" -- init --ssh --apply $GITHUB_USERNAME
$ source ~/.profile
```

#### More cautious approach

```bash
$ scp -r $SOURCE_HOST:~/.password-store ~/.
$ scp $SOURCE_HOST:~/ake_gpg_private.key ~/.
$ gpg --import ~/ake_gpg_private.key
$ sh -c "$(curl -fsLS get.chezmoi.io)"
$ source ~/.profile
$ chezmoi init --ssh $GITHUB_USERNAME
$ chezmoi diff
$ chezmoi apply
@ source ~/.profile
```
