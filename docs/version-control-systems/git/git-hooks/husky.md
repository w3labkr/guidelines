# husky

Modern native git hooks made easy. You can use it to lint your commit messages, run tests, lint code, etc... when you commit or push.

- [typicode.github.io/husky](https://typicode.github.io/husky){:target="_blank"}
- [github.com/typicode/husky](https://github.com/typicode/husky){:target="_blank"}

## Installation

`husky-init` is a one-time command to quickly initialize a project with husky.

```shell
npx husky-init && npm install
```

## Uninstallation

```shell
npm uninstall husky && git config --unset core.hooksPath
```

## Configuration

```json
{
    "husky": {
        "hooks": {}
    },
}
```

## Git-flow

If using git-flow you need to ensure your git-flow hooks directory is set to use Husky's (`.husky` by default).

```shell
git config gitflow.path.hooks .husky
```

To revert the git-flow hooks directory back to its default you need to reset the config to point to the default Git hooks directory.

```shell
git config gitflow.path.hooks .git/hooks
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
