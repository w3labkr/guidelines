# React

## Installation

```shell
npm install --save-dev eslint eslint-config-prettier eslint-plugin-prettier eslint-plugin-import eslint-plugin-react eslint-plugin-react-hooks
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
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        }
    },
    "extends": [
        "eslint:recommended",
        "plugin:import/recommended",
        "plugin:react/recommended",
        "plugin:react-hooks/recommended",
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

### [eslint-plugin-react](https://www.npmjs.com/package/eslint-plugin-react){:target="_blank"}

React specific linting rules for eslint

```shell
npm install --save-dev eslint-plugin-react
```

```json
{
  "extends": ["plugin:react/recommended"]
}
```

### [eslint-plugin-react-hooks](https://www.npmjs.com/package/eslint-plugin-react-hooks){:target="_blank"}

eslint-plugin-react-hooks

```shell
npm install --save-dev eslint-plugin-react-hooks
```

```json
{
  "extends": ["plugin:react-hooks/recommended"]
}
```
