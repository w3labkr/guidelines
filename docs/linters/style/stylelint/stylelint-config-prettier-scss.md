# stylelint-config-prettier-scss

Turns off all CSS and SCSS rules that are unnecessary or might conflict with Prettier (extends stylelint-config-prettier).

- [github.com/prettier/stylelint-config-prettier-scss](https://github.com/prettier/stylelint-config-prettier-scss){:target="_blank"}

## Installation

```shell
npm install --save-dev stylelint-config-prettier-scss
```

## Configuration

Make sure to put it last, so it will override other configs.

```json
{
  "extends": [
    // other configs ...
    "stylelint-config-prettier-scss"
  ]
}
```
