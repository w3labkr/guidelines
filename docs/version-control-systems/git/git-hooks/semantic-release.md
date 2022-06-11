# semantic-release

Fully automated version management and package publishing.

- [semantic-release.gitbook.io/semantic-release](https://semantic-release.gitbook.io/semantic-release/){:target="_blank"}
- [github.com/semantic-release/semantic-release](https://github.com/semantic-release/semantic-release){:target="_blank"}

## Installation

Recommend installing semantic-release locally.

```shell
npm install --save-dev semantic-release
```

And running the semantic-release command with npx:

```shell
npx semantic-release
```

## Configuration

.releaserc.yml

```shell
{
  "plugins":
    [
      "@semantic-release/commit-analyzer",
      "@semantic-release/release-notes-generator",
      "@semantic-release/npm",
      "@semantic-release/github",
    ],
  "branches": ["main"],
}
```
