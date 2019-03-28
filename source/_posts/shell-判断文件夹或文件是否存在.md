---
title: shell 判断文件夹或文件是否存在
tags:
  - Linux
originContent: ''
categories:
  - 工作笔记
toc: false
translate_title: the-shell-determines-if-a-folder-or-file-exists
date: 2019-03-28 18:48:51
---

## 判断文件夹是否存在
```sh
if [ -d "/data/" ];then
echo "文件夹存在"
else
echo "文件夹不存在"
fi
```

### 判断文件是否存在
```sh
if [ -f "/data/filename" ];then
echo "文件存在"
else
echo "文件不存在"
fi
```

### 文件比较符
```sh
-e 判断对象是否存在
-d 判断对象是否存在，并且为目录
-f 判断对象是否存在，并且为常规文件
-L 判断对象是否存在，并且为符号链接
-h 判断对象是否存在，并且为软链接
-s 判断对象是否存在，并且长度不为0
-r 判断对象是否存在，并且可读
-w 判断对象是否存在，并且可写
-x 判断对象是否存在，并且可执行
-O 判断对象是否存在，并且属于当前用户
-G 判断对象是否存在，并且属于当前用户组
-nt 判断file1是否比file2新  [ "/data/file1" -nt "/data/file2" ]
-ot 判断file1是否比file2旧  [ "/data/file1" -ot "/data/file2" ]
```
