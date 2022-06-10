# Git Hooks

Like many other Version Control Systems, Git has a way to fire off custom scripts when certain important actions occur.

[git-scm.com/book/en/v2/Customizing-Git-Git-Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks){:target="_blank"}

## Installation

```shell
npm install --save-dev husky lint-staged
npm set-script prepare "husky install" && npm run prepare
npx husky add .husky/pre-commit "npx lint-staged --allow-empty"
```

```shell
npm install && npm run prepare
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

## Dependencies

### [husky](https://www.npmjs.com/package/husky){:target="_blank"}

Git hooks made easy 🐶 woof!

```shell
npm install --save-dev husky
```

```json
{
    "husky": {
        "hooks": {
            "pre-commit": "lint-staged"
        }
    }
}
```

### [lint-staged](https://www.npmjs.com/package/lint-staged){:target="_blank"}

Run linters on git staged files.

```shell
npm install --save-dev lint-staged
```

Prior to version 10, tasks had to manually include git add as the final step. This behavior has been integrated into lint-staged itself in order to prevent race conditions with multiple tasks editing the same files. If lint-staged detects git add in task configurations, it will show a warning in the console. Please remove git add from your configuration after upgrading.

Bad

```json
{
    "lint-staged": {"*.js": ["eslint --fix", "git add"]}
}
```

Good

```json
{
    "lint-staged": {"*.js": ["eslint --fix"]}
}
```
