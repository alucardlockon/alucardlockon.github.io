---
title: Atom安装插件的几个方法
---

Atom是一个很好用的编辑器，之前一直在纠结了用什么编辑器好，在对比了VSCode/Sublime Text3和Atom之后，我还是继续选择了Atom。Atom一个重要的功能就是插件(或者说package)，但是身在你国，Atom插件安装总是有点不稳定，比如下图：  
![install卡住了有木有?](http://obsq1xssc.bkt.clouddn.com/20160812-02.JPG)

在Atom设置界面中点击下载插件以后因为网络原因大多数情况都会卡住/报错。所以，还是自己手动安装需要的插件吧。  
### 方法一：使用apm安装工具
apm(Atom Package Manager)是atom的包管理工具，可以方便的管理Atom的插件。  
下面以安装插件atom-beautify为例:  
首先打开你的cmd/bash,切换到atom的插件目录  
```
$ cd ~/.atom/packages
```
使用  
```
$ apm install <package-name>
```
这里的<package-name>换为atom-beautify，运行命令。等待一些时间后，ok！atom-beautify安装完成。  
![安装](http://obsq1xssc.bkt.clouddn.com/20160812-03.JPG)  
重新打开你的Atom，是不是已经可以看到菜单里有atom-beautify了?  
![安装后的菜单](http://obsq1xssc.bkt.clouddn.com/20160812-04.JPG)   
### 方法二：使用git clone整个插件的仓库  
这种方法可能会少相关依赖，需要自行在package里运行`npm install <node-package>`安装相关的依赖。  
在atom.io上(或者在atom设置界面中跳转到插件的网页)找到插件页面，点击Repo跳到插件的github仓库，将<repo-url>替换为仓库的地址，然后在packages目录下运行下列命令：
```
$ git clone <repo-url>
```
### 方法三：使用自己创建的仓库
为了保证各个设备的Atom设置同步，可以自己新建一个git仓库，把自己的插件及配置文件(config.cson,snippets.cson等等...) 提交上去，今后就可以方便的安装自己提交上去的插件啦！  
```
$ git clone https://github.com/alucardlockon/MyAtomPackagesAndConfig
```
![我的atom设置同步仓库](http://obsq1xssc.bkt.clouddn.com/20160812-01.JPG)