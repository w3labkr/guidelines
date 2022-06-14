# gulp-concat

Streaming concat middleware for gulp.

- [github.com/gulp-community/gulp-concat](https://github.com/gulp-community/gulp-concat){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-concat
```

## Configuration

```javascript
const concat = require('gulp-concat');
 
gulp.task('scripts', function() {
  return gulp.src('./lib/*.js')
    .pipe(concat('all.js'))
    .pipe(gulp.dest('./dist/'));
});
```
