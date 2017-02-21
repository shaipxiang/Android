---
layout: post
title: Android Studio常用插件
category: Android Studio
comments: true
---

![](http://upload-images.jianshu.io/upload_images/2926311-df8e33e1763dbcad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
导读：Android Studio是一个功能全面的开发环境，装备了为各种设备——从智能手表到汽车——开发Android应用程序所需要的所有功能。不过总是有改进的余地，Android Studio对此提供了对第三方插件的支持，下面本文将介绍一些比较实用的插件。

___


####第三方插件安装方法：
打开Android Studio，Settings—>Plugins，选择Browser...在线安装，输入插件名字搜索安装既可，也可以选择磁盘安装，安装完成后重启生效。

> 注意事项：代理设置关闭才能搜索到插件。

#####1、Sexy Editror
      设置编辑区背景图片，作用不大，只是为了好玩^_^
      
#####2、ButterKnife Zelezny
      ButterKnife 注解生成器，使用起来非常简单方便。
      
#####3、[SelectorChapek](https://github.com/inmite/android-selector-chapek)
      资源文件生成selector文件专用，只需要设置好图片的规范命名即可。

![命名规范](http://upload-images.jianshu.io/upload_images/2926311-d4aab755d610826a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![生成文件示例](http://upload-images.jianshu.io/upload_images/2926311-9bae09b79174a8ce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 4、[GsonFormat](https://github.com/zzz40500/GsonFormat)
      现在大多数服务端api都以json数据格式返回，而客户端需要根据api接口生成相应的实体类，这个插件把这个过程自动化了，赶紧使用起来吧。

#####5、Android Parcelable Code Generator
     Android中的序列化有两种方式，分别是实现Serializable接口和Parcelable接口，但在Android中是推荐使用Parcelable，只不过我们这种方式要比Serializable方式要繁琐，那么有了这个插件一切就ok了。

#####6、LeakCanary
Android 和 Java 内存泄露检测,开发阶段使用，强烈建议。
使用说明：https://www.liaohuqiu.net/cn/posts/leak-canary-read-me/
推荐博文：http://www.jianshu.com/p/a8900eb3de12

#####7、adb idea
开发阶段快速进行安装app缓存清空，便于测试调试。

#####8、Android Postfix completion 强大
根据后缀提醒快速完成代码

#####9、Adb wifi  /  adb wifiadb
无线调试应用

#####10、JsonOnlineViewer
可实现直接在android studio中调试接口数据，可以选择请求类型，自定义请求头及请求体，json数据格式化后展示，配合着Gsonformat会不会不错呢？

#####11、**Android Holo Colors Generator**
没用过，Android Holo Colors Generator是一个允许你为你的应用程序随心所欲地创建Android布局组件的插件。此插件会生成所有必要的可在项目中使用的相关的XML画板和样式资源。

#####12、codota
该网站搜集了大量的代码，号称超过700W的代码实例。

#####13、**[GradleDependenciesHelperPlugin](https://github.com/ligi/GradleDependenciesHelperPlugin)**
Maven gradle依赖自动补全

#####14、**Genymotion **  强大强大
注册下载安装Genymotion
android studio安装插件，重启后关联Genymotion安装目录，重启电脑生效
  Genymotion模拟器下载失败解决方法：
- 到C:\Users\yourname
\AppData\Local\Genymobile\Genymotion\ova该目录下找ova文件，yourname就是你自己的电脑用户名。
- 拼接网址，直接用下载工具下载ova文件
[http://files2.genymotion.com/dists/6.0.0
/ova/genymotion_vbox86p_6.0_151118_185105.ova
](http://files2.genymotion.com/dists/6.0.0/ova/genymotion_vbox86p_6.0_151118_185105.ova)
上面的网址就是下载网址，直接用浏览器或者下载工具下载即可。
前面的6.0.0就是版本号，后面标红色的文件就是你的ova文件名称。
- 如果遇到不能导入ova的情况，直接升级virtual box即可。 virtual box 存放镜像的位置为C:\Users\yourname
\VirtualBox VMs\，升级virtualbox后直接到该文件夹下
