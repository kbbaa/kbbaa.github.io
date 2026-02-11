---
layout: default
title: "Landscape – UK OSINT"
date: 2026-02-11
tags: [uk-osint, osint, esteganografia, forense]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación: Landscape</h1>
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/Landscape.jpg' | relative_url }}" alt="Imagen Landscape" style="max-width: 30%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

## Introducción

En este ejercicio partimos de una imagen en la que sabemos que existe texto oculto, aunque a simple vista apenas es perceptible. Si observamos con atención la zona del cielo, podemos distinguir ligeras variaciones de tonalidad en el gris, lo que sugiere la presencia de caracteres muy difuminados.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/Landscape1.jpg' | relative_url }}" alt="Análisis de tonalidad" style="max-width: 30%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

## Análisis y Proceso

Dado que se trata de un caso típico de texto oculto mediante manipulación de contraste, recurro directamente a **Forensically**, una herramienta gratuita muy útil para análisis forense de imágenes. Su módulo de *Noise Analysis* y *Contrast Enhancement* permite resaltar patrones que normalmente pasarían desapercibidos.

El proceso consiste en ir ajustando parámetros —contraste, exposición, ruido, equalización— hasta encontrar la combinación que revele la información oculta. No existe un ajuste universal: es cuestión de iterar, comparar resultados y detectar cualquier patrón emergente.

Tras varias pruebas y ajustes finos, finalmente se consigue extraer el texto oculto presente en la imagen.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/landscape2.png' | relative_url }}" alt="Texto revelado" style="max-width: 60%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">

  <div style="margin-top: 1.5rem; font-size: 1.2rem;">
    <strong>FLAG 🚩:</strong> <code>osintuk{SKY1234}</code>
  </div>
</div>

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
