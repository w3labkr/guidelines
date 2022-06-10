---
sort: 9
---

# Linters

## Table of Contents

{% include list.liquid all=true %}

## Integration with Git Hooks

You need to install the husky and lint-staged node packages. See [here]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks.html) for more information.

```json
{
    "lint-staged": {
        "*.{css, scss, less, postcss}": [
            "stylelint --fix"
        ],
        "*.{js, jsx}": [
            "eslint --fix"
        ],
        "*.php": [
            "php ./vendor/bin/php-cs-fixer fix"
        ]
    }
}
```
