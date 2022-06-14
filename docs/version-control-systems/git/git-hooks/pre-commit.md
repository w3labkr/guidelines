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

[pre-commit.com/hooks.html](https://pre-commit.com/hooks.html){:target="_blank"}

## Integration with Formatter

- [black]({{ site.baseurl }}/docs/formatters/black.html#integration-with-git-hooks)
- [js-beautify]({{ site.baseurl }}/docs/formatters/js-beautify.html#integration-with-git-hooks)
- [prettier]({{ site.baseurl }}/docs/formatters/prettier.html#integration-with-git-hooks)

## Integration with Linter

- [flake8]({{ site.baseurl }}/docs/linters/python/flake8.html#integration-with-git-hooks)
- [style]({{ site.baseurl }}/docs/linters/style/#integration-with-git-hooks)
- [Javascript]({{ site.baseurl }}/docs/linters/javascript/#integration-with-git-hooks)
- [commitlint](commitlint.html#integration-with-pre-commit)
