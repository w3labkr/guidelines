# gulp-if

Conditionally run a task.

- [github.com/robrich/gulp-if](https://github.com/robrich/gulp-if){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-if
```

## Configuration

```javascript
const gulp = require('gulp');
const useref = require('gulp-useref');

gulp.task('default', function () {
  return gulp.src('app/*.html')
    .pipe(useref())
    .pipe(gulp.dest('dist'));
});
```
