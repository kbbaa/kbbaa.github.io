---
layout: default
title: Sobre mí
permalink: /sobre-mi/
---

<div class="hero">
  <style>
    .avatar-img {
      animation: avatarImgPulse 4s ease-in-out infinite !important;
      border-color: #00b4d8 !important;
    }
    .avatar-glow {
      animation: avatarCyanPulseCustom 4s ease-in-out infinite !important;
      box-shadow: 0 0 20px #00b4d8 !important;
    }
    @keyframes avatarImgPulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.05); }
    }
    @keyframes avatarCyanPulseCustom {
      0%, 100% {
        opacity: 0.6;
        transform: scale(1.01);
        box-shadow: 0 0 15px #00b4d8;
      }
      50% {
        opacity: 0.9;
        transform: scale(1.06);
        box-shadow: 0 0 35px #00b4d8, 0 0 50px rgba(0, 180, 216, 0.4);
      }
    }
  </style>
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
      margin: 2rem auto;
      padding: 2.5rem 2rem;
      background: linear-gradient(135deg, rgba(5, 15, 26, 0.85), rgba(0, 119, 182, 0.15));
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border: 1px solid rgba(0, 180, 216, 0.25);
      border-radius: 24px;
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
      overflow: hidden;
    }
    .skills-outer-container::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(0, 180, 216, 0.5), transparent);
      z-index: 2;
    }
    .radar-legend {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      justify-content: center;
      margin-top: 1.5rem;
    }
    .radar-legend span {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 12px;
      color: #dff0f8;
      font-family: 'JetBrains Mono', monospace;
    }
    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 2px;
      background: #00b4d8;
      display: inline-block;
    }
    @media (max-width: 768px) {
      .skills-outer-container { padding: 1.5rem 1rem; margin: 1rem auto; }
    }
  </style>

  <div class="skills-outer-container">
    <div style="position: relative; width: 100%; height: 520px;">
      <canvas id="radarChart"></canvas>
    </div>
    <div class="radar-legend">
      <span><i class="legend-dot"></i>Nivel actual</span>
    </div>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
  <script>
    document.addEventListener('DOMContentLoaded', function () {
      const ctx = document.getElementById('radarChart').getContext('2d');
      new Chart(ctx, {
        type: 'radar',
        data: {
          labels: [
            'OSINT Core',
            'Geolocation',
            'HUMINT & Social Eng.',
            'IMINIT',
            'Dark Web Investigation',
            'Malware Analysis'
          ],
          datasets: [{
            label: 'Nivel actual',
            data: [95, 90, 85, 80, 75, 88],
            backgroundColor: 'rgba(0, 180, 216, 0.18)',
            borderColor: '#00b4d8',
            borderWidth: 2,
            pointBackgroundColor: '#48cae4',
            pointBorderColor: '#0077b6',
            pointBorderWidth: 2,
            pointRadius: 5,
            pointHoverRadius: 7,
            pointHoverBackgroundColor: '#90e0ef',
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: {
            legend: { display: false },
            tooltip: {
              callbacks: { label: (ctx) => ' ' + ctx.raw + '%' },
              backgroundColor: '#050f1a',
              borderColor: '#00b4d8',
              borderWidth: 1,
              titleColor: '#dff0f8',
              bodyColor: '#48cae4',
              titleFont: { family: 'JetBrains Mono', size: 12 },
              bodyFont: { family: 'JetBrains Mono', size: 13, weight: '500' },
              padding: 10,
            }
          },
          scales: {
            r: {
              min: 0,
              max: 100,
              ticks: {
                stepSize: 25,
                display: true,
                color: 'rgba(0, 180, 216, 0.5)',
                backdropColor: 'transparent',
                font: { family: 'JetBrains Mono', size: 10 },
                callback: (v) => v + '%'
              },
              grid: { color: 'rgba(0, 180, 216, 0.2)', lineWidth: 1 },
              angleLines: { color: 'rgba(0, 180, 216, 0.25)', lineWidth: 1 },
              pointLabels: {
                color: '#dff0f8',
                font: { family: 'JetBrains Mono', size: 12, weight: '500' }
              }
            }
          },
          animation: { duration: 1800, easing: 'easeInOutQuart' }
        }
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
      animation: shake 0.2s infinite;
      animation-delay: 0.5s;
    }
    @keyframes shake {
      0%   { transform: translateY(-5px) scale(1.2) rotate(0deg); }
      25%  { transform: translateY(-5px) scale(1.2) rotate(3deg); }
      50%  { transform: translateY(-5px) scale(1.2) rotate(0deg); }
      75%  { transform: translateY(-5px) scale(1.2) rotate(-3deg); }
      100% { transform: translateY(-5px) scale(1.2) rotate(0deg); }
    }
  </style>
  <h2>Vamos a Conectar</h2>
  <p style="color: var(--text-secondary); font-size: 1.1rem; margin-bottom: 2rem;">
    ¿Interesado en colaborar o simplemente charlar sobre OSINT?
  </p>
  <div class="social-links" style="justify-content: center; gap: 3rem; display: flex;">
    <a href="https://github.com/kbbaa" target="_blank" title="GitHub" class="hero-social-link">
      <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.003-.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    </a>
    <a href="https://www.linkedin.com/in/biel-rosales-2a488220b/" target="_blank" title="LinkedIn" class="hero-social-link">
      <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
    </a>
    <a href="mailto:rosalesmartinezbiel2@gmail.com" title="Email" class="hero-social-link">
      <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
    </a>
  </div>
</section>
