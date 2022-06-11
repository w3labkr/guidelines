# JS-Beautify

Beautifier for javascript.

- [beautifier.io](https://beautifier.io/){:target="_blank"}
- [github.com/beautify-web/js-beautify](https://github.com/beautify-web/js-beautify){:target="_blank"}

## Installation

```shell
npm install --save-dev js-beautify
```

## Configuration

Loading settings from environment or .jsbeautifyrc

```json
{
    "indent_size": 2,
    "indent_char": " ",
    "indent_with_tabs": false,
    "editorconfig": false,
    "eol": "\n",
    "end_with_newline": false,
    "indent_level": 0,
    "preserve_newlines": true,
    "max_preserve_newlines": 10,
    "space_in_paren": false,
    "space_in_empty_paren": false,
    "jslint_happy": false,
    "space_after_anon_function": false,
    "space_after_named_function": false,
    "brace_style": "collapse",
    "unindent_chained_methods": false,
    "break_chained_methods": false,
    "keep_array_indentation": false,
    "unescape_strings": false,
    "wrap_line_length": 120,
    "e4x": false,
    "comma_first": false,
    "operator_position": "before-newline",
    "indent_empty_lines": false,
    "templating": ["auto"],
    "unformatted": ["wbr", "pre", "code", "textarea", "style", "script"]
}
```

## Integration with visual studio code

Install through vscode extensions. Search for [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify){:target="_blank"}.

**settings.json**

```json
{
    "html.validate.styles": false,
    "html.validate.scripts": false,
    "html.format.enable": false,

    "beautify.language": {
        "html": ["htm", "html", "ejs", "jinja"]
    },
    "beautify.ignore": ["*.css", "*.js", "*.jsx", "*.ts", "*.tsx"],

    "[html]": {
        "editor.defaultFormatter": "HookyQR.beautify",
        "editor.tabSize": 2,
        "editor.formatOnSave": true
    },
}
```

Controls whether the built-in HTML language support validates embedded styles.

```json
{
    "html.validate.styles": false,
}
```

Controls whether the built-in HTML language support validates embedded scripts.

```json
{
    "html.validate.scripts": false,
}
```

Enable/disable default HTML formatter.

```json
{
    "html.format.enable": false,
}
```

Link file types to the beautifier type

```json
{
    "beautify.language": {
        "html": ["htm", "html", "ejs", "jinja"]
    },
}
```

List of paths to ignore when using VS Code format command, including format on save. Uses glob pattern matching.

```json
{
    "beautify.ignore": ["*.css", "*.js", "*.jsx", "*.ts", "*.tsx"],
}
```

Configure settings to be overridden for the html language.

```json
{
    "[html]": {
        "editor.defaultFormatter": "HookyQR.beautify",
        "editor.tabSize": 2,
        "editor.formatOnSave": true
    },
}
```

## Integration with Git Hooks

Javascript requires the [husky]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/husky.html) and [lint-staged]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/lint-staged.html) packages to be installed.

```shell
npm -g install js-beautify
```

```json
{
    "lint-staged": {
        "*.{htm, html}": [
            "js-beautify --type 'html' --replace"
        ]
    }
}
```

To use Python, you need to install the [pre-commit]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/pre-commit.html) package.

```yaml
repos:
  - repo: https://github.com/aufdenpunkt/pre-commit-js-beautify
    rev: 1.13.0
    hooks:
      - id: js-beautify
        additional_dependencies: ["js-beautify@1.14.3"]
        language: node
        files: \.(htm|html)$
        args: ["--replace"]
```
