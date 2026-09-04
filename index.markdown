---
layout: page
title: News
---


<div class="news-home">
  <section class="news-intro" aria-labelledby="news-intro-title">
    <div class="news-title-banner">
      <h1 id="news-intro-title">Biodiversity in a changing world</h1>
    </div>

    <div class="news-intro-details">
      <p class="news-lede">
        Research updates, new papers, field observations, and stories from our lab
        at Xiamen University.
      </p>

      <aside class="news-focus" aria-label="Research focus">
        <p>Research focus</p>
        <ul>
          <li>Biodiversity</li>
          <li>Functional traits</li>
          <li>Global change</li>
        </ul>
      </aside>
    </div>
  </section>

  <section class="news-section" aria-labelledby="latest-news-title">
    <div class="news-section-heading">
      <h2 id="latest-news-title">Latest news</h2>
      <a href="{{ '/news/' | relative_url }}">News archive →</a>
    </div>

    {%- for item in site.data.news limit: 3 -%}
    <article class="news-story{% if item.featured %} news-story-featured{% endif %}">
      <div class="news-meta">
        <time datetime="{{ item.year }}">{{ item.year }}</time>
        <span>{{ item.category }}</span>
      </div>
      <div class="news-story-body">
        {%- if item.featured -%}<p class="news-story-label">Featured research</p>{%- endif -%}
        <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
        <p>{{ item.summary }}</p>
      </div>
    </article>
    {%- endfor -%}
  </section>
</div>
