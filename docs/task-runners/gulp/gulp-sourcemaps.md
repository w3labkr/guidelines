# gulp-sourcemaps

Sourcemap support for gulpjs.

- [github.com/gulp-sourcemaps/gulp-sourcemaps](https://github.com/gulp-sourcemaps/gulp-sourcemaps){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-sourcemaps
```

## Configuration

```javascript
var gulp = require('gulp');
var plugin1 = require('gulp-plugin1');
var plugin2 = require('gulp-plugin2');
var sourcemaps = require('gulp-sourcemaps');

gulp.task('javascript', function () {
    return gulp.src('src/**/*.js')
        .pipe(sourcemaps.init())
        .pipe(plugin1())
        .pipe(plugin2())
        .pipe(sourcemaps.write('.'))
        .pipe(gulp.dest('dest'));
});
```
