---
title: Romain Caneill
description: Doctor in Physical Oceanography
permalink: /
layout: default
---

<img alt="Picture of Romain Caneill" src="/assets/images/romain.jpg" width="40%" style="float: right; margin: 0 0 0 15px;">

# About Me

I am a doctor in physical oceanography, now working as a postdoc within the [SASIP project](https://sasip-climate.github.io/), in Grenoble, France.

<article style="width:50%;">
Last blog post: 
{% for post in site.posts limit:1 %}
    {{ post.title }}
    <div class="meta">{{ post.date | date_to_string }}</div>
    <div class="meta"><i>{{ post.description_long }}</i></div>
    <a href="{{ post.url }}">Read more...</a>
{% endfor %}
</article>

# Publications

{% include publications.html %}

## Miscellaneous

* PhD Thesis.
<br>From alpha to beta ocean: Exploring the role of surface buoyancy fluxes and seawater thermal expansion in setting the upper ocean stratification
<br>[Available in my website](phd_thesis)
