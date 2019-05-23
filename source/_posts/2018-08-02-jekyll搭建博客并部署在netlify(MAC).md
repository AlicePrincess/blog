---
layout: post
title: 'jekyll搭建博客并部署在netlify(MAC)'
subtitle: '快速搭建一个属于自己的博客，并且不需要数据库的存储和服务器的要求'
date: 2018-08-02
categories: 技术
cover: 'http://pcvfuus6c.bkt.clouddn.com/cover/blog_1.jpg'
tags: 技术 jekyll 博客
---
### jekyll是什么

jekyll是一个简单的免费的Blog生成工具，类似WordPress。但是和WordPress又有很大的不同，原因是jekyll只是一个生成静态网页的工具，不需要数据库支持。但是可以配合第三方服务,例如Disqus。最关键的是jekyll可以免费部署在Github上，而且可以绑定自己的域名。

### 安装ruby(同时会自动安装gem)
mac下面自带了Ruby环境（查看是否有ruby）
```bash
ruby -v 
```
输出
```bash
ruby 2.3.3p222 (2016-11-21 revision 56859) [universal.x86_64-darwin17]
```
+ jekyll 最新版要求 ruby 2.1或更高,所以更新ruby

### Jekyll 环境配置

安装 jekyll

```bash
gem install jekyll  
```

创建博客

```bash
jekyll new myBlog 
```

进入博客目录

```bash
cd myBlog
```
打包项目

```bash
jekyll build
```
运行项目

```bash
jekyll server
```
* jekyll提供了很多的主题可以直接使用[主题官网](http://jekyllthemes.org/)
* 在github或者gitlab上创建一个代码托管的仓库，并将代码提交
### netlify中配置部署
* 打开[netlify](https://app.netlify.com/)的官网
* 注册一个账号
* 选择sites
![](http://pcvfuus6c.bkt.clouddn.com/article/2018_8_3_1.png)
* 根据自己的代码存储选择托管平台
![](http://pcvfuus6c.bkt.clouddn.com/article/2018_8_3_2.png)
* 选择自己博客的仓库
![](http://pcvfuus6c.bkt.clouddn.com/article/2018_8_3_3.png)
* build command中写jekyll build，publish directory中写_site
![](http://pcvfuus6c.bkt.clouddn.com/article/2018_8_3_4.png)
* 最后点deploy site就好了

#### 如果你有自己的域名可以把自己的域名绑定上
![](http://pcvfuus6c.bkt.clouddn.com/article/2018_8_3_5.png)

#### 如果没有域名也可以设置netlify提供的域名的二级域名前缀
![](http://pcvfuus6c.bkt.clouddn.com/article/2018_8_3_6.png)

### 这样博客就大功告成了！