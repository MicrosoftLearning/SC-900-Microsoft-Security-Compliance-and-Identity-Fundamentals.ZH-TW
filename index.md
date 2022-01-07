---
title: 線上託管說明
permalink: index.html
layout: home
---

# 內容目錄

下面列出了每個實驗練習和演示的超連結。

## 實驗室

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| 模組 | 實驗室 |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## 示範

{% assign demos = site.pages | where_exp:"page", "page.url contains '/Instructions/Demos'" %}
| 模組 | 示範 |
| --- | --- | 
{% for activity in demos  %}| {{ activity.demo.module }} | [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
