# merge-stream

Merge multiple streams into one interleaved stream.

- [github.com/grncdr/merge-stream](https://github.com/grncdr/merge-stream){:target="_blank"}

## Installation

```shell
npm install --save-dev merge-stream
```

## Configuration

```javascript
const mergeStream = require("merge-stream");

gulp.task('lint', function() {
  return mergeStream(
    gulp.src('src/*.html').pipe(htmlValidator()),
    gulp.src('src/*.js').pipe(jsHint())
  );
});
```
