# eslint-plugin-react-hooks

This ESLint plugin enforces the Rules of Hooks.

- [github.com/facebook/react](https://github.com/facebook/react){:target="_blank"}

## Installation

```shell
npm install --save-dev eslint-plugin-react-hooks
```

## Configuration

```json
{
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        }
    },
    "extends": [
        "plugin:react-hooks/recommended"
    ],
}
```
