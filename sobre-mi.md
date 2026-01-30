---
layout: default
title: Sobre mí
permalink: /sobre-mi/
---

<div class="hero">
  <div class="hero-scanner"></div>
  <div class="avatar-container">
    <div class="avatar-glow"></div>
    <img src="{{ '/assets/img/oso1.png' | relative_url }}" alt="Biel Rosales" class="avatar-img">
  </div>
  <h1>Hola, soy <span class="neon-text">Biel</span></h1>
  <p>OSINT Investigator apasionado por el análisis de fuentes abiertas y la verificación de información digital</p>
  
  <div class="terminal-container" style="max-width: 600px; margin: 2rem auto; text-align: left;">
    <div class="terminal-header">
      <div class="terminal-dot dot-red"></div>
      <div class="terminal-dot dot-yellow"></div>
      <div class="terminal-dot dot-green"></div>
      <span style="margin-left: 10px; color: #8b949e; font-size: 0.8rem;">investigator@kbbaa: ~</span>
    </div>
    <div class="terminal-body">
      <div class="terminal-line">
        <span class="terminal-prompt">$</span>
        <span class="terminal-command">whoami</span>
      </div>
      <div class="terminal-output">Biel Rosales - OSINT Specialist & Cybersecurity Analyst</div>
      <div class="terminal-line">
        <span class="terminal-prompt">$</span>
        <span class="terminal-command">cat skills.json</span>
      </div>
      <div class="terminal-output">
        {<br>
        &nbsp;&nbsp;"focus": ["OSINT", "Open-Source-Analyst", "Geolocation", "Fact-checking"],<br>
        &nbsp;&nbsp;"status": "Active_Investigation"<br>
        }
      </div>
    </div>
  </div>

  <div style="margin-top: 2rem;">
    <a href="{{ '/assets/pdf/cv-biel.pdf' | relative_url }}" class="btn-primary" download>
      Descargar CV (PDF)
    </a>
  </div>
</div>

<section>
  <div class="highlight-box">
    <p style="font-size: 1.1rem; margin: 0; line-height: 1.8;">
      Me especializo en <strong>Open Source Intelligence (OSINT)</strong>, aplicando metodologías estructuradas para la recolección, análisis y verificación de información de fuentes públicas. Mi enfoque combina habilidades técnicas con pensamiento crítico para resolver retos complejos de investigación digital.
    </p>
  </div>
</section>

