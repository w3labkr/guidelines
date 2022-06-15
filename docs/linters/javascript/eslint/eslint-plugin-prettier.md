# eslint-plugin-prettier

ESLint plugin for Prettier formatting.

- [github.com/prettier/eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier){:target="_blank"}

## Installation

```shell
npm install --save-dev eslint-plugin-prettier
```

## Configuration

Make sure to put it last, so it gets the chance to override other configs.

```json
{
  "extends": [
    "eslint:recommended",
    "plugin:prettier/recommended"
  ]
}
```
