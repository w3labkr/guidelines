# gulp-uglify

Minify JavaScript with UglifyJS3.

- [github.com/terinjokes/gulp-uglify](https://github.com/terinjokes/gulp-uglify){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-uglify
```

## Configuration

Conditionally filter content

```javascript
var gulpif = require('gulp-if');
var uglify = require('gulp-uglify');

var condition = true; // TODO: add business logic

gulp.task('task', function() {
  gulp.src('./src/*.js')
    .pipe(gulpif(condition, uglify()))
    .pipe(gulp.dest('./dist/'));
});
```

Ternary filter

```javascript
var gulpif = require('gulp-if');
var uglify = require('gulp-uglify');

var condition = function (file) {
  // TODO: add business logic
  return true;
}

gulp.task('task', function() {
  gulp.src('./src/*.js')
    .pipe(gulpif(condition, uglify()))
    .pipe(gulp.dest('./dist/'));
});
```
