---
sort: 2
---

# Yarn Package Manager

Fast, reliable, and secure dependency management.

- [yarnpkg.com/](https://yarnpkg.com/){:target="_blank"}
- [github.com/yarnpkg/yarn](https://github.com/yarnpkg/yarn){:target="_blank"}

## Installation

**Node.js >=16.10**

Corepack is included by default with all Node.js installs, but is currently opt-in. To enable it, run the following command:

```shell
corepack enable
```

**Node.js <16.10**

Corepack isn't included with Node.js in versions before the 16.10; to address that, run:

```shell
npm i -g corepack
```

**Updating to the latest versions**

Any time you'll want to update Yarn to the latest version, just run:

```shell
yarn set version stable
```

## Usage

Starting a new project.

```shell
yarn init -y
```

The following existing package.json:

```json
{
  "name": "name",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "clean:dir": "rm -rf node_modules",
    "clean:cache": "yarn cache clean",
    "clean": "yarn run clean:dir && yarn run clean:cache",
    "build": "yarn run clean && yarn install"
  },
  "keywords": [],
  "author": "",
  "license": "MIT"
}
```

## Commands

Installing all the dependencies

```shell
yarn install
```

Install packages globally on your operating system.

```shell
yarn add global <package...>
```

Installs a package and any packages that it depends on.

```shell
yarn add [package]
yarn add [package] --dev
```

Removes an unused package from your current package.

```shell
yarn remove [package]
```

Upgrade Dependencies To The Latest Versions Using Yarn.

```shell
yarn up [package]
```

Upgrade all the packages in your package.json to the latest version

```shell
yarn add global npm-check-updates
npm-check-updates -u
yarn add --dev yarn-upgrade-all
```

## Command Reference

[classic.yarnpkg.com/en/docs/cli](https://classic.yarnpkg.com/en/docs/cli){:target="_blank"}