<section>
  <h2 style="text-align: center; margin-bottom: 3rem;">Habilidades Técnicas</h2>
  
  <style>
    .skills-outer-container {
      position: relative;
      max-width: 850px;
      margin: 4rem auto;
      padding: 2rem;
    }

    /* Blobs de luz de fondo (Efecto Neon de la imagen) */
    .skills-glow-blob {
      position: absolute;
      width: 400px;
      height: 400px;
      border-radius: 50%;
      filter: blur(100px);
      z-index: -1;
      opacity: 0.5;
    }
    .blob-blue {
      top: -100px;
      left: -100px;
      background: rgba(9, 105, 218, 0.6);
    }
    .blob-purple {
      bottom: -100px;
      right: -100px;
      background: rgba(236, 72, 153, 0.4);
    }

    .skills-wrapper {
      position: relative;
      padding: 3rem 2.5rem;
      /* Cristal azul opaco con degradado */
      background: linear-gradient(135deg, rgba(13, 17, 23, 0.8), rgba(9, 105, 218, 0.2));
      backdrop-filter: blur(25px);
      -webkit-backdrop-filter: blur(25px);
      /* Borde fino y brillante tipo cristal */
      border: 1px solid rgba(255, 255, 255, 0.15);
      border-radius: 24px;
      box-shadow: 
        0 20px 50px rgba(0, 0, 0, 0.5),
        inset 0 0 20px rgba(255, 255, 255, 0.05);
      overflow: hidden;
    }

    /* Brillo en el borde superior del cristal */
    .skills-wrapper::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
      z-index: 2;
    }

    .skill-item {
      margin-bottom: 2.5rem;
      position: relative;
    }

    .skill-info {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.8rem;
    }

    .skill-name {
      font-family: 'JetBrains Mono', monospace;
      font-weight: 600;
      font-size: 1rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 12px;
      text-shadow: 0 2px 10px rgba(0,0,0,0.5);
    }

    .progress-bar-container {
      width: 100%;
      height: 14px;
      background: rgba(0, 0, 0, 0.3);
      border-radius: 100vw;
      overflow: hidden;
      border: 1px solid rgba(255, 255, 255, 0.05);
      position: relative;
    }

    .progress-fill {
      height: 100%;
      width: 0;
      /* Degradado neon vibrante */
      background: linear-gradient(90deg, #007cf0, #00dfd8);
      border-radius: 100vw;
      position: relative;
      transition: width 2.5s cubic-bezier(0.22, 1, 0.36, 1);
      box-shadow: 0 0 20px rgba(0, 223, 216, 0.4);
    }

    .progress-fill::after {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: linear-gradient(
        90deg,
        transparent,
        rgba(255, 255, 255, 0.2),
        transparent
      );
      animation: barScan 3s infinite;
    }

    @keyframes barScan {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }

    .skill-tooltip {
      position: absolute;
      bottom: 28px;
      left: 0;
      transform: translateX(-50%);
      background: #007cf0;
      color: white;
      padding: 4px 10px;
      border-radius: 6px;
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.75rem;
      font-weight: 800;
      opacity: 0;
      transition: 
        opacity 0.6s ease-out,
        left 2.5s cubic-bezier(0.22, 1, 0.36, 1);
      pointer-events: none;
      z-index: 10;
      box-shadow: 0 4px 15px rgba(0,0,0,0.4);
    }

    .skill-tooltip::after {
      content: '';
      position: absolute;
      top: 100%;
      left: 50%;
      transform: translateX(-50%);
      border: 6px solid transparent;
      border-top-color: #007cf0;
    }

    .animate .progress-fill { width: var(--target-width); }
    .animate .skill-tooltip { opacity: 1; left: var(--target-width); }

    @media (max-width: 768px) {
      .skills-outer-container { padding: 1rem; margin: 2rem auto; }
      .skills-wrapper { padding: 2rem 1.5rem; }
      .skills-glow-blob { width: 250px; height: 250px; }
    }
  </style>

  <div class="skills-outer-container">
    <div class="skills-glow-blob blob-blue"></div>
    <div class="skills-glow-blob blob-purple"></div>

    <div class="skills-wrapper" id="skillsSection">
      <!-- Skill 1 -->
      <div class="skill-item" data-percent="95">
        <div class="skill-info">
          <span class="skill-name"><span>📍</span> OSINT Core</span>
        </div>
        <div class="progress-bar-container">
          <div class="progress-fill" style="--target-width: 95%;"></div>
        </div>
        <div class="skill-tooltip" style="--target-width: 95%;">95%</div>
      </div>

      <!-- Skill 2 -->
      <div class="skill-item" data-percent="90">
        <div class="skill-info">
          <span class="skill-name"><span>🌍</span> Geolocation</span>
        </div>
        <div class="progress-bar-container">
          <div class="progress-fill" style="--target-width: 90%;"></div>
        </div>
        <div class="skill-tooltip" style="--target-width: 90%;">90%</div>
      </div>

      <!-- Skill 3 -->
      <div class="skill-item" data-percent="85">
        <div class="skill-info">
          <span class="skill-name"><span>🛠️</span> Analytic Tools</span>
        </div>
        <div class="progress-bar-container">
          <div class="progress-fill" style="--target-width: 85%;"></div>
        </div>
        <div class="skill-tooltip" style="--target-width: 85%;">85%</div>
      </div>

      <!-- Skill 4 -->
      <div class="skill-item" data-percent="80">
        <div class="skill-info">
          <span class="skill-name"><span>💻</span> Technical Skills</span>
        </div>
        <div class="progress-bar-container">
          <div class="progress-fill" style="--target-width: 80%;"></div>
        </div>
        <div class="skill-tooltip" style="--target-width: 80%;">80%</div>
      </div>

      <!-- Skill 5 -->
      <div class="skill-item" data-percent="75">
        <div class="skill-info">
          <span class="skill-name"><span>🕸️</span> Web Scraping</span>
        </div>
        <div class="progress-bar-container">
          <div class="progress-fill" style="--target-width: 75%;"></div>
        </div>
        <div class="skill-tooltip" style="--target-width: 75%;">75%</div>
      </div>

      <!-- Skill 6 -->
      <div class="skill-item" data-percent="88">
        <div class="skill-info">
          <span class="skill-name"><span>📊</span> Data Analysis</span>
        </div>
        <div class="progress-bar-container">
          <div class="progress-fill" style="--target-width: 88%;"></div>
        </div>
        <div class="skill-tooltip" style="--target-width: 88%;">88%</div>
      </div>
    </div>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const observerOptions = {
        threshold: 0.2
      };

      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('animate');
          }
        });
      }, observerOptions);

      document.querySelectorAll('.skill-item').forEach(item => {
        observer.observe(item);
      });
    });
  </script>
</section>

<section>
  <h2 style="text-align: center;">Metodología de Trabajo</h2>
  <div class="grid">
    <div class="card">
      <div class="neon-text" style="font-size: 2rem; margin-bottom: 1rem; font-family: 'JetBrains Mono', monospace;">01</div>
      <h3>Rigor Técnico</h3>
      <p>Cada investigación sigue un proceso estructurado y documentado, garantizando resultados reproducibles y verificables.</p>
    </div>

    <div class="card">
      <div class="neon-text" style="font-size: 2rem; margin-bottom: 1rem; font-family: 'JetBrains Mono', monospace;">02</div>
      <h3>Ética Profesional</h3>
      <p>Respeto absoluto por la privacidad y uso responsable de la información pública disponible.</p>
    </div>

    <div class="card">
      <div class="neon-text" style="font-size: 2rem; margin-bottom: 1rem; font-family: 'JetBrains Mono', monospace;">03</div>
      <h3>Aprendizaje Continuo</h3>
      <p>Constante actualización en técnicas, herramientas y metodologías de investigación OSINT.</p>
    </div>
  </div>
</section>

<section style="text-align: center;">
  <h2>Vamos a Conectar</h2>
  <p style="color: #94a3b8; font-size: 1.1rem; margin-bottom: 2rem;">
    ¿Interesado en colaborar o simplemente charlar sobre OSINT?
  </p>
  <div class="hero-buttons">
  <a href="https://www.linkedin.com/in/biel-rosales-2a488220b/" target="_blank" class="btn-secondary">LinkedIn</a>
  <a href="https://github.com/kbbaa" target="_blank" class="btn-secondary">GitHub</a>
  <a href="mailto:rosalesmartinezbiel2@gmail.com" class="btn-secondary">Email</a>
</div>
</section>
