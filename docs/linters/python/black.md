# Black

The uncompromising Python code formatter.

- [black.readthedocs.io/en/stable/](https://black.readthedocs.io/en/stable/){:target="_blank"}
- [github.com/psf/black](https://github.com/psf/black){:target="_blank"}

## Installation

```shell
pip install black
```

Jupyter Notebooks

```shell
pip install 'black[jupyter]'
```

## Comment

It doesn’t reformat blocks that start with # fmt: off and end with `# fmt: on`, or lines that ends with `# fmt: skip`. `# fmt: on/off` have to be on the same level of indentation.

```python
# fmt: off

j = [1,
     2,
     3
]

# fmt: on
```

## Integration with visual studio code

**settings.json**

```json
{
    "python.formatting.provider": "black",
    "python.formatting.blackArgs": ["--line-length", "88"],

    "[python]": {
        "editor.defaultFormatter": "ms-python.python",
        "editor.tabSize": 4,
        "editor.formatOnSave": true,
    },
}
```

Provider for formatting. Possible options include 'autopep8', 'black', and 'yapf'.

```json
{
    "python.formatting.provider": "black",
}
```

Arguments passed in. Each argument is as separate item in the array.

```json
{
    "python.formatting.blackArgs": ["--line-length", "88"],
}
```

Configure settings to be overridden for the python language.

```json
{
    "[python]": {
        "editor.defaultFormatter": "ms-python.python",
        "editor.tabSize": 4,
        "editor.formatOnSave": true,
    },
}
```

## Integration with Git Hooks

You need to install the pre-commit python packages. See [here]({{ site.baseurl }}/docs/version-control-systems/git/pre-commit.html) for more information.

```yaml
repos:
  - repo: https://github.com/psf/black
    rev: 22.3.0
    hooks:
      - id: black
        language_version: python3.9
        args: ["--line-length=88"]
```
