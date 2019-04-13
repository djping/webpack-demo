# output management

  本节介绍了如何使用变量来生成js文件以及2个插件来处理文件
  
  ```
  当有多个入口文件时，我们为每个文件加不同的'前缀'
  module.export = {
    entry: {
      app: './src/index.js',
      print: './src/print.js/
    },
    output: {
      filename: '[name]'.bundle.js',
      path: path.resolve(__dirname,dist)
    }
  }
  ```
  
  ```
  html-webpack-plugin和clean-webpack-plugin插件的使用，前者是生成一个新的index.html，会覆盖原本html文件；后者则是清除指定文件夹下（这里是dist）多余的文件
  
  npm install html-webpack-plugin --save-dev
  ....
  
  const HtmlWebpackPlugin = require('html-webpack-plugin')
  const CleanWebpackPlugin = require('clean-webpack-plugin')

  module.export = {
    entry:{},
    plugins: [
      new CleanWebpackPlugin(),
      new HtmlWebpackPlugin({
        titile: 'output management'
      })
    ]
  }
  
  ```
  
