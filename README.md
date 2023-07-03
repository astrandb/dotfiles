# My dotfiles

### Setup a new machine

#### Quick start

```bash
$ gpg --import public_gpg.key
$ gpg --import private_gpg.key
$ # scp -r ~/.password-store $TARGET_HOST:
$ sh -c "$(curl -fsLS get.chezmoi.io)" -- init --ssh --apply $GITHUB_USERNAME
$ source ~/.profile
```

#### More cautious approach

```bash
$ gpg --import public_gpg.key
$ gpg --import private_gpg.key
$ # scp -r ~/.password-store $TARGET_HOST:
$ sh -c "$(curl -fsLS get.chezmoi.io)"
$ source ~/.profile
$ chezmoi init --ssh $GITHUB_USERNAME
$ chezmoi diff
$ chezmoi apply
@ source ~/.profile
```
