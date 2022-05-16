---
title: "News"
layout: textlay
excerpt: "Vera-Licona Lab at the Center for Cell Analysis and Modeling at UConn Health."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline | markdownify}}</em></p>
{% endfor %}
