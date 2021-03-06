# commitlint

Lint commit messages.

- [commitlint.js.org](https://commitlint.js.org/){:target="_blank"}
- [github.com/conventional-changelog/commitlint](https://github.com/conventional-changelog/commitlint){:target="_blank"}

## Usage

In general the pattern mostly looks like this:

```text
type(scope?): subject
```

scope is optional; multiple scopes are supported (current delimiter options: `"/"`, `"\"` and `","`)

```text
fix(server): send cors headers
```

Common types according to [commitlint-config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional){:target="_blank"} can be:

- build: Builds - Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- chore: Chores - Other changes that don't modify src or test files
- ci: Continuous Integrations - Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- docs: Documentation - Documentation only changes
- feat: Features - A new feature
- fix: Bug Fixes - A bug fix
- perf: Performance Improvements - A code change that improves performance
- refactor: Code Refactoring - A code change that neither fixes a bug nor adds a feature
- revert: Reverts - Reverts a previous commit
- style: Styles - Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- test: Tests - Adding missing tests or correcting existing tests

## Integration with husky

Install commitlint cli and conventional config.

```shell
npm install --save-dev @commitlint/config-conventional @commitlint/cli
```

Configure commitlint to use conventional config.

```shell
echo "module.exports = { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
```

Add hook:

```shell
cat <<EEE > .husky/commit-msg
#!/bin/sh
. "\$(dirname "\$0")/_/husky.sh"

npx --no -- commitlint --edit "\${1}"
EEE
```

Make hook executable

```shell
chmod a+x .husky/commit-msg
```

## Integration with pre-commit

A pre-commit hook for commitlint

```yaml
repos:
  - repo: https://github.com/alessandrojcm/commitlint-pre-commit-hook
    rev: v8.0.0
    hooks:
      - id: commitlint
        stages: [commit-msg]
        additional_dependencies: ['@commitlint/config-conventional']
```
