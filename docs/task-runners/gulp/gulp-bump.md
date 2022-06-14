# gulp-bump

Bump any version in any file which supports semver with gulp (gulpjs.com).

- [github.com/stevelacy/gulp-bump](https://https://github.com/stevelacy/gulp-bump){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-bump
```

## Configuration

```javascript
const gulp = require('gulp');
const bump = require('gulp-bump');

gulp.task('bump', function(){
  gulp.src('./package.json')
  .pipe(bump())
  .pipe(gulp.dest('./'));
});
```
