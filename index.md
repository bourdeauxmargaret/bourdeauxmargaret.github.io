---
layout: page
---

<section class="home-hero">
  <h1>Practice to Policy</h1>
  <p>Humanity is facing a formidable set of health security threats—health crises that can rapidly overwhelm health systems, spark widespread death and disability, and destabilize states, regions and societies. These include the rising risks of pandemics, environmental contamination, and climate-change related health conditions; direct targeting of health systems during armed conflicts and cyberwarfare; and unintended consequences from emerging bioengineering and artificial intelligence technologies.</p> 
  <p>Health Security Policy Academy, a policy think-tank in the Division of Global Health Equity at MassGeneral Brigham, aims to advance policy-related knowledge about the most pressing health security challenges of our time. We use a unique “practice to policy” approach: we leverage the knowledge of front line health care providers, bench and field researchers, and public health practitioners to inform policy analysis and formulation to ensure our work is practical, high impact, and grounded in the mission of securing health for all.</p>
</section>

<section class="home-section">
  <h2>Our Projects</h2>
  <div class="home-project-grid">
    {% assign home_projects = site.projects | sort: "title" %}
    {% for project in home_projects limit: 4 %}
      <a class="home-project-card" href="{{ project.url | relative_url }}">
        <h3>{{ project.title }}</h3>
        {% if project.subtitle %}<p>{{ project.subtitle }}</p>{% endif %}
      </a>
    {% endfor %}
  </div>
</section>

<section class="home-section">
  <h2>Featured</h2>
  {% assign featured_post = site.posts | first %}
  {% if featured_post %}
    <div class="home-featured">
      <h3><a href="{{ featured_post.url | relative_url }}">{{ featured_post.title }}</a></h3>
      <p>{{ featured_post.excerpt | strip_html | truncate: 200 }}</p>
    </div>
  {% else %}
    <div class="home-featured">
      <h3>No featured post yet</h3>
      <p>Add a post in the blog to feature here.</p>
    </div>
  {% endif %}
</section>

<section class="home-section">
  <h2>Recent publications</h2>
  {% assign recent_pubs = site.publications | sort: "title" %}
  <ul class="home-secondary-list">
    {% for pub in recent_pubs limit: 3 %}
      <li><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></li>
    {% endfor %}
  </ul>
</section>
