---
title: 在NexT中实现Bootstrap Callout
date: 2017-08-22 23:52:59
tags:
	- LearningPath
	- hexo
	- NexT
categories: Programming
---

NexT supported <strong>bootstrap callout</strong>.


{% codeblock lang:html %}{% note class_name %}Context (markdown supported){% endnote %}{% endcodeblock %}

{% note %} Context with undefined class {% endnote %}

{% note default %} Context with default class {% endnote %}

{% note primary %} Context with primary class {% endnote %}

{% note success %} Context with success class {% endnote %}

{% note info %} Context with info class {% endnote %}

{% note warning %} Context with warning class {% endnote %}

{% note danger %} Context with danger class {% endnote %}


{% codeblock lang:html %}
{% note %} Context with undefined class {% endnote %}

{% note default %} Context with default class {% endnote %}

{% note primary %} Context with primary class {% endnote %}

{% note success %} Context with success class {% endnote %}

{% note info %} Context with info class {% endnote %}

{% note warning %} Context with warning class {% endnote %}

{% note danger %} Context with danger class {% endnote %} 
{% endcodeblock %}



