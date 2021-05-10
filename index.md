---
layout: article
titles:
  # @end locale config
---


### A short story

<img class="image image--xl" src="https://github.com/WenjieLi06/ResearchSite/raw/gh-pages/Images/Picture_Wenjie.jpeg"/>{:.shadow}

Wenjie was born in a beautiful small city (Ganzhou) lying in the southeastern part of China. In 2010, he started his undergraduate study in Fudan University as an independent recruitment student and later joined professor Gengfeng Zheng’s research group. After one year’s research training, he started his independent project on WO3 Nanoflakes for Enhanced Photoelectrochemical Conversion with the support from CURE endowment fellowship.
Wenjie’s research interest is energy harvesting, conversion and storage. He decided to follow his interest and pursuing a better understanding of the science behind practical "energy manipulation" in graduate school. Short after joining Prof. Song Jin's research group in University of Wisconsin-Madison, he found that solar energy could be a good solution to fill the gap between fossil fuel era and nuclear fission era. Due to the intermittent nature of sunlight, the design of practical round-trip solar energy utilization systems requires both efficient solar energy conversion and inexpensive large-scale energy storage. He devoted most of his time in graduate school to the understanding, development and demonstration of a novel type of integrated solar flow battery device and hopefully paved the way for a practical new approach to harvesting, storing and utilizing the intermittent solar energy with high energy conversion efficiency and storage density. 
Having been trained as an electrochemist, Wenjie likes to think about the flow of electrons and ions through materials and interfaces, and ways to control them. He believes electrochemistry is a powerful tool and he is passionate about using it to develop different energy manipulating units to solve problems, satisfy needs and create new applications. 

### Recent News

{% for news in site.news limit:3%}
  <p class="blogdate">{{ news.date | date: "%d %B %Y" }}</p>
  <p>{{ news.content | markdownify }}</p>
{% endfor %}
