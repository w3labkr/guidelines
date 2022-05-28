# CSS

PostCSS gulp plugin to pipe CSS through several plugins, but parse CSS only once.

- [gulp-postcss](https://www.npmjs.com/package/gulp-postcss){:target="_blank"}

## Installation

```shell
npm install --save-dev postcss gulp-postcss autoprefixer cssnano
```

## Configuration

```javascript
const gulp = require('gulp');
const postcss = require('gulp-postcss');
const autoprefixer = require('autoprefixer');
const cssnano = require('cssnano');

gulp.task('css', function () {
    return gulp.src('./src/*.css')
        .pipe(postcss([autoprefixer(), cssnano()]))
        .pipe(gulp.dest('./dest'));
});
```

## Dependencies

### [autoprefixer](https://www.npmjs.com/package/autoprefixer){:target="_blank"}

PostCSS plugin to parse CSS and add vendor prefixes to CSS rules using values from Can I Use. It is recommended by Google and used in Twitter and Alibaba.

```shell
npm install --save-dev autoprefixer
```

### [cssnano](https://cssnano.co/){:target="_blank"}

A modular minifier, built on top of the PostCSS ecosystem.

```shell
npm install --save-dev cssnano postcss
```
