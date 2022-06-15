# Git Hooks

Like many other Version Control Systems, Git has a way to fire off custom scripts when certain important actions occur.

- [git-scm.com/book/en/v2/Customizing-Git-Git-Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks){:target="_blank"}

## List of Hooks

- applypatch-msg
- commit-msg
- fsmonitor-watchman
- post-update
- pre-applypatch
- pre-commit
- pre-merge-commit
- pre-push
- pre-rebase
- pre-receive
- prepare-commit-msg
- push-to-checkout
- update

<https://github.com/git/git/tree/master/templates>

## pre-commit Hooks

Javascript

- [husky](husky.html)  
   Modern native git hooks made easy. You can use it to lint your commit messages, run tests, lint code, etc... when you commit or push.

- [lint-staged](lint-staged.html)  
   Run linters on git staged files.

Python

- [pre-commit](pre-commit.html)  
   A framework for managing and maintaining multi-language pre-commit hooks.

## Conventional Commits

- [commitizen](commitizen.html)  
   The commitizen command line utility.

- [commitlint](commitlint.html)  
   Lint commit messages.

## Automate Versioning

- [standard-version](standard-version.html)  
   Automate versioning and CHANGELOG generation, with semver.org and conventionalcommits.org

- [semantic-release](semantic-release.html)  
   Fully automated version management and package publishing.
