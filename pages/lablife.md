---
layout: lablife
title: LAB LIFE
subtitle:
permalink: /lablife/
feature-img: "assets/img/header/lablife.jpg"
gallery_path: "assets/img/pexels"
excluded: true
position: 5
tags:
---
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-N20PHKXPCL"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-N20PHKXPCL');
</script>

This is a photo gallery made from the static files in the `assets/img/pexels` folder. 
I wanted to automatically create a simple gallery from a folder without having to create a markdown page as you would for the portfolio.


{% include gallery.html gallery_path=page.gallery_path %}
