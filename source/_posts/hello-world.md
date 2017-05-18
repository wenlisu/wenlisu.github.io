title: 'HEXO+Github,搭建属于自己的博客'
categories: 手册
date: 2017-05-18 10:08:21
---
HEXO+Github,搭建属于自己的博客
=============
前言
-------------
一直都想拥有个属于自己的博客，之前买过域名做过静态展示类型的个人网站，苦于那时的自己对数据库操作不怎么了解，所以没有将其继续发展成动态网站并且维护下去，那是觉得自己需要搭建个动态博客，应该不只要会前端，后台至少也应该要懂些。  
直到偶然的机会让我遇到了[Hexo](https://hexo.io)，Hexo+Github的结合让谁都能轻轻松松搭建起属于自己的博客，相当COOL，相信不久的将来，Hexo就会流行起来。   
Hexo出自于台湾大学生[tommy351](http://twitter.com/tommy351)之手，基于node.js环境的静态博客程序，Hexo生成的静态网页可以直接放到GitHub Pages，BAE，SAE等平台上，大概生活中所有的创新都来源于对现状的不满意，[Hexo 颯爽登場！](https://zespia.tw/blog/2012/10/11/hexo-debut/)一篇来自[tommy351](http://twitter.com/tommy351)对[Octopress](http://octopress.org/)的吐槽。

 环境准备
=============

## 安装node
到[Node.js](https://nodejs.org/en)官网下载相应平台的最新版本，一路安装即可，比较喜欢折腾的同学可以通过安装[nvm](https://github.com/creationix/nvm)或者n`n是Node的一个模块`来安装或管理node版本，体验也是相当不错的，我是用的nvm`^o^推荐`。

## 安装Git
目前市面上也有图形化界面版，例如[SmartGit](http://www.syntevo.com/smartgit/download)，挺方便直观的。  
如果想要看起来高大上点的话，可以选择`shell`，并在上面输入要执行的命令。首先，你可以试着输入git，看看系统有没有安装Git。
```
git
The program 'git' is currently not installed. You can install it by typing:
sudo apt-get install git
```
通过一条`sudo apt-get install git`就可以直接完成Git的安装，非常简单。
 Github
=============
```
* 首先注册一个『GitHub』帐号。
* 建立与你用户名对应的仓库，仓库名为『your_user_name.github.com』或者『your_user_name.github.io』,我用的是后缀io
* 添加SSH公钥到『Account settings -> SSH Keys -> Add SSH Key』 
```
![](http://ww3.sinaimg.cn/large/006tKfTcgy1ffplg4xs2kj30xp0kb40y.jpg)
 Hexo
=============
前提是必须先安装 [Node.js](https://nodejs.org/en)，在安装node.js过程中不懂的尽情问Google吧。   
```
npm install hexo -g
```

## 初始化
如果制定 `<folder>`，便会在目前的文件夹下建立一个名为 `<folder>` 的新文件，否则会在目前文件下初始化。
```
hexo init <folder>
cd <folder>
```

## 安装依赖包
```
npm install
```
## 生产静态文件 && 服务
```
hexo generate || hexo g 
hexo server   || hexo s 
```
启动本地服务器，默认情况下，打开`http://localhost:4000/`。  
到目前状态下，个人博客雏形基本已经完成，接下来，将讲讲如何