---
title: "Dev Hub"
published: true
---

<h1 class="title">Dev Hub Blog</h1>

{% for post in site.posts limit:5000 %}
<div class="post">

    <p><a href="{{ site.baseurl }}{{ post.url }}" rel="bookmark" title="{{ post.title }}" style="color:#000;"><h4><strong>{{ post.title }}</strong></h4></a>
    <p><i><strong><span class="small">Posted on</span> <span class="post-date">{{ post.date | date:"%m-%d-%Y" }}</span></strong></i></p>
    <p><a href="{{ site.baseurl }}{{ post.url }}" rel="bookmark" title="{{ post.title }}"><img src="{{ post.image }}" width="150" align="right" style="padding: 15px;" /></a></p>
    <p>{{ post.content | strip_html | truncatewords: 100 }}...<a href="{{ site.baseurl }}{{ post.url }}" rel="bookmark" title="{{ post.title }}" style="color:#000; font-weight: bold;">read more</a>.</p>
    <br />
    <hr />

</div>
{% endfor %}
