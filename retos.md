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
    font-size: 2.2rem;
    font-weight: 800;
    font-family: 'JetBrains Mono', monospace;
    color: var(--text-primary);
    letter-spacing: -1px;
  }

  /* Decorative Branch Line (L-shape) */
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

  /* Animations for each platform */
  .branch-gralhix {
    animation: growLine 0.5s ease-out forwards, rainbow-blue 3s infinite linear !important;
  }
  .branch-thm {
    animation: growLine 0.5s ease-out forwards, rainbow-red 3s infinite linear !important;
  }
  .branch-htb {
    animation: growLine 0.5s ease-out forwards, rainbow-green 3s infinite linear !important;
  }
  .branch-uk {
    animation: growLine 0.5s ease-out forwards, rainbow-uk 3s infinite linear !important;
  }

  @keyframes rainbow-blue {
    0% { border-color: #0ea5e9; filter: drop-shadow(0 0 5px #0ea5e9); }
    33% { border-color: #00f2ff; filter: drop-shadow(0 0 8px #00f2ff); }
    66% { border-color: #3b82f6; filter: drop-shadow(0 0 5px #3b82f6); }
    100% { border-color: #0ea5e9; filter: drop-shadow(0 0 5px #0ea5e9); }
  }

  @keyframes rainbow-red {
    0% { border-color: #ef4444; filter: drop-shadow(0 0 5px #ef4444); }
    33% { border-color: #f87171; filter: drop-shadow(0 0 8px #f87171); }
    66% { border-color: #dc2626; filter: drop-shadow(0 0 5px #dc2626); }
    100% { border-color: #ef4444; filter: drop-shadow(0 0 5px #ef4444); }
  }

  @keyframes rainbow-green {
    0% { border-color: #22c55e; filter: drop-shadow(0 0 5px #22c55e); }
    33% { border-color: #4ade80; filter: drop-shadow(0 0 8px #4ade80); }
    66% { border-color: #16a34a; filter: drop-shadow(0 0 5px #16a34a); }
    100% { border-color: #22c55e; filter: drop-shadow(0 0 5px #22c55e); }
  }

  @keyframes rainbow-uk {
    0% { border-color: #00247d; filter: drop-shadow(0 0 5px #00247d); }
    33% { border-color: #cf142b; filter: drop-shadow(0 0 8px #cf142b); }
    66% { border-color: #ffffff; filter: drop-shadow(0 0 5px #ffffff); }
    100% { border-color: #00247d; filter: drop-shadow(0 0 5px #00247d); }
  }

  /* Arrow head inherited color */
  .branch-line::after {
    content: '';
    position: absolute;
    right: -10px;
    bottom: -8px;
    width: 0;
    height: 0;
    border-top: 6px solid transparent;
    border-bottom: 6px solid transparent;
    border-left: 10px solid inherit;
    border-left-color: inherit;
  }

  .platform-container.active .branch-line {
    display: block;
  }

  .platform-content {
    max-height: 0;
    overflow: hidden;
    transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
    padding-left: 0;
    opacity: 0;
  }

  .platform-container.active .platform-content {
    max-height: 3000px;
    padding-left: 110px; /* Offset for the branch line */
    padding-top: 40px;
    opacity: 1;
  }

  @keyframes growLine {
    from { height: 0; width: 0; opacity: 0; }
    to { height: 60px; width: 100px; opacity: 0.6; }
  }

  .platform-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(min(100%, 320px), 1fr));
    gap: 2rem;
  }

  @media (max-width: 768px) {
    .platform-container.active .platform-content {
      padding-left: 20px;
    }
    .branch-line {
      display: none !important;
    }
  }
</style>

<div class="hero">
  <div class="hero-scanner"></div>
  <h1>Writeups OSINT</h1>
  <p>Colección de retos resueltos con metodología detallada, herramientas utilizadas y lecciones aprendidas</p>
</div>

<section>
  <!-- Sección Gralhix -->
  <div class="platform-container" id="gralhix-section">
    <div class="platform-header" onclick="togglePlatform('gralhix-section')">
      <img src="{{ '/assets/img/gralhix-site-icon.png' | relative_url }}" alt="Gralhix" class="platform-logo">
      <h2 class="platform-title">Gralhix</h2>
    </div>
    
    <div class="branch-line branch-gralhix"></div>
    
    <div class="platform-content">
      <div class="platform-grid">
        {% assign gralhix_posts = site.posts | where_exp: "post", "post.tags contains 'gralhix'" | reverse %}
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
      </div>
    </div>
  </div>

  <!-- Sección TryHackMe -->
  <div class="platform-container" id="thm-section">
    <div class="platform-header" onclick="togglePlatform('thm-section')">
      <img src="{{ '/assets/img/TryHackMe.png' | relative_url }}" alt="TryHackMe" class="platform-logo">
      <h2 class="platform-title">TryHackMe</h2>
    </div>
    
    <div class="branch-line branch-thm"></div>
    
    <div class="platform-content">
      <div class="platform-grid">
        {% assign thm_posts = site.posts | where_exp: "post", "post.tags contains 'tryhackme'" | reverse %}
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

  <!-- Sección HackTheBox -->
  <div class="platform-container" id="htb-section">
    <div class="platform-header" onclick="togglePlatform('htb-section')">
      <img src="{{ '/assets/img/HTB.png' | relative_url }}" alt="HackTheBox" class="platform-logo">
      <h2 class="platform-title">HackTheBox</h2>
    </div>
    
    <div class="branch-line branch-htb"></div>
    
    <div class="platform-content">
      <div class="platform-grid">
        {% assign htb_posts = site.posts | where_exp: "post", "post.tags contains 'hackthebox'" | reverse %}
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

  <!-- Sección UK OSINT -->
  <div class="platform-container" id="uk-section">
    <div class="platform-header" onclick="togglePlatform('uk-section')">
      <img src="{{ '/assets/img/uk-osint.png' | relative_url }}" alt="UK OSINT" class="platform-logo">
      <h2 class="platform-title">UK OSINT</h2>
    </div>
    
    <div class="branch-line branch-uk"></div>
    
    <div class="platform-content">
      <div class="platform-grid">
        {% assign uk_posts = site.posts | where_exp: "post", "post.tags contains 'uk-osint'" | reverse %}
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


  {% if site.posts.size == 0 %}
  <div class="highlight-box" style="text-align: center; padding: 3rem;">
    <h3 style="margin-bottom: 1rem; color: #f97316;">Contenido en desarrollo</h3>
    <p style="color: #94a3b8; margin: 0;">
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

<section style="background: linear-gradient(135deg, rgba(var(--bg-primary-rgb), 0.4), rgba(9, 105, 218, 0.05)); backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px); padding: 3rem; border-radius: 24px; border: 1px solid rgba(255, 255, 255, 0.1); margin-top: 4rem; position: relative; overflow: hidden;">
  <div style="position: absolute; top: 0; left: 0; right: 0; height: 1px; background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);"></div>
  <h3 style="text-align: center; margin-bottom: 1.5rem; color: #ffffff; text-shadow: 0 2px 10px rgba(0,0,0,0.3);">Sobre estos writeups</h3>
  <p style="text-align: center; color: var(--text-secondary); max-width: 800px; margin: 0 auto; line-height: 1.8; font-size: 1.1rem;">
    Cada writeup está diseñado para ser <strong>educativo y reproducible</strong>. Incluye el proceso completo de investigación, desde la observación inicial hasta las conclusiones finales, con todas las herramientas y técnicas utilizadas documentadas.
  </p>
</section>
