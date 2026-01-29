---
layout: default
title: Herramientas OSINT
permalink: /herramientas/
---

<style>
  .search-container {
    max-width: 100%;
    width: min(600px, 95%);
    margin: 2rem auto;
    position: relative;
    z-index: 10;
  }

  .tools-wrapper {
    position: relative;
    z-index: 10;
  }
  
  .search-input {
    width: 100%;
    padding: 1.2rem 2rem;
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    background: rgba(var(--bg-primary-rgb), 0.5);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    color: var(--text-primary);
    font-size: 1rem;
    outline: none;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  }
  
  .search-input:focus {
    border-color: var(--accent-primary);
    background: rgba(var(--bg-primary-rgb), 0.8);
    box-shadow: 0 0 20px rgba(9, 105, 218, 0.2);
    transform: translateY(-2px);
  }

  .tool-section {
    transition: all 0.3s ease;
  }

  .hidden {
    display: none !important;
  }

  .tool-card {
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 2.5rem 2rem;
  }

  .tool-category h2 {
    text-align: center;
    margin-bottom: 3rem;
    font-weight: 700;
    letter-spacing: -0.5px;
  }

  .tool-category h3 {
    text-align: center;
    color: var(--text-primary);
    margin-bottom: 1.5rem;
  }

  .tags {
    justify-content: center;
  }

  .tool-card p {
    flex-grow: 1;
    font-size: 0.95rem;
    line-height: 1.6;
    margin-bottom: 2rem;
  }

  .tool-link-btn {
    margin-top: auto;
    width: 100%;
    padding: 0.8rem 1.5rem;
    background: rgba(var(--bg-primary-rgb), 0.3);
    border: 1px solid rgba(9, 105, 218, 0.3);
    border-radius: 8px;
    color: var(--accent-primary);
    font-weight: 600;
    font-size: 0.9rem;
    transition: all 0.3s cubic-bezier(0.22, 1, 0.36, 1);
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .tool-link-btn:hover {
    background: var(--accent-primary);
    color: white;
    text-decoration: none;
    border-color: var(--accent-primary);
    transform: translateY(-2px);
    box-shadow: 0 0 20px rgba(9, 105, 218, 0.5);
  }
</style>

<div class="hero">
  <div class="hero-scanner"></div>
  <h1>Herramientas & Recursos OSINT</h1>
  <p>Mi arsenal personal de herramientas y extensiones preferidas para la investigación y análisis digital.</p>
</div>

<div class="search-container">
  <input type="text" id="tool-search" class="search-input" placeholder="Buscar herramienta, categoría o descripción...">
  <div id="no-results" class="hidden" style="text-align: center; margin-top: 2rem; padding: 2rem; background: var(--bg-secondary); border-radius: 8px; border: 1px solid var(--border-color);">
    <p style="font-size: 1.2rem; color: var(--text-primary); margin: 0;">🔍 No se encontraron herramientas que coincidan con tu búsqueda.</p>
  </div>
</div>

<section class="tools-wrapper">
  <div id="platform-section" class="tool-category" style="margin-bottom: 5rem;">
    <h2>Plataformas y Frameworks OSINT</h2>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="maltego plataformas frameworks visual relaciones">
        <h4>Maltego</h4>
        <p>Análisis visual de relaciones entre personas, dominios, IPs y organizaciones.</p>
        <a href="https://www.maltego.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="spiderfoot plataformas frameworks automatizada modulos">
        <h4>SpiderFoot</h4>
        <p>Recolección automatizada de OSINT con cientos de módulos de inteligencia.</p>
        <a href="https://www.spiderfoot.net/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="recon-ng plataformas frameworks modular cli comandos">
        <h4>Recon-ng</h4>
        <p>Framework modular en línea de comandos para reconocimiento de objetivos.</p>
        <a href="https://github.com/lanmaster53/recon-ng" target="_blank" class="tool-link-btn">GitHub Repo</a>
      </div>
      <div class="project-card tool-card" data-keywords="babel x plataformas frameworks ia nlp avanzada">
        <h4>Babel X</h4>
        <p>Plataforma OSINT avanzada que utiliza IA y procesamiento de lenguaje natural (NLP).</p>
        <a href="https://www.babelstreet.com/babel-x" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="1trace plataformas frameworks suite dark web blockchain">
        <h4>1TRACE</h4>
        <p>Suite integral de investigación digital que abarca OSINT, Dark Web y blockchain.</p>
        <a href="https://1trace.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>
  </div>

  <div id="recon-section" class="tool-category" style="margin-bottom: 5rem;">
    <h2>Reconocimiento y Análisis</h2>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="theharvester reconocimiento analisis correos subdominios hosts">
        <h4>theHarvester</h4>
        <p>Recolección de correos, subdominios y hosts públicos.</p>
        <a href="https://github.com/laramies/theHarvester" target="_blank" class="tool-link-btn">GitHub Repo</a>
      </div>
      <div class="project-card tool-card" data-keywords="foca reconocimiento analisis metadatos documentos">
        <h4>FOCA</h4>
        <p>Extracción y análisis de metadatos ocultos en documentos.</p>
        <a href="https://github.com/ElevenPaths/FOCA" target="_blank" class="tool-link-btn">GitHub Repo</a>
      </div>
      <div class="project-card tool-card" data-keywords="shodan reconocimiento analisis dispositivos servicios buscador">
        <h4>Shodan</h4>
        <p>El buscador de referencia para dispositivos y servicios expuestos en Internet.</p>
        <a href="https://www.shodan.io/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="censys reconocimiento analisis infraestructura certificados">
        <h4>Censys</h4>
        <p>Análisis profundo de infraestructuras, certificados y hosts.</p>
        <a href="https://censys.io/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="greynoise reconocimiento analisis ruido filtrado">
        <h4>GreyNoise</h4>
        <p>Identificación de "ruido" automatizado para filtrar escaneos masivos.</p>
        <a href="https://www.greynoise.io/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="leakix reconocimiento analisis fugas datos servicios">
        <h4>LeakIX</h4>
        <p>Indexación de servicios mal configurados y fugas de datos públicas.</p>
        <a href="https://leakix.net/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>
  </div>

  <div id="extension-section" class="tool-category" style="margin-bottom: 5rem;">
    <h2>Browser OSINT (Extensiones)</h2>
    
    <h3 style="margin-top: 2rem;">Análisis General</h3>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="intelhub extensiones analisis texto imagenes metadatos">
        <h4>IntelHub</h4>
        <p>Análisis local de texto, imágenes, dominios y metadatos.</p>
        <a href="https://chromewebstore.google.com/detail/intelhub/jfjpgfklmjdhabodgghmjclpgnpiejlh" target="_blank" class="tool-link-btn">Extensión Chrome</a>
      </div>
      <div class="project-card tool-card" data-keywords="ozzi extensiones ioc buscador ips hashes">
        <h4>OZZI</h4>
        <p>Búsqueda automática de IOCs (IPs, hashes, dominios, URLs).</p>
        <a href="https://ozzi.ai/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="wappalyzer extensiones tecnologias web cms">
        <h4>Wappalyzer</h4>
        <p>Identificación de tecnologías web usadas en sitios.</p>
        <a href="https://www.wappalyzer.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="builtwith extensiones tecnologias frameworks deteccion">
        <h4>BuiltWith</h4>
        <p>Detección de tecnologías y frameworks usados en sitios web.</p>
        <a href="https://builtwith.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="web archives extensiones historico wayback versiones">
        <h4>Web Archives</h4>
        <p>Acceso rápido a versiones antiguas de páginas web.</p>
        <a href="https://web.archive.org/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>

    <h3 style="margin-top: 3rem;">Correos y Perfiles</h3>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="hunter extensiones correos corporativos email">
        <h4>Hunter.io</h4>
        <p>Descubrimiento de correos corporativos y dominios.</p>
        <a href="https://hunter.io/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="clearbit extensiones perfiles empresas conectividad">
        <h4>Clearbit Connect</h4>
        <p>Información pública sobre empresas y dominios.</p>
        <a href="https://clearbit.com/resources/tools/connect" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="rocketreach extensiones emails perfiles profesionales">
        <h4>RocketReach</h4>
        <p>Búsqueda de emails y perfiles profesionales avanzados.</p>
        <a href="https://rocketreach.co/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>

    <h3 style="margin-top: 3rem;">Imágenes y Geolocalización</h3>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="reveye extensiones inversa imagenes buscador">
        <h4>RevEye</h4>
        <p>Búsqueda inversa de imágenes en múltiples motores.</p>
        <a href="https://chromewebstore.google.com/detail/reveye-reverse-image-sear/keaaclcjhehbbapnphnmpiklalfhelgf" target="_blank" class="tool-link-btn">Extensión Chrome</a>
      </div>
      <div class="project-card tool-card" data-keywords="exif viewer extensiones metadatos imagenes datos">
        <h4>EXIF Viewer</h4>
        <p>Visualización de metadatos EXIF en imágenes.</p>
        <a href="https://chromewebstore.google.com/detail/exif-viewer-pro/mmbhfeiddhndihdjeganjggkmjapkffm" target="_blank" class="tool-link-btn">Extensión Chrome</a>
      </div>
      <div class="project-card tool-card" data-keywords="invid extensiones video verificacion imagenes">
        <h4>InVID</h4>
        <p>Verificación de imágenes y vídeos para investigación.</p>
        <a href="https://www.invid-project.eu/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>
  </div>

  <div id="darkweb-section" class="tool-category" style="margin-bottom: 5rem;">
    <h2>Dark Web & Deep Web</h2>
    <p style="text-align: center; color: var(--text-secondary); margin-bottom: 2rem;">⚠️ Uso exclusivo con fines legales y de investigación.</p>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="ahmia dark web buscadores onion">
        <h4>Ahmia</h4>
        <p>Buscador de servicios .onion en la red Tor.</p>
        <a href="https://ahmia.fi/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="darksearch dark web buscadores tor">
        <h4>DarkSearch.io</h4>
        <p>Motor de búsqueda para la dark web.</p>
        <p class="tor-warning">
          ⚠️ Solo funciona con navegador Tor (.onion).
        </p>
        <a href="http://darkzqtmbdeauwq5mzcmgeeuhet42fhfjj4p5wbak3ofx2yqgecoeqyd.onion/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="duckduckgo tor dark web buscadores privado">
        <h4>DuckDuckGo (Tor)</h4>
        <p>Buscador privado integrado en la red Tor.</p>
        <a href="https://duckduckgo.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="onionland dark web buscadores directorio onion">
        <h4>OnionLand Search</h4>
        <p>Directorio y buscador de enlaces .onion.</p>
        <a href="https://www.onionland.io/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="torch dark web buscadores historico tor">
        <h4>Torch</h4>
        <p>Buscador histórico y popular de la red Tor.</p>
        <p class="tor-warning">
          ⚠️ Solo funciona con navegador Tor (.onion).
        </p>
        <a href="http://torchdeedp3i2jigzjdmfpn5ttjhthh5wbmda2rr3jvqjg5p77c54dqd.onion/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>
  </div>

  <div id="search-engines-section" class="tool-category" style="margin-bottom: 5rem;">
    <h2>Buscadores Privados</h2>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="searxng buscadores privacidad metabuscador">
        <h4>Searx / SearxNG</h4>
        <p>Metabuscador open source centrado en privacidad.</p>
        <a href="https://searx.space/" target="_blank" class="tool-link-btn">Instancias</a>
      </div>
      <div class="project-card tool-card" data-keywords="duckduckgo buscadores privacidad general">
        <h4>Gibiru</h4>
        <p>Buscador privado general que no rastrea.</p>
        <a href="https://gibiru.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="brave search buscadores privacidad independiente">
        <h4>Brave Search</h4>
        <p>Buscador independiente sin rastreo de usuarios.</p>
        <a href="https://search.brave.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
    </div>
  </div>

  <div id="resources-section" class="tool-category" style="margin-bottom: 5rem;">
    <h2>Recursos y Frameworks</h2>
    <div class="grid">
      <div class="project-card tool-card" data-keywords="osint framework recursos directorio herramientas">
        <h4>OSINT Framework</h4>
        <p>Directorio completo y estructurado de herramientas OSINT.</p>
        <a href="https://osintframework.com/" target="_blank" class="tool-link-btn">Visitar Sitio</a>
      </div>
      <div class="project-card tool-card" data-keywords="awesome osint recursos github lista curada">
        <h4>Awesome OSINT</h4>
        <p>Lista comunitaria curada de recursos OSINT en GitHub.</p>
        <a href="https://github.com/jivoi/awesome-osint" target="_blank" class="tool-link-btn">GitHub Repo</a>
      </div>
      <div class="project-card tool-card" data-keywords="bellingcat recursos herramientas investigacion guias">
        <h4>Bellingcat Tools</h4>
        <p>Herramientas y guías de investigación de Bellingcat.</p>
        <a href="https://www.bellingcat.com/category/resources/" target="_blank" class="tool-link-btn">Toolkit</a>
      </div>
    </div>
  </div>
</section>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const searchInput = document.getElementById('tool-search');
    const cards = document.querySelectorAll('.tool-card');
    const categories = document.querySelectorAll('.tool-category');
    const subheaders = document.querySelectorAll('h3[style*="margin-top"]');

    searchInput.addEventListener('input', function() {
      const searchTerm = searchInput.value.toLowerCase();
      let totalVisible = 0;
      
      cards.forEach(card => {
        const title = card.querySelector('h3, h4').textContent.toLowerCase();
        const description = card.querySelector('p').textContent.toLowerCase();
        const keywords = card.getAttribute('data-keywords').toLowerCase();
        
        if (title.includes(searchTerm) || description.includes(searchTerm) || keywords.includes(searchTerm)) {
          card.classList.remove('hidden');
          totalVisible++;
        } else {
          card.classList.add('hidden');
        }
      });

      // Show/Hide "No results" message
      const noResults = document.getElementById('no-results');
      if (totalVisible === 0 && searchTerm !== '') {
        noResults.classList.remove('hidden');
      } else {
        noResults.classList.add('hidden');
      }

      // Hide categories if all cards inside are hidden
      categories.forEach(category => {
        const visibleCards = category.querySelectorAll('.tool-card:not(.hidden)');
        if (visibleCards.length === 0) {
          category.classList.add('hidden');
        } else {
          category.classList.remove('hidden');
        }
      });

      // Handle subheaders visibility (Browser OSINT subcategories)
      subheaders.forEach(h3 => {
        let nextSibling = h3.nextElementSibling;
        let anyVisible = false;
        if (nextSibling && nextSibling.classList.contains('grid')) {
          anyVisible = nextSibling.querySelectorAll('.tool-card:not(.hidden)').length > 0;
        }
        
        if (!anyVisible && searchTerm !== '') {
          h3.classList.add('hidden');
        } else {
          h3.classList.remove('hidden');
        }
      });
    });

    // Trigger initial state
    searchInput.dispatchEvent(new Event('input'));
  });
</script>
