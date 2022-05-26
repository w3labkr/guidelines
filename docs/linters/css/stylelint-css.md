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
                "empty-line-between-groups": false
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
        "order/properties-order": []
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
        "order/order": [],
        "order/properties-order": [],
        "plugin/rational-order": [
            true,
            {
                "border-in-box-model": true,
                "empty-line-between-groups": false
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
        "block-no-empty": null,
        "property-no-vendor-prefix": null
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
