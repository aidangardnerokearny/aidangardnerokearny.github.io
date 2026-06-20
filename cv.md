---
layout: default
title: CV
permalink: /cv/
---

<section class="section page-head">
  <div class="section__grid">
    <p class="section__label">CV</p>
    <div class="prose cv-head">
      <p>A condensed version is below.</p>
      {%- if site.cv_pdf != "" -%}
      <p><a class="btn btn--solid" href="{{ site.cv_pdf | relative_url }}">Download full CV (PDF) ↓</a></p>
      {%- endif -%}
    </div>
  </div>
</section>

{%- assign cv = site.data.cv -%}

<section class="section section--alt">
  <div class="section__grid">
    <p class="section__label">Education</p>
    <div class="timeline">
      {%- for e in cv.education -%}
      <div class="entry">
        <div class="entry__period">{{ e.period }}</div>
        <div class="entry__body">
          <h3 class="entry__title">{{ e.degree }}</h3>
          <p class="entry__place">{{ e.place }}</p>
          {%- if e.detail -%}<p class="entry__detail">{{ e.detail }}</p>{%- endif -%}
        </div>
      </div>
      {%- endfor -%}
    </div>
  </div>
</section>

<section class="section">
  <div class="section__grid">
    <p class="section__label">Experience</p>
    <div class="timeline">
      {%- for e in cv.experience -%}
      <div class="entry">
        <div class="entry__period">{{ e.period }}</div>
        <div class="entry__body">
          <h3 class="entry__title">{{ e.role }}</h3>
          <p class="entry__place">{{ e.place }}</p>
          {%- if e.detail -%}<p class="entry__detail">{{ e.detail }}</p>{%- endif -%}
        </div>
      </div>
      {%- endfor -%}
    </div>
  </div>
</section>

{%- if cv.teaching and cv.teaching.size > 0 -%}
<section class="section section--alt">
  <div class="section__grid">
    <p class="section__label">Teaching</p>
    <div class="timeline">
      {%- for e in cv.teaching -%}
      <div class="entry">
        <div class="entry__period">{{ e.period }}</div>
        <div class="entry__body">
          <h3 class="entry__title">{{ e.role }}</h3>
          <p class="entry__place">{{ e.place }}</p>
        </div>
      </div>
      {%- endfor -%}
    </div>
  </div>
</section>
{%- endif -%}

{%- if cv.skills and cv.skills.size > 0 -%}
<section class="section">
  <div class="section__grid">
    <p class="section__label">Skills</p>
    <div class="skills">
      {%- for s in cv.skills -%}
      <div class="skills__row">
        <span class="skills__group">{{ s.group }}</span>
        <span class="skills__items">{{ s.items }}</span>
      </div>
      {%- endfor -%}
    </div>
  </div>
</section>
{%- endif -%}
