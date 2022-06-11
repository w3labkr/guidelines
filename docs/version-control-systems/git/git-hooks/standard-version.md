# Standard Version

> standard-version is deprecated. v9.5.0 (2022-05-15)

Automate versioning and CHANGELOG generation, with semver.org and conventionalcommits.org

- [github.com/conventional-changelog/standard-version](https://github.com/conventional-changelog/standard-version){:target="_blank"}

## Installation

```shell
npm install --save-dev standard-version
```

## Configuration

```json
{
    "scripts": {
        "release": "standard-version"
    }
}
```

## Commands

First Release

```shell
npx standard-version --first-release
```

Cutting Releases

```shell
npx standard-version
```

Release as a Pre-Release

```shell
npx standard-version -- --prerelease
```
