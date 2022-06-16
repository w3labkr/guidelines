# gulp-shell

A handy command line interface for gulp.

- [github.com/sun-zheng-an/gulp-shell](https://github.com/sun-zheng-an/gulp-shell){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-shell
```

## Configuration

```javascript
const gulp = require('gulp')
const shell = require('gulp-shell')

gulp.task('greet', shell.task('echo Hello, World!'))
```
