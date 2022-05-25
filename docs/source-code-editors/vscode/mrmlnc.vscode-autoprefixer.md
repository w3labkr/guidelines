# Autoprefixer

Parse CSS and add vendor prefixes to rules by Can I Use.

- [autoprefixer.github.io/](https://autoprefixer.github.io/){:target="_blank"}
- [github.com/postcss/autoprefixer](https://github.com/postcss/autoprefixer){:target="_blank"}

## Installation

Install through vscode extensions. Search for [Autoprefixer](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer){:target="_blank"}.

## Configuration

**settings.json**

```json
{
    "autoprefixer.formatOnSave": false,
    "autoprefixer.ignoreFiles": [
        "**/*.min.css"
    ],
    "autoprefixer.options": {
        "browsers": [
            "> 0.5%",
            "last 2 versions",
            "Firefox ESR",
            "not dead"
        ]
    },
}
```

Add vendor prefixes to CSS when you save a file.

```json
{
    "autoprefixer.formatOnSave": false,
}
```

An optional array of glob-patterns to ignore files.

```json
{
    "autoprefixer.ignoreFiles": [
        "**/*.min.css"
    ],
}
```

Any options supported by autoprefixer.

```json
{
    "autoprefixer.options": {
        "browsers": [
            "> 0.5%",
            "last 2 versions",
            "Firefox ESR",
            "not dead"
        ]
    },
}
```

## Troubleshooting

Disallow vendor prefixes for properties in .stylelintrc when autoprefixer.formatOnSave is set to true.

```json
{
    "rules": {
        "property-no-vendor-prefix": null
    }
}
```
