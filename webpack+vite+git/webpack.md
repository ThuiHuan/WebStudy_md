# 一、webpack

## <u>1.基本概念</u>🙌

本质上**webpack** 是一个用于现代 JavaScript 应用程序的 *静态模块打包工具*将浏览器不识别的语法编译成浏览器识别的语法。

主要分为开发模式与生产模式，生产模式是项目部署上线，会压缩js代码。

## **配置ts的webpack项目：**

1.初始化项目并生成package.json文件：npm init -y 

2.安装webpack的依赖，cnpm/npm：国内镜像/国外

安装国内镜像：npm install -g cnpm -registry=https://registry.npm.taobao.org

安装基本依赖：

```js
//-D是开发依赖；webpack打包工具的核心代码；webpack-cli：webpack的命令行工具；typescript：核心代码；ts-loader：webpack与typescript的整合
cnpm i -D webpack webpack-cli typescript ts-loader
```

3.编写webpack.config.js的配置文件，编写tsconfig.json配置文件，修改package.json文件，加上”build“:"webpack"命令

webpack.config.js是webpack的配置文件

package.json是项目的配置文件，常见的配置有配置项目启动、打包命令，声明依赖包等

## **webpack**

1.下载webpack插件，自动生成html文件

cnpm i -D html-webpack-plugin

**在webpack.config.js文件下引入插件**

2.webpack开发服务器插件

cnpm i -D webpack-dev-server

**在package.json里设置start命令**

```
   "scripts": {
   "start": "webpack server --open chrom.exe"
     },
```

3.编译器清空dist然后再重新生成

cnpm i -D clean-webpack-plugin

**在webpack.config.js文件下引入clean插件**

## babel的作用

把新的技术转换成就浏览器的兼容

1.把新语法转换为旧语法

2.把一些新的技术（比如新的类和新的对象）在旧浏览器得到兼容

### babel的使用

1.下载依赖

```js
//@babel/core babel核心的工具；babel/perset-env是预先设置的环境（兼容浏览器，什么环境转换什么环境的代码）；
//babel-loader是把babel和webpack结合的工具；core-js模拟js运行的环境
cnpm i -D @babel/core @babel/preset-env babel-loader core-js
```

# 