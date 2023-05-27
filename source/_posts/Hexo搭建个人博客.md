---
title: Hexo零基础搭建个人博客
date: 2020-01-01 18:59:53
tags:
    - "blog"
    - "hexo"
categories:
    - "hexo"
---
# Hexo零基础搭建个人博客
Hexo是一个基于 node.js的快速生成静态博客的开源框架,支持 Markdown和大多数 Octopress
插件,一个命令即可部署到 Github页面、 Giteee、 Heroku等,强大的APl,可无限扩展,拥有
数百个主题和插件。

简单来说就是一个不用你写代码，就能搭建一套属于你自己的个人博客网站 应用（零基础小白也会）。

你可以在上面编写文章，做笔记，写日记，码代码。（一个属于你的世界！一个可供别人访问的个人世界）

另外Hero还提供了大量主题模版供用户下载。你的博客网站将可以时不时的换一种主题风格，赏心悦目，简直完美！

## 环境准备
1、安装Node.js
2、安装Git

## 开始安装Hexo
```
npm install -g hexo-cli
```
初始化hexo，新建存储博客的文件夹
```
hexo init blog
```
进入文件夹，安装一下npm
```
cd blog
```

```
npm install
```
启动服务站点
```
hexo g
```

```
hexo server
```
访问http://localhost:4000/

## 将hexo博客站点上传到github上
这里需要安装一个hexo的上传插件deploy-git
```
npm install hexo-deployer-git --save
```
 修改hexo配置文件指定仓库路径
可在文件夹中直接打开文件，也可通过vim直接编辑
找到Deployment加上（注意空格）
```
deploy:
  type: git
  repo: 你的仓库路径
  branch: master
```
## 推送hexo站点文件
```
hexo g
```
推送过程中需要输入你的github用户名和密码。但是在2021年8月14日开始github官方就加强安全访问。不能通过原有账号密码git访问，密码需要用官方的token或者采用ssh公私钥访问。否则会出现下图：鉴权失败（用户名密码错误）
```
    官方原话：

    近年来，GitHub 客户受益于 GitHub.com 的许多安全增强功能，例如双因素身份验证、登录警报、经过验证的设备、防止使用泄露密码和 WebAuthn 支持。 这些功能使攻击者更难获取在多个网站上重复使用的密码并使用它来尝试访问您的 GitHub 帐户。 尽管有这些改进，但由于历史原因，未启用双因素身份验证的客户仍能够仅使用其GitHub 用户名和密码继续对 Git 和 API 操作进行身份验证。

    从 2021 年 8 月 13 日开始，我们将在对 Git 操作进行身份验证时不再接受帐户密码，并将要求使用基于令牌（token）的身份验证，例如个人访问令牌（针对开发人员）或 OAuth 或 GitHub 应用程序安装令牌（针对集成商） GitHub.com 上所有经过身份验证的 Git 操作。 您也可以继续在您喜欢的地方使用 SSH 密钥
```
解决方式就是获取token，登录github设置setting->Developer Settings->Prosonal access tokens 创建一个新token。然后就可以拿这个token当密码输入了。
![1](https://img-blog.csdnimg.cn/img_convert/d37913a8a514a257bb25eb18fdc495fd.png)
![2](https://img-blog.csdnimg.cn/img_convert/af90dc7f99118b6b9c334b066ac7a560.png)
用户名和token输入后，上传成功。
输入你的仓库名称,即可访问成功。
https://你的仓库名称.github.io/

## 更换主题
博客样式太死板，想换成属于自己的风格，没问题我们可以更换博客的主题，来达到我们想要的风格。
到GitHub上搜索hexo主题或者hero自带的主题https://hexo.io/themes/
按照各自的主题文档上面一步步操作即可。
