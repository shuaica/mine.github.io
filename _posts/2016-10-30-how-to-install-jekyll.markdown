---
layout:     post
title:      "Windows下Jekyll本地安装"
date:       2016-10-30 12:00:00
author:     "Xshuai"
header-img: "img/post-bg-jekyll.png"
tags:
    - Jekyll
    - ruby
---

> 就记录下windows下Jekyll的安装

## 安装Ruby 

[Ruby安装文件下载地址](http://rubyinstaller.org/downloads/)

下载对应版本，我的电脑是64位的下载64位的版本；

然后就是windows下傻瓜式的安装了，双击安装即可。

记得在安装过程中会让你勾选`Add Ruby executables to your path`，不勾选的话，后面在window中设置下环境哪里设置下也是可以的。

 *ruby安装目录勿使用空格，勿使用特殊字符，勿安装在中文目录下。当然我没有尝试过如果这样做，会发生什么。*
 
## 安装Ruby DevKit

下载Ruby DevKit：[Ruby DevKit 下载地址] (http://rubyinstaller.org/downloads/)

下载选择对应的版本，例如win64位等。

双击安装会出现解压目录，我安装在C盘了，`C:\devkit`

## 初始化
- 1.cd 进入C:\devkit目录
- 2.执行以下命令
	`ruby dk.rb init
    ruby dk.rb install `
    > ruby dk.rb install 居然失败了，多尝试几次，不知所以然

## 安装Jekyll
- 使用命令
`gem install jekyll`
 国内网络环境大多会报错，请翻墙
- 不想翻墙的话就改下源
`gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/`
 以上命令如果报ssl错误。尝试使用以下命令
`gem sources --add http://gems.ruby-china.org/ --remove https://rubygems.org/`
*这两个命令的区别是http和https的去吧，孩子可是要认真一点儿啊*
- 检查下
` gem sources -l` 出现
https://gems.ruby-china.org
请确保只有 gems.ruby-china.org

## that's all! done!