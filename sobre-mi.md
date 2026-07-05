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
    <img src="{{ '/assets/img/perfil.jpg' | relative_url }}" alt="Biel Rosales" class="avatar-img">
  </div>
  <h1><span class="neon-text">Biel Rosales</span></h1>
  <p>Estudiante de FP Grado Superior en Ciberseguridad. Especializado en Ciberinteligencia, OSINT y resolución documentada de investigaciones.</p>


  <div style="max-width: 600px; margin: 2rem auto; background: var(--bg-secondary); border: 1px solid var(--border-color); border-radius: 12px; padding: 1.5rem 2rem; text-align: left;">
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem 2rem; font-size: 0.95rem;">
      <div><span style="color: var(--text-secondary); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.5px;">Formación</span><p style="margin: 0.2rem 0 0; color: var(--text-primary); font-weight: 600;">FP Grado Superior en Ciberseguridad</p></div>
      <div><span style="color: var(--text-secondary); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.5px;">Ubicación</span><p style="margin: 0.2rem 0 0; color: var(--text-primary); font-weight: 600;">Barcelona</p></div>
      <div><span style="color: var(--text-secondary); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.5px;">Especialización</span><p style="margin: 0.2rem 0 0; color: var(--text-primary); font-weight: 600;">OSINT, SOCMINT, IMINT, Google Dorks</p></div>
      <div><span style="color: var(--text-secondary); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.5px;">Objetivo</span><p style="margin: 0.2rem 0 0; color: var(--text-primary); font-weight: 600;">Inteligencia de fuentes abiertas</p></div>
    </div>
  </div>

</div>

<section>
  <div class="highlight-box">
    <p style="font-size: 1.1rem; margin: 0; line-height: 1.8;">
      Tengo 19 años y estoy finalizando un <strong>Grado Superior en Ciberseguridad</strong>. Desde el principio lo que más me atrajo del sector no fue solo la técnica, sino entender cómo suceden las cosas: cómo se construye una investigación desde cero, cómo se conectan puntos que a primera vista no tienen relación.
      <br><br>
      Eso me llevó al OSINT de forma natural. Me di cuenta de que con un nombre, una red social, o cualquier dato aparentemente insignificante, se puede reconstruir una huella digital completa. Lo que para otros es un callejón sin salida, para mí es el punto de partida.
      <br><br>
      Trabajo principalmente con <strong>Google Dorks, SOCMINT</strong> y análisis de redes sociales, combinando herramientas según lo que cada investigación requiere. Todos los writeups de este portfolio los he resuelto de forma <strong>completamente independiente</strong>, aplicando metodología propia. Actualmente me estoy formando de manera autodidacta en OSINT avanzado y evaluando especializaciones del sector.
    </p>
  </div>
</section>

<section>
  <h2 style="text-align: center; margin-bottom: 3rem;">Habilidades Técnicas</h2>

  <style>
    .skills-outer-container {
      max-width: 850px;
      margin: 2rem auto;
      padding: 2rem;
      background: var(--bg-primary);
      border: 1px solid var(--border-color);
      border-radius: 16px;
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
      color: var(--text-secondary);
    }
    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 2px;
      background: var(--accent-primary);
      display: inline-block;
    }
    .radar-disclaimer {
      text-align: center;
      font-size: 0.78rem;
      color: var(--text-secondary);
      margin-top: 1rem;
      font-style: italic;
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
      <span><i class="legend-dot"></i>Nivel actual (autoevaluación honesta)</span>
    </div>
    <p class="radar-disclaimer">// Nivel 100 = experto profesional con años de experiencia en entorno real</p>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
  <script>
    document.addEventListener('DOMContentLoaded', function () {
      const ctx = document.getElementById('radarChart').getContext('2d');
      new Chart(ctx, {
        type: 'radar',
        data: {
          labels: [
            'Google Dorks',
            'SOCMINT',
            'Geolocalización / IMINT',
            'Análisis de metadatos',
            'HUMINT digital',
            'Dark Web / OPSEC'
          ],
            datasets: [{
            label: 'Nivel actual',
            data: [72, 68, 65, 55, 50, 30],
            backgroundColor: 'rgba(59, 130, 246, 0.15)',
            borderColor: '#3b82f6',
            borderWidth: 2,
            pointBackgroundColor: '#3b82f6',
            pointBorderColor: '#fff',
            pointBorderWidth: 2,
            pointRadius: 5,
            pointHoverRadius: 7,
            pointHoverBackgroundColor: '#60a5fa',
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: {
            legend: { display: false },
              tooltip: {
              callbacks: { label: (ctx) => ' ' + ctx.raw + '/100' },
              backgroundColor: 'var(--bg-primary)',
              borderColor: 'var(--border-color)',
              borderWidth: 1,
              titleColor: 'var(--text-primary)',
              bodyColor: 'var(--text-secondary)',
              titleFont: { family: 'Inter', size: 12 },
              bodyFont: { family: 'Inter', size: 13, weight: '500' },
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
                color: 'var(--text-secondary)',
                backdropColor: 'transparent',
                font: { family: 'Inter', size: 10 },
                callback: (v) => v
              },
              grid: { color: 'var(--border-color)', lineWidth: 1 },
              angleLines: { color: 'var(--border-color)', lineWidth: 1 },
              pointLabels: {
                color: 'var(--text-primary)',
                font: { family: 'Inter', size: 12, weight: '500' }
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
  <h2 style="text-align: center;">Cómo trabajo</h2>
  <div class="grid">
    <div class="card">
      <div style="font-size: 1.8rem; font-weight: 700; color: var(--accent-primary); margin-bottom: 0.75rem;">01</div>
      <h3>Empiezo con poco</h3>
      <p>Un nombre, un alias, una foto. Me interesa lo que otros descartan: los datos que parecen no llevar a ningún sitio suelen ser el mejor punto de partida.</p>
    </div>
    <div class="card">
      <div style="font-size: 1.8rem; font-weight: 700; color: var(--accent-primary); margin-bottom: 0.75rem;">02</div>
      <h3>Conecto los puntos</h3>
      <p>OSINT es sobre relaciones entre datos, no datos aislados. Busco vínculos entre perfiles, familiares, metadatos y huellas digitales para construir el mapa completo.</p>
    </div>
    <div class="card">
      <div style="font-size: 1.8rem; font-weight: 700; color: var(--accent-primary); margin-bottom: 0.75rem;">03</div>
      <h3>Documento todo</h3>
      <p>Cada investigación queda registrada con metodología, herramientas y razonamiento. Si no puedes reproducirlo, no puedes verificarlo.</p>
    </div>
  </div>
</section>

<section style="text-align: center;">
  <style>
    .hero-social-link {
      color: var(--text-secondary);
      transition: color 0.2s ease, transform 0.2s ease;
      display: inline-flex;
    }
    .hero-social-link:hover {
      color: var(--accent-primary);
      transform: translateY(-3px);
      text-decoration: none;
    }
  </style>
  <h2>Contacto</h2>
  <p style="color: var(--text-secondary); font-size: 1.1rem; margin-bottom: 2rem;">
    ¿Tienes un proyecto, una propuesta o simplemente quieres hablar de OSINT?
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
