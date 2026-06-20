---
layout: default
title: Portfolio
permalink: /portfolio/
---

<section class="section page-head">
  <div class="section__grid">
    <p class="section__label">Publications</p>
    <div class="prose">
      <p>
        Including a lot of stuff from my undergrad. I think it's important to be able to see a realistic improvement timeline out there. Nothing pops out perfect without having done a lot of worse attempts first.
      </p>
    </div>
  </div>
</section>

<section class="section section--alt">
  <div class="section__grid">
    <p class="section__label">&nbsp;</p>
    <div class="pub-list">
      {%- comment -%} group entries by year, newest first {%- endcomment -%}
      {%- assign by_year = site.data.portfolio.list | sort: "year" | reverse -%}
      {%- assign current_year = "" -%}
      <ul>
        {%- for pub in by_year -%}
          {%- if pub.year != current_year -%}
            {%- unless forloop.first -%}</div></li>{%- endunless -%}
            <li class="pub-year">
              <span class="pub-year__num">{{ pub.year }}</span>
              <div class="pub-year__items">
          {%- endif -%}

              <div class="pub pub--stacked">
                {%- include pub.html pub=pub -%}
              </div>

          {%- assign current_year = pub.year -%}
          {%- if forloop.last -%}</div></li>{%- endif -%}
        {%- endfor -%}
      </ul>
    </div>
  </div>
</section>
