---
title: "Vera-Licona Lab - Software"
layout: gridlay
excerpt: "Vera-Licona Lab -- Software."
sitemap: false
permalink: /software/
---


# Software

{% assign number_printed = 0 %}
{% for software in site.data.softlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if software.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ software.title }}</pubtit>
  <img src="/images/softpic/{{ software.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ software.description }}</p>
  <p>{{ software.authors }}</p>
  <p><a href="{{ software.link.url }}">{{ software.link.display }}</a></p>
  <p class="well"> {{ software.news1 }}</p>
  <p class="well"> {{ software.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

