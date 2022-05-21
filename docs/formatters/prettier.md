# Prettier

Prettier is an opinionated code formatter.

- [prettier.io/](https://prettier.io/){:target="_blank"}
- [github.com/prettier/prettier](https://github.com/prettier/prettier){:target="_blank"}

## Installation

```shell
npm install --save-dev prettier
```

## Configuration

Prettier uses cosmiconfig for [configuration](https://prettier.io/docs/en/options.html){:target="_blank"} file support. A .prettierrc file written in JSON or YAML.

```json
{
    "printWidth": 120,
    "tabWidth": 2,
    "useTabs": false,
    "semi": true,
    "singleQuote": true,
    "quoteProps": "as-needed",
    "jsxSingleQuote": false,
    "trailingComma": "es5",
    "bracketSpacing": true,
    "bracketSameLine": false,
    "jsxBracketSameLine": false,
    "arrowParens": "always",
    "requirePragma": false,
    "insertPragma": false,
    "proseWrap": "preserve",
    "htmlWhitespaceSensitivity": "css",
    "vueIndentScriptAndStyle": false,
    "endOfLine": "lf",
    "embeddedLanguageFormatting": "auto",
    "singleAttributePerLine": false
}
```

To exclude files from formatting, create a .prettierignore file in the root of your project.

```txt
# By default prettier ignores files in version control systems directories
**/.git
**/.svn
**/.hg
**/node_modules

# Ignore all HTML files:
*.html

# Ignore minify files:
*.min.css
*.min.js

# Ignore specific files:
#...
```

## Integration with visual studio code

Install through vscode extensions. Search for [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode){:target="_blank"}.

**settings.json**

Configure settings to be overridden for the css language.

```json
{
    "[css]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": true
    },
}
```

Configure settings to be overridden for the javascript language.

```json
{
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.tabSize": 2,
        "editor.formatOnSave": true
    },
}
```
