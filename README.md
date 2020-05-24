# webpack

## webpack性能优化

1、项目中，关于性能优化，从哪几方面做？

2、webpack原理
entry：一个可执行模块或库的入口文件
chunk：出口，多个文件组成的一个代码块，例如把一个 可执行模块和它所有依赖的模块组合和一个chunk这体现了webpack的打包机制。
loader：文件转换器，例如把ES6转换成ES5，scss转换为css。
plugin：插件，用于扩展webpack的功能，在webpack构建生命周期的节点上加入扩展hook为webpack加入功能。

3、打包工具：

- es6 -> es5
- 把js整合成一个js文件
- 减少了http请求；提高了项目的性能；项目优化；
- 压缩代码； 支持less sass

4、配置文件

- babel-loader  
- style-loader  
- css-loader
- url-loader  
- file-loader  
- vue-loader .vue;

webpack.config.js

``` webpack
module.exports = {
         entry :"",
         output:{
           filename:"",
           path :""

         },
         module:{
             rules:[
                 {test:/\.css$/,use:[""]}
             ]
         },
         plugins:[
             new HtmlWebpackPlugins({
                 template:"../src/index.html"
             })
         ]
     }
```
