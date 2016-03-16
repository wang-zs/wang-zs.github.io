---
title: "工具"
description: "目录"
layout: post
date: 2016-03-14 23:23:44 +0800
thumbnail: http://web.chenjun.com/images/vector_jerry_8ball_by_svezate-d6lzyyh.png
categories: [工具]
tags: [jekyll, github]
comments: yes
---
有空的话就看看：

github pages有两类：
你如果起个名为chendell.github.io的repository, 那么他的master分支上的文件就能在chendell.github.io的根目录访问到。
而如果是其他的repositories，比如这个repository名字叫node，那么建一个gh-pages分支，该分支下的文件就能在chendell.github.io/node/下访问到。

1. 门槛：需要理解 Github 的工作方式，熟悉 Github 客户端，熟悉 Html 与 CSS；
2. 不妨一边开始写静态模板，一边了解 Jekyll 布局所用到的 Liquid Tag，磨刀不误砍柴工；
3. Jekyll 博客，可以看作是一套文件结构，通过 Jekyll 程序编译成静态网站。如果不熟悉命令，完全可以不安装 Jekyll，只需按照要求的格式创建文件后再上传到 Github，然后访问主页就可以了，因为 Github Pages 便是由 Jekyll 驱动的，或者直接使用 Jekyll-Bootstrap 的结构；
4. Jekyll 的文件结构大概可以这样分：配置文件 _config.yml，布局文件 _layouts，模块文件 _includes，插件 _plugin，文章 _posts，其他文件（不以下划线开头的文件及文件夹都会完整的拷贝到生成的静态网站中，比如 CSS 文件、图片等），以及将会生成的静态站 _site；
5. Jekyll 命令很简单，先使用 cd 命令进入目标文件夹，然后输入 jekyll --server 生成网站，浏览器中输入 0.0.0.0:4000 访问生成的静态网站，jekyll --server --auto 命令将开启实时更新，修改文件后在浏览器中刷新就可看到效果，对本地调试很有帮助；
6. Github Pages 禁用所有插件，需要使用自定义插件，只能上传生成的网站文件 _site，或者试试 这个办法 ;
7. 想写草稿不想被编译？创建一个以下划线开头文件夹就会被忽略，例如在 _posts 下创建 _drafts 存储草稿；
8. 默认的 Markdown 引擎问题很多，建议替换成 RDiscount。