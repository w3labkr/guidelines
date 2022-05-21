---
sort: 1
---

# Visual Studio Code

Visual Studio Code is a distribution of the Code.

- [code.visualstudio.com/](https://code.visualstudio.com/){:target="_blank"}
- [github.com/microsoft/vscode](https://github.com/microsoft/vscode){:target="_blank"}

## Marketplace

One place for all extensions for Visual Studio, Azure DevOps Services, Azure DevOps Server and Visual Studio Code.

[marketplace.visualstudio.com/vscode](https://marketplace.visualstudio.com/vscode){:target="_blank"}

## Extensions

**Essential extensions**

- [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager){:target="_blank"}  
  Easily switch between projects  

- [SFTP](https://marketplace.visualstudio.com/items?itemName=liximomo.sftp){:target="_blank"}  
  SFTP/FTP sync  

- [Autoprefixer](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer){:target="_blank"}  
  Parse CSS and add vendor prefixes automatically.  

**Recommended extensions**

- [One Dark Pro](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme){:target="_blank"}  
  Atom‘s iconic One Dark theme for Visual Studio Code  

- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons){:target="_blank"}  
  Icons for Visual Studio Code  

- [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag){:target="_blank"}  
  Automatically add HTML/XML close tag, same as Visual Studio IDE or Sublime Text  

- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag){:target="_blank"}  
  Auto rename paired HTML/XML tag  

- [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils){:target="_blank"}  
  A convenient way of creating, duplicating, moving, renaming and deleting files and directories.  

- [Indent 4-to-2](https://marketplace.visualstudio.com/items?itemName=Compulim.indent4to2){:target="_blank"}  
  Convert indentation from tab or 4 spaces into 2 spaces  

## Settings

**settings.json**

Configure file associations to languages (e.g. `"*.extension": "html"`). These have precedence over the default associations of the languages installed.

```json
{
  "files.associations": {
    "*.html": "html",
    "*.vue": "html",
    "*.ejs": "html",
    "*.jinja": "html",
    "*.jsx": "javascriptreact",
    "*.tsx": "typescriptreact"
  },
}
```

Configure [glob patterns](https://code.visualstudio.com/docs/editor/codebasics#_advanced-search-options){:target="_blank"} for excluding files and folders in fulltext searches and quick open. Inherits all glob patterns from the `files.exclude` setting.

```json
{
  "search.exclude": {
    "**/node_modules": true,
    "**/bower_components": true,
    "**/*.code-search": true,
    "**/package-lock.json": true,
    "**/yarn-lock.json": true,
    "**/Gemfile.lock": true,
    "**/.history": true
  },
}
```

Format a file on save. A formatter must be available, the file must not be saved after delay, and the editor must not be shutting down.

```json
{
  "editor.formatOnSave": false,
}
```

Insert spaces when pressing `Tab`. This setting is overridden based on the file contents when `editor.detectIndentation` is on.

```json
{
  "editor.insertSpaces": true,
}
```

Controls whether `editor.tabSize#` and `#editor.insertSpaces` will be automatically detected when a file is opened based on the file contents.

```json
{
  "editor.detectIndentation": false,
}
```

Enable Emmet abbreviations in languages that are not supported by default. Add a mapping here between the language and Emmet supported language.

```json
{
  "emmet.includeLanguages": {
    "php": "html",
    "ejs": "html",
    "vue-html": "html",
    "vue": "html",
    "jinja-html": "html",
    "jinja": "html",
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },
}
```

## Uninstall

```shell
rm -rf $HOME/Library/Application\ Support/Code
rm -rf $HOME/.vscode
```

Remove VSCode from application

[how-to-completely-uninstall-vscode-on-mac](https://stackoverflow.com/questions/42603103/how-to-completely-uninstall-vscode-on-mac){:target="_blank"}