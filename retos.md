---
layout: default
title: Retos OSINT
permalink: /retos/
---

<style>
  .platform-container {
    margin-bottom: 4rem;
    position: relative;
  }

  .platform-header {
    display: inline-flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 1.5rem;
    border-radius: 12px;
    transition: all 0.4s cubic-bezier(0.22, 1, 0.36, 1);
    z-index: 2;
    position: relative;
    background: rgba(var(--bg-primary-rgb), 0.4);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.05);
    cursor: pointer;
  }

  .platform-header:hover {
    background: rgba(var(--bg-primary-rgb), 0.6);
    border-color: var(--accent-primary);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    transform: translateY(-2px);
  }

  .platform-logo {
    width: 60px;
    height: 60px;
    object-fit: cover;
    border-radius: 12px;
    border: 2px solid rgba(255, 255, 255, 0.1);
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    transition: all 0.3s ease;
  }

  .platform-header:hover .platform-logo {
    border-color: var(--accent-primary);
    transform: scale(1.1) rotate(5deg);
  }

  .platform-title {
    margin: 0;
    font-size: 2rem;
    font-weight: 700;
    font-family: 'Inter', sans-serif;
    color: var(--text-primary);
    letter-spacing: -0.5px;
  }

  .branch-line {
    position: absolute;
    top: 60px;
    left: 25px;
    width: 100px;
    height: 60px;
    border-left: 3px solid var(--accent-primary);
    border-bottom: 3px solid var(--accent-primary);
    border-bottom-left-radius: 15px;
    opacity: 0.8;
    pointer-events: none;
    display: none;
    filter: drop-shadow(0 0 5px var(--accent-primary));
  }


  .platform-container.active .branch-line { display: block; }

  .platform-content {
    max-height: 0;
    overflow: hidden;
    transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
    padding-left: 0;
    opacity: 0;
  }

  .platform-container.active .platform-content {
    max-height: 3000px;
    padding-left: 110px;
    padding-top: 40px;
    opacity: 1;
  }

  @keyframes growLine {
    from { height: 0; width: 0; opacity: 0; }
    to   { height: 60px; width: 100px; opacity: 0.6; }
  }

  .platform-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(min(100%, 320px), 1fr));
    gap: 2rem;
  }

  @media (max-width: 768px) {
    .platform-container.active .platform-content { padding-left: 20px; }
    .branch-line { display: none !important; }
  }
</style>

<div class="hero">
  <h1>Writeups OSINT</h1>
  <p>Colección de retos resueltos con metodología detallada, herramientas utilizadas y lecciones aprendidas</p>
</div>

