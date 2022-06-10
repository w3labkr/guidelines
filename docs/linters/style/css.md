# CSS

## Installation

```shell
npm install --save-dev prettier stylelint stylelint-config-prettier stylelint-config-rational-order stylelint-config-recommended stylelint-config-styled-components stylelint-csstree-validator stylelint-order stylelint-prettier 
```

## Configuration

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

## Dependencies

### [stylelint-config-recommended](https://www.npmjs.com/package/stylelint-config-recommended){:target="_blank"}

The recommended shareable config for Stylelint

```shell
npm install --save-dev stylelint-config-recommended
```

```json
{
    "extends": [
        "stylelint-config-recommended"
    ],
}
```

### [stylelint-config-styled-components](https://www.npmjs.com/package/stylelint-config-styled-components){:target="_blank"}

The shareable stylelint config for stylelint-processor-styled-components

```shell
npm install --save-dev stylelint-config-styled-components
```

```json
{
    "extends": [
        "stylelint-config-styled-components",
    ],
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

### [stylelint-prettier](https://www.npmjs.com/package/stylelint-prettier){:target="_blank"}

Stylelint plugin for Prettier formatting

```shell
npm install --save-dev prettier stylelint-prettier
```

```json
{
    "extends": [
        "stylelint-prettier/recommended"
    ]
}
```

### [stylelint-config-prettier](https://www.npmjs.com/package/stylelint-config-prettier){:target="_blank"}

Turns off all rules that are unnecessary or might conflict with prettier. Make sure to put it last, so it will override other configs.

```shell
npm install --save-dev stylelint-config-prettier
```

```json
{
  "extends": ["stylelint-prettier/recommended"]
}
```

### [stylelint-csstree-validator](https://www.npmjs.com/package/stylelint-csstree-validator){:target="_blank"}

A stylelint plugin based on csstree to examinate CSS syntax. It examinates at-rules and declaration values to match W3C specs and browsers extensions. It might be extended in future to validate other parts of CSS.

```shell
npm install --save-dev stylelint-csstree-validator
```

```json
{
    "plugins": [
        "stylelint-csstree-validator"
    ],
    "rules": {
        "csstree/validator": true
    }
}
```

## Rules

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

## Troubleshooting

Cannot find module 'prettier' Require stack

```shell
npm install --save-dev prettier stylelint-prettier
```

Stylelint: Could not find "stylelint-config-prettier". Do you need a `configBasedir`?

```shell
npm install --save-dev stylelint-csstree-validator
```

## Integration with visual studio code

Install through vscode extensions. Search for [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint){:target="_blank"}.

**settings.json**

```json
{
    "stylelint.enable": true,
    "stylelint.validate": ["css", "less", "postcss"],
    "stylelint.snippet": ["css", "less", "postcss"],

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
    "stylelint.validate": ["css", "less", "postcss"],
}
```

An array of language ids which snippets are provided by Stylelint.

```json
{
    "stylelint.snippet": ["css", "less", "postcss"],
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
