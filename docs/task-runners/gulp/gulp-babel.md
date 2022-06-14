# gulp-babel

Use next generation JavaScript, today, with Babel.

- [github.com/babel/gulp-babel](https://github.com/babel/gulp-babel){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-babel @babel/core @babel/preset-env
```

## Configuration

```javascript
const gulp = require('gulp');
const babel = require('gulp-babel');

gulp.task('default', () =>
    gulp.src('src/app.js')
        .pipe(babel())
        .pipe(gulp.dest('dist'))
);
```
