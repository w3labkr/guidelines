---
sort: 3
---

# rbenv

Manage your app's Ruby environment.

- [github.com/rbenv/rbenv](https://github.com/rbenv/rbenv){:target="_blank"}

## Installation

The [rbenv-installer](https://github.com/rbenv/rbenv-installer){:target="_blank"} script idempotently installs or updates rbenv on your system. If Homebrew is detected, installation will proceed using brew install/upgrade

```shell
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/HEAD/bin/rbenv-installer | bash
```

## Configuration

Add ~/.rbenv/bin to your $PATH for access to the rbenv command-line utility.

```shell
$ vim ~/.bashrc
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"
```

Restart your shell so the path changes take effect.

```shell
exec $SHELL
```

## Commands

Lists all Ruby versions known to rbenv, and shows an asterisk next to the currently active version.

```shell
rbenv versions
```

list latest stable versions.

```shell
rbenv install -l
```

list all local versions.

```shell
rbenv install -L
```

install a Ruby version.

```shell
rbenv install 3.1.2
```

Sets the global version of Ruby to be used in all shells by writing the version name to the ~/.rbenv/version file.

```shell
rbenv global 3.1.2
exec $SHELL
ruby -v
```

Sets a local application-specific Ruby version by writing the version name to a .ruby-version file in the current directory.

```shell
rbenv local 3.1.2
```

Uninstalling rbenv.

```shell
rm -rf `rbenv root`
```

Uninstalling rbenv on MacOS.

```shell
brew uninstall rbenv
```

Uninstalling rbenv on Debian, Ubuntu, and their derivatives.

```shell
sudo apt purge rbenv
```
