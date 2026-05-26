---
layout: single
title: "Online Resources"
permalink: /resources/
author_profile: true
---

<style>
  /* Premium Resource Page Styling */
  .filter-nav {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin: 1.5rem 0 2.5rem 0;
    border-bottom: 1px solid rgba(0, 0, 0, 0.08);
    padding-bottom: 1.25rem;
  }

  .filter-btn {
    background: transparent;
    border: 1px solid rgba(0, 0, 0, 0.12);
    color: inherit;
    padding: 0.5rem 1.25rem;
    border-radius: 25px;
    font-size: 0.9rem;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.25s cubic-bezier(0.2, 0.8, 0.2, 1);
    outline: none;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }

  .filter-btn:hover {
    background: rgba(0, 0, 0, 0.04);
    transform: translateY(-1px);
    border-color: rgba(0, 0, 0, 0.24);
  }

  .filter-btn.active {
    background: #333333;
    color: #ffffff;
    border-color: #333333;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
  }

  .resources-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
    gap: 1.75rem;
    margin-top: 1rem;
  }

  .resource-card-container {
    transition: opacity 0.25s cubic-bezier(0.4, 0, 0.2, 1), 
                transform 0.25s cubic-bezier(0.4, 0, 0.2, 1);
    will-change: opacity, transform;
  }

  .resource-card {
    background: rgba(255, 255, 255, 0.9);
    border: 1px solid rgba(0, 0, 0, 0.07);
    border-radius: 14px;
    padding: 1.5rem;
    height: 100%;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.02);
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    display: flex;
    flex-direction: column;
    position: relative;
    overflow: hidden;
  }

  /* Dynamic color bar on top */
  .resource-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
    background: var(--category-color, #0984e3);
    transition: height 0.25s ease;
  }

  .resource-card:hover::before {
    height: 6px;
  }

  .resource-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.08);
    border-color: var(--category-color, rgba(0, 0, 0, 0.15));
  }

  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 0.75rem;
  }

  .category-pill {
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    padding: 0.25rem 0.65rem;
    border-radius: 20px;
    background: var(--category-color-light, rgba(9, 132, 227, 0.15));
    color: var(--category-color, #0984e3);
  }

  .resource-title {
    font-size: 1.15rem !important;
    margin: 0 0 0.75rem 0 !important;
    font-weight: 700;
    line-height: 1.35;
  }

  .resource-link {
    color: inherit !important;
    text-decoration: none !important;
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    transition: color 0.2s ease;
  }

  .resource-link:hover {
    color: var(--category-color, #0984e3) !important;
  }

  .resource-link i {
    font-size: 0.85rem;
    opacity: 0.6;
    transition: transform 0.2s ease, opacity 0.2s ease;
  }

  .resource-link:hover i {
    transform: translate(2px, -2px);
    opacity: 1;
  }

  .resource-description {
    font-size: 0.9rem;
    line-height: 1.6;
    color: #555555;
    margin-bottom: 1.5rem;
    flex-grow: 1;
  }

  .card-footer {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-top: auto;
    border-top: 1px solid rgba(0, 0, 0, 0.04);
    padding-top: 0.75rem;
  }

  .tag-pill {
    font-size: 0.7rem;
    background: #f1f2f6;
    color: #57606f;
    padding: 0.15rem 0.5rem;
    border-radius: 6px;
    font-weight: 500;
    transition: background 0.2s ease;
  }

  .resource-card:hover .tag-pill {
    background: #e4e7eb;
  }

  /* Dark mode support */
  @media (prefers-color-scheme: dark) {
    .filter-nav {
      border-bottom-color: rgba(255, 255, 255, 0.08);
    }
    
    .filter-btn {
      border-color: rgba(255, 255, 255, 0.15);
    }
    
    .filter-btn:hover {
      background: rgba(255, 255, 255, 0.06);
      border-color: rgba(255, 255, 255, 0.3);
    }
    
    .filter-btn.active {
      background: #ffffff;
      color: #1c1c1e;
      border-color: #ffffff;
    }
    
    .resource-card {
      background: rgba(30, 30, 35, 0.85);
      border-color: rgba(255, 255, 255, 0.06);
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
    }
    
    .resource-card:hover {
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.5);
    }
    
    .resource-description {
      color: #a4a4aa;
    }
    
    .tag-pill {
      background: rgba(255, 255, 255, 0.06);
      color: #98989f;
    }
    
    .resource-card:hover .tag-pill {
      background: rgba(255, 255, 255, 0.1);
    }
  }
</style>

I maintain this collection of outstanding online resources, research portals, libraries, and interactive materials that I find useful or inspiring. Use the buttons below to filter resources by category.

<!-- Filter Buttons -->
<div class="filter-nav">
  <button class="filter-btn active" data-filter="all">
    <i class="fas fa-th-large"></i> All Resources
  </button>
  <button class="filter-btn" data-filter="physics">
    <i class="fas fa-atom"></i> Physics
  </button>
  <button class="filter-btn" data-filter="mathematics">
    <i class="fas fa-square-root-alt"></i> Mathematics
  </button>
  <button class="filter-btn" data-filter="tools">
    <i class="fas fa-tools"></i> Academic Tools
  </button>
</div>

<!-- Resources Grid -->
<div class="resources-grid">
  {% for resource in site.data.resources %}
    {% assign cat = resource.category | downcase %}
    
    {% if cat == 'physics' %}
      {% assign color = '#00b894' %}
      {% assign light_color = 'rgba(0, 184, 148, 0.12)' %}
    {% elsif cat == 'mathematics' %}
      {% assign color = '#6c5ce7' %}
      {% assign light_color = 'rgba(108, 92, 231, 0.12)' %}
    {% elsif cat == 'tools' %}
      {% assign color = '#e17055' %}
      {% assign light_color = 'rgba(225, 112, 85, 0.12)' %}
    {% else %}
      {% assign color = '#0984e3' %}
      {% assign light_color = 'rgba(9, 132, 227, 0.12)' %}
    {% endif %}

    <div class="resource-card-container" data-category="{{ cat }}" style="--category-color: {{ color }}; --category-color-light: {{ light_color }};">
      <article class="resource-card">
        <div class="card-header">
          <span class="category-pill">{{ resource.category }}</span>
        </div>
        
        <h3 class="resource-title">
          <a class="resource-link" href="{{ resource.url }}" target="_blank" rel="noopener noreferrer">
            {{ resource.title }} <i class="fas fa-external-link-alt"></i>
          </a>
        </h3>
        
        <p class="resource-description">
          {{ resource.description }}
        </p>
        
        {% if resource.tags %}
          <div class="card-footer">
            {% for tag in resource.tags %}
              <span class="tag-pill">#{{ tag | downcase }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </article>
    </div>
  {% endfor %}
</div>

<!-- Light and Smooth Filter Logic -->
<script>
  document.addEventListener('DOMContentLoaded', function() {
    const filterButtons = document.querySelectorAll('.filter-btn');
    const cards = document.querySelectorAll('.resource-card-container');

    filterButtons.forEach(button => {
      button.addEventListener('click', () => {
        // Toggle active button style
        filterButtons.forEach(btn => btn.classList.remove('active'));
        button.classList.add('active');

        const filterValue = button.getAttribute('data-filter');

        cards.forEach(card => {
          const cardCat = card.getAttribute('data-category');
          
          if (filterValue === 'all' || cardCat === filterValue) {
            // Unhide & animate back in
            card.style.display = 'block';
            // Slight timeout to let layout register, enabling smooth scale/fade transitions
            setTimeout(() => {
              card.style.opacity = '1';
              card.style.transform = 'scale(1)';
            }, 20);
          } else {
            // Animate out & hide
            card.style.opacity = '0';
            card.style.transform = 'scale(0.95)';
            setTimeout(() => {
              card.style.display = 'none';
            }, 200);
          }
        });
      });
    });
  });
</script>
