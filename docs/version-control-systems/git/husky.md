# Husky

Modern native git hooks made easy. You can use it to lint your commit messages, run tests, lint code, etc... when you commit or push.

- [typicode.github.io/husky](https://typicode.github.io/husky){:target="_blank"}
- [github.com/typicode/husky](https://github.com/typicode/husky){:target="_blank"}

## Installation

```shell
npm install --save-dev husky
npm set-script prepare "husky install"
npm run prepare
```

After clone repository:

```shell
npm install && npm run prepare
```

## Uninstallation

```shell
npm uninstall husky && git config --unset core.hooksPath
```

## Configuration

```json
{
    "husky": {
        "hooks": {
            "pre-commit": ""
        }
    },
}
```

## Troubleshooting

Command not found

```shell
# ~/.huskyrc
# This loads nvm.sh and sets the correct PATH before running hook
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

.git/hooks/ not working after uninstall

```shell
git config --unset core.hooksPath
```
