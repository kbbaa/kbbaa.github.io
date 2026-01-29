---
layout: default
title: "OhSINT – TryHackMe"
date: 2026-01-29
tags: [tryhackme, osint, investigacion]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación: OhSINT</h1>
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT1.jpg' | relative_url }}" alt="OhSINT1" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

## ¿De qué es el avatar de este usuario?
Al analizar los metadatos de la imagen con ExifTool, se encuentra un campo de copyright atribuido al nombre “OWoodflint”.
Buscando ese nombre en redes sociales, aparece una cuenta en X (Twitter) donde el avatar es claramente la imagen de un gato.

**Respuesta:** `Cat`

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT2.png' | relative_url }}" alt="OhSINT2" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## ¿En qué ciudad se encuentra esta persona?
En una de sus páginas personales, el usuario menciona estar temporalmente en Nueva York:
“I'm in New York right now…”
Sin embargo, en su perfil de GitHub se presenta con la frase:
“Hi all, I am from London…”
Esto confirma que su ciudad de origen es Londres.

**Respuesta:** `London`

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT3.png' | relative_url }}" alt="OhSINT3" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## ¿Cuál es el SSID del WAP al que se conectó?
ExifTool revela el BSSID de la red WiFi utilizada.
Con ese dato, se consulta Wigle.net, una base de datos de redes inalámbricas.
Filtrando por ubicación (Londres), se identifica el SSID correspondiente.

**Respuesta:** `UnileverWifi`

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT3.jpg.png' | relative_url }}" alt="OhSINT3 SSID" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## ¿Cuál es su dirección de correo electrónico personal?
La dirección de correo aparece públicamente en su perfil de GitHub, dentro de la sección de contacto.

**Respuesta:** `OWoodflint@gmail.com`

---

## ¿En qué sitio encontró su dirección de correo electrónico?
La dirección se encuentra directamente en su perfil de GitHub, en la sección de contacto del repositorio personal.

**Respuesta:** `GitHub`

---

## ¿A dónde se fue de vacaciones?
En una de sus páginas personales, el usuario indica que está en Nueva York y que actualizará su sitio con nuevas fotos desde allí.
Esto confirma que su destino vacacional fue Nueva York.

**Respuesta:** `New York`

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT4.png' | relative_url }}" alt="OhSINT4" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## ¿Cuál es la contraseña de la persona?
La contraseña está oculta en el HTML de su sitio web.
No aparece como comentario ni en campos visibles, sino como texto blanco sobre fondo blanco, lo que la hace invisible a simple vista.
Al seleccionar todo el contenido con Ctrl + A, el texto oculto se revela.

**Respuesta:** `pennYDr0pper.!`

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT5.png' | relative_url }}" alt="OhSINT5" style="max-width: 100%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/OhSINT6.png' | relative_url }}" alt="OhSINT6" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## Conclusión
Este reto demuestra la importancia de cruzar información entre diferentes plataformas (redes sociales, GitHub, metadatos) para construir un perfil completo de un objetivo. La persistencia en la búsqueda y el análisis de detalles técnicos como el BSSID son claves en OSINT.

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
