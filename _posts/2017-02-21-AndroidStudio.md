---
layout: post
title: Android Studio入门常见问题
category: Android Studio
comments: true
---


![](http://upload-images.jianshu.io/upload_images/2926311-95d15673eb47efe1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
题注：以前学习Android Studio在有道云上做的散记，现在转移到GitHub Page上
___

### HTTP代理设置
1. 到android studio安装目录，打开bin目录，编辑idea.properties, 在文件末尾添加:
```
disable.android.first.run=true
```
这将禁用第一次运行
2.再次打开android studio将进入欢迎页面，点击Config..., 搜索HTTP，即可设置HTTP代理
3.删掉Step 1 中所加的那一行，再次启动android studio，就可以使用你的HTTP代理下载SDK等组件了。

###保存Studio配置
1. 选择 File -> Export Settings...，选择到处后的存放地址，保存为 settings.jar
2.把这个 jar 包保存起来。
3.换机或者重装导入配置，选择 File -> Import Settings...，然后选择第二步中的 jar 包，选择需要导入的模块，点击 OK 即可。

###SDK更新失败
1.打开SDK目录 安装时默认地址为C:\Users\Administrator\AppData\Local\Android\sdk 。打开SDKManager，选择Tools下的Options，将如图所示选项勾上。也就是others中第一个选项.
2.然后打开C:\WINDOWS\system32\drivers\etc中的hosts文件，在最后一行添加如下内容：
```
　　203.208.46.146 www.google.com
　　74.125.113.121 developer.android.com
　　203.208.46.146 dl.google.com
　　203.208.46.146 dl-ssl.google.com
```
###引用jar文件
1、将jar包拷贝到moudle的libs目录下
2、右键jar，Add as library,然后选择moudle
3、打开App目录下有个build.gradle文件应该项目结构文件，上述的动作只是为了在在文件下添加
```
dependencies {
      compile files('libs/android-support-v13.jar')
      compile files('libs/odata4j-0.7.0-clientbundle.jar')
}
```

###引用so文件
java.lang.UnsatisfiedLinkError: Couldn't load library xxxx from loader dalvik.system.PathClassLoader
引用so文件失败
1、在“src/main”目录中新建名为“jniLibs”的目录；
2、复制so文件到“jniLibs”目录内。
###引用第三方源码库
1、将第三方源码导入同一个project或者放在同文件夹下
2、接下来需要手工修改项目跟目录下settings.gadle 添加
```
    include ':App',':Httpzoid'
```
这里必须手工修改没有其他方法
然后在打开App/build.gradle这个文件，添加
```
  dependencies{
    compile project(':Httpzoid')
  }
```
3、在项目Httpzoid目录下添加一个build.gradle的这个文件，内容如下
 ```
buildscript {
repositories {
mavenCentral()
}
dependencies {
classpath 'com.android.tools.build:gradle:0.6.+'
}
}
apply plugin: 'android-library'
 
repositories {
mavenCentral()
}
 
android {
compileSdkVersion 18
buildToolsVersion "17.0.0"
 
defaultConfig {
minSdkVersion 14
targetSdkVersion 18
}
 
 
sourceSets {
main {
manifest.srcFile 'AndroidManifest.xml'
java.srcDirs = ['src']
resources.srcDirs = ['src']
aidl.srcDirs = ['src']
renderscript.srcDirs = ['src']
}
}
}
 
dependencies {
compile 'com.android.support:appcompat-v7:+'
compile files('libs/gson-2.2.4.jar')
}
```
###中文乱码问题
- IDE乱码
File > Settings > Appearance & Behavior > Appearance，将default fonts改为SimSun
- 代码中
File > Settings > Editor > File Encodings 里Project Encoding改为UTF-8，下面Default Coding for properties 也改为UTF-8
- Gradle乱码
代码中的中文注释乱码：
项目下的build.gradle下添加以下代码即可解决 
```
tasks.withType(Compile) {  
    options.encoding = "UTF-8"  
}  
```
Gradle2.0+环境下需将Compile改为JavaCompile
```
tasks.withType(JavaCompile) {  
    options.encoding = "UTF-8"  
}  
```
###利用JavaDoc生成项目API文档
1. 在Android Studio中的菜单项中点击Generate JavaDoc
2.如果你的项目中有以“UTF8”做编码的java文件，那么你在这里必须要带上参数: -encoding utf-8 -charset utf-8，否则会报错
###删除不用的项目
1.最新版的Android studio已经可以完全删除项目了，点击File——Project Structure
2.在Project Structure页面，选中要删除的项目，点击上面的减号图标。
3.弹出“Remove Module”的弹框，点击Yes，然后ok
4.在项目上点击右键，delete就可以把module删除掉了
