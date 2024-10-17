---
layout: page
title: 学习博客
description: 分享学习路程，心得体会。
keywords: YaJun Yang, 杨亚军
comments: true
menu: 关于
permalink: /about/
---

我是Magician，分享学习笔记，日常内容。

来自山西农业大学无人机创新团队。


## 联系

<ul>
{% for website in site.data.social %}
<li>{{website.sitename }}：<a href="{{ website.url }}" target="_blank">@{{ website.name }}</a></li>
{% endfor %}
</ul>


## 技能

{% for skill in site.data.skills %}
### {{ skill.name }}
<div class="btn-inline">
{% for keyword in skill.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
