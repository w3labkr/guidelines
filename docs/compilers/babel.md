# Babel

Babel is a compiler for writing next generation JavaScript.

- [babel.dev](https://babel.dev/){:target="_blank"}
- [github.com/babel/babel](https://github.com/babel/babel){:target="_blank"}

## Installation

```shell
npm install --save-dev @babel/core @babel/cli @babel/node
```

## Configuration

`package.json`

```json
{ 
    "scripts": {
        "start": "node index.js", 
        "start:dev": "babel-node index.js"
    },
}
```

Run the script.

```shell
npm run start:dev
```

## Presets

### @babel/preset-env

A Babel preset for each environment.

```shell
npm install --save-dev @babel/preset-env
```

`.babelrc.json`

```json
{ 
    "presets" : ["@babel/preset-env"]
}
```

### @babel/preset-react

Babel preset for all React plugins.

```shell
npm install --save-dev @babel/preset-react
```

`.babelrc.json`

```json
{ 
    "presets": ["@babel/preset-react"]
}
```

### @babel/preset-typescript

Babel preset for TypeScript.

```shell
npm install --save-dev @babel/preset-typescript
```

`.babelrc.json`

```json
{ 
    "presets": ["@babel/preset-typescript"]
}
```

## Dependencies

### [@babel/core](https://www.npmjs.com/package/@babel/core){:target="_blank"}

Babel compiler core.

```shell
npm install --save-dev @babel/core
```

### [@babel/cli](https://www.npmjs.com/package/@babel/cli){:target="_blank"}

Babel command line.

```shell
npm install --save-dev @babel/cli
```

### [@babel/node](https://www.npmjs.com/package/@babel/node){:target="_blank"}

Babel command line.

```shell
npm install --save-dev @babel/node
```
