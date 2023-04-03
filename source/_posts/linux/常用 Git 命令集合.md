---
title: 常用 Git 命令集合
date: 2021-8-03 14:59:53
tags: linux
categories: linux
mathjax: true
---

将本地仓库与远程仓库对接
对Git进行初始化：
```
git init
```
```
git add .
git commit -m 'xxx'
```
拷贝远程仓库链接：

以 GitHub 为例：git@github.com:{用户名}/{仓库名}.git

在预对接的本地仓库根目录执行：
```
git remote add origin git@github.com:{用户名}/{仓库名}.git
```
继续执行（请注意，在此步骤之前，需要生成公私钥，并将公钥上传至Github）：
以master分支为例.
```
git push -u origin master
```
生成公、私钥
为了鉴别谁在控制仓库，需要使用公私钥对身份进行校验以确保安全.
生成公私钥的方法如下：
```
ssh-keygen -t rsa -C "youremail@example.com"

<Enter> // 回车

<Enter> // 回车

<Enter> // 回车
```
存放公私钥的目录在~\

公钥的扩展名为.pub，私钥无扩展名.

将公钥上传至https://github.com/settings/keys ，即可完成公私钥配置.
将本地仓库与远程仓库同步(合并)

以master分支为例.
```
git pull origin master
```
将本地仓库同步到远程仓库(合并)
以master分支为例.
```
git push origin master
```
克隆远程库到本地
```
git clone <仓库远程地址>
```
查看仓库状态
```
git status
```
比较仓库文件
git diff
回溯版本
```
git reset
```
新建分支与切换、合并、删除分支
分支是用来将特性开发绝缘开来的。在你创建仓库的时候，master 是"默认的"分支。在其他分支上进行开发，完成后再将它们合并到主分支上。
```
git checkout -b <name> // 新建分支

git checkout <name> // 切换分支

git merge <name> // 合并分支

git branch -d <name> // 删除分支
```
