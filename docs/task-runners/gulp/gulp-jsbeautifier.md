# gulp-jsbeautifier

Beautify js, css, html and json files using Gulp and js-beautify.

- [github.com/tarunc/gulp-jsbeautifier](https://github.com/tarunc/gulp-jsbeautifier){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-jsbeautifier
```

## Configuration

```javascript
const gulp = require('gulp');
const beautify = require('gulp-jsbeautifier');
 
gulp.task('beautify', () =>
  gulp.src(['./*.html'])
    .pipe(beautify())
    .pipe(gulp.dest('./dist'))
);
```
