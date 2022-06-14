# gulp-conventional-changelog

Generate a changelog using conventional-changelog.

- [github.com/conventional-changelog/conventional-changelog/tree/master/packages/gulp-conventional-changelog](https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/gulp-conventional-changelog){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-conventional-changelog
```

## Configuration

```javascript
const gulp = require('gulp');
const conventionalChangelog = require('gulp-conventional-changelog');

gulp.task('changelog', function () {
  return gulp.src('CHANGELOG.md')
    .pipe(conventionalChangelog({
      preset: 'conventionalcommits'
    }))
    .pipe(gulp.dest('./'));
});
```

Note: If your `options.releaseCount` is 0 (regenerate all changelog from previous releases) you can just use conventional-changelog directly or not to read the file at all.

```javascript
const gulp = require('gulp');
const conventionalChangelog = require('gulp-conventional-changelog');

gulp.task('changelog', function () {
  return gulp.src('CHANGELOG.md')
    .pipe(conventionalChangelog({
      preset: 'conventionalcommits',
      releaseCount: 0
    }))
    .pipe(gulp.dest('./'));
});
```
