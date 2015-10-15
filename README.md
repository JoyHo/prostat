# prostat

> add statistic data to page

## 开始
This plugin requires Grunt.

安装插件

```shell
npm install prostat --save-dev
```

在Gruntfile中加载插件

```js
grunt.loadNpmTasks('prostat');
```

## The "prostat" task

执行任务，建议放在开发服务器dev任务中执行

```js
grunt.registerTask('dev', [
        'express:dev',
        // TODO: browserSync 视乎和 livereload 不兼容
        // 'browserSync',
        'prostat',//看这里
        'watch'
]);
```

### 配置

#### Default Options

options里面可以有其他自定义参数
```js
prostat: {
            default_options: {
              options: {
                targetFile : 'public/views/index_ui.html',//脚本插入到哪个页面，必填。这里可以是数组形式，即[xxxx,xxxx,xxxx]
                pg :　'diwali_holiday',//页面名称，必填
                ch : 'India'//市场，必填
              }
            }
          }
```

## License
Copyright (c) 2015 heyanzhu. Licensed under the MIT license.
