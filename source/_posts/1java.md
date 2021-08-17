---
title: 1-JAVA开发入门
date: 2021-08-17
---

# <p style="color: darkcyan">JAVA特点</p>

1. 简单易用
<mark style="background-color:#CCC">不使用指针，而是引用，并且提供了自动垃圾回收机制，不用过多操心内存管理问题</mark>
2. 安全可靠
<mark style="background-color:#CCC">JAVA程序运行之前会利用字节确认器进行代码安全检查，确保程序不会存在非法访问</mark>
3. 跨平台
<mark style="background-color:#CCC">可以在不同的操作系统上运行JAVA程序</mark>
4. 面向对象
<mark style="background-color:#CCC">事务看成对象，关系看成继承</mark>
5. 支持多线程
<mark style="background-color:#CCC">JAVA有多线程接口</mark>

---

# <p style="color: darkcyan">JDK和JRE</p>

## 定义

**JRE(Java Runtime Enviroment)**  是Java的运行环境。面向Java程序的使用者，而不是开发者。如果你仅下载并安装了JRE，那么你的系统只能运行Java程序。JRE是运行Java程序所必须环境的集合，包含JVM标准实现及 Java核心类库。它包括Java虚拟机、Java平台核心类和支持文件。它不包含开发工具(编译器、调试器等)。

**JDK(Java Development Kit)又称J2SDK(Java2 Software Development Kit)**  是Java开发工具包，它提供了Java的开发环境(提供了编译器javac等工具，用于将java文件编译为class文件)和运行环境(提 供了JVM和Runtime辅助包，用于解析class文件使其得到运行)。如果你下载并安装了JDK，那么你不仅可以开发Java程序，也同时拥有了运 行Java程序的平台。JDK是整个Java的核心，包括了Java运行环境(JRE)，一堆Java工具tools.jar和Java标准类库 (rt.jar)。

## 区别

**JRE主要包含**：java类库的class文件(都在lib目录下打包成了jar)和虚拟机(jvm.dll)

**JDK主要包含**：java类库的 class文件(都在lib目录下打包成了jar)并自带一个JRE。那么为什么JDK要自带一个JRE呢？而且jdk/jre/bin下的client 和server两个文件夹下都包含jvm.dll(说明JDK自带的JRE有两个虚拟机)

只需要运行JAVA程序JRE即可，若要开发，就选JDK。这个解释够简便吧？

---

# <p style="color: darkcyan">JAVA运行机制</p>

这个很简单，下面演示一套流程

**Java文件(*.java文件)**
↓
javac编译
↓
**字节码文件(编译生成.class文件)**
↓
java解释执行
↓
**计算机可识别的机器码文件**

---

# <p style="color: darkcyan">环境变量配置</p>

这个不过多阐述，直接放图(注意路径)

![CLASSPATH](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/1-java1.png)
![JAVAHOME](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/1-java2.png)
![PATH](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/1-java3.png)


END