---
layout: default
title: Biel Rosales | OSINT & Ciberseguridad
---

<style>
  .hero-social-link {
    color: var(--text-secondary);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    display: inline-flex;
  }
  .hero-social-link:hover {
    color: var(--accent-primary);
    transform: translateY(-5px) scale(1.2);
    filter: drop-shadow(0 0 8px var(--accent-primary));
    /* La vibración comienza tras 0.5s de hover */
    animation: shake 0.2s infinite;
    animation-delay: 0.5s;
  }

  @keyframes shake {
    0% { transform: translateY(-5px) scale(1.2) rotate(0deg); }
    25% { transform: translateY(-5px) scale(1.2) rotate(3deg); }
    50% { transform: translateY(-5px) scale(1.2) rotate(0deg); }
    75% { transform: translateY(-5px) scale(1.2) rotate(-3deg); }
    100% { transform: translateY(-5px) scale(1.2) rotate(0deg); }
  }
</style>

<div class="hero">
  <div class="hero-scanner"></div>
  <h1>Biel Rosales</h1>
  <p style="font-size: 1.5rem; color: var(--accent-primary); font-family: 'JetBrains Mono', monospace; margin-bottom: 1rem;">Especialista en OSINT & Analista de Ciberseguridad</p>
  <p>Investigación técnica, geolocalización avanzada y verificación de activos digitales con rigor analítico.</p>
  <div class="social-links" style="margin-bottom: 2rem; justify-content: center; gap: 2.5rem; display: flex;">
    <a href="https://github.com/kbbaa" target="_blank" title="GitHub" class="hero-social-link">
      <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.003-.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    </a>
    <a href="https://www.linkedin.com/in/biel-rosales-2a488220b/" target="_blank" title="LinkedIn" class="hero-social-link">
      <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
    </a>
    <a href="mailto:rosalesmartinezbiel2@gmail.com" title="Email" class="hero-social-link">
      <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
    </a>
  </div>
  <div class="hero-buttons">
    <a href="{{ '/retos' | relative_url }}" class="btn-primary">Ver Investigaciones</a>
  </div>
</div>

<section style="margin: 4rem 0;">
  <div class="grid">
    <div class="card" style="text-align: center; padding: 2rem;">
      <div style="margin-bottom: 1rem;">
        <img src="{{ '/assets/img/lupa.png' | relative_url }}" alt="Investigación" style="height: 60px; width: auto;">
      </div>
      <h3>Investigación</h3>
      <p>Metodologías estructuradas para la recolección de inteligencia técnica y corporativa.</p>
    </div>
    <div class="card" style="text-align: center; padding: 2rem;">
      <div style="margin-bottom: 1rem;">
        <img src="{{ '/assets/img/mapa.png' | relative_url }}" alt="Geolocalización" style="height: 60px; width: auto;">
      </div>
      <h3>Geolocalización</h3>
      <p>Análisis geoespacial y verificación de imágenes mediante técnicas de IMINT avanzadas.</p>
    </div>
    <div class="card" style="text-align: center; padding: 2rem;">
      <div style="margin-bottom: 1rem;">
        <img src="{{ '/assets/img/escudo.png' | relative_url }}" alt="Ciberseguridad" style="height: 60px; width: auto;">
      </div>
      <h3>Ciberseguridad</h3>
      <p>Identificación de superficies de ataque y fugas de información sensible.</p>
    </div>
  </div>
</section>

<section class="carousel-section" style="text-align: center;">
  <div class="carousel-glow carousel-glow-1"></div>
  <div class="carousel-glow carousel-glow-2"></div>
  
  <h2>Últimos Writeups OSINT</h2>
  
  <div class="carousel-container">
    <div class="carousel-wrapper">
      <div class="carousel-track">
        {% if site.posts.size > 0 %}
          {% assign carousel_posts = site.posts | slice: 0, 5 %}
          {% comment %} First set of slides {% endcomment %}
          {% for post in carousel_posts %}
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">{{ post.date | date: "%d de %B, %Y" }}</div>
              <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
              <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
              <div class="carousel-tags">
                {% for tag in post.tags %}
                <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
                {% endfor %}
              </div>
            </div>
          </div>
          {% endfor %}
          {% comment %} Duplicate set for infinite loop {% endcomment %}
          {% for post in carousel_posts %}
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">{{ post.date | date: "%d de %B, %Y" }}</div>
              <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
              <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 20 }}</p>
              <div class="carousel-tags">
                {% for tag in post.tags %}
                <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
                {% endfor %}
              </div>
            </div>
          </div>
          {% endfor %}
        {% else %}
          {% comment %} Static fallback duplicated {% endcomment %}
          {% for i in (1..2) %}
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">22 de Enero, 2026</div>
              <h3><a href="{{ '/retos' | relative_url }}" class="stretched-link">Ejercicio OSINT #004</a></h3>
              <p>Análisis de geolocalización avanzada mediante IMINT.</p>
              <div class="carousel-tags">
                <span class="tag">osint</span>
                <span class="tag">geolocalizacion</span>
              </div>
            </div>
          </div>
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">21 de Enero, 2026</div>
              <h3><a href="{{ '/retos' | relative_url }}" class="stretched-link">Ejercicio OSINT #003</a></h3>
              <p>Identificación de monumentos y análisis de fuentes abiertas.</p>
              <div class="carousel-tags">
                <span class="tag">osint</span>
                <span class="tag">monumentos</span>
              </div>
            </div>
          </div>
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">18 de Enero, 2026</div>
              <h3><a href="{{ '/retos' | relative_url }}" class="stretched-link">Ejercicio OSINT #007</a></h3>
              <p>Ubicación de fotografía mediante análisis forense visual.</p>
              <div class="carousel-tags">
                <span class="tag">osint</span>
                <span class="tag">analisis-visual</span>
              </div>
            </div>
          </div>
          {% endfor %}
        {% endif %}
      </div>
    </div>
  </div>
</section>
