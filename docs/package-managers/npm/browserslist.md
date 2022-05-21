# Browserslist

Share target browsers between different front-end tools, like Autoprefixer, Stylelint and babel-preset-env.

- [browserslist.dev/](https://browserslist.dev/){:target="_blank"}
- [www.npmjs.com/package/browserslist](https://www.npmjs.com/package/browserslist){:target="_blank"}

## Installation

```shell
npm install --save-dev browserslist
```

## Configuration

package.json

```json
{
    "browserslist": [
        "> 0.5%",
        "last 2 versions",
        "Firefox ESR",
        "not dead"
    ]
}
```

.browserslistrc

```text
# Browsers that we support

> 0.5%
last 2 versions
Firefox ESR
not dead
```
