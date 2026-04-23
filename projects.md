---
title: "Projects"
permalink: /projects/
layout: single
---

<div class="grid__wrapper">
  {% for post in site.posts %}
    <div class="grid__item">
      <article class="archive__item">
        <h2 class="archive__item-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h2>
        {% if post.excerpt %}
          <p class="archive__item-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 160 }}</p>
        {% endif %}
      </article>
    </div>
  {% endfor %}
</div>

<style>
.grid__wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  margin-top: 20px;
}
.grid__item {
  border: 1px solid #e8e8e8;
  padding: 15px;
  border-radius: 5px;
  background-color: #fff;
}
.archive__item-title {
  margin-top: 0;
  font-size: 1.2rem;
}
.archive__item-excerpt {
  font-size: 0.9rem;
  color: #555;
}
@media (max-width: 800px) {
  .grid__wrapper {
    grid-template-columns: 1fr;
  }
}
</style>
