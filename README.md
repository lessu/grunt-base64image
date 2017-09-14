# grunt-base64image
> Base64 images in your css file.


## Getting Started
This plugin requires Grunt `~0.4.4`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-css-base64image --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-css-base64image');
```


## Base64 Image Task

css-base64image任务使用[css-base64-images](https://github.com/maxzhang/css-base64-images)项目编码图片。
这个版本是fork自https://github.com/maxzhang/grunt-base64image,
追加了css的相对路径和绝对路径的功能

### Compile Options

#### styles : String
指定CSS源目录
#### relative : String
指定CSS中相对路径的目录，
如果没有指定，那么默认采用styles
#### root : String
指定CSS中"/image/a.png"这样的绝对路径的的根目录


#### dest : String
指定输出目录


### Usage Examples
```js
module.exports = function(grunt) {
    grunt.loadNpmTasks('grunt-css-base64image');

    grunt.initConfig({
        pkg: grunt.file.readJSON('package.json'),

        base64image: {
            css: {
                styles: 'app/styles/',
                root  : "src/images",
                relative: 'src/images/',
                dest: 'dest/styles/base64/'
            }
        }
    });
};
```

