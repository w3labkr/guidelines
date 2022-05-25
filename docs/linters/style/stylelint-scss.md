# SCSS

## Installation

```shell
```

## Configuration

```shell
```

## Dependencies

### [dependency](dependency){:target="_blank"}

```shell
```

```json
```


## Integration with visual studio code

Install through vscode extensions. Search for [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint){:target="_blank"}.

**settings.json**

```json
{
    "scss.validate": false,
    "scss.lint.emptyRules": "ignore",
    "scss.lint.unknownProperties": "ignore",

    "stylelint.enable": true,
    "stylelint.validate": ["css", "scss", "less", "postcss"],
    "stylelint.snippet": ["css", "scss", "less", "postcss"],

    "[scss]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
}
```

Enables or disables all validations.

```json
{
    "scss.validate": false,
}
```

Do not use empty rulesets.

```json
{
    "scss.lint.emptyRules": "ignore",
}
```

Unknown property.

```json
{
    "scss.lint.unknownProperties": "ignore",
}
```

Control whether Stylelint is enabled or not.

```json
{
    "stylelint.enable": true,
}
```

An array of language ids which should be validated by Stylelint.

```json
{
    "stylelint.validate": ["css", "scss", "less", "postcss"],
}
```

An array of language ids which snippets are provided by Stylelint.

```json
{
    "stylelint.snippet": ["css", "scss", "less", "postcss"],
}
```

Configure settings to be overridden for the scss language.

```json
{
    "[scss]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
}
```

## Troubleshooting

```shell
```
