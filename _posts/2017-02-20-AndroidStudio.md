---
layout: post
title: Android Studio Code Template个性化设置
category: Android Studio
comments: true
---

![](http://upload-images.jianshu.io/upload_images/2926311-cf8fb9f33104bac6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

题注：Android Studio的体验性确实要比Eclipse上的效率高，下面的几点小配置可能对你的代码规范起到一点小小的作用
___

##导读

- 添加文件描述
- 添加方法注释
- logcat配置

___
###添加文件描述
step1: 点击 setting>>Editor>>File and code Templates 
step2: 选中includes标签 
step3: 点击File Header 
step4: 在右边输入框输入以下内容

```
  /** 
    * author: ${USER} 
    * created on: ${DATE} ${TIME} 
    * description: 
    */
```

###添加方法注释
step1: 点击 setting>>Editor>>File and code Templates 
step2: 选中includes标签 
step3: 点击绿色的”+”新建一个名为”Method Header”的子元素 
step4: 选中新建的”Method Header”，在右边输入框输入以下内容，点击OK

```
  /**
   * description: <一句话功能简述> 
   * @param [参数1] [参数1说明] 
   * @param [参数2] [参数2说明] 
   * @return [返回类型说明] 
   * @exception/throws [违例类型] [违例说明] 
   * @see [类、类#方法、类#成员] 
   */
```

step5: settings>>keymap>>Other>>fix doc comment 
step6:右击fix doc comment 选择 Add Keyboard shortcut 
step7:按下自己喜欢的快捷键,点击OK，再点击OK
###Logcat配置
File->Settings 或Ctrl + Alt +S 找到 Editor -> Colors &Fonts -> Android Logcat 或在上面的搜索框中输入Logcat 点中Verbose , Info, Debug等选项，然后在后面将Use Inberited attributes 去掉勾选 再将 Foreground 前的复选框选上，就可以双击后面的框框去选择颜色了 Apply–>OK

```
      Log级别色值
      VERBOSE     BBBBBB
      DEBUG        0070BB
      INFO           48BB31
      WARN         BBBB23
      ERROR        FF0006
      ASSERT       8F0005
```
