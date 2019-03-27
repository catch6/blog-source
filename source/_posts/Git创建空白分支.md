---
title: Git创建空白分支
tags:
  - Git
categories:
  - 工作笔记
toc: false
translate_title: git-creates-a-blank-branch
date: 2019-01-24 18:30:57
---

今天在部署hexo的博客的时候，需要在github上创建两个分支：一个是发布分支 master 一个是源码分支source。
这就需要开一个空白分支，具体方法如下： 

```sh
# 在 git 上创建项目的时候可以选择添加一个 readme.md，然后 clone 下来
git clone https://github.com/CatchLife/catchlife.github.io
# 切换到 source 分支
git checkout --orphan source
# 清空文件
git rm -rf .
# 把源码文件放进去，或者直接修改 readme.md 文件，然后 提交到远程
git add .
git commit -m "init"
git push origin source
```