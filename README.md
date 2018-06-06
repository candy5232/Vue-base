本人使用的是mac
===

Mac环境下搭建vue.js开发环境
=====

#1、安装node.js
-----
安装地址：https://nodejs.org/en/

安装步骤：http://www.runoob.com/nodejs/nodejs-install-setup.html

安装成功验证：

![](https://candy5232.github.io/Vue-base/images/1.png)



#2、基于node.js,利用淘宝npm镜像安装相关依赖
-----
在cmd里直接输入：

npm install -g cnpm --registry=https://registry.npm.taobao.org

等待安装
![](https://candy5232.github.io/Vue-base/images/2.png)

#3、安装全局vue-cli脚手架,用于帮助搭建所需的模板框架
打开终端，输入：cnpm install -g vue-cli

安装成功验证：

输入vue
![](https://candy5232.github.io/Vue-base/images/3.png)


#4、搭建第一个vue项目
打开终端 按下图操作 创建一个名为“my_jrojects”的项目

![](https://candy5232.github.io/Vue-base/images/4.png)
![](https://candy5232.github.io/Vue-base/images/5.png)

验证，在Finder中打开我的电脑，找到名为“my_demo”的文件夹
![](https://candy5232.github.io/Vue-base/images/6.png)

或者通过终端 cd my_jrojects 然后利用ls操作进行查看：

#5、运行
在这里我们可以选用IDE运行或者直接用终端运行
![](https://candy5232.github.io/Vue-base/images/5.png)

（1）在终端运行

![](https://candy5232.github.io/Vue-base/images/9.png)
运行效果如下：

![](https://candy5232.github.io/Vue-base/images/7.png)

![](https://candy5232.github.io/Vue-base/images/8.png)



GitHub上README.md的简单介绍
====
1、编辑README文件

大标题（一级标题）：在文本下面加等于号，那么上方的文字就变成了大标题，等于号的个数无限制，但一定要大于0

大标题
====
 

中标题（二级标题）：在文本下面加下划线，那么上方的文本就变成了中标题，下划线个数无限制，中标题比大标题低一级

中标题
-------
 

 1~6级标题：文本大小依次减小，以#号开头，多少个#号就是多少级标题，#号和标题名称要并排写

#一级标题
##二级标题
###三级标题
####四级标题
#####五级标题
######六级标题
插入圆点符号：编辑的时候使用的是星号 *，星号后面要有一个空格，否则为普通星号

* 列表一
* 列表二
* 列表三
 

二级圆点、三级圆点：多加一个Tab，即第二行一个Tab，第三行两个Tab

* 列表一
    * 列表二
        *列表三
 

缩进：

>缩进一
>>缩进二
>>>缩进三
>>>>缩进四
>>>>>缩进五
 

插入链接

[百度](http://baidu.com)
 

插入网络图片：![](网络图片链接地址)，即叹号!+方括号[]+括号()，如果不加叹号!就会变成普通文本，方括号里可以加入一些 标识性的信息

![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")  
 

插入GITHub仓库里的图片：![](图片链接地址)，即叹号!+方括号[]+括号()，URL写法：http://github.com/自己的用户名/项目名/raw/分支名/存放图片的文件夹/文件夹里的图片名字

给图片加上超链接：即点击一个图片进入指定网页，方括号里写自己起的标识名称，上下两行标识要一致。

[![baidu]](http://baidu.com)  
[baidu]:http://www.baidu.com/img/bdlogo.gif "百度Logo"  
 

插入代码片段：在代码上下行用```标记，注意`符号是tab键上面那个，要实现语法高亮，则在```后面加上编程语言的名称

复制代码
```Java
public static void main(String[] args){}
```

```javascript
document.getElementById("ts").innerHTML="Hello"
```
复制代码
换行：使用标签<br>

单行文本：前面使用两个Tab

多行文本:每行行首加两个Tab

部分文字高亮：使用``包围，这个符号不是单引号，而是Tab上方，数字1左边那个按键的符号

文字超链接格式：[要显示的文字](链接的地址"鼠标悬停显示")，在URL之后用双引号括起来一个字符串，即鼠标悬停显示的文本，可不写




怎样在vue项目下添加ESLint
=====
简易搭建
ESLint官网网址

ESLint中文官网

如果你是想在自己的项目里搭建ESLint，就可以按照官网的指示，

以全局安装举例，

npm install -g eslint
然后初始化

eslint --init
它会问你一些问题，你可以按照你的喜好进行配置，我选的是popular下面的standard，生成的文件是js格式，那么就会创建出eslintrc.js文件：

module.exports = {
"extends": "standard"
};
然后就可以简单的lint某个文件了：

$ eslint yourfile.js
在vue的项目里新添加ESLint
有的时候，早期的时候，我们建立vue项目的时候，可能图简便，并没有初始化ESLint、单元测试等等模块，那么就需要后添加进去。

如果是现在新建一个项目，通过vue-cli的问答就可以轻松初始化ESLint的配置。

这里说一下怎样在老项目里新添加ESLint。

首先，我先用vue-cli创建了一个新项目，在初始化的时候，选择安装eslint，

选择standard规则，然后就生成了eslintrc.js，把生成的这个文件拷贝到要加ESlint的老项目里。

// https://eslint.org/docs/user-guide/configuring
module.exports = {
  //默认情况下，ESLint 会在所有父级目录里寻找配置文件，一直到根目录。如果你想要你所有项目都遵循一个特定的约定时，这将会很有用，但有时候会导致意想不到的结果。为了将 ESLint 限制到一个特定的项目，在你项目根目录下的 package.json 文件或者 .eslintrc.* 文件里的 eslintConfig 字段下设置 "root": true。ESLint 一旦发现配置文件中有 "root": true，它就会停止在父级目录中寻找。
  root: true,
  parser: 'babel-eslint',
  parserOptions: {
    sourceType: 'module'
  },
  env: {
    browser: true,
  },
  // https://github.com/standard/standard/blob/master/docs/RULES-en.md
  extends: 'standard',
  // required to lint *.vue files
  plugins: [
    'html'
  ],
  // add your custom rules here
  'rules': {
    // allow paren-less arrow functions 要求箭头函数的参数使用圆括号
    'arrow-parens': 0,
    // allow async-await 强制 generator 函数中 * 号周围使用一致的空格
    'generator-star-spacing': 0,
    // allow debugger during development
    'no-debugger': process.env.NODE_ENV === 'production' ? 2 : 0
  }
}
然后找到package.json，把ESLint相关的依赖加进去（也可以一个一个进行安装，或者有更好的办法。。）

clipboard.png

    "babel-eslint": "^7.1.1",   "eslint": "^3.19.0",

    "eslint-friendly-formatter": "^3.0.0",
    "eslint-loader": "^1.7.1",
    "eslint-plugin-html": "^3.0.0",
    "eslint-config-standard": "^10.2.1",
    "eslint-plugin-promise": "^3.4.0",
    "eslint-plugin-standard": "^3.0.1",
    "eslint-plugin-import": "^2.7.0",
    "eslint-plugin-node": "^5.2.0", 
然后在webpack.base.conf.js的rules里添加

 {
        test: /\.(js|vue)$/,
        loader: 'eslint-loader',
        enforce: 'pre',
        include: [resolve('src'), resolve('test')],
        options: {
          formatter: require('eslint-friendly-formatter')
        }
      },
再npm install一下，应该就可以了。








