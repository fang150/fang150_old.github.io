---
layout: posts
permalink: /archive/
title: "Posts"
author_profile: true
header:
  image: "/images/winter_cover.jpg"
---


{% comment %}
=======================
The purpose of this snippet is to list all the tags you have in your site.
=======================
{% endcomment %}
{% for tag in tags %}
	<a href="#{{ tag | slugify }}"> {{ tag }} </a>
{% endfor %}
