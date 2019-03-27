---
title: hexo-theme-pure源码修改记录--为部署到阿里云oss做准备
tags:
  - hexo
originContent: ''
categories:
  - 工作笔记
toc: false
translate_title: >-
  hexothemepure-source-code-change-record-prepared-for-deployment-to-alibaba-cloud-oss
date: 2019-03-27 23:41:06
---

由于oss要求访问必须是绝对文件路径，不能自动寻找index.html，所以修改源码，把hexo主题中xxx/格式改为xx/index.html，方便接下来主题升级时修改对应文件。

修改以下文件，在路径变量后添加index.html

```txt
\themes\pure\layout\_common\header.ejs
\themes\pure\layout\_partial\archive-post.ejs
\themes\pure\layout\_partial\item-post.ejs
\themes\pure\layout\_partial\pagination.ejs
\themes\pure\layout\_partial\post\copyright.ejs
\themes\pure\layout\_partial\post\date.ejs
\themes\pure\layout\_partial\post\nav.ejs
\themes\pure\layout\_partial\post\thumbnail.ejs
\themes\pure\layout\_partial\post\title.ejs
\themes\pure\layout\_widget\recent_posts.ejs
\themes\pure\layout\categories.ejs
\themes\pure\layout\category.ejs
\themes\pure\layout\tag.ejs
\themes\pure\layout\tags.ejs
```

