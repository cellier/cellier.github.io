---
layout: page
permalink: /archive/
---


{% assign post_year1 = "" %}

{% for post in site.posts %}{% capture post_year2 %}{{ post.date | date: '%Y' }}{% endcapture %}{% if post_year1 != post_year2 %}{% assign post_year1 = post_year2 %}

#### {{ post_year1 }}



{% endif %}
   
<a href="{{ post.url }}" target="_self"> 

{{ post.title }}<span class="pull-right">{{ post.date | date:'%m月%d日' }}</span>

</a>

{% endfor %}


<!-- 
{% for post in site.posts %}
{% unless post.next %}
<h1 class="page-data-year">{{ post.date | date: '%Y' }}</h1>
{% else %}
{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
{% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
{% if year != nyear %}
<h1 class="page-data-year">{{ post.date | date: '%Y' }}</h1>
{% endif %}
{% endunless %}

<a href="{{ post.url }}" target="_self"> {{ post.title }}  <span class="pull-right">{{ post.date | date:'%m月%d日' }}</span>

{% endfor %}
-->