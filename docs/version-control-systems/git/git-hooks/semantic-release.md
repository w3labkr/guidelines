# semantic-release

Fully automated version management and package publishing.

- [semantic-release.gitbook.io/semantic-release](https://semantic-release.gitbook.io/semantic-release/){:target="_blank"}
- [github.com/semantic-release/semantic-release](https://github.com/semantic-release/semantic-release){:target="_blank"}

## Installation

Recommend installing semantic-release locally.

```shell
npm install --save-dev semantic-release @semantic-release/changelog
```

And running the semantic-release command with npx:

```shell
npx semantic-release
```

## Configuration

A `.releaserc` file, written in YAML or JSON, with optional extensions: `.yaml`/`.yml`/`.json`/`.js`

```json
{
    "branches": ["master", "next"],
    "plugins": [
        "@semantic-release/commit-analyzer",
        "@semantic-release/release-notes-generator",
        "@semantic-release/changelog",
        "@semantic-release/npm",
        "@semantic-release/git"
    ]
}
```

Via CLI argument:

```shell
npx semantic-release --branches next
```
