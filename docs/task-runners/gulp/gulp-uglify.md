# gulp-uglify

Minify JavaScript with UglifyJS3.

- [github.com/terinjokes/gulp-uglify](https://github.com/terinjokes/gulp-uglify){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-uglify
```

## Configuration

```javascript
const gulp = require('gulp');
const uglify = require('gulp-uglify');

gulp.task('default', () =>
    gulp.src('src/app.js')
        .pipe(uglify())
        .pipe(gulp.dest('dist'))
);
```
