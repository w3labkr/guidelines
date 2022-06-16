# pre-commit

A framework for managing and maintaining multi-language pre-commit hooks.

- [pre-commit.com](https://pre-commit.com/){:target="_blank"}
- [github.com/pre-commit/pre-commit](https://github.com/pre-commit/pre-commit){:target="_blank"}

## Installation

```shell
pip install pre-commit
pre-commit sample-config > .pre-commit-config.yaml
pre-commit install
```

## Configuration

```shell
# See https://pre-commit.com for more information
# See https://pre-commit.com/hooks.html for more hooks
repos:
  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.3.0
    hooks:
      - id: trailing-whitespace
      - id: end-of-file-fixer
      - id: check-yaml
      - id: check-added-large-files
  - repo: https://github.com/psf/black
    rev: 22.3.0
    hooks:
      - id: black
```

## Supported Hooks

- [pre-commit.com/hooks.html](https://pre-commit.com/hooks.html){:target="_blank"}

## Integration with Formatter

- [black]({{ site.baseurl }}/docs/formatters/black.html#integration-with-git-hooks)  
   The uncompromising Python code formatter.

- [js-beautify]({{ site.baseurl }}/docs/formatters/js-beautify.html#integration-with-git-hooks)  
   Beautifier for javascript.

- [prettier]({{ site.baseurl }}/docs/formatters/prettier.html#integration-with-git-hooks)  
   Prettier is an opinionated code formatter.

## Integration with Linter

- [flake8]({{ site.baseurl }}/docs/linters/python/flake8.html#integration-with-git-hooks)  
   flake8 is a python tool that glues together pycodestyle, pyflakes, mccabe, and third-party plugins to check the style and quality of some python code.

- [stylelint]({{ site.baseurl }}/docs/linters/style/stylelint/#integration-with-git-hooks)  
   A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

- [eslint]({{ site.baseurl }}/docs/linters/javascript/eslint/#integration-with-git-hooks)  
   Find and fix problems in your JavaScript code.

- [commitlint](commitlint.html#integration-with-pre-commit)  
   Lint commit messages.
