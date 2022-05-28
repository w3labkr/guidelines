# ES5 (ECMAScript5)

## Installation

```shell
npm install --save-dev eslint eslint-config-prettier eslint-plugin-prettier
```

## Configuration

```json
{
    "env": {
        "browser": true,
        "node": true
    },
    "parserOptions": {
        "ecmaVersion": 5,
        "sourceType": "script"
    },
    "extends": [
        "eslint:recommended",
        "plugin:prettier/recommended"
    ],
    "ignorePatterns": [
        "**/*.min.js"
    ],
    "rules": {
        "prettier/prettier": "error",
        "arrow-body-style": "off",
        "prefer-arrow-callback": "off",
        "no-unused-vars": "off",
        "no-shadow-restricted-names": "off"
    }
}
```

## Dependencies

### [eslint-config-prettier](https://www.npmjs.com/package/eslint-config-prettier){:target="_blank"}

Turns off all rules that are unnecessary or might conflict with Prettier.

```shell
npm install --save-dev eslint-config-prettier
```

Make sure to put it last, so it gets the chance to override other configs.

```json
{
  "extends": ["plugin:prettier/recommended"]
}
```

### [eslint-plugin-prettier](https://www.npmjs.com/package/eslint-plugin-prettier){:target="_blank"}

ESLint plugin for Prettier formatting.

```shell
npm install --save-dev eslint-plugin-prettier
```

Make sure to put it last, so it gets the chance to override other configs.

```json
{
  "extends": ["plugin:prettier/recommended"]
}
```
