# release-it

Automate versioning and package publishing.

- [github.com/release-it/release-it](https://github.com/release-it/release-it){:target="_blank"}

## Installation

```shell
npm init release-it
```

Now you can run npm run release from the command line (put release-it arguments behind the -- ):

```shell
npm run release
npm run release -- minor --ci
```

Use npx to run release-it directly from anywhere:

```shell
npx release-it
```

## Configuration

Here's a quick example `.release-it.json`:

```json
{
    "git": {
        "commitMessage": "chore: release v${version}"
    },
    "github": {
        "release": true
    }
}
```
