# cssnano

A modular minifier, built on top of the PostCSS ecosystem.

- [cssnano](https://cssnano.co){:target="_blank"}
- [github.com/cssnano/cssnano](https://github.com/cssnano/cssnano){:target="_blank"}

## Installation

```shell
npm install --save-dev cssnano postcss
```

## Configuration

```javascript
const gulp = require('gulp');
const postcss = require('gulp-postcss');
const cssnano = require('cssnano');

gulp.task('css', function () {
    return gulp.src('./src/*.css')
        .pipe(postcss([cssnano()]))
        .pipe(gulp.dest('./dest'));
});
```
