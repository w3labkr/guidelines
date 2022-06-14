# gulp-rename

gulp-rename is a gulp plugin to rename files easily.

- [github.com/hparra/gulp-rename](https://github.com/hparra/gulp-rename){:target="_blank"}

## Installation

```shell
npm install --save-dev gulp-rename
```

## Configuration

rename via a fixed object

```javascript
const rename = require("gulp-rename");

gulp.src("./src/main/text/hello.txt")
  .pipe(rename({
    dirname: "main/text/ciao",
    basename: "aloha",
    prefix: "bonjour-",
    suffix: "-hola",
    extname: ".md"
  }))
  .pipe(gulp.dest("./dist")); // ./dist/main/text/ciao/bonjour-aloha-hola.md
```
