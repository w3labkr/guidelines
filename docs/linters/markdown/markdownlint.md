# MarkdownLint

Markdown linting and style checking for Visual Studio Code.

- [github.com/DavidAnson/vscode-markdownlint](https://github.com/DavidAnson/vscode-markdownlint){:target="_blank"}

## Integration with visual studio code

Install through vscode extensions. Search for [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint){:target="_blank"}.

**settings.json**

```json
{
    "[markdown]": {
        "editor.defaultFormatter": "DavidAnson.vscode-markdownlint",
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.fixAll.markdownlint": true
        }
    },
}
```

Format a file on save. A formatter must be available, the file must not be saved after delay, and the editor must not be shutting down.

```json
{
    "editor.formatOnSave": true,
}
```

Automatically fix violations when saving a Markdown document.

```json
{
    "editor.codeActionsOnSave": {
        "source.fixAll.markdownlint": true
    }
}
```
