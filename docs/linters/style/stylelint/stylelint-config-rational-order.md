# stylelint-config-rational-order

Stylelint config that sorts related property declarations by grouping together in the rational order.

- [github.com/constverum/stylelint-config-rational-order](https://github.com/constverum/stylelint-config-rational-order){:target="_blank"}

## Installation

```shell
npm install --save-dev stylelint-order stylelint-config-rational-order
```

## Configuration

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
