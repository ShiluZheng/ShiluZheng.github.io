---
layout: page
title: News Archive
permalink: /news/
---

<div class="news-archive">
  <header class="news-archive-header">
    <h1>News archive</h1>
    <p>Research updates, publications, and news from Zheng Lab.</p>
  </header>

  <section class="news-archive-list" aria-label="All news">
    {%- for item in site.data.news -%}
    <article class="news-archive-item">
      <div class="news-meta">
        <time datetime="{{ item.year }}">{{ item.year }}</time>
        <span>{{ item.category }}</span>
      </div>
      <div>
        <h2><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
        <p>{{ item.summary }}</p>
      </div>
    </article>
    {%- endfor -%}
  </section>
</div>
