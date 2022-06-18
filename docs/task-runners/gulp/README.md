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

Creating Tasks

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

Watching Files

```javascript
const { watch } = require('gulp');

function css() {
  // body omitted
}

exports.default = function() {
  watch('src/*.css', css);
};
```

## Popular plugins

- [gulpjs.com/plugins](https://gulpjs.com/plugins){:target="_blank"}

## Recommended plugins

HTML

- [gulp-file-include](gulp-file-include.html)  
   a gulp plugin for file include.

- [gulp-jsbeautifier](gulp-jsbeautifier.html)  
   Beautify js, css, html and json files using Gulp and js-beautify.

- [gulp-imagemin](gulp-imagemin.html)  
   Minify PNG, JPEG, GIF and SVG images with imagemin.

CSS

- [gulp-postcss](gulp-postcss.html)  
   PostCSS gulp plugin to pipe CSS through several plugins, but parse CSS only once.

- [autoprefixer](autoprefixer.html)  
   PostCSS plugin to parse CSS and add vendor prefixes to CSS rules using values from Can I Use. It is recommended by Google and used in Twitter and Alibaba.

- [cssnano](cssnano.html)  
   A modular minifier, built on top of the PostCSS ecosystem.

- [gulp-sass](gulp-sass.html)  
   SASS plugin for gulp.

- [gulp-inline-css](gulp-inline-css.html)  
   Inline linked css in an html file. Useful for emails.

Javascript

- [gulp-babel](gulp-babel.html)  
   Use next generation JavaScript, today, with Babel.

- [gulp-uglify](gulp-uglify.html)  
   Minify JavaScript with UglifyJS3.

Git

- [gulp-conventional-changelog](gulp-conventional-changelog.html)  
   Generate a changelog using conventional-changelog.

Misc

- [del](del.html)  
   Delete files and directories.

- [gulp-if](gulp-if.html)  
   Conditionally run a task.

- [gulp-rename](gulp-rename.html)  
   gulp-rename is a gulp plugin to rename files easily.

- [gulp-sourcemaps](gulp-sourcemaps.html)  
   Sourcemap support for gulpjs.

- [gulp-concat](gulp-concat.html)  
   Streaming concat middleware for gulp.

- [gulp-useref](gulp-useref.html)  
   Parse build blocks in HTML files to replace references to non-optimized scripts or stylesheets.

- [gulp-header](gulp-header.html)  
   Gulp extension to add a header to file(s) in the pipeline.

- [merge-stream](merge-stream.html)  
   Merge multiple streams into one interleaved stream.

- [gulp-shell](gulp-shell.html)  
   A handy command line interface for gulp.
