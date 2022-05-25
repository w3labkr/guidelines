# Javascript

## ESLint

Find and fix problems in your JavaScript code.

- [eslint.org/](https://eslint.org/){:target="_blank"}
- [github.com/eslint/eslint](https://github.com/eslint/eslint){:target="_blank"}

## Installation

```shell
npm install --save-dev eslint
```

## Configuration

This can be in the form of an .eslintrc.* file or an eslintConfig field in a package.json file, both of which ESLint will look for and read automatically.

{% include list.liquid all=true %}

## Integration with visual studio code

Install through vscode extensions. Search for [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint){:target="_blank"}.

**settings.json**

```json
{
    "javascript.format.enable": false,
    "javascript.validate.enable": false,

    "eslint.format.enable": true,
    "eslint.validate": ["javascript", "javascriptreact", "typescript", "typescriptreact"],

    "[javascript]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        },
    },
}
```

Enable/disable default JavaScript formatter.

```json
{
    "javascript.format.enable": false,
}
```

Enable/disable JavaScript validation.

```json
{
    "javascript.validate.enable": false,
}
```

Enables ESLint as a formatter.

```json
{
    "eslint.format.enable": true,
}
```

An array of language ids which should be validated by ESLint. If not installed ESLint will show an error.

```json
{
    "eslint.validate": ["javascript", "javascriptreact", "typescript", "typescriptreact"],
}
```

Configure settings to be overridden for the javascript language.

```json
{
    "[javascript]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        },
    },
}
```
