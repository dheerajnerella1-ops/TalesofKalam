---
layout: default
title: Home
---

<div class="hero">
  <div>
    <h1>Welcome</h1>
    <p class="muted">Explore bespoke calligraphy, original artworks, and fashion illustrations. Commission pieces for weddings, gifts, and special moments.</p>
    <div style="margin-top:.5rem">
      <a class="btn primary" href="#calligraphy">Start with Calligraphy</a>
      <a class="btn" href="#arts">See Arts</a>
      <a class="btn" href="#fashion">Fashion Illustrations</a>
    </div>
  </div>
  <img src="{{ "/assets/gallery/hero.jpg" | relative_url }}" alt="Hero artwork">
</div>

<div id="calligraphy" class="section">
  <h2>Calligraphy</h2>
  <p>Elegant scripts for names, vows, logos, and gifts. I work with archival inks on cotton paper and also offer digital outputs for print.</p>
  <div class="grid">
    {% assign items = site.posts | where_exp: "p", "p.categories contains 'calligraphy'" | slice: 0, 6 %}
    {% for post in items %}
      <div class="card">
        {% if post.image %}<img src="{{ post.image }}" alt="{{ post.title }}">{% endif %}
        <div class="pad">
          <div class="tag">{{ post.date | date: "%b %d, %Y" }}</div>
          <h3 style="margin:.2rem 0"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p class="muted">{{ post.excerpt | strip_html | truncate: 120 }}</p>
        </div>
      </div>
    {% endfor %}
  </div>
</div>

<div id="arts" class="section">
  <h2>Arts</h2>
  <p>Original artworks in ink and mixed media. From minimal compositions to bold textures, each piece balances rhythm and contrast.</p>
  <div class="grid">
    {% assign items = site.posts | where_exp: "p", "p.categories contains 'arts'" | slice: 0, 6 %}
    {% for post in items %}
      <div class="card">
        {% if post.image %}<img src="{{ post.image }}" alt="{{ post.title }}">{% endif %}
        <div class="pad">
          <div class="tag">{{ post.date | date: "%b %d, %Y" }}</div>
          <h3 style="margin:.2rem 0"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p class="muted">{{ post.excerpt | strip_html | truncate: 120 }}</p>
        </div>
      </div>
    {% endfor %}
  </div>
</div>

<div id="fashion" class="section">
  <h2>Fashion Illustrations</h2>
  <p>Stylized figures and garment studies for editorials and custom portraits. Choose digital delivery or signed prints.</p>
  <div class="grid">
    {% assign items = site.posts | where_exp: "p", "p.categories contains 'fashion'" | slice: 0, 6 %}
    {% for post in items %}
      <div class="card">
        {% if post.image %}<img src="{{ post.image }}" alt="{{ post.title }}">{% endif %}
        <div class="pad">
          <div class="tag">{{ post.date | date: "%b %d, %Y" }}</div>
          <h3 style="margin:.2rem 0"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p class="muted">{{ post.excerpt | strip_html | truncate: 120 }}</p>
        </div>
      </div>
    {% endfor %}
  </div>
</div>

<div class="section about-bottom">
  <img src="{{ "/assets/gallery/about.jpg" | relative_url }}" alt="About me">
  <div>
    <h2>About me</h2>
    <p>I am a lettering artist focused on timeless craftsmanship. My studio offers custom commissions and workshops for beginners and teams.</p>
  </div>
</div>