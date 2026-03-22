---
layout: articles
title: Current Members
---

{% assign principal_members = site.currentMember | where_exp: 'member', "member.position contains 'Principal'" %}
{% assign graduate_members = site.currentMember | where_exp: 'member', "member.position contains 'Graduate' or member.position contains 'Postdoctoral'" %}
{% assign undergraduate_members = site.currentMember | where_exp: 'member', "member.position contains 'Undergraduate'" %}

### Principal Investigator

<div class="grid grid--p-3">
  {% for member in principal_members %}
  <div class="cell cell--12 cell--sm-6 cell--lg-4">
    <div class="item">
      <div class="item__image">
        <a href="{{ member.url }}">
          <img class="image image--lg" src="{{ member.cover }}" alt="{{ member.title }}">
        </a>
      </div>
      <div class="item__content">
        <div class="item__header">
          <h4><a href="{{ member.url }}">{{ member.title }}</a></h4>
        </div>
        <div class="item__description">
          <p style="font-size: 1.05em; margin-top: 0.25rem;">{{ member.position }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

### Graduate Students

<div class="grid grid--p-3">
  {% for member in graduate_members %}
  <div class="cell cell--12 cell--sm-6 cell--lg-4">
    <div class="item">
      <div class="item__image">
        <a href="{{ member.url }}">
          <img class="image image--lg" src="{{ member.cover }}" alt="{{ member.title }}">
        </a>
      </div>
      <div class="item__content">
        <div class="item__header">
          <h4><a href="{{ member.url }}">{{ member.title }}</a></h4>
        </div>
        <div class="item__description">
          <p style="font-size: 1.05em; margin-top: 0.25rem;">{{ member.position }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

### Undergraduate Students

<div class="grid grid--p-3">
  {% for member in undergraduate_members %}
  <div class="cell cell--12 cell--sm-6 cell--lg-4">
    <div class="item">
      <div class="item__image">
        <a href="{{ member.url }}">
          <img class="image image--lg" src="{{ member.cover }}" alt="{{ member.title }}">
        </a>
      </div>
      <div class="item__content">
        <div class="item__header">
          <h4><a href="{{ member.url }}">{{ member.title }}</a></h4>
        </div>
        <div class="item__description">
          <p style="font-size: 1.05em; margin-top: 0.25rem;">{{ member.position }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>