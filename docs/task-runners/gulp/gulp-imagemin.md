# gulp-imagemin

Minify PNG, JPEG, GIF and SVG images with imagemin.

- [github.com/sindresorhus/gulp-imagemin](https://github.com/sindresorhus/gulp-imagemin){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-imagemin
```

## Configuration

```javascript
const gulp = require('gulp');
const imagemin = require('gulp-imagemin');

gulp.src('src/images/*')
  .pipe(imagemin())
  .pipe(gulp.dest('dist/images'));
```

## Troubleshooting - gulp-imagemin 8.0.0

Error [ERR_REQUIRE_ESM]: require() of ES Module ... not supported.

```shell
npm install --save-dev gulp-imagemin@7.1.0
npm install --save-dev @types/gulp-imagemin@7.0.3
```

- [bobbyhadz.com/blog/javascript-gulp-error-err-require-esm-of-es-module](https://bobbyhadz.com/blog/javascript-gulp-error-err-require-esm-of-es-module){:target="_blank"}
