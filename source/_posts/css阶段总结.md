---
title: CSS阶段总结
date: 2017-09-01 18:18:56
tags:
	- hexo
	- CSS
	- LearningPath
categories: Programmming
---

<p class = "note warning">这些东西太容易遗忘了。整理记录一下。
~~**大部分摘自w3school。**~~</p>

# 基础语法

{% codeblock lang:css %}selector {declaration1; declaration2; ... declarationN }{%  endcodeblock %}

{% codeblock lang:css %}selector {property: value}{% endcodeblock %}

<p class = "note danger">注意：空格和大小写没有影响。</p>

---

{% codeblock lang:css %}h1,h2,h3,h4,h5,h6 {
  color: green;
  }{% endcodeblock %}
> 多分组
 
{% codeblock lang:css %}body {
    font-family: Verdana, sans-serif;
    }{% endcodeblock %}
> 继承：body元素中的子元素诸如`p, td, ul, ol, ul, li, dl, dt, dd`都将继承该属性

---
## 派生选择器
>派生选择器允许你根据文档的上下文关系来确定某个标签的样式。

{% codeblock lang:css %}strong {
     color: red;
    }

h2 {
     color: red;
    }

h2 strong {
     color: blue;
    }{% endcodeblock %}

{% codeblock lang:html %}<p>The strongly emphasized word in this paragraph is<strong>red</strong>.</p>
<h2>This subhead is also red.</h2>
<h2>The strongly emphasized word in this subhead is<strong>blue</strong>.</h2>{% endcodeblock %}

---
## id选择器

> id选择器用<code class = code>#</code>定义。

{% codeblock lang:css %}#red {color:red;}
#green {color:green;}{% endcodeblock %}

{% codeblock lang:html %}<p id="red">这个段落是红色。</p>
<p id="green">这个段落是绿色。</p>{% endcodeblock %}

<p class = "note danger">id 属性只能在每个 HTML 文档中出现一次。</p>

---
## 类选择器
> 在 CSS 中，类选择器以一个点号显示：

{% codeblock lang:css %}.center {text-align: center}{% endcodeblock %}
{% codeblock lang:html %}<h1 class="center">
This heading will be center-aligned
</h1>

<p class="center">
This paragraph will also be center-aligned.
</p>{% endcodeblock %}

<p class = "note danger">类名的第一个字符不能使用数字。</p>

---

## 属性选择器
> 对带有指定属性的 HTML 元素设置样式。
可以为拥有指定属性的 HTML 元素设置样式，而不仅限于 class 和 id 属性。

{% codeblock lang:css %}[title]
{
color:red;
}{% endcodeblock %}

---

# CSS框模型

<img src="http://www.w3school.com.cn/i/ct_boxmodel.gif"></img>