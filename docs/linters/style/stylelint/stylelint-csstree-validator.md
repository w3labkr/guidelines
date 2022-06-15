# stylelint-csstree-validator

A stylelint plugin based on csstree to examinate CSS syntax. It examinates at-rules and declaration values to match W3C specs and browsers extensions. It might be extended in future to validate other parts of CSS.

- [github.com/csstree/stylelint-validator](https://github.com/csstree/stylelint-validator){:target="_blank"}

## Installation

```shell
npm install --save-dev stylelint-csstree-validator
```

## Configuration

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
