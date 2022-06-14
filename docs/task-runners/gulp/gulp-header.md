# gulp-header

Gulp extension to add a header to file(s) in the pipeline.

- [github.com/gulp-community/gulp-header](https://github.com/gulp-community/gulp-header){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-header
```

## Configuration

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
