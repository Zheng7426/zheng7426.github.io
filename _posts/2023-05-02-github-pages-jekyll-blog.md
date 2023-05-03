---
title: 使用 Jekyll 和 GitHub Pages 来建立静态博客网站
category: GitHub
author: Hz.
---

[初始化](#初始化)

[安装Ruby](#安装-ruby)

[安装Jekyll](#安装-jekyll)

## 初始化
首先在 GitHub 上新建一个代码仓库(repository)，取名为 `<username>.github.io`。username 即你的 GitHub 用户名。

## 安装 Ruby
Jekyll 本身是一个 RubyGem，即你可以在 Gemfile 中将其作为依赖来引入。

Jekyll 所需的环境如下：

* Rudy 2.5.0 或更高版本

    我们可以在控制台使用如下命令查看现有的 ruby 版本确认其是否已经被安装: `ruby -v`

* RubyGems `gem -v`

* GCC 以及 Make `gcc -v`, `g++ -v`, `make -v`

计算机系统为 MacOS 的用户最好不要使用系统自带的 ruby，否则可能会遇到这样的问题:

* 执行个gem相关的命令时总是有权限问题需要用 sudo 输入密码 

* 版本过于陈旧无法正常安装依赖

按照 Jekyll [官网](https://jekyllrb.com/docs/installation/macos/)的说法，MacOS 用户最好去额外安装一个新的 Ruby 版本。


## 安装 Jekyll
满足以上环境要求之后，运行命令安装 Jekyll: `gem install jekyll bundler` 。

创建一个新的 Gemfile 以列出博客项目的依赖: `bundle init`

在 Gemfile 中添加 `gem "jekyll"`

运行 `bundle` 来针对刚才添加的 Gemfile 依赖来安装 gems:

```bash
Bundle complete! 1 Gemfile dependency, 30 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
```

由于 Jekyll 是静态网站生成器(static site generator)，在看见网页内容之前我们首先需要对其进行构建:

```bash
bundle exec jekyll build
```

使用 bundle exec 是为了确保使用的 jekyll 版本是我们 Gemfile 中所指定的版本。

## 使用模版

## Liquid
Liquid 是 Shopify 开发的一种模版语言(template language)。
 