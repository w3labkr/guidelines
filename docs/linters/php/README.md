# PHP

## Table of Contents

{% include list.liquid all=true %}

## Integration with Git Hooks

Javascript requires the [husky]({{ site.baseurl }}/docs/version-control-systems/git/husky.html) and [lint-staged]({{ site.baseurl }}/docs/version-control-systems/git/lint-staged.html) packages to be installed.

```json
{
    "lint-staged": {
        "*.php": [
            "php ./vendor/bin/php-cs-fixer fix"
        ]
    }
}
```
