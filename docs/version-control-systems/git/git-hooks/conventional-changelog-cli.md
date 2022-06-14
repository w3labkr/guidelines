# conventional-changelog-cli

Generate a changelog from git metadata.

- [github.com/conventional-changelog/conventional-changelog](https://github.com/conventional-changelog/conventional-changelog){:target="_blank"}

## Installation

```shell
npm install -g conventional-changelog-cli
```

Quick start

```shell
conventional-changelog -p conventionalcommits -i CHANGELOG.md -s
```

## Configuration

```json
{
    "scripts": {
        "version": "conventional-changelog -p conventionalcommits -i CHANGELOG.md -s && git add CHANGELOG.md"
    }
}
```

## Integration with Gulp

You need to install the [gulp-conventional-changelog]({{ site.baseurl }}/docs/task-runners/gulp/gulp-conventional-changelog.md) package.
