## GitHub Page修改根据minixalpha提供的飞鸟集GitHub page框架快速搭建
---

### 修改
 - 去掉disqus评论（需要翻墙），增加多说评论
 - 增加站内搜索，百度和google都测试了，没成功，先隐藏了，分析原因应该是子页面是解析md文件的原因，有想实验的可以共同探讨
 - 修改底部导航栏
---

## 基于 GitHub Pages 搭建的极简博客，所有操作都可以直接通过浏览器完成。

可以通过访问 [示例](http://shaipxiang.github.io/android/) 看到最终
的效果

## 教程

### 使用方法(此示例为原作者地址：飞鸟集)

1. 注册 GitHub，得到用户名，例如 minixalpha
2. 到 [StrayBirds](https://github.com/minixalpha/StrayBirds) 页面，单击右上
角的 Fork
3. 到你 Fork 后的项目中，将 `_config.yml` 中的 username 修改为你的用户名 minixbeta
4. 访问你的博客 http://minixbeta.github.io/StrayBirds/

![create_project](/images/create_project.gif)

**注意如果你是第一次使用 GitHub Pages，可能不会马上生效，等一段时间即可**

**按照配置中说的方法修改项目名称可能会加快这一进程**

### 配置

* 修改主题

在 `_confg.yml` 下修改 theme 的值。

**注意修改主题后，并不会马上生效，GitHub 还要反应一段时间，所以请耐心等待**

**修改主题后, 按照配置中说的方法修改项目名称可能会加快这一进程**

可选主题包括：

- hack
	![hack-demo](/images/hack-demo.png)
- leap-day
	![leap-day-demo](/images/leap-day-demo.png)
- merlot
	![merlot-demo](/images/merlot-demo.png)
- midnight
	![midnight-demo](/images/midnight-demo.png)
- minimal
	![minimal-demo](/images/minimal-demo.png)
- modernist
	![modernist-demo](/images/modernist-demo.png)
- slate
	![slate-demo](/images/slate-demo.png)
- time-machine
	![time-machine-demo](/images/time-machine-demo.png) 
- kunka
	![kunka-demo](/images/kunka-demo.png)

* 修改项目名

例如将 StrayBirds 修改为 blog，那么你需要做的是

1. 在项目的 Setting 中将 Repository name 从 StrayBirds 修改为 blog
2. 将 `_config.yml` 中的 baseurl 修改为 /blog
3. 通过 http://minixbeta.github.io/blog/ 来访问你的新博客

![create_post](/images/change_project_name.gif)


* 修改评论系统用户名（此处做了修改，关闭disqus，增加多说）
disqus评论系统需要翻墙，国内访问限制较多，修改为多说评论
需要先去注册一下，复制JavaScript代码进文章详情页面即可。

**千万注意: 复制代码时一定要修改JavaScript中的三个值，此处参考我的代码，不然就评论不到页面中去了**

### 添加文章

在 `_post` 目录下添加形如 `2017-01-01-title.md` 的文章，用 markdown 格式
撰写博客，会自动分配到对应的目录中（目录没有会自动创建）

例如：

```
---
layout: post
title: Java 中的并发
comments: true
category: 技术
---


## 如何创建一个线程

按 Java 语言规范中的说法，创建线程只有一种方式，就是创建一个 Thread 对象。而从 HotSpot 虚拟机的角度看，创建一个虚拟机线程
有两种方式，一种是创建 Thread 对象，另一种是创建 一个本地线程，加入到虚拟机线程中。

...

```

其中 `layout` 表示布局，不用改变，`title` 表示文章题目，`comments` 表示是否要开户评，此处为disqus可不管。

![create_post](/images/create_post.gif)

## 感谢

Thanks to authors of the themes:

* [hack](https://github.com/sundaykofax/baby-legs), Licence: None
* [leap-day](https://github.com/mattgraham/leapday), Licence: [Creative Commons Attribution](http://creativecommons.org/licenses/by/3.0/)
* [merlot](https://github.com/cameronmcefee/headsmart/tree/gh-pages), Licence: None
* [midnight](https://github.com/briandoll/change-inside-surroundings.vim/tree/gh-pages), Licence: None
* [minimal](https://github.com/orderedlist/minimal), Licence: [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/)
* [modernist](https://github.com/orderedlist/modernist), Licence: [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/)
* [slate](https://github.com/jasoncostello/slate), Licence: MIT
* [time-machine](https://github.com/jonrohan/time-machine-theme), Licence: None
* [kunka](https://github.com/pizn/kunka), Licence: MIT, author: [zhanxin.info](http://www.zhanxin.info/)

All the themes are intergrated in the blog template, with some modifies.
