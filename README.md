本人使用的是mac

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

npm install -g cnpm –registry=https://registry.npm.taobao.org

等待安装

#3、安装全局vue-cli脚手架,用于帮助搭建所需的模板框架
打开终端，输入：cnpm install -g vue-cli

安装成功验证：

输入vue

![](https://candy5232.github.io/Vue-base/images/2.png)

#4、搭建第一个vue项目
打开终端 按下图操作 创建一个名为“my_jrojects”的项目

![](https://candy5232.github.io/Vue-base/images/3.png)

验证，在Finder中打开我的电脑，找到名为“my_demo”的文件夹
![](https://candy5232.github.io/Vue-base/images/6.png)

或者通过终端 cd my_jrojects 然后利用ls操作进行查看：

![](https://candy5232.github.io/Vue-base/images/4.png)
#5、运行
在这里我们可以选用IDE运行或者直接用终端运行
![](https://candy5232.github.io/Vue-base/images/5.png)

（1）在终端运行

![](https://candy5232.github.io/Vue-base/images/9.png)
运行效果如下：

![](https://candy5232.github.io/Vue-base/images/7.png)

![](https://candy5232.github.io/Vue-base/images/8.png)

