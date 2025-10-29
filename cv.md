---
layout: page
title: CV
permalink: /cv/
---

<section class="section">
  <div class="section__header">
    <h2 class="section__title">Education</h2>
    <p class="section__subtitle">Weizmann Institute of Science</p>
  </div>
  <div class="card">
    <h3 class="card__title">MSc Chemistry</h3>
    <p class="card__meta">Advisors: Prof. Milko van der Boom &amp; Dr. Michal Lahav</p>
    <p class="card__body">
      Thesis: <em>Tailoring the Electrochromic Properties of Thin Films with a Nanoscale Metal-Organic Insulating Interlayer</em>
    </p>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">Research focus</h2>
    <p class="section__subtitle">Electrochemistry · electrochromic thin films · organic electronics</p>
  </div>
  <div class="tag-grid">
    <span class="tag">Electrochromic device stacks</span>
    <span class="tag">Photo-electrochromic hybrids</span>
    <span class="tag">DSSC workflows</span>
    <span class="tag">Graphene integration</span>
    <span class="tag">Cu(111) single-crystal routes</span>
    <span class="tag">Spectroscopy analytics</span>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">Experience</h2>
  </div>
  <div class="highlight-grid">
    {% for item in site.data.experience %}
    <div class="card">
      <h3 class="card__title">{{ item.role }}</h3>
      <p class="card__meta">{{ item.org }} · {{ item.location }} · {{ item.period }}</p>
      <ul class="bullet-list">
        {% for b in item.bullets %}
        <li>{{ b }}</li>
        {% endfor %}
      </ul>
    </div>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section__header">
    <h2 class="section__title">Skills</h2>
  </div>
  <div class="card">
    <p><strong>Technical:</strong> {% for s in site.data.skills.technical %}{{ s }}{% unless forloop.last %} · {% endunless %}{% endfor %}</p>
    <p><strong>Tools:</strong> {% for s in site.data.skills.tools %}{{ s }}{% unless forloop.last %} · {% endunless %}{% endfor %}</p>
    <p><strong>Methods:</strong> {% for s in site.data.skills.methods %}{{ s }}{% unless forloop.last %} · {% endunless %}{% endfor %}</p>
  </div>
</section>
