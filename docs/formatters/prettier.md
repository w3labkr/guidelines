# Prettier

Prettier is an opinionated code formatter.

- [prettier.io](https://prettier.io/){:target="_blank"}
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

## Ignoring Code

HTML

```html
<!-- prettier-ignore -->
```

CSS

```css
/* prettier-ignore */
```

javascript

```javascript
// prettier-ignore
```

JSX

```javascript
{/* prettier-ignore */}
```

YAML

```yaml
# prettier-ignore
```

## Integration with Git Hooks

Javascript requires the [husky]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/husky.html) and [lint-staged]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/lint-staged.html) packages to be installed.

```shell
npm -g install prettier
```

```json
{
    "lint-staged": {
        "*.{css, scss, less, postcss}": [
            "prettier --write"
        ],
        "*.{js, jsx, ts, tsx}": [
            "prettier --write"
        ]
    }
}
```

To use Python, you need to install the [pre-commit]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks/pre-commit.html) package.

```yaml
repos:
  - repo: https://github.com/pre-commit/mirrors-prettier
    rev: v2.6.2
    hooks:
      - id: prettier
        additional_dependencies: ["prettier@2.6.2"]
        language: node
        files: \.(css|scss|sass|js|jsx)$
        args: ["--write"]
```
