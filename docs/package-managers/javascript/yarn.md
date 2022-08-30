# yarn

Fast, reliable, and secure dependency management.

- [yarnpkg.com](https://yarnpkg.com/){:target="_blank"}
- [github.com/yarnpkg/yarn](https://github.com/yarnpkg/yarn){:target="_blank"}

## Installation

`Node.js >=16.10`

Corepack is included by default with all Node.js installs, but is currently opt-in. To enable it, run the following command:

```shell
corepack enable
```

`Node.js <16.10`

Corepack isn't included with Node.js in versions before the 16.10; to address that, run:

```shell
npm i -g corepack
```

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
    "clean": "yarn clean:dir && yarn clean:cache",
    "reinstall": "yarn clean && yarn install"
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
yarn add global [package]
```

Installs a package and any packages that it depends on.

```shell
yarn add [package]
yarn add [package] --dev
```

Upgrades packages to their latest version based on the specified range.

```shell
yarn upgrade
yarn upgrade left-pad
yarn upgrade left-pad@^1.0.0
yarn upgrade left-pad grunt
yarn upgrade @angular
```

yarn upgrade --pattern <pattern> will upgrade all packages that match the pattern.

```shell
yarn upgrade --pattern gulp
yarn upgrade left-pad --pattern "gulp|grunt"
yarn upgrade --latest --pattern "gulp-(match|newer)"
```

Removes an unused package from your current package.

```shell
yarn remove [package]
```

Upgrade Dependencies To The Latest Versions Using Yarn.

```shell
yarn up [package]
```

Running this command will clear the global cache.

```shell
yarn cache clean
```

Upgrade all the packages in your package.json to the latest version

```shell
yarn add global npm-check-updates
npm-check-updates -u
yarn add --dev yarn-upgrade-all
```

## Command Reference

- [classic.yarnpkg.com/en/docs/cli](https://classic.yarnpkg.com/en/docs/cli){:target="_blank"}
