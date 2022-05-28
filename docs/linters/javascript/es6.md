# ES6 (ECMAScript6)

## Installation

```shell
npm install --save-dev eslint eslint-config-prettier eslint-plugin-prettier eslint-plugin-import
```

## Configuration

```json
{
    "env": {
        "browser": true,
        "node": true
    },
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module"
    },
    "extends": [
        "eslint:recommended",
        "plugin:import/recommended",
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

### [eslint-plugin-import](https://www.npmjs.com/package/eslint-plugin-import){:target="_blank"}

ESLint plugin with rules that help validate proper imports.

```shell
npm install --save-dev eslint-plugin-import
```

```json
{
  "extends": ["plugin:import/recommended"]
}
```
