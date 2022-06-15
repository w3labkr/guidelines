# gulp-sass

SASS plugin for gulp.

- [github.com/sass/dart-sass](https://github.com/sass/dart-sass){:target="_blank"}
- [github.com/dlmanning/gulp-sass](https://github.com/dlmanning/gulp-sass){:target="_blank"}

## Installation

```shell
npm install --save-dev sass gulp-sass
```

## Configuration

To use gulp-sass in a CommonJS module (which is most Node.js environments).

```javascript
const gulp = require('gulp');
const sass = require('gulp-sass')(require('sass'));

gulp.task('css', function () {
    return gulp.src('./sass/**/*.scss')
        .pipe(sass().on('error', sass.logError))
        .pipe(gulp.dest('./dest'));
});
```

To use gulp-sass in an ECMAScript module (which is supported in newer Node.js 14 and later).

```javascript
import dartSass from 'sass';
import gulpSass from 'gulp-sass';

const sass = gulpSass(dartSass);
```
