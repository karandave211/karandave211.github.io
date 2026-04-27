---
title: "Projects"
permalink: /projects/
layout: single
---

<div class="filter-buttons">
  <button class="filter-btn active" data-filter="all">All</button>
  <button class="filter-btn" data-filter="SEO">SEO</button>
  <button class="filter-btn" data-filter="Market Research">Market Research</button>
  <button class="filter-btn" data-filter="Digital Strategy">Digital Strategy</button>
  <button class="filter-btn" data-filter="Technical SEO">Technical SEO</button>
</div>

<div class="projects-grid" id="projectsGrid">
  {% for post in site.posts %}
    {% assign post_categories = post.categories | join: ',' | downcase %}
    <div class="project-card" data-categories="{{ post.categories | join: ',' | downcase }}">
      <div class="project-card-content">
        <h3 class="project-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h3>
        {% if post.excerpt %}
          <p class="project-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 120 }}</p>
        {% endif %}
        <div class="project-meta">
          {% for category in post.categories limit:1 %}
            <span class="project-category">{{ category }}</span>
          {% endfor %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<style>
.filter-buttons {
  text-align: center;
  margin: 1rem 0 2rem;
}
.filter-btn {
  background: #f0f0f0;
  border: none;
  padding: 8px 20px;
  margin: 5px;
  border-radius: 30px;
  cursor: pointer;
  font-size: 0.9rem;
  transition: all 0.2s ease;
}
.filter-btn.active {
  background: #3498db;
  color: white;
}
.filter-btn:hover {
  background: #ddd;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1rem;
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
  margin: 0 0 0.75rem;
  font-size: 1.2rem;
}
.project-title a {
  color: #2c3e50;
  text-decoration: none;
}
.project-excerpt {
  color: #555;
  font-size: 0.9rem;
  margin-bottom: 1rem;
}
.project-category {
  background: #f0f0f0;
  padding: 0.2rem 0.6rem;
  border-radius: 20px;
  font-size: 0.7rem;
  color: #666;
}
@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
  console.log("Filter script loaded");
</style>

<script>
(function() {
  var buttons = document.querySelectorAll('.filter-btn');
  var cards = document.querySelectorAll('.project-card');

  if (!buttons.length || !cards.length) {
    console.log("Filter elements not found");
    return;
  }

  function filterCards(category) {
    category = category.toLowerCase();
    cards.forEach(function(card) {
      var cardCategories = card.getAttribute('data-categories') || '';
      if (category === 'all' || cardCategories.indexOf(category) !== -1) {
        card.style.display = 'block';
      } else {
        card.style.display = 'none';
      }
    });
  }

  buttons.forEach(function(btn) {
    btn.addEventListener('click', function(e) {
      var filterValue = this.getAttribute('data-filter');
      buttons.forEach(function(b) { b.classList.remove('active'); });
      this.classList.add('active');
      filterCards(filterValue);
    });
  });

  // Ensure "All" is active and showing everything on page load
  var activeBtn = document.querySelector('.filter-btn.active');
  if (!activeBtn) {
    var allBtn = document.querySelector('.filter-btn[data-filter="all"]');
    if (allBtn) allBtn.classList.add('active');
  }
  filterCards('all');
})();
</script>
