# SCSS

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
        "string-quotes": "single"
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
        "string-quotes": "single"
    }
}
```
