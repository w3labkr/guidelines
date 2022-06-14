# Gulp

A toolkit to automate & enhance your workflow.

- [gulpjs.com](https://gulpjs.com/){:target="_blank"}
- [github.com/gulpjs/gulp](https://github.com/gulpjs/gulp){:target="_blank"}

## Installation

Install the gulp command line utility

```shell
npm install --global gulp-cli
```

Install the gulp package in your devDependencies

```shell
npm install --save-dev gulp
```

## Configuration

Create a file named gulpfile.js

```javascript
function defaultTask(cb) {
  // place code for your default task here
  cb();
}

exports.default = defaultTask
```

### Creating Tasks

```javascript
const { series, parallel } = require('gulp');

function clean() {
  // body omitted
}

function cssTranspile() {
  // body omitted
}

function cssMinify() {
  // body omitted
}

function jsTranspile() {
  // body omitted
}

function jsBundle() {
  // body omitted
}

function jsMinify() {
  // body omitted
}

function publish() {
  // body omitted
}

exports.build = series(
  clean,
  parallel(cssTranspile, series(jsTranspile, jsBundle)),
  parallel(cssMinify, jsMinify),
  publish
);
```

### Watching Files

```javascript
const { watch } = require('gulp');

function clean() {
  // body omitted
}

function javascript() {
  // body omitted
}

function css() {
  // body omitted
}

exports.default = function() {
  watch('src/*.css', css);
  watch('src/*.js', javascript);
};
```

## Tablel of Contents

HTML

- [gulp-file-include](gulp-file-include.html)
- [gulp-jsbeautifier](gulp-jsbeautifier.html)
- [gulp-imagemin](gulp-imagemin.html)

CSS

- [gulp-postcss](gulp-postcss.html)
- [autoprefixer](autoprefixer.html)
- [cssnano](cssnano.html)
- [gulp-sass](gulp-sass.html)

Javascript

- [gulp-babel](gulp-babel.html)
- [gulp-uglify](gulp-uglify.html)

Git

- [gulp-conventional-changelog](gulp-conventional-changelog.html)
- [gulp-bump](gulp-bump.html)

Misc

- [del](del.html)
- [gulp-rename](gulp-rename.html)
- [gulp-sourcemaps](gulp-sourcemaps.html)
- [gulp-concat](gulp-concat.html)
- [gulp-header](gulp-header.html)
- [merge-stream](merge-stream.html)
