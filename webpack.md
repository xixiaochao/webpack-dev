# webpack

## note

### 模块

- node模块的规范commonjs
- cmd seajs amd require
- esmodule
  - 如何定义模块 (一个js就是一个模块)
  - 如何导出模块  (export)
  - 如何使用模块  (import)

### webpack定义

webpack是一款强大的模块加载器兼打包工具，它能把各种资源，例如JS（含JSX）、coffee、样式（含less/sass）、图片等都作为模块来使用和处理,优势如下:

- webpack优势
1.webpack 是以commonJS的形式来书写，但对AMD/CMD的支持也很全面,方便旧项目进行代码迁移
2.能被模块化的不仅仅是JS,还包括各种资源文件
3.开发便捷，能替代部分gulp的工作，比如打包、混淆压缩、图片转base64等
4.扩展性强，插件机制完善，特别是支持React热插拔

#### 1.先下载webpack

- npm init -y
- npm install webpack -save-dev

#### 2.webpack 使用

在package.json中配置一个脚本，这个脚本用的命令是webpack.会去当前的node_modules下找bin对应的webpack名字让其执行，执行的就是bin/webpack.js,webpack.js需要当前目录下有个名字叫webpack.config.js的文件，我们通过npm run build执行的目录是当前文件的目录，所以会去当前目录下查找

#### 3.解析es6

babel转义es6 -> es5
1、安装babel

- npm install babel-core --save-dev
- npm install babel-loader --save-dev

2、让翻译官拥有解析es6语法的功能

- npm install babel-preset-es2015 --save-dev

3、解析es7语法的

- npm install babel-preset-stage-0 --save-dev

#### 4.解析样式

1、- css-loader将css解析成模块，将解析的内容插入到style标签内(style-loader)

- npm install css-loader style-loader --save-dev

2、## less,sass,stylus(预处理语言)

- less-loader less
- sass-loader sass
- stylus-loader stylus
npm install less less-loader --save-dev

#### 5.解析图片

- file-loader url-loader(是依赖于file-loader的)
npm install file-loader url-loader --save-dev

#### 6. 需要解析html插件

- 插件的作用是以我们自己的html为模板将打包后的结果，自动引入到html中产出到dist目录下
npm install html-webpack-plugin --save-dev

#### 7. webpack-dev-server

- 这里面内置了服务，可以帮我们启动一个端口号，当代码更新时，可以自动打包（内存中打包），代码有变化就重新执行
npm install webpack-dev-server --save-dev
