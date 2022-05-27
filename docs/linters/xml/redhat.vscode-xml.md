# XML

Editing XML in Visual Studio Code made easy

- [github.com/redhat-developer/vscode-xml](https://github.com/redhat-developer/vscode-xml){:target="_blank"}

## Integration with visual studio code

Install through vscode extensions. Search for [XML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml){:target="_blank"}.

**settings.json**

```json
{
    "[xml]": {
        "editor.defaultFormatter": "redhat.vscode-xml",
        "editor.formatOnSave": true
    },
}
```

Defines a default formatter which takes precedence over all other formatter settings. Must be the identifier of an extension contributing a formatter.

```json
{
    "editor.defaultFormatter": "redhat.vscode-xml",
}
```

Format a file on save. A formatter must be available, the file must not be saved after delay, and the editor must not be shutting down.

```json
{
    "editor.formatOnSave": true,
}
```
