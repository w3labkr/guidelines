# lint-staged

Run linters on git staged files.

- [github.com/okonet/lint-staged](https://github.com/okonet/lint-staged){:target="_blank"}

## Dependency

[Husky](husky.html) is a popular choice for configuring git hooks.

## Installation

```shell
npm install --save-dev lint-staged
```

Add a hook:

```shell
npx husky add .husky/pre-commit "npx lint-staged --allow-empty"
```

## Configuration

```json
{
    "husky": {
        "hooks": {
            "pre-commit": "lint-staged"
        }
    },
    "lint-staged": {}
}
```

Prior to version 10, tasks had to manually include git add as the final step. This behavior has been integrated into lint-staged itself in order to prevent race conditions with multiple tasks editing the same files. If lint-staged detects git add in task configurations, it will show a warning in the console. Please remove git add from your configuration after upgrading.

Bad

```json
{
    "lint-staged": {
        "*.js": ["eslint --fix", "git add"]
    }
}
```

Good

```json
{
    "lint-staged": {
        "*.js": ["eslint --fix"]
    }
}
```

## Integration with Formatter

- [js-beautify]({{ site.baseurl }}/docs/formatters/js-beautify.html)
- [prettier]({{ site.baseurl }}/docs/formatters/prettier.html)

## Integration with Linter

- [stylelint]({{ site.baseurl }}/docs/linters/style/README.html)
- [eslint]({{ site.baseurl }}/docs/linters/javascript/README.html)
- [php-cs-fixer]({{ site.baseurl }}/docs/linters/php/php-cs-fixer.html)
