---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
  h2{
    margin-bottom: 0px;
  }
  a:link{
    text-decoration: none;
    color: black
  }
</style>

A neat overview over my research can be found [here](/files/Research_Overview.pdf)

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<div>
<h2> Published </h2>
{% for post in site.publications reversed %}
    {% if post.is_preprint == false %}
  {% include archive-single.html %}
  {% endif %}
{% endfor %}
</div>

<div>
<h2> Preprint </h2>
{% for post in site.publications reversed %}
  {% if post.is_preprint %}
  {% include archive-single.html %}
  {% endif %}
{% endfor %}
</div>