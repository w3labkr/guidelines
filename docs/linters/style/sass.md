# SASS (SCSS)

## Installation

```shell
npm install --save-dev prettier stylelint stylelint-scss stylelint-config-recommended-scss stylelint-config-prettier-scss stylelint-order stylelint-config-rational-order
```

## Configuration

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

## Dependencies

### [stylelint-scss](https://www.npmjs.com/package/stylelint-scss){:target="_blank"}

A collection of SCSS specific linting rules for Stylelint

```shell
npm install stylelint-scss
```

```json
{
  "plugins": [
    "stylelint-scss"
  ],
  "rules": {
    "at-rule-no-unknown": null,
    "scss/at-rule-no-unknown": true,
  }
}
```

### [stylelint-config-recommended-scss](https://www.npmjs.com/package/stylelint-config-recommended-scss){:target="_blank"}

The recommended shareable SCSS config for stylelint.

```shell
npm install --save-dev stylelint-config-recommended-scss
```

```json
{
  "extends": "stylelint-config-recommended-scss"
}
```

### [stylelint-config-prettier-scss](https://www.npmjs.com/package/stylelint-config-prettier-scss){:target="_blank"}

Turns off all CSS and SCSS rules that are unnecessary or might conflict with Prettier (extends stylelint-config-prettier).

```shell
npm install --save-dev stylelint-config-prettier-scss
```

Make sure to put it last, so it will override other configs.

```json
{
  "extends": [
    // other configs ...
    "stylelint-config-prettier-scss"
  ]
}
```

### [stylelint-order](https://www.npmjs.com/package/stylelint-order){:target="_blank"}

A plugin pack of order related linting rules for Stylelint.

```shell
npm install --save-dev stylelint-order
```

```json
{
    "plugins": [
        "stylelint-order"
    ],
    "rules": {
        "order/order": [],
    },
}
```

### [stylelint-config-rational-order](https://www.npmjs.com/package/stylelint-config-rational-order){:target="_blank"}

Stylelint config that sorts related property declarations by grouping together in the rational order.

```shell
npm install --save-dev stylelint-order stylelint-config-rational-order
```

```json
{
    "extends": [
        "stylelint-config-rational-order"
    ],
    "plugins": [
        "stylelint-order",
        "stylelint-config-rational-order/plugin"
    ],
    "rules": {
        "order/properties-order": [],
        "plugin/rational-order": [
            true,
            {
                "border-in-box-model": true,
                "empty-line-between-groups": true
            }
        ],
    }
}
```

## Rules

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

**settings.json**

```json
{
    "stylelint.enable": true,
    "stylelint.validate": ["css", "scss", "less", "postcss"],
    "stylelint.snippet": ["css", "scss", "less", "postcss"],

    "scss.validate": false,
    "scss.lint.emptyRules": "ignore",
    "scss.lint.unknownProperties": "ignore",

    "[scss]": {
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
    "scss.validate": false,
}
```

Do not use empty rulesets.

```json
{
    "scss.lint.emptyRules": "ignore",
}
```

Unknown property.

```json
{
    "scss.lint.unknownProperties": "ignore",
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

Configure settings to be overridden for the scss language.

```json
{
    "[scss]": {
        "editor.formatOnSave": false,
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
}
```
