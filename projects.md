---
title: "Projects"
permalink: /projects/
layout: single
---

<div class="projects-grid">
  {% for post in site.posts %}
    <div class="project-card">
      <div class="project-card-content">
        <h3 class="project-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h3>
        {% if post.excerpt %}
          <p class="project-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 120 }}</p>
        {% endif %}
        <div class="project-meta">
          {% if post.categories %}
            <span class="project-category">{{ post.categories | first }}</span>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.project-card {
  background: #fff;
  border: 1px solid #e8e8e8;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.project-card-content {
  padding: 1.25rem;
}

.project-title {
  margin: 0 0 0.75rem 0;
  font-size: 1.2rem;
}

.project-title a {
  color: #2c3e50;
  text-decoration: none;
}

.project-title a:hover {
  color: #3498db;
}

.project-excerpt {
  color: #555;
  font-size: 0.9rem;
  line-height: 1.5;
  margin: 0 0 1rem 0;
}

.project-category {
  display: inline-block;
  background: #f0f0f0;
  padding: 0.2rem 0.6rem;
  border-radius: 20px;
  font-size: 0.7rem;
  color: #666;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
}
</style>
