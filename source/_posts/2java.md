---
title: 2-JAVAcmd和开发软件的编码格式
data: 2021-8-21
---

# 编码格式

使用cmd来编译.Java文件时，需要使文件编码格式和cmd编码格式保持一致，否则使用cmd编译时会报错

![cmd编码格式](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/gbk1.png)

![开发软件编码格式](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/gbk2.png)

# cmd  中 java命令和javac命令

首先编写.java文件，这里我懒得用txt写，就直接在eclipse里写好了

![](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/helloworld.png)

接下来运行

![](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/helloworld4.png)

随后我们在cmd中检验一下（注意java文件的包路径！）

``` ba
javac helloworld.java
//该目录下会生成文件helloworld.class
java hello
//执行主类hello，不是执行hello.class文件！
```

执行第一条语句时会在对应文件夹生成class文件

![](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/helloworld2.png)

随后解析，生成的结果与前面的一致！

![](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/helloworld3.png)

# 开发细节

1.Java源文件以.java为扩展名。源文件的基本组成部分是类(class)

2.Java应用程序的执行入口是main()方法。它有固定的书写格式:public static void main(Stringl] args){.….}

3.Java语言严格区分大小写。

4.Java方法由一条条语句构成，每个语句以“;”结束。

5.大括号都是成对出现的，缺一不可。[习惯，先写争再写代码]

6.一个源文件中最多只能有一个public类。其它类的个数不限

7.如果源文件包含一个public类，则文件名必须按该类名命名!

8.一个源文件中最多只能有一个public类。其它类的个数不限，也可以将main方法写在非public类中，然后指定运行非public类，这样入口方法就是非public的main方法

END
