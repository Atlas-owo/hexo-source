---
title: git basic
date: 2017-08-14 18:40:39
tags: 
	- git
	- LearningPath
categories: Programming
---

## creat repositories

``` bash
$ git init
```

将当前目录变成git可以管理的仓库

## add file

``` bash
$ git add
```

 将文件推送至缓存区

 ``` bash
$ git commit -m 
```
"xxx" 将文件提交至仓库

``` bash
$ git status 
```

仓库实时状态

## time machine

``` bash
$ git diff <file>
```

查看仓库与工作区file文件的差别

``` bash
$ git log
```

历史记录

``` bash
$ git reset HEAD^
```

(或版本号) 回退至某一版本

``` bash
$ git reflog
```

历史命令

``` bash
$ git checkout -- <file>
```

丢弃工作区更改

``` bash
$ git reset HEAD <file>
```

可以把暂存区的修改撤销掉（unstage），重新放回工作区

## with github

``` bash 
$ git push origin master
```

本地库推送至远端库

``` bash 
$ git clone url
```

从远端库克隆