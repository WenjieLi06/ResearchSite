---
layout: page
title: Current Members
---

<div class="members-grid">
  {% for member in site.currentMember %}
    <article class="member-card">
      {% if member.cover %}
        <a href="{{ member.url | relative_url }}" class="member-card__image-link">
          <img src="{{ member.cover | relative_url }}" alt="{{ member.title }}" class="member-card__image">
        </a>
      {% endif %}
      <div class="member-card__meta">
        <h3 class="member-card__title">{{ member.title }}</h3>
        {% if member.position %}
          <p class="member-card__position">{{ member.position }}</p>
          <p class="member-card__email"> <a style="color:#0272AC; font-weight: normal;" href="mailto: {{member.email}}">{{member.email}}</a></p>
        {% endif %}
      </div>
    </article>
  {% endfor %}
</div>

<style>
  .members-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1.5rem;
  }

  .member-card {
    margin: 0;
    text-align: center;
  }

  .member-card__image {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 8px;
    display: block;
  }

  .member-card__meta {
    margin-top: 0.75rem;
  }

  .member-card__title {
    margin: 0;
    font-size: 1.1rem;
  }

  .member-card__position {
    margin: 0.35rem 0 0;
    color: #5a5a5a;
    font-size: 0.95rem;
  }
  .member-card__email {
    margin: 0.35rem 0 0;
    color: #5a5a5a;
    font-size: 0.95rem;
  }
</style>
