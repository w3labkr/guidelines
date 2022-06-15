# Stylelint

A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

- [stylelint.io](https://stylelint.io/){:target="_blank"}
- [github.com/stylelint/stylelint](https://github.com/stylelint/stylelint){:target="_blank"}

## Installation

```shell
npm install --save-dev stylelint
```

## Configuration

The .stylelintrc file (without extension) can be in JSON or YAML format.

## CSS

Installation

```shell
npm install --save-dev prettier stylelint stylelint-config-prettier stylelint-config-rational-order stylelint-config-recommended stylelint-config-styled-components stylelint-csstree-validator stylelint-order stylelint-prettier 
```

Configuration

```json
{
    "extends": [
        "stylelint-config-recommended",
        "stylelint-config-styled-components",
        "stylelint-config-rational-order",
        "stylelint-prettier/recommended"
    ],
    "plugins": [
        "stylelint-csstree-validator",
        "stylelint-order",
        "stylelint-config-rational-order/plugin"
    ],
    "ignoreFiles": [
        "**/*.js",
        "**/*.min.css"
    ],
    "rules": {
        "csstree/validator": true,
        "order/order": [],
        "order/properties-order": [],
        "plugin/rational-order": [
            true,
            {
                "border-in-box-model": true,
                "empty-line-between-groups": true
            }
        ],
        "block-no-empty": null,
        "property-no-vendor-prefix": null
    }
}
```

Dependencies

- [stylelint-config-recommended](stylelint-config-recommended.html)  
   The recommended shareable config for Stylelint.

- [stylelint-config-styled-components](stylelint-config-styled-components.html)  
   The shareable stylelint config for stylelint-processor-styled-components.

- [stylelint-order](stylelint-order.html)  
   A plugin pack of order related linting rules for Stylelint.

- [stylelint-config-rational-order](stylelint-config-rational-order.html)  
   Stylelint config that sorts related property declarations by grouping together in the rational order.

- [stylelint-prettier](stylelint-prettier.html)  
   Stylelint plugin for Prettier formatting.

- [stylelint-config-prettier](stylelint-config-prettier.html)  
   Turns off all rules that are unnecessary or might conflict with prettier. Make sure to put it last, so it will override other configs.

- [stylelint-csstree-validator](stylelint-csstree-validator.html)  
   A stylelint plugin based on csstree to examinate CSS syntax. It examinates at-rules and declaration values to match W3C specs and browsers extensions. It might be extended in future to validate other parts of CSS.

Disallow empty blocks.

```json
{
    "rules": {
        "block-no-empty": null
    }
}
```

Disallow vendor prefixes for properties.

```json
{
    "rules": {
        "property-no-vendor-prefix": null
    }
}
```

## SASS (SCSS)

Installation

```shell
npm install --save-dev prettier stylelint stylelint-scss stylelint-config-recommended-scss stylelint-config-prettier-scss stylelint-order stylelint-config-rational-order
```

Configuration

```json
{
    "extends": [
        "stylelint-config-recommended-scss",
        "stylelint-config-rational-order",
        "stylelint-config-prettier-scss"
    ],
    "plugins": [
        "stylelint-scss",
        "stylelint-order",
        "stylelint-config-rational-order/plugin"
    ],
    "ignoreFiles": [
        "**/*.js",
        "**/*.css"
    ],
    "rules": {
        "order/order": [],
        "order/properties-order": [],
        "plugin/rational-order": [
            true,
            {
                "border-in-box-model": true,
                "empty-line-between-groups": true
            }
        ],
        "at-rule-no-unknown": null,
        "scss/at-rule-no-unknown": true,
        "string-quotes": "single",
        "indentation": 2
    }
}
```

Dependencies

- [stylelint-scss](stylelint-scss.html)  
   A collection of SCSS specific linting rules for Stylelint.

- [stylelint-config-recommended-scss](stylelint-config-recommended-scss.html)  
   The recommended shareable SCSS config for stylelint.

- [stylelint-config-prettier-scss](stylelint-config-prettier-scss.html)  
   Turns off all CSS and SCSS rules that are unnecessary or might conflict with Prettier (extends stylelint-config-prettier).  

- [stylelint-order](stylelint-order.html)  
   A plugin pack of order related linting rules for Stylelint.

- [stylelint-config-rational-order](stylelint-config-rational-order.html)  
   Stylelint config that sorts related property declarations by grouping together in the rational order.

Disallow unknown at-rules.

```json
{
    "rules": {
        "at-rule-no-unknown": null,
        "scss/at-rule-no-unknown": true,
    }
}
```

Specify single or double quotes around strings.

```json
{
    "rules": {
        "string-quotes": "single",
    }
}
```

Specify indentation.

```json
{
    "rules": {
        "indentation": 2
    }
}
```

## Integration with visual studio code

Install through vscode extensions. Search for [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint){:target="_blank"}.

`settings.json`

```json
{
    "stylelint.enable": true,
    "stylelint.validate": ["css", "scss", "less", "postcss"],
    "stylelint.snippet": ["css", "scss", "less", "postcss"],

    "css.validate": false,
    "css.lint.emptyRules": "ignore",
    "css.lint.unknownProperties": "ignore",

    "[css]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },

    "scss.validate": false,
    "scss.lint.emptyRules": "ignore",
    "scss.lint.unknownProperties": "ignore",

    "[scss]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
}
```

Enables or disables all validations.

```json
{
    "css.validate": false,
}
```

Do not use empty rulesets.

```json
{
    "css.lint.emptyRules": "ignore",
}
```

Unknown property.

```json
{
    "css.lint.unknownProperties": "ignore",
}
```

Control whether Stylelint is enabled or not.

```json
{
    "stylelint.enable": true,
}
```

An array of language ids which should be validated by Stylelint.

```json
{
    "stylelint.validate": ["css", "scss", "less", "postcss"],
}
```

An array of language ids which snippets are provided by Stylelint.

```json
{
    "stylelint.snippet": ["css", "scss", "less", "postcss"],
}
```

Configure settings to be overridden for the css language.

```json
{
    "[css]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
}
```

## Integration with Git Hooks

Javascript requires the [husky]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/husky.html) and [lint-staged]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/lint-staged.html) packages to be installed.

```json
{
    "lint-staged": {
        "*.{css, scss, less, postcss}": [
            "stylelint --fix"
        ]
    }
}
```

To use Python, you need to install the [pre-commit]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/pre-commit.html) package.

```yaml
repos:
  - repo: https://github.com/awebdeveloper/pre-commit-stylelint
    rev: 0.0.2
    hooks:
      - id: stylelint
        additional_dependencies:
          [
            "stylelint@14.7.1",
            "stylelint-config-prettier@9.0.3",
            "stylelint-config-rational-order@0.1.2",
            "stylelint-config-recommended@7.0.0",
            "stylelint-config-styled-components@0.1.1",
            "stylelint-csstree-validator@2.0.0",
            "stylelint-order@5.0.0",
            "stylelint-prettier@2.0.0",
          ]
        language: node
        files: \.(css|scss|sass)$
        args: ["--fix"]
```

## Troubleshooting

Cannot find module 'prettier' Require stack

```shell
npm install --save-dev prettier stylelint-prettier
```

Stylelint: Could not find "stylelint-config-prettier". Do you need a `configBasedir`?

```shell
npm install --save-dev stylelint-csstree-validator
```
