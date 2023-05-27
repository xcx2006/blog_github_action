---
title: github_action翻车记录
date: 2023-01-31 17:59:53
comment: true
excerpt: "我真傻，真的。我单知道github_action自动搭建博客比较困难，可…"
tags:
    - "翻车"
    - "github"
    - "hexo"
categories:
    - "github"
---
这是我的配置文件
```
name: 自动部署
# 当有改动推送到master分支时，启动Action
on:
  push:
    branches:
      - main

  release:
    types:
      - published

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: 检查分支
        uses: actions/checkout@v2
        with:
          ref: main

      - name: 安装 Node
        uses: actions/setup-node@v1
        with:
          node-version: "19.x"

      - name: 安装 Hexo
        run: |
          export TZ='Asia/Shanghai'
          npm install hexo-cli -g
      - name: 缓存 Hexo
        id: cache-npm
        uses: actions/cache@v3
        env:
          cache-name: cache-node-modules
        with:
          path: node_modules
          key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
          restore-keys: |
            ${{ runner.os }}-build-${{ env.cache-name }}-
            ${{ runner.os }}-build-
            ${{ runner.os }}-
      - name: 安装依赖
        if: ${{ steps.cache-npm.outputs.cache-hit != 'true' }}
        run: |
          npm install gulp-cli -g #全局安装gulp
          npm install --save
      - name: 生成静态文件
        run: |
          hexo clean
          hexo g
      - name: 部署到Github
        uses: JamesIves/github-pages-deploy-action@v4
        with:
          token: 别想看了
          repository-name: xcx2006/xcx2006.github.io
          branch: main
          folder: public
          commit-message: "${{ github.event.head_commit.message }} Updated By Github Actions"
```
好不容易才把github action配置好，结果发现之前的博客文章没有标注时间的全部都乱了。
![](https://i.328888.xyz/2023/01/31/8eh7t.jpeg)
原因：有一部分偷懒没标注时间。同步到仓库后默认时间全部都变动了。
只能重新添加时间=(
