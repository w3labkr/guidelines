# Javascript

## Installation

```shell
npm install --save-dev gulp-uglify gulp-babel @babel/core @babel/preset-env
```

## Configuration

```javascript
const gulp = require('gulp');
const babel = require('gulp-babel');
const uglify = require('gulp-uglify');

gulp.task('default', () =>
    gulp.src('src/app.js')
        .pipe(babel())
        .pipe(uglify())
        .pipe(gulp.dest('dist'))
);
```

## Dependencies

### [gulp-babel](https://www.npmjs.com/package/gulp-babel){:target="_blank"}

Use next generation JavaScript, today, with Babel.

```shell
npm install --save-dev gulp-babel @babel/core @babel/preset-env
```

### [gulp-uglify](https://www.npmjs.com/package/gulp-uglify){:target="_blank"}

Minify JavaScript with UglifyJS3.

```shell
npm install --save-dev gulp-uglify
```
