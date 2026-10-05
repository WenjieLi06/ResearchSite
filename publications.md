---
layout: article
title: Publications  
---

[Google Scholar](https://scholar.google.com/citations?user=q2CN_UYAAAAJ&hl=en){:.button.button--primary.button--rounded}



{% assign publication_sections = 'current,before-nankai' | split: ',' %}
{% for section in publication_sections %}

{% if section == 'before-nankai' %}
## Before Nankai
{% endif %}

<ol class="publication-list" reversed>


{% for publications in site.publications reversed %}

{% assign publication_number = publications.path | split: '/' | last | split: '_' | first | plus: 0 %}
{% if section == 'current' and publication_number <= 25 %}
  {% continue %}
{% elsif section == 'before-nankai' and publication_number > 25 %}
  {% continue %}
{% endif %}

{% if publications.level == 'primary' %}

<li value="{{ publication_number }}">
<details>

 <summary>  
 	<span>  
	{{ publications.author }} 
	<b>{{ publications.title }}</b> 
	<i>{{ publications.journal }}</i> 
	<b>{{ publications.year }}</b>  
	(<a style="color:#0272AC;" href="{{ publications.link }}">Link</a>)
</span> 
 </summary>

  {{ publications.content }}

</details>

</li>

{% else %}
<li value="{{ publication_number }}">
<span>  
	{{ publications.author }} 
	<b>{{ publications.title }}</b> 
	<i>{{ publications.journal }}</i>
	<b>{{ publications.year }}</b>  
	(<a style="color:#0272AC;" href="{{ publications.link }}">Link</a>)

</span> 
</li>
{% endif %}

{% endfor %}

</ol>

{% endfor %}
