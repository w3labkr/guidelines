# eslint-plugin-react

React specific linting rules for eslint.

- [github.com/jsx-eslint/eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react){:target="_blank"}

## Installation

```shell
npm install --save-dev eslint-plugin-react
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
        "plugin:react/recommended"
    ],
}
```
