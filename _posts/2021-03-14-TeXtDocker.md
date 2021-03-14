---
layout: article
title: 'jekyll-TeXt Win10开发环境搭建'
key: 16
category: Document
tags:
- 博客
- 教程
---

## 安装Win10版本Docker

具体步骤省略

## 生成Gemfile.lock文件

克隆TeXt主题/或者你的TeXtRepo

```bash
git clone https://github.com/kitian616/jekyll-TeXt-theme.git
```
在根目录打开PowerShell，运行：

```bash
docker run -v /D/GitHub/niconewbeee.github.io:/usr/src/app -w /usr/src/app ruby:2.7 bundle install
```
将 /D/GitHub/niconewbeee.github.io 替换成Gemfile所在地址

这样就生成了Gemfile.lock 文件

## 创建Docker镜像
```bash
docker-compose -f ./docker/docker-compose.build-image.yml build
```

## 本地预览
```bash
docker-compose -f ./docker/docker-compose.default.yml up
```

[TeXt官方教程](https://tianqi.name/jekyll-TeXt-theme/docs/zh/quick-start)
[NicoNewBeee的博客](https://lzdnico.github.io/niconewbeee.github.io/)
[Telegram频道](https://t.me/clashwebgroup)

