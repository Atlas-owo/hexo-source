---
title: 在NexT中使用自定义css样式
date: 2017-08-26 13:51:57
tags:
	- hexo
	- LearningPath
	- CSS
	- NexT
---
<div class="note info"><p class = big>Big!</p>surprise.</div>


在NexT中自带有`bootstrap callout`，但是在更多的情况下，自定义的css样式是不可或缺的。

NexT的css样式储存在`hexo\themes\next\source\css`中。
通过在此目录中的main.styl来插入自定义css样式
{% codeblock %}// CSS Style Guide: http://codeguide.co/#css

$scheme    = hexo-config('scheme') ? hexo-config('scheme') : 'Muse';
$variables = base $scheme custom;
$mixins    = base $scheme custom;

// Variables Layer
// --------------------------------------------------
for $variable in $variables
  @import "_variables/" + $variable

// Mixins Layer
// --------------------------------------------------
for $mixin in $mixins
  @import "_mixins/" + $mixin;

// Common Layer
// --------------------------------------------------

// Scaffolding
@import "_common/scaffolding";

// Layout
@import "_common/outline";

// Components
@import "_common/components";

// Schemes Layer
// --------------------------------------------------
@import "_schemes/" + $scheme;

// Custom Layer
// --------------------------------------------------
@import "_custom/custom";
{% endcodeblock %}
可以看到再最后已经有了`Cusotom Layer`的选项。但是稳妥一点的方法是再添加一个。

在最后一行插入
{% codeblock %}//My Layer
// --------------------------------------------------
@import "_my/mycss";{% endcodeblock %}

然后在新建目录`./my`，在其中创建`mycss.styl`。
在`mycss.styl`中写入自定义css样式即可。
例如：
{% codeblock lang:css %}.big{
font-size:35px;
}

.code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 4px;
}{% endcodeblock %}
其中big类是一个简单的加大，code类是从bootstrap里扒过来的代码样式。文首便是big类的效果。

{% codeblock lang:html %}
<code class = code>&lt;Put your code here&gt;</code>{% endcodeblock %}

<code class = code>&lt;Put your code here&gt;</code>便是code类的效果，可以看到与bootstrap效果相同。