<section>
  <div class="platform-container" id="gralhix-section">
    <div class="platform-header" onclick="togglePlatform('gralhix-section')">
      <img src="{{ '/assets/img/gralhix-site-icon.png' | relative_url }}" alt="Gralhix" class="platform-logo">
      <h2 class="platform-title">Gralhix</h2>
    </div>
    <div class="branch-line branch-gralhix"></div>
    <div class="platform-content">
      <div class="platform-grid">
        {% assign gralhix_posts = site.posts | where_exp: "post", "post.tags contains 'gralhix'" | where_exp: "post", "post.hidden != true" | reverse %}
        {% for post in gralhix_posts %}
        <div class="card">
          <div class="card-date">{{ post.date | date: "%d de %B, %Y" }}</div>
          <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
          <div class="tags">
            {% for tag in post.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
            {% endfor %}
          </div>
        </div>
        {% endfor %}
        {% if gralhix_posts.size == 0 %}
        <p style="grid-column: 1/-1; text-align: center; color: var(--text-secondary); padding: 2rem;">
          Próximamente retos de Gralhix.
        </p>
        {% endif %}
      </div>
    </div>
  </div>

  <div class="platform-container" id="thm-section">
    <div class="platform-header" onclick="togglePlatform('thm-section')">
      <img src="{{ '/assets/img/TryHackMe.png' | relative_url }}" alt="TryHackMe" class="platform-logo">
      <h2 class="platform-title">TryHackMe</h2>
    </div>
    <div class="branch-line branch-thm"></div>
    <div class="platform-content">
      <div class="platform-grid">
        {% assign thm_posts = site.posts | where_exp: "post", "post.tags contains 'tryhackme'" | where_exp: "post", "post.hidden != true" | reverse %}
        {% for post in thm_posts %}
        <div class="card">
          <div class="card-date">{{ post.date | date: "%d de %B, %Y" }}</div>
          <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
          <div class="tags">
            {% for tag in post.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
            {% endfor %}
          </div>
        </div>
        {% endfor %}
        {% if thm_posts.size == 0 %}
        <p style="grid-column: 1/-1; text-align: center; color: var(--text-secondary); padding: 2rem;">
          Investigándose... 🔍 (Próximamente retos de TryHackMe)
        </p>
        {% endif %}
      </div>
    </div>
  </div>

  <div class="platform-container" id="htb-section">
    <div class="platform-header" onclick="togglePlatform('htb-section')">
      <img src="{{ '/assets/img/HTB.png' | relative_url }}" alt="HackTheBox" class="platform-logo">
      <h2 class="platform-title">HackTheBox</h2>
    </div>
    <div class="branch-line branch-htb"></div>
    <div class="platform-content">
      <div class="platform-grid">
        {% assign htb_posts = site.posts | where_exp: "post", "post.tags contains 'hackthebox'" | where_exp: "post", "post.hidden != true" | reverse %}
        {% for post in htb_posts %}
        <div class="card">
          <div class="card-date">{{ post.date | date: "%d de %B, %Y" }}</div>
          <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
          <div class="tags">
            {% for tag in post.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
            {% endfor %}
          </div>
        </div>
        {% endfor %}
        {% if htb_posts.size == 0 %}
        <p style="grid-column: 1/-1; text-align: center; color: var(--text-secondary); padding: 2rem;">
          Investigándose... 🔍 (Próximamente retos de HackTheBox)
        </p>
        {% endif %}
      </div>
    </div>
  </div>

  <div class="platform-container" id="uk-section">
    <div class="platform-header" onclick="togglePlatform('uk-section')">
      <img src="{{ '/assets/img/uk-osint.png' | relative_url }}" alt="UK OSINT" class="platform-logo">
      <h2 class="platform-title">UK OSINT</h2>
    </div>
    <div class="branch-line branch-uk"></div>
    <div class="platform-content">
      <div class="platform-grid">
        {% assign uk_posts = site.posts | where_exp: "post", "post.tags contains 'uk-osint'" | where_exp: "post", "post.hidden != true" | reverse %}
        {% for post in uk_posts %}
        <div class="card">
          <div class="card-date">{{ post.date | date: "%d de %B, %Y" }}</div>
          <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
          <div class="tags">
            {% for tag in post.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
            {% endfor %}
          </div>
        </div>
        {% endfor %}
        {% if uk_posts.size == 0 %}
        <p style="grid-column: 1/-1; text-align: center; color: var(--text-secondary); padding: 2rem;">
          Investigándose... 🔍 (Próximamente retos de UK OSINT)
        </p>
        {% endif %}
      </div>
    </div>
  </div>

  <div class="platform-container" id="soterctf-section">
    <div class="platform-header" onclick="togglePlatform('soterctf-section')">
      <img src="{{ '/assets/img/soterctf.png' | relative_url }}" alt="SoterCTF" class="platform-logo">
      <h2 class="platform-title">SoterCTF</h2>
    </div>
    <div class="branch-line branch-soterctf"></div>
    <div class="platform-content">
      <div class="platform-grid">
        {% assign soterctf_posts = site.posts | where_exp: "post", "post.tags contains 'soterctf'" | where_exp: "post", "post.hidden != true" | reverse %}
        {% for post in soterctf_posts %}
        <div class="card">
          <div class="card-date">{{ post.date | date: "%d de %B, %Y" }}</div>
          <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
          <div class="tags">
            {% for tag in post.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
            {% endfor %}
          </div>
        </div>
        {% endfor %}
        {% if soterctf_posts.size == 0 %}
        <p style="grid-column: 1/-1; text-align: center; color: var(--text-secondary); padding: 2rem;">
          Investigándose... 🔍 (Próximamente retos de SoterCTF)
        </p>
        {% endif %}
      </div>
    </div>
  </div>

  {% if site.posts.size == 0 %}
  <div class="highlight-box" style="text-align: center; padding: 3rem;">
    <h3 style="margin-bottom: 1rem;">Contenido en desarrollo</h3>
    <p style="color: var(--text-secondary); margin: 0;">
      Estoy trabajando en nuevos writeups OSINT. Vuelve pronto para ver más análisis detallados.
    </p>
  </div>
  {% endif %}
</section>

<script>
  function togglePlatform(id) {
    const section = document.getElementById(id);
    section.classList.toggle('active');
  }
</script>

<section style="background: linear-gradient(135deg, rgba(var(--bg-primary-rgb), 0.4), rgba(0, 119, 182, 0.08)); backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px); padding: 3rem; border-radius: 24px; border: 1px solid rgba(0, 180, 216, 0.15); margin-top: 4rem; position: relative; overflow: hidden;">
  <div style="position: absolute; top: 0; left: 0; right: 0; height: 1px; background: linear-gradient(90deg, transparent, rgba(0, 180, 216, 0.3), transparent);"></div>
  <h3 style="text-align: center; margin-bottom: 1.5rem; color: var(--text-primary);">Sobre estos writeups</h3>
  <p style="text-align: center; color: var(--text-secondary); max-width: 800px; margin: 0 auto; line-height: 1.8; font-size: 1.1rem;">
    Cada writeup está diseñado para ser <strong>educativo y reproducible</strong>. Incluye el proceso completo de investigación, desde la observación inicial hasta las conclusiones finales, con todas las herramientas y técnicas utilizadas documentadas.
  </p>
</section>
