---
title: Romain Caneill
description: Doctor in Physical Oceanography
permalink: /
layout: default
---

<img alt="Picture of Romain Caneill" src="/assets/images/romain.jpg" width="40%" style="float: right; margin: 0 0 0 15px;">

# About Me

I am a doctor in physical oceanography, and I am now working as a postdoc
within the [SASIP project](https://sasip-climate.github.io/)
project in Grenoble, France.

I pursued my Ph.D. studies at the Department of Marine Sciences,
University of Gothenburg, Sweden, supervised by Fabien Roquet.
My doctoral research investigated the factors influencing the
upper ocean stratification, particularly near the polar transition zones
between the alpha and beta oceans.
Throughout my academic journey, I have actively contributed to teaching
physical oceanography courses at the University of Gothenburg.
I believe that science should be open and reproducible,
and I am a full advocate of FOSS.
Therefore, I have been an exercise leader at one CodeRefinery workshop,
and I participate in open-source initiatives,
contributing to Python packages like xnemogcm, xgcm, and gsw-xarray.
Beyond academia, I have a professional diploma in carpentry,
I play the guitar, and I love mountains.


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
