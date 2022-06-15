# eslint-config-prettier

Turns off all rules that are unnecessary or might conflict with Prettier.

- [github.com/prettier/eslint-config-prettier](https://github.com/prettier/eslint-config-prettier){:target="_blank"}

## Installation

```shell
npm install --save-dev eslint-config-prettier
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
