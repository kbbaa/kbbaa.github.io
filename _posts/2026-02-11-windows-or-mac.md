---
layout: default
title: "WINDOWS or MAC – UK OSINT"
date: 2026-02-11
tags: [uk-osint, osint, investigacion]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación: WINDOWS or MAC</h1>
</div>

## Introducción

En este desafío se nos entrega una imagen completamente distorsionada, con un efecto de remolino que recuerda a filtros aplicados en programas como Photoshop o editores online.

## Análisis y Proceso

A primera vista no parece un reto especialmente complejo. El objetivo es revertir el filtro lo suficiente como para obtener una imagen reconocible y poder realizar una búsqueda inversa.

Para ello utilicé **GIMP**, un excelente editor gratuito. Concretamente, apliqué el filtro de **Girar y comprimir**, ajustando los parámetros hasta conseguir una versión más estable y legible de la fotografía.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/uk-osint.png' | relative_url }}" alt="UK OSINT Challenge" style="max-width: 50%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

## Identificación

Una vez obtenida una imagen mínimamente clara, procedemos a realizar una búsqueda inversa de imagen para identificar a la persona que aparece. Tras localizar al individuo, ya podemos obtener la flag del reto.

**Flag 🚩:** `osintuk{Lee_Mack}`

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
