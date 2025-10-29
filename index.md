---
layout: home
title: Noga Levinson
---

<div class="hero">
  <p class="hero__eyebrow">Electrochemistry · Organic electronics · Functional thin films</p>
  <h1 class="hero__title">Materials chemist advancing electrochromic and photo-active devices.</h1>
  <p class="hero__lede">
    I design molecular interfaces and device workflows that turn thin-film chemistry into reliable optoelectronic performance.
    My MSc work at the Weizmann Institute focuses on electrochromic stacks, photo-electrochromic hybrids, and graphene-enabled architectures.
  </p>
  <div class="hero__meta">
    <span>MSc Chemistry · Weizmann Institute of Science</span>
    <span>Advisors: Prof. Milko van der Boom &amp; Dr. Michal Lahav</span>
  </div>
  <div class="hero__actions">
    <a class="button button--primary" href="/cv/">View CV</a>
    <a class="button button--ghost" href="/about/">More about me</a>
  </div>
</div>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">Focus areas</h2>
    <p class="section__subtitle">Translating nanoscale control into responsive devices</p>
  </div>
  <div class="tag-grid">
    <span class="tag">Electrochromic thin films</span>
    <span class="tag">Photo-electrochromic hybrids</span>
    <span class="tag">Graphene integration</span>
    <span class="tag">Cu(111) single-crystal preparation</span>
    <span class="tag">Spectroscopy-driven analysis</span>
    <span class="tag">Lab IT &amp; automation</span>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">What I’m working on</h2>
    <p class="section__subtitle">Current priorities across the lab and data stack</p>
  </div>
  <div class="highlight-grid">
    <div class="card">
      <h3 class="card__title">Electrochromic film engineering</h3>
      <p class="card__body">
        Tailoring nanoscale interlayers to modulate ion transport, optical contrast, and cycling stability across electrochromic devices.
      </p>
    </div>
    <div class="card">
      <h3 class="card__title">Protocol design</h3>
      <p class="card__body">
        Building reproducible testing flows, from potentiostatic programs to reliability tracking and figure-ready data pipelines.
      </p>
    </div>
    <div class="card">
      <h3 class="card__title">Photo-electrochromic coupling</h3>
      <p class="card__body">
        Exploring photovoltaic stacks that power in-situ tint modulation for low-power, adaptive optics.
      </p>
    </div>
    <div class="card">
      <h3 class="card__title">Lab infrastructure</h3>
      <p class="card__body">
        Supporting 2D Generation with instrument IT, structured data archives, and lightweight Python automation.
      </p>
    </div>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">Featured projects</h2>
    <p class="section__subtitle">Selected research initiatives and tooling</p>
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
    <h2 class="section__title">Recent writing &amp; outputs</h2>
    <p class="section__subtitle">Formal publications and thesis work</p>
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
    <h2 class="section__title">Let’s collaborate</h2>
  </div>
  <div class="callout">
    <strong>Available for conversations</strong> on electrochromic device prototyping, spectroscopy workflows, or lab data infrastructure. Reach out via LinkedIn or email and I’ll follow up.
  </div>
</section>
