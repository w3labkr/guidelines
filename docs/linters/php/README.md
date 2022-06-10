# PHP

## Table of Contents

{% include list.liquid all=true %}

## Integration with Git Hooks

You need to install the husky and lint-staged node packages. See [here](/docs/version-control-systems/git/git-hooks.html) for more information.

```json
{
    "lint-staged": {
        "*.php": [
            "php ./vendor/bin/php-cs-fixer fix"
        ]
    }
}
```
