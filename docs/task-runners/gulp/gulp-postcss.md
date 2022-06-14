# gulp-postcss

PostCSS gulp plugin to pipe CSS through several plugins, but parse CSS only once.

- [postcss.org](https://postcss.org){:target="_blank"}
- [github.com/postcss/postcss](https://github.com/postcss/postcss){:target="_blank"}
- [github.com/postcss/gulp-postcss](https://github.com/postcss/gulp-postcss){:target="_blank"}

## Installation

```shell
npm install --save-dev postcss gulp-postcss
```

## Configuration

```javascript
const gulp = require('gulp');
const postcss = require('gulp-postcss');

gulp.task('css', function () {
    return gulp.src('./src/*.css')
        .pipe(postcss())
        .pipe(gulp.dest('./dest'));
});
```
