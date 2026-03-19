---
layout: article
titles:
show_title: false
---

## Welcome to the Li Lab

 <p style="font-size: 1.2em">We study electrochemical energy conversion across scales, from single-electron events to the collective behavior of Avogadro-scale systems, aiming to uncover fundamental mechanisms and unlock new electrochemical applications. </p>



## Pictures

<style>
  .swiper-demo {
    height: 500px;
  }
  .swiper-demo .swiper__slide {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3rem;
    color: #fff;
  }
  .swiper-demo--image .swiper__slide:nth-child(n) {
    background-color: #000000;
  }
</style>


<div class="swiper my-3 swiper-demo swiper-demo--image swiper-1">
  <div class="swiper__wrapper">
    <div class="swiper__slide"><img class="lightbox-ignore" src="/images/swiper/01.png"/></div>
    <div class="swiper__slide"><img class="lightbox-ignore" src="/images/swiper/02.png"/></div>
    <div class="swiper__slide"><img class="lightbox-ignore" src="/images/swiper/03.png"/></div>
    <div class="swiper__slide"><img class="lightbox-ignore" src="/images/swiper/04.png"/></div>
  </div>
  <div class="swiper__button swiper__button--prev fas fa-chevron-left"></div>
  <div class="swiper__button swiper__button--next fas fa-chevron-right"></div>
</div>

<script>
  {%- include scripts/lib/swiper.js -%}
  var SOURCES = window.TEXT_VARIABLES.sources;
  window.Lazyload.js(SOURCES.jquery, function() {
    $('.swiper-1').swiper();
  });
</script>



## Recent News
{% for news in site.news reversed limit:3% }
  <h4 class="blogdate">{{ news.date | date: "%d %B %Y" }}</h4>
  <p>{{ news.content | markdownify }}</p>
{% endfor %}

