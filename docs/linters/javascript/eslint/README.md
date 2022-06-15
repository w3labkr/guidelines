# ESLint

Find and fix problems in your JavaScript code.

- [eslint.org](https://eslint.org/){:target="_blank"}
- [github.com/eslint/eslint](https://github.com/eslint/eslint){:target="_blank"}

## Installation

```shell
npm install --save-dev eslint eslint-config-prettier eslint-plugin-prettier
```

## Configuration

This can be in the form of an .eslintrc.* file or an eslintConfig field in a package.json file, both of which ESLint will look for and read automatically.

### ES5 (EcmaScript5)

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

Dependencies

- [eslint-config-prettier](eslint-config-prettier.html)  
   Turns off all rules that are unnecessary or might conflict with Prettier.

- [eslint-plugin-prettier](eslint-plugin-prettier.html)  
   ESLint plugin for Prettier formatting.

### ES6 (EcmaScript6)

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

Dependencies

- [eslint-plugin-import](eslint-plugin-import.html)  
   ESLint plugin with rules that help validate proper imports.

### React

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

Dependencies

- [eslint-plugin-react](eslint-plugin-react.html)  
   React specific linting rules for eslint.

- [eslint-plugin-react-hooks](eslint-plugin-react-hooks.html)  
   This ESLint plugin enforces the Rules of Hooks.

## Integration with visual studio code

Install through vscode extensions. Search for [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint){:target="_blank"}.

`settings.json`

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

Javascript requires the [husky]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/husky.html) and [lint-staged]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/lint-staged.html) packages to be installed.

```json
{
    "lint-staged": {
        "*.{js, jsx}": [
            "eslint --fix"
        ]
    }
}
```

To use Python, you need to install the [pre-commit]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/pre-commit.html) package.

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
