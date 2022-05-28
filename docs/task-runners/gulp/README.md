# Gulp

A toolkit to automate & enhance your workflow.

- [gulpjs.com/](https://gulpjs.com/){:target="_blank"}
- [github.com/gulpjs/gulp](https://github.com/gulpjs/gulp){:target="_blank"}

## Directory Structure

```text
.
├── dist/
│   ├── style.css
│   ├── style.min.css
│   ├── style.min.css.map
│   ├── script.js
│   ├── script.min.js
│   └── script.min.js.map
└── src/
    ├── assets/
    │   ├── image/
    │   ├── js/
    │   └── scss/
    ├── data/
    ├── template-parts/
    │   ├── breadcrumb.html
    │   └── hero.html
    ├── templates/
    ├── footer.html
    ├── header.html
    ├── index.html
    ├── sidebar-1.html
    └── sidebar-2.html
```

Directory tree created by [tree.nathanfriend.io](https://tree.nathanfriend.io/)

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

## Dependencies

```shell
npm install --save-dev del gulp-rename gulp-sourcemaps gulp-concat gulp-header merge-stream
```

### [del](https://www.npmjs.com/package/del){:target="_blank"}

Delete files and directories

```shell
npm install --save-dev del
```

```javascript
const del = require('del');

del(['dist/']);
```

### [gulp-rename](https://www.npmjs.com/package/gulp-rename){:target="_blank"}

gulp-rename is a gulp plugin to rename files easily.

```shell
npm install --save-dev gulp-rename
```

rename via a fixed object

```javascript
const rename = require("gulp-rename");

gulp.src("./src/main/text/hello.txt")
  .pipe(rename({
    dirname: "main/text/ciao",
    basename: "aloha",
    prefix: "bonjour-",
    suffix: "-hola",
    extname: ".md"
  }))
  .pipe(gulp.dest("./dist")); // ./dist/main/text/ciao/bonjour-aloha-hola.md
```

### [gulp-sourcemaps](https://www.npmjs.com/package/gulp-sourcemaps){:target="_blank"}

Sourcemap support for gulpjs.

```shell
npm install --save-dev gulp-sourcemaps
```

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

### [gulp-concat](https://www.npmjs.com/package/gulp-concat){:target="_blank"}

Streaming concat middleware for gulp.

```shell
npm install --save-dev gulp-concat
```

```javascript
const concat = require('gulp-concat');
 
gulp.task('scripts', function() {
  return gulp.src('./lib/*.js')
    .pipe(concat('all.js'))
    .pipe(gulp.dest('./dist/'));
});
```

### [gulp-header](dependency){:target="_blank"}

Gulp extension to add a header to file(s) in the pipeline.

```shell
npm install --save-dev gulp-header
```

```javascript
const header = require('gulp-header');
 
const pkg = require('./package.json');
const banner = [
  '/**',
  ' * Copyright (c) <%= new Date().getFullYear() %> <%= pkg.author %>',
  ' * <%= pkg.name %> - <%= pkg.description %>',
  ' * @version v<%= pkg.version %>',
  ' * @link <%= pkg.homepage %>',
  ' * @license <%= pkg.license %>',
  ' */',
  '',
].join('\n');

gulp.src('./foo/*.js')
  .pipe(header(banner, { pkg: pkg }))
  .pipe(gulp.dest('./dist/'));
```

### [merge-stream](https://www.npmjs.com/package/merge-stream){:target="_blank"}

Merge (interleave) a bunch of streams.

```shell
npm install --save-dev merge-stream
```

```javascript
const mergeStream = require("merge-stream");

gulp.task('lint', function() {
  return mergeStream(
    gulp.src('src/*.html').pipe(htmlValidator()),
    gulp.src('src/*.js').pipe(jsHint())
  );
});
```
