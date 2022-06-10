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

## Table of Contents

{% include list.liquid all=true %}

## Integration with visual studio code

Install through vscode extensions. Search for [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint){:target="_blank"}.

**settings.json**

```json
{
    "javascript.format.enable": false,
    "javascript.validate.enable": false,

    "eslint.format.enable": true,
    "eslint.validate": ["javascript", "javascriptreact"],

    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
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
    "eslint.validate": ["javascript", "javascriptreact"],
}
```

Configure settings to be overridden for the javascript language.

```json
{
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        },
    },
}
```

## Integration with Git Hooks

You need to install the husky and lint-staged node packages. See [here]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks.html) for more information.

```json
{
    "lint-staged": {
        "*.{js, jsx}": [
            "eslint --fix"
        ]
    }
}
```

You need to install the pre-commit python packages. See [here]({{ site.baseurl }}/docs/version-control-systems/git/pre-commit.html) for more information.

```yaml
repos:
  - repo: https://github.com/pre-commit/mirrors-eslint
    rev: v8.17.0
    hooks:
      - id: eslint
        additional_dependencies:
          - eslint@8.13.0
          - eslint-config-prettier@8.5.0
          - eslint-plugin-import@2.26.0
          - eslint-plugin-prettier@4.0.0
        language: node
        files: \.(js|jsx)$
        types: [file]
        args: ["--fix"]
```
