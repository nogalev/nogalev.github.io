---
layout: home
title: Noga Levinson
---

<div class="hero">
  <p class="hero__eyebrow">Electrochemistry · Organic electronics · Functional thin films</p>
  <h1 class="hero__title">I build electrochromic and photo-active devices that respond reliably in the lab. ✨</h1>
  <p class="hero__lede">
    I'm an MSc chemist at the Weizmann Institute translating molecular design into repeatable device behaviour. My recent work
    tunes metal-organic interlayers, light-assisted switching, and graphene-enabled electrodes to push thin-film performance.
  </p>
  <div class="hero__meta">
    <span>🎓 MSc Chemistry · Weizmann Institute of Science</span>
    <span>🧑‍🏫 Advisors: Prof. Milko van der Boom &amp; Dr. Michal Lahav</span>
  </div>
  <div class="hero__actions">
    <a class="button button--primary" href="/cv/">📄 View CV</a>
    <a class="button button--ghost" href="/about/">🔬 About my work</a>
  </div>
</div>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">🎯 Focus areas</h2>
    <p class="section__subtitle">Where chemistry meets device engineering</p>
  </div>
  <div class="tag-grid">
    <span class="tag">Electrochromic thin films</span>
    <span class="tag">Photo-electrochromic hybrids</span>
    <span class="tag">Graphene interfaces</span>
    <span class="tag">Cu(111) single-crystal preparation</span>
    <span class="tag">Spectroscopy-driven analysis</span>
    <span class="tag">Lab IT &amp; automation</span>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">🧪 Current priorities</h2>
    <p class="section__subtitle">Practical questions I’m exploring right now</p>
  </div>
  <div class="highlight-grid">
    <div class="card">
      <h3 class="card__title">Interlayer engineering ⚙️</h3>
      <p class="card__body">
        Mapping how nanoscale metal-organic barriers control ion transport, contrast, and lifetime in electrochromic stacks.
      </p>
    </div>
    <div class="card">
      <h3 class="card__title">Device protocols 📊</h3>
      <p class="card__body">
        Designing test plans, calibration notebooks, and data hygiene loops that keep experiments reproducible.
      </p>
    </div>
    <div class="card">
      <h3 class="card__title">Light-assisted switching ☀️</h3>
      <p class="card__body">
        Combining photovoltaic layers with electrochromic modulation for adaptive, low-power surfaces.
      </p>
    </div>
    <div class="card">
      <h3 class="card__title">Lab infrastructure 🛠️</h3>
      <p class="card__body">
        Supporting 2D Generation with instrument IT, structured data archives, and lightweight Python automations.
      </p>
    </div>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">🧩 Projects</h2>
    <p class="section__subtitle">Selected research and tooling</p>
  </div>
  {% assign featured_projects = site.projects | sort: "date" | reverse %}
  <div class="project-grid">
    {% for project in featured_projects %}
    <a class="card" href="{{ project.url | relative_url }}">
      <h3 class="card__title">{{ project.title }}</h3>
      {% if project.date %}
      <p class="card__meta">{{ project.date | date: "%b %Y" }}</p>
      {% endif %}
      <p class="card__body">{{ project.excerpt | strip_html | truncate: 140 }}</p>
    </a>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">📚 Publications &amp; writing</h2>
    <p class="section__subtitle">Formal outputs and works in progress</p>
  </div>
  {% assign sorted_pubs = site.publications | sort: "year" | reverse %}
  <div class="publication-list">
    {% for pub in sorted_pubs %}
    <div class="publication-item">
      <div class="pub-title">{{ pub.title }}</div>
      <div class="pub-meta">{{ pub.venue }} · {{ pub.year }} · {{ pub.status }}</div>
      {% if pub.links %}
      <p>
        {% for link in pub.links %}
          <a href="{{ link.url }}">{{ link.label }}</a>{% unless forloop.last %} · {% endunless %}
        {% endfor %}
      </p>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">🤝 Let’s collaborate</h2>
  </div>
  <div class="callout">
    <p><strong>Open to conversations</strong> about electrochromic prototyping, spectroscopy analytics, or setting up reliable lab data systems.</p>
    <p>Reach out via LinkedIn or email and I’ll follow up.</p>
  </div>
</section>
