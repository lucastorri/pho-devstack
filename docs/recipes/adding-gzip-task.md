# GZip dist gulp task

1. Install [gulp-gzip](https://www.npmjs.org/package/gulp-gzip) <br>
  `npm install gulp-gzip --save-dev`

2. Add the following code to your Gulpfile:

```javascript
var gzip = require('gulp-gzip');

gulp.task('gzip', ['index'], function(cb) {
  gulp.src('./dist/**')
    .pipe(gzip({
      append: true,
      level: 9
    }))
    .pipe(gulp.dest('dist'))
    .on('end', cb);
  });
```

3. Run the new task <br>
  `gulp gzip`
