---
layout: article
title: Publication  
---

[Google Scholar](https://scholar.google.com/citations?user=q2CN_UYAAAAJ&hl=en){:.button.button--primary.button--rounded}



<ol reversed>


{% for publications in site.publications reversed %}

<li>

<details>

 <summary>  
 	<span>  

	{{ publications.author }} 
	<b>{{ publications.title }}</b> 
	<i>{{ publications.journal }}</i> 
	<b>{{ publications.year }}</b>  

</span> 
 </summary>

  {{ publications.content }}

</details>

</li>


{% endfor %}

</ol>
