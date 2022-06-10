# Style

## Stylelint

A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

- [stylelint.io/](https://stylelint.io/){:target="_blank"}
- [github.com/stylelint/stylelint](https://github.com/stylelint/stylelint){:target="_blank"}

## Installation

```shell
npm install --save-dev stylelint
```

## Configuration

The .stylelintrc file (without extension) can be in JSON or YAML format.

## Table of Contents

{% include list.liquid all=true %}

## Integration with Git Hooks

You need to install the husky and lint-staged node packages. See [here]({{ site.baseurl }}/docs/version-control-systems/git/git-hooks.html) for more information.

```json
{
    "lint-staged": {
        "*.{css, scss, less, postcss}": [
            "stylelint --fix"
        ]
    }
}
```

You need to install the pre-commit python packages. See [here]({{ site.baseurl }}/docs/version-control-systems/git/pre-commit.html) for more information.

```yaml
repos:
  - repo: https://github.com/awebdeveloper/pre-commit-stylelint
    rev: 0.0.2
    hooks:
      - id: stylelint
        additional_dependencies:
          [
            "stylelint@14.7.1",
            "stylelint-config-prettier@9.0.3",
            "stylelint-config-rational-order@0.1.2",
            "stylelint-config-recommended@7.0.0",
            "stylelint-config-styled-components@0.1.1",
            "stylelint-csstree-validator@2.0.0",
            "stylelint-order@5.0.0",
            "stylelint-prettier@2.0.0",
          ]
        language: node
        files: \.(css|scss|sass)$
        args: ["--fix"]
```
