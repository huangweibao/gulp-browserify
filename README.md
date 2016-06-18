# gulp-browserify
gulpfile.js配置文件


var gulp = require('gulp');
var browserify = require('browserify');
var source = require('vinyl-source-stream');
var reactify = require('reactify');
gulp.task('任务名称', function(){
   return browserify('入后文件的路径')
   .transform(reactify)//jsx--->js
   .bundle() //----合并
   .pipe(source('合并后的文件名'))
   .pipe(gulp.dest('文件保存的文件夹名'));
});
