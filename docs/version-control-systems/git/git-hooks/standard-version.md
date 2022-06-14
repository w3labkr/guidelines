# standard-version

> standard-version is deprecated. v9.5.0 (2022-05-15)

Automate versioning and CHANGELOG generation, with semver.org and conventionalcommits.org

- [github.com/conventional-changelog/standard-version](https://github.com/conventional-changelog/standard-version){:target="_blank"}

## Installation

```shell
npm install --save-dev standard-version
```

## Configuration

`package.json`

```json
{
    "scripts": {
        "release": "standard-version"
    }
}
```

Any of the command line parameters accepted by standard-version can instead be provided via configuration. Please refer to the [conventional-changelog-config-spec](https://github.com/conventional-changelog/conventional-changelog-config-spec){:target="_blank"} for details on available configuration options.

`.versionrc`

```json
{
    "types": [
        { "type": "build", "section": "Builds", "hidden": true },
        { "type": "chore", "section": "Chores", "hidden": true },
        { "type": "ci", "section": "Continuous Integrations", "hidden": true },
        { "type": "docs", "section": "Documentation", "hidden": true },
        { "type": "feat", "section": "Features", "hidden": false },
        { "type": "fix", "section": "Bug Fixes", "hidden": false },
        { "type": "perf", "section": "Performance Improvements", "hidden": true },
        { "type": "refactor", "section": "Code Refactoring", "hidden": true },
        { "type": "revert", "section": "Reverts", "hidden": true },
        { "type": "style", "section": "Styles", "hidden": true },
        { "type": "test", "section": "Tests", "hidden": true }
    ]
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
