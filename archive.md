---
layout: page
title: Daftar Isi
permalink: /archive/
---
<section class="archive-post-list">
<h1>{{ page.title }}</h1>
<ul>
{% for post in site.posts %}
    {% capture post_year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% if post_year == page.year %}
            <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>       
    {% endif %}
{% endfor %}
</ul>
</section>
