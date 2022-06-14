# XML

Editing XML in Visual Studio Code made easy

- [github.com/redhat-developer/vscode-xml](https://github.com/redhat-developer/vscode-xml){:target="_blank"}

## Integration with visual studio code

Install through vscode extensions. Search for [XML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml){:target="_blank"}.

`settings.json`

Configure settings to be overridden for the xml language.

```json
{
    "[xml]": {
        "editor.defaultFormatter": "redhat.vscode-xml",
        "editor.tabSize": 4,
        "editor.formatOnSave": true
    },
}
```
