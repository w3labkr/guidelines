# pre-commit

A framework for managing and maintaining multi-language pre-commit hooks.

- [pre-commit.com/](https://pre-commit.com/){:target="_blank"}
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
