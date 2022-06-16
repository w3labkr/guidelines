# gulp-inline-css

Inline linked css in an html file. Useful for emails.

- [github.com/jonkemp/gulp-inline-css](https://github.com/jonkemp/gulp-inline-css){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-inline-css
```

## Configuration

```javascript
const gulp = require('gulp');
const inlineCss = require('gulp-inline-css');

gulp.task('default', function() {
    return gulp.src('./*.html')
        .pipe(inlineCss({
          applyStyleTags: true,
          applyLinkTags: true,
          removeStyleTags: true,
          removeLinkTags: true,
          preserveMediaQueries: false,
          applyWidthAttributes: false,
          applyTableAttributes: false,
          removeHtmlSelectors: true,
        }))
        .pipe(gulp.dest('build/'));
});
```
