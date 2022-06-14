# Format HTML in PHP

Provides formatting for the HTML code in PHP files using JSbeautify - Works well paired with a PHP.

- [github.com/RiFi2k/format-html-in-php](https://github.com/RiFi2k/format-html-in-php){:target="_blank"}

## Integration with visual studio code

Install through vscode extensions. Search for [Format HTML in PHP](https://marketplace.visualstudio.com/items?itemName=rifi2k.format-html-in-php){:target="_blank"}.

`settings.json`

```json
{
    "html.format.enable": true,
    "html.format.contentUnformatted": "wbr,pre,code,textarea,style,script",
    "html.format.endWithNewline": true,
    "html.format.extraLiners": "head, body, /html",
    "html.format.indentHandlebars": false,
    "html.format.indentInnerHtml": false,
    "html.format.maxPreserveNewLines": null,
    "html.format.preserveNewLines": true,
    "html.format.wrapLineLength": 120,
    "html.format.wrapAttributes": "auto",
}
```

Enable/disable default HTML formatter.

```json
{
    "html.format.enable": true,
}
```

List of tags, comma separated, where the content shouldn't be reformatted. `null` defaults to the `pre` tag.

```json
{
    "html.format.contentUnformatted": "wbr,pre,code,textarea,style,script",
}
```

End with a newline.

```json
{
    "html.format.endWithNewline": true,
}
```

List of tags, comma separated, that should have an extra newline before them. `null` defaults to `"head, body, /html"`.

```json
{
    "html.format.extraLiners": "head, body, /html",
}
```

Format and indent `{{#foo}}` and `{{/foo}}`.

```json
{
    "html.format.indentHandlebars": false,
}
```

Indent `<head>` and `<body>` sections.

```json
{
    "html.format.indentInnerHtml": false,
}
```

Maximum number of line breaks to be preserved in one chunk. Use `null` for unlimited.

```json
{
    "html.format.maxPreserveNewLines": null,
}
```

Controls whether existing line breaks before elements should be preserved. Only works before elements, not inside tags or for text.

```json
{
    "html.format.preserveNewLines": true,
}
```

Maximum amount of characters per line (0 = disable).

```json
{
    "html.format.wrapLineLength": 120,
}
```

Wrap attributes.

```json
{
    "html.format.wrapAttributes": "auto",
}
```
