# Flake8

flake8 is a python tool that glues together pycodestyle, pyflakes, mccabe, and third-party plugins to check the style and quality of some python code.

- [flake8.pycqa.org](https://flake8.pycqa.org){:target="_blank"}
- [github.com/PyCQA/flake8](https://github.com/PyCQA/flake8){:target="_blank"}

## Installation

```shell
pip install flake8
```

## Configuration

Minimal black compatible flake8 configuration.

```text
[flake8]
max-line-length = 88
extend-ignore = E203
```

## Integration with visual studio code

**settings.json**

```json
{
    "python.linting.flake8Enabled": true,
    "python.linting.enabled": true,
    "python.linting.lintOnSave": true,
}
```

Whether to lint Python files using flake8

```json
{
    "python.linting.flake8Enabled": true,
}
```

Whether to lint Python files.

```json
{
    "python.linting.enabled": true,
}
```

Whether to lint Python files when saved.

```json
{
    "python.linting.lintOnSave": true,
}
```

## Integration with Git Hooks

You need to install the pre-commit python packages. See [here](/docs/version-control-systems/git/pre-commit.html) for more information.

```yaml
repos:
  - repo: https://gitlab.com/pycqa/flake8
    rev: 3.9.2
    hooks:
      - id: flake8
```
