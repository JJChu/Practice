﻿# html js点击按钮滚动跳转定位到页面指定位置（DIV）的方法代码

标签（空格分隔）： html 奇技淫巧

---

>　　对于网页编程开发人员来说，在网站页面开发的过程中，有时候我们需要实现当点击一个按钮或者超链接时，立刻滚动跳转定位到本页面中指定的位置。对于大多数的编程老手来说，这些都不是什么难事，但对于一些新手或者没有深入学习编程开发的人来说，可能不知道如何去实现，在这里就和大家分享一下html js点击按钮滚动跳转定位到页面指定位置（DIV）的方法代码。

　　这里主要分为两种情况，分别是点击锚点实现跳转和点击button按钮实现跳转页面，下面就分别探讨一下两种方式的具体实现代码。
　　
###一：通过html锚点实现滚动定位到页面指定位置（DIV）：
>如果我们要点击实现跳转的地方是一个html锚点，也就是点击一个A标签超链接实现跳转，可以把A标签的href属性直接指向跳转指定位置的div，代码实现思路如下：
```
<a href="#abc">点击跳转</a>

<div id="abc">将要跳转到这里</div>
```
点击上面A链接将会滚动跳转到同一页面中id="abc"的那个div处，需要注意的是跳转指定位置div的id是唯一的，A标签直接指向此id，id前面别忘了加上#号。

###二：通过点击button按钮使用js实现滚定跳转到页面指定位置（DIV）：
>如果我们要点击实现跳转的地方是一个button按钮的话，由于button不能添加href，所以我们只好使用js跳转代码来实现，具体代码示例如下：
```
<script>
    function onTopClick() {
         window.location.hash = "#abc";
   }
</script>
<input  type="button" name="Submit" value="提交" onclick="javascript:onTopClick();" />

<div id="abc">跳转到的位置</div>
```
　　上面这段代码，点击提交按钮，将会滚定跳转定位到同一页面id="abc"的div处。这段js点击跳转页面代码实现的原理是：页面各元素赋予唯一ID，点击提交按钮触发js点击事件，js通过ID滚动跳转定位到该元素，window.location.hash = "#abc"指的就是定位到当前页面id="abc"的div。


