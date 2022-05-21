# Black

The uncompromising Python code formatter.

- [https://black.readthedocs.io/en/stable/](https://black.readthedocs.io/en/stable/){:target="_blank"}
- [https://github.com/psf/black](https://github.com/psf/black){:target="_blank"}

## Installation

```shell
pip install black
```

## Integration with visual studio code

**settings.json**

Provider for formatting. Possible options include 'autopep8', 'black', and 'yapf'.

```json
{
    "python.formatting.provider": "black",
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