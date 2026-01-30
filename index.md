---
layout: default
title: Biel Rosales | OSINT & Ciberseguridad
---

<div class="hero">
  <div class="hero-scanner"></div>
  <h1>Biel Rosales</h1>
  <p style="font-size: 1.5rem; color: var(--accent-primary); font-family: 'JetBrains Mono', monospace; margin-bottom: 1rem;">Especialista en OSINT & Analista de Ciberseguridad</p>
  <p>Investigación técnica, geolocalización avanzada y verificación de activos digitales con rigor analítico.</p>
  <div class="hero-buttons">
    <a href="{{ '/retos' | relative_url }}" class="btn-primary">Ver Investigaciones</a>
    <a href="https://www.linkedin.com/in/biel-rosales-2a488220b/" target="_blank" class="btn-secondary">Conectar en LinkedIn</a>
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
  
  <div class="carousel-container" style="max-width: 1000px; margin: 2rem auto; padding: 0 1rem;">
    <div class="carousel-wrapper">
      <div class="carousel-track">
        {% if site.posts.size > 0 %}
          {% assign recent_posts = site.posts | slice: 0, 3 %}
          {% for post in recent_posts %}
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">{{ post.date | date: "%d de %B, %Y" }}</div>
              <h3><a href="{{ post.url }}" class="stretched-link">{{ post.title }}</a></h3>
              <p>{{ post.excerpt | default: "Análisis OSINT detallado con proceso paso a paso y herramientas utilizadas." | strip_html | truncatewords: 25 }}</p>
              <div class="carousel-tags">
                {% for tag in post.tags %}
                <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
                {% endfor %}
              </div>
            </div>
          </div>
          {% endfor %}
        {% else %}
          <!-- Slide 1 -->
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">22 de Enero, 2026</div>
              <h3><a href="{{ '/retos' | relative_url }}" class="stretched-link">Ejercicio OSINT #004 – Complejo turístico</a></h3>
              <p>Análisis de geolocalización de un resort tropical usando búsqueda inversa de imágenes y comparación satelital para identificar la ubicación exacta.</p>
              <div class="carousel-tags">
                <span class="tag">osint</span>
                <span class="tag">geolocalizacion</span>
                <span class="tag">imagenes</span>
              </div>
            </div>
          </div>
          
          <!-- Slide 2 -->
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">21 de Enero, 2026</div>
              <h3><a href="{{ '/retos' | relative_url }}" class="stretched-link">Ejercicio OSINT #003 – Imagen de un monumento</a></h3>
              <p>Identificación de un monumento histórico mediante análisis visual, búsqueda de fuentes abiertas y verificación de contexto cultural.</p>
              <div class="carousel-tags">
                <span class="tag">osint</span>
                <span class="tag">monumentos</span>
                <span class="tag">geolocalizacion</span>
              </div>
            </div>
          </div>
          
          <!-- Slide 3 -->
          <div class="carousel-slide">
            <div class="carousel-card">
              <div class="carousel-date">18 de Enero, 2026</div>
              <h3><a href="{{ '/retos' | relative_url }}" class="stretched-link">Ejercicio OSINT #007 – Ubicación de una fotografía</a></h3>
              <p>Análisis forense de una imagen para determinar su ubicación exacta mediante el estudio de sombras, vegetación y elementos urbanos.</p>
              <div class="carousel-tags">
                <span class="tag">osint</span>
                <span class="tag">gralhix</span>
                <span class="tag">analisis-visual</span>
              </div>
            </div>
          </div>
        {% endif %}
      </div>
    </div>
    
    <div class="carousel-btn carousel-btn-prev">‹</div>
    <div class="carousel-btn carousel-btn-next">›</div>
    
    <div class="carousel-indicators">
      {% if site.posts.size > 0 %}
        {% for i in (1..3) %}
        <div class="carousel-indicator {% if forloop.first %}active{% endif %}"></div>
        {% endfor %}
      {% else %}
        <div class="carousel-indicator active"></div>
        <div class="carousel-indicator"></div>
        <div class="carousel-indicator"></div>
      {% endif %}
    </div>
  </div>
</section>
