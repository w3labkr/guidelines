# gulp-file-include

a gulp plugin for file include.

- [github.com/haoxins/gulp-file-include](https://github.com/haoxins/gulp-file-include){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-file-include
```

## Configuration

```javascript
const fileinclude = require('gulp-file-include');
const gulp = require('gulp');

gulp.task('fileinclude', function() {
  gulp.src(['index.html'])
    .pipe(fileinclude({
      prefix: '@@',
      basepath: '@file'
    }))
    .pipe(gulp.dest('./'));
});
```
