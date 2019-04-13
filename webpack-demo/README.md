# webpack学习，来源官网[https://webpack.js.org/guides/getting-started/#basic-setup](https://webpack.js.org/guides/getting-started/#basic-setup)

* [get_start](#get_start)
* [asset](#asset)

## get_start

  ```
  初始化
  npm init -y
  npm install webpack --save-dev
  npm install webpack-cli --save-dev
  ```
 配置package.json
 ```
 "build": "webpack"
 ```
 配置webpack.config.js
 
 ```
 const path = require('paht')
 module.export = {
  enry:,
  output:,
 }
 ```
 ## asset
  静态资源的添加需要安装css-loader,style-loader,file-loader模块
  ```
  webpack.config.js配置
  moudle.export = {
    .........
    module: {
      rules: [
        {
          test:/.\css$/,
          use: ['css-loader','style-loader']
        }
      ]
    }
  }
  
