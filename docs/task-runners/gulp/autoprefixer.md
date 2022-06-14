# autoprefixer

PostCSS plugin to parse CSS and add vendor prefixes to CSS rules using values from Can I Use. It is recommended by Google and used in Twitter and Alibaba.

- [autoprefixer](https://www.npmjs.com/package/autoprefixer){:target="_blank"}
- [github.com/postcss/autoprefixer](https://github.com/postcss/autoprefixer){:target="_blank"}

## Installation

```shell
npm install --save-dev autoprefixer
```

## Configuration

```javascript
const gulp = require('gulp');
const postcss = require('gulp-postcss');
const autoprefixer = require('autoprefixer');

gulp.task('css', function () {
    return gulp.src('./src/*.css')
        .pipe(postcss([autoprefixer()]))
        .pipe(gulp.dest('./dest'));
});
```
