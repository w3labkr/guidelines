# gulp-useref

Parse build blocks in HTML files to replace references to non-optimized scripts or stylesheets.

- [github.com/jonkemp/gulp-useref](https://github.com/jonkemp/gulp-useref){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-useref
```

## Configuration

```javascript
const gulp = require('gulp');
const useref = require('gulp-useref');

gulp.task('default', function () {
  return gulp.src('app/*.html')
    .pipe(useref())
    .pipe(gulp.dest('dist'));
});
```

If you want to minify your assets or perform some other modification, you can use gulp-if to conditionally handle specific types of assets.

```javascript
const gulp = require('gulp');
const useref = require('gulp-useref');
const gulpif = require('gulp-if');
const uglify = require('gulp-uglify');
const minifyCss = require('gulp-clean-css');

gulp.task('html', function () {
  return gulp.src('app/*.html')
    .pipe(useref())
    .pipe(gulpif('*.js', uglify()))
    .pipe(gulpif('*.css', minifyCss()))
    .pipe(gulp.dest('dist'));
});
```
