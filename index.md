---
layout: article
titles:
  # @end locale config
---

<div class="item">
  <div class="item__image">
    <img class="image image--lg" src="/images/Picture_Wenjie.jpg">  
  </div>
  <div class="item__content">
    <div class="item__header">
      <h3>Wenjie Li</h3>
    </div>
    <div class="item__description">
      <p>Postdoctoral Associate <br>
         Department of Chemistry&Chemical Biology <br>
         Cornell University
      </p>
    </div>
  </div>
</div>


___

### Pictures

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

___

### Recent News
{% for news in site.news limit:3%}
  <h4 class="blogdate">{{ news.date | date: "%d %B %Y" }}</h4>
  <p>{{ news.content | markdownify }}</p>
{% endfor %}

