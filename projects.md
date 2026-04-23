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
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1.75rem;
  margin: 2rem 0;
}

.project-card {
  background: #fff;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.12);
}

.project-card-content {
  padding: 1.5rem;
}

.project-title {
  margin: 0 0 0.75rem 0;
  font-size: 1.25rem;
  font-weight: 600;
  line-height: 1.4;
}

.project-title a {
  color: #2c3e50;
  text-decoration: none;
  transition: color 0.2s ease;
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

.project-meta {
  margin-top: 0.75rem;
}

.project-category {
  display: inline-block;
  background: #f0f0f0;
  padding: 0.2rem 0.6rem;
  border-radius: 20px;
  font-size: 0.7rem;
  font-weight: 500;
  color: #666;
  letter-spacing: 0.3px;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 1.25rem;
  }
  
  .project-card-content {
    padding: 1.25rem;
  }
}
</style>
