---
layout: page
title: NEWS
permalink: /news/
position: 4
feature-img: "assets/img/header/news.png"
hide: false
---
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-N20PHKXPCL"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-N20PHKXPCL');
</script>

<div class="news-timeline"> 
{% assign current_year = "" %} 
{% for post in site.posts %} 
{% assign post_year = post.date | date: "%Y" %} 
{% if post_year != current_year %} 
{% assign current_year = post_year %} 
<h2 class="timeline-year"> {{ current_year }} </h2> 
{% endif %} 
<div class="timeline-item"> 
<div class="timeline-date"> {{ post.date | date: "%d %b" }} </div> <div class="timeline-content"> 
{% if post.thumbnail %} <div class="timeline-thumb"> <a href="{{ post.url | relative_url }}"> <img src="{{ post.thumbnail | relative_url }}" alt="{{ post.title }}"> </a> </div> 
{% endif %} <div class="timeline-text"> <h3> <a href="{{ post.url | relative_url }}"> {{ post.title }} </a> </h3> 
<p> {{ post.excerpt | strip_html | truncate: 180 }} </p> 
<a href="{{ post.url | relative_url }}"> Read More → </a> </div> </div> </div> {% endfor %} </div>