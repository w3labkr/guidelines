# Style

## Stylelint

A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

- [stylelint.io/](https://stylelint.io/){:target="_blank"}
- [github.com/stylelint/stylelint](https://github.com/stylelint/stylelint){:target="_blank"}

## Installation

```shell
npm install --save-dev stylelint
```

## Configuration

The .stylelintrc file (without extension) can be in JSON or YAML format.

{% include list.liquid all=true %}

## Integration with visual studio code

Install through vscode extensions. Search for [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint){:target="_blank"}.

**settings.json**

Enables or disables all validations.

```json
{
    "css.validate": false,
    "scss.validate": false,
    "less.validate": false,
}
```

Do not use empty rulesets.

```json
{
    "css.lint.emptyRules": "ignore",
    "scss.lint.emptyRules": "ignore",
    "less.lint.emptyRules": "ignore",
}
```

Unknown property.

```json
{
    "css.lint.unknownProperties": "ignore",
    "scss.lint.unknownProperties": "ignore",
    "less.lint.unknownProperties": "ignore",
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

Configure settings to be overridden for the css language.

```json
{
    "[css]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
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

Configure settings to be overridden for the less language.

```json
{
    "[less]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.stylelint": true
        }
    },
}
```
