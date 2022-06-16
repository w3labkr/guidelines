# lint-staged

Run linters on git staged files.

- [github.com/okonet/lint-staged](https://github.com/okonet/lint-staged){:target="_blank"}

## Dependency

- [Husky](husky.html) is a popular choice for configuring git hooks.

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

- [js-beautify]({{ site.baseurl }}/docs/formatters/js-beautify.html#integration-with-git-hooks)  
   Beautifier for javascript.

- [prettier]({{ site.baseurl }}/docs/formatters/prettier.html#integration-with-git-hooks)  
   Prettier is an opinionated code formatter.

## Integration with Linter

- [stylelint]({{ site.baseurl }}/docs/linters/style/stylelint/#integration-with-git-hooks)  
   A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

- [eslint]({{ site.baseurl }}/docs/linters/javascript/eslint/#integration-with-git-hooks)  
   Find and fix problems in your JavaScript code.

- [php-cs-fixer]({{ site.baseurl }}/docs/linters/php/php-cs-fixer.html#integration-with-git-hooks)  
   A tool to automatically fix PHP Coding Standards issues.

- [commitlint](commitlint.html#integration-with-pre-commit)  
   Lint commit messages.
