# npm

the package manager for JavaScript

- [npmjs.com](https://www.npmjs.com/){:target="_blank"}
- [github.com/npm/cli](https://github.com/npm/cli){:target="_blank"}

## Trends

NPM package comparison

- [npmtrends.com](https://www.npmtrends.com/){:target="_blank"}

## Packages

Essential packages

{% include list.liquid all=true %}

## Usage

Create a package.json file.

```shell
npm init -y
```

Specifics of npm's package.json handling.

```json
{
  "name": "name",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "clean:dir": "rm -rf node_modules",
    "clean:cache": "npm cache clean --force",
    "clean": "npm run clean:dir && npm run clean:cache",
    "reinstall": "npm run clean && npm install"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

## Commands

Install a package.

```shell
npm install
npm i
```

Package will appear in your devDependencies.

```shell
npm install --save-dev <package...>
npm i -D <package...>
```

This uninstalls a package, completely removing everything npm installed on its behalf.

```shell
npm uninstall
```

This runs the build command from a package's "scripts" object.

```shell
npm run build
```

This command will check the registry to see if any (or, specific) installed packages are currently outdated.

```shell
npm outdated
```

Upgrade all the packages in your package.json to the latest version.

```shell
npm install -g npm-check-updates
ncu -u
npm update
npm install
```

Bump a package version.

```shell
npm version [<newversion> | major | minor | patch | premajor | preminor | prepatch | prerelease | from-git]
```

## Command Reference

- [docs.npmjs.com/cli/v8/commands](https://docs.npmjs.com/cli/v8/commands){:target="_blank"}
- [nodejs.dev/learn/update-all-the-nodejs-dependencies-to-their-latest-version](https://nodejs.dev/learn/update-all-the-nodejs-dependencies-to-their-latest-version){:target="_blank"}

## Integration with visual studio code

- [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script){:target="_blank"}  
  npm support for VS Code.  

- [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense){:target="_blank"}  
  Visual Studio Code plugin that autocompletes npm modules in import statements.  
