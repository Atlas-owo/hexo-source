---
title: NexT内建标签：突破容器宽度限制的图片
date: 2017-08-24 23:28:13
tags: 
	- hexo
	- NexT
	- LearningPath
categories: Programming
---

一般情况下，在markdown中调用HTML显示图片效果如下

{% codeblock lang:html %}
<img src="https://cdn.reimu.net/uploads/2017/08/tumblr_o7u1w4bsDX1vthenho1_500.jpg">
{% endcodeblock %}

<img src="https://cdn.reimu.net/uploads/2017/08/tumblr_o7u1w4bsDX1vthenho1_500.jpg">

在img中加入 `class = "full-image"` 

{% codeblock lang:html %}
<img class=full-image src="https://cdn.reimu.net/uploads/2017/08/tumblr_o7u1w4bsDX1vthenho1_500.jpg">
{% endcodeblock %}

<img class=full-image src="https://cdn.reimu.net/uploads/2017/08/tumblr_o7u1w4bsDX1vthenho1_500.jpg">

图片突破了容器限制，显得更加突出。