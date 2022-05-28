# MarkdownLint

Markdown linting and style checking for Visual Studio Code.

- [github.com/DavidAnson/vscode-markdownlint](https://github.com/DavidAnson/vscode-markdownlint){:target="_blank"}

## Integration with visual studio code

Install through vscode extensions. Search for [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint){:target="_blank"}.

**settings.json**

Configure settings to be overridden for the markdown language.

```json
{
    "[markdown]": {
        "editor.defaultFormatter": "DavidAnson.vscode-markdownlint",
        "editor.tabSize": 4,
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.fixAll.markdownlint": true
        }
    },
}
```
