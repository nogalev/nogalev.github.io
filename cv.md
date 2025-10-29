---
layout: page
title: CV
permalink: /cv/
---

## Education
- MSc Chemistry - Weizmann Institute of Science
  - Advisors: Prof. Milko van der Boom - Dr. Michal Lahav
  - Thesis: Tailoring the Electrochromic Properties of Thin Films with a Nanoscale Metal-Organic Insulating Interlayer

## Research Focus
Electrochemistry - electrochromic thin films - organic electronics - photo-electrochromic devices - DSSCs - graphene - Cu(111)

## Experience
{% for item in site.data.experience %}
**{{ item.role }}**, {{ item.org }} - {{ item.location }}  
*{{ item.period }}*  
{% for b in item.bullets %}- {{ b }}
{% endfor %}
{% endfor %}

## Skills
**Technical:** {% for s in site.data.skills.technical %}{{ s }}{% unless forloop.last %} - {% endunless %}{% endfor %}  
**Tools:** {% for s in site.data.skills.tools %}{{ s }}{% unless forloop.last %} - {% endunless %}{% endfor %}  
**Methods:** {% for s in site.data.skills.methods %}{{ s }}{% unless forloop.last %} - {% endunless %}{% endfor %}
