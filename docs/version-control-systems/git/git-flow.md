# Git Flow

A collection of Git extensions to provide high-level repository operations for Vincent Driessen's branching model.

- [github.com/nvie/gitflow](https://github.com/nvie/gitflow){:target="_blank"}

## Description

- branch: master, develop
- prefix: feature, bugfix, release, hotfix, support, versiontag

Creating feature/release/hotfix/support branches.

- feature: the `<base>` arg must be a commit on develop.
- release the `<base>` arg must be a commit on develop.
- hotfix the `<base>` arg must be a commit on master.
- support the `<base>` arg must be a commit on master.

## Installation

MacOS

```shell
brew install git-flow-avh
```

Ubuntu

```shell
apt-get install git-flow
```

## Configuration

```shell
git flow init -d
```

## Syntax

```shell
git flow <prefix-name> <subcommand> <feature-name>
```

## Commands

To list/start/finish feature branches, use:

```shell
git flow feature
  git flow feature start <name> [<base>]
  git flow feature finish <name>
```

To push/pull a feature branch to the remote repository, use:

```shell
git flow feature publish <name>
  git flow feature pull <remote> <name>
```

To list/start/finish release branches, use:

```shell
git flow release
git flow release start <release> [<base>]
git flow release finish <release>
```

```shell
git push --tags
```

To list/start/finish hotfix branches, use:

```shell
git flow hotfix
git flow hotfix start <release> [<base>]
git flow hotfix finish <release>
```

To list/start support branches, use:

```shell
git flow support
git flow support start <release> <base>
```
