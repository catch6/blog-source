---
title: '解决deepin下sudo: add-apt-repository：找不到命令'
tags:
  - Deepin
originContent: ''
categories:
  - 工作笔记
toc: false
translate_title: solve-the-sudo-addaptrepository-under-deepin-command-not-found
date: 2018-12-06 18:30:18
---

因为 deepin 自身没有支持这个命令需要手动安装，执行如下命令就可以正常使用了

```sh
sudo apt-get install python-software-properties
sudo apt-get install software-properties-common
```