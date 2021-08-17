---
title: 4-HTML标签-格式化
date: 2021-08-07
---
OK！我是薯角，废话不多说，直接开始正题

## &lt;abbr&gt;
标签指示简称或缩写，通过对缩写进行标记，您能够为浏览器、拼写检查和搜索引擎提供有用的信息。
**实例**
标记一个缩写:
``` bash
The <abbr title="People's Republic of China">PRC</abbr> was founded in 1949.
```
**提示**:可以在 &lt;abbr&gt;标签中使用全局的 title 属性，这样就能够在鼠标指针移动到&lt;abbr&gt;元素上时显示出简称/缩写的完整版本。


## &lt;bdo&gt;
bdo 元素可覆盖默认的文本方向。
**实例**
``` bash
<bdo dir="rtl">Here is some text</bdo>
```
## 可选属性
| 属性 | 值 | 描述 |
| --- | --- | --- |
| dir | ltr<br />rtl | 定义文字方向 |


## &lt;blockquote&gt;
&lt;blockquote&gt; 标签定义块引用。
&lt;blockquote&gt;与&lt;/blockquote&gt;之间的所有文本都会从常规文本中分离出来，经常会在左、右两边进行缩进（增加外边距），而且有时会使用斜体。也就是说，块引用拥有它们自己的空间。
**实例**
标记长的引用:
``` bash
<blockquote>
Here is a long quotation here is a long quotation here is a long quotation 
here is a long quotation here is a long quotation here is a long quotation 
here is a long quotation here is a long quotation here is a long quotation.
</blockquote>
```
**提示**：请使用 q 元素来标记短的引用。
**注释**：如需把页面作为 strict XHTML 进行验证，那么 &lt;blockquote&gt; 元素必须包含块级元素，比如这样：
``` bash
<blockquote>
<p>here is a long quotation here is a long quotation</p>
</blockquote>
```
| 属性 | 值 | 描述 |
| --- | --- | --- |
| cite | 链接 | 规定引用来源 |


## &lt;del&gt;
定义文档中已被删除的文本(文本上加删除线)
**实例**
``` bash
a dozen is <del>20</del> 12 pieces
```
**注释**：请与 &lt;ins&gt; 标签配合使用，来描述文档中的更新和修正。

| 属性 | 值 | 描述 |
| --- | --- | --- |
| cite | 链接 | 指向另外一个文档的 URL，此文档可解释文本被删除的原因 |
| datetime | YYYYMMDD | 定义文本被删除的日期和时间 |


## &lt;ins&gt;
定义已经被插入文档中的文本(文本上加下划线)
**实例**
带有已删除部分和新插入部分的文本：
``` bash
a dozen is <del>20</del> <ins>12</ins> pieces
```
| 属性 | 值 | 描述 |
| --- | --- | --- |
| cite | 链接 | 指向另外一个文档的 URL，此文档可解释文本被删除的原因 |
| datetime | YYYYMMDD | 定义文本被删除的日期和时间 |


## &lt;mark&gt;
定义带有记号的文本(加黄底)
**实例**
``` bash
<p>Do not forget to buy <mark>milk</mark> today.</p>
```
**注释**:配合style="background-color:xxx"可以改变标注颜色


## &lt;meter&gt;
定义已知范围或分数值内的标量测量。也被称为 gauge（尺度）。
例子：磁盘用量、查询结果的相关性，等等。
**实例**
``` bash
<meter value="3" min="0" max="10">十分之三</meter>
<meter value="0.6">60%</meter> 
```
**注释**:标签不应用于指示进度（在进度条中）。如果标记进度条，请使用 &lt;progress&gt; 标签。


## &lt;progress&gt;
标示任务的进度（进程），是 HTML 5 中的新标签
**实例**
正在进行的下载
``` bash
<progress value="22" max="100"></progress> 
```
| 属性 | 值 | 描述 |
| -- | --- | --- |
| max | number | 规定任务一共需要多少工作 |
| value | number | 规定已经完成多少任务 |

**提示**:请结合&lt;progress&gt;标签与 JavaScript 一同使用，来显示任务的进度。
**注释**:&lt;progress&gt;标签不适合用来表示度量衡（例如，磁盘空间使用情况或查询结果）。如需表示度量衡，请使用 &lt;meter&gt; 标签代替
 

## 上下标
``` bash
<sub></sub>#上标
<sup></sup>#下标
<ruby>你好<rt>nihao</rt><ruby>#类似于拼音
```


## &lt;template&gt;
&lt;template&gt;标记用作容纳页面加载时对用户隐藏的 HTML 内容的容器。
&lt;template&gt;中的内容可以稍后使用 JavaScript 呈现。
如果您有一些需要重复使用的 HTML 代码，则可以使用&lt;template&gt;标记。如果在没有&lt;template&gt;标记的情况下执行此操作，必须使用 JavaScript 创建 HTML 代码，以防止浏览器呈现这些代码。
**实例**
使用&lt;template&gt;保留页面加载时隐藏的内容。使用 JavaScript 来显示
``` bash
<button onclick="showContent()">显示被隐藏的内容</button>

<template>
  <h2>Flower</h2>
  <img src="img_white_flower.jpg" width="214" height="204">
</template>

<script>
function showContent() {
  var temp = document.getElementsByTagName("template")[0];
  var clon = temp.content.cloneNode(true);
  document.body.appendChild(clon);
}
</script>
```
点击前后效果如下
![6-pic1](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/6-pic1.png)
![6-pic2](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/6-pic2.png)

**实例2**
对数组中的每个项，都使用一个新的 div 元素来填充网页。每个 div 元素的 HTML 代码都在 template 元素内：
``` bash
<!DOCTYPE html>
<html>
<body>
<style>
.myClass {
  color: white;
  background-color: DodgerBlue;
  padding: 20px;
  text-align: center;
  margin: 10px;
}
</style>
<h1>template 元素</h1>
<p>本例使用包含数组中每个项目的新 div 元素来填充网页。</p>
<p>每个 div 的 HTML 代码在 template 元素内。</p>
<p>单击下面的按钮，显示 template 元素中的隐藏内容。</p>
<button onclick="showContent()">显示隐藏的内容</button>
<template>
  <div class="myClass">我喜欢：</div>
</template>
<script>
var myArr = ["奥迪", "宝马", "奔驰", "大众", "捷豹", "沃尔沃"];
function showContent() {
  var temp, item, a, i;
  temp = document.getElementsByTagName("template")[0];
  #从template中获取div元素
  item = temp.content.querySelector("div");
  #循环数组中的元素
  for (i = 0; i < myArr.length; i++) {
    #基于template创建节点
    a = document.importNode(item, true);
    #从数组中添加数据
    a.textContent += myArr[i];
    #将新节点附加到任意位置
    document.body.appendChild(a);
  }
}
</script>
</body>
</html>
```
演示前后效果如下
![6-template1](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/6-template1.png)
![6-template2](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/6-template2.png)

**实例3**
检查&lt;template&gt;的浏览器支持：
``` bash
<script>
if (document.createElement("template").content) {
  document.write("Your browser supports template!");
} else {
  document.write("您的浏览器不支持 template！");
}
</script>
```
显示结果如下
![6-template3](https://hexo-4grmu8ecde66adf2-1306730064.tcloudbaseapp.com/pic/6-template3.png)

---
END




