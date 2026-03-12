---
layout: article
title: what's up
---

{% for news in site.news %}

  <h4 class="blogdate"> {{ news.date | date: "%d %B %Y" }} </h4>

  <p>{{ news.content }}</p>

{% endfor %}