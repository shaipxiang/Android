---
layout: post
title: 正则学习记录
category: Regular Expression
comments: true
---

![](http://upload-images.jianshu.io/upload_images/2926311-b09ddca34ef2e8ae.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
题注：正则表达式也称为规则表达式或字符串规则表达式，此文记录正则表达式的一些基本用法，适合正则入门使用。

___



  #### 基本规则

  #### 示例

```  
  英文文档中查找单词 hi
  正则： \bhi\b
  \b代表空格，隔离him,history等单词
```

```
  三位区号8位数字的电话号
  正则： 0\d\d-\d\d\d\d\d\d\d\d      简化： 0\d{2}-\d{8}
```

- #####常用元字符

      ^       匹配字符串的开始   
      $      匹配字符串的结束   
      .       匹配除换行符外的所有字符    
      \d     匹配数字    
      \w     匹配字符或数字或下划线或汉字    
      \s     匹配任意的空白符    
      \b     匹配单词的开始或结束

- #####匹配类型 POSIX和PEAL
  POSIX:
  
      [:upper:]        匹配所有的大写字母    
      [:lower:]        匹配所有的小写字母    
      [:alpha:]        匹配所有的字母    
      [:alnum:]        匹配所有的数字和字母    
      [:digit:]        匹配所有的数字    
      [:xdigit:]        匹配所有的16进制字符，等价于[0-9A-Fa-f]   
      [:punct:]        匹配所有的标点符号，等价于[.,'''?!;:]
    
  PERL:
  
      \n      换行符
      \r       回车符
      \t       制表符
      \d      任一十进制数字
      \s       任一空白字符
      \w     任一“字”可见的字符

```
  匹配QQ号  5-12位
  表达式：  ^\d{5,12}$
```

- 字符转义

      转义字符     \
      比如  匹配\      表达式：\\\
      类似  \\.    \\*   \\+等等
  

- 常用限定符

      *      匹配0次或多次 
      ?      匹配0次或1次 
      +      匹配1次或多次 
      {n}    匹配n次 
      {n,}   匹配n次或更多次 
      {n,m}匹配n到m次

- 字符范围

      [aeiou]   匹配任意一个元音字母  
      [.?!]        匹配标点符号 
      所以[0-9]   等同  \d 
      [a-z0-9A-Z_]  等同 \w

- 反义

    有定义的元字符大写，即为反义，字符集前面加上^ 也为反义
  
      \W      匹配任意不是字母、数字、下划线或汉字的字符   
      \D       匹配任意不是数字的字符   
      \S       匹配任意不是空白符的字符    
      \B       匹配不是单词开始或结束的字符    
      [^X]     匹配任一不是X的字符    
      [^aeiou]  匹配任一不是元音字母的字符

- 并列

      用  |  表示或者，合并为一组使用  
      用 （）表示是一个字表达式

```
  匹配座机号
  0\d{2}-\d{8}|0\d{3}-\d{7}
```

```
  匹配Ip地址
  ^(\d[1,2]|1\d\d|2[0-4]\d|25[0-5]\.){3}((\d[1,2]|1\d\d|2[0-4]\d|25[0-5])$
```