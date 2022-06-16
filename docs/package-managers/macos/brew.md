# Homebrew

The missing package manager for macOS (or Linux).

- [brew.sh](https://brew.sh){:target="_blank"}
- [github.com/Homebrew/brew](https://github.com/Homebrew/brew){:target="_blank"}

## Installation

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Commands

formula is usually the name of the formula to install.

```shell
brew install <formula>
brew uninstall <formula>
```

Fetch the newest version of Homebrew and all formulae from GitHub using git(1) and perform any necessary migrations.

```shell
brew update
```

Upgrade outdated casks and outdated, unpinned formulae using the same options they were originally installed with, plus any appended brew formula options.

```shell
brew upgrade
```

Remove stale lock files and outdated downloads for all formulae and casks, and remove old versions of installed formulae.

```shell
brew cleanup
```

Check your system for potential problems.

```shell
brew doctor
```

## Command Reference

- [docs.brew.sh/Manpage](https://docs.brew.sh/Manpage){:target="_blank"}

## Troubleshooting

Permission denied

```shell
sudo chown -R $(whoami) $(brew --prefix)/*
```
