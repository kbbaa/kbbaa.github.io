---
layout: default
title: "Ejercicio OSINT #002 – Ubicación de un edificio"
date: 2025-03-17
tags: [gralhix, osint, geolocalizacion, arquitectura, busqueda-inversa]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación OSINT #002</h1>
</div>

## 1. Objetivo del Reto
Identificar la ubicación exacta, el nombre y la altura de la estructura más alta visible en la fotografía proporcionada.

---

## 2. Análisis Visual y Puntos de Interés
Al analizar la imagen, se extrajeron los siguientes elementos clave para la geolocalización:

*   **Identificadores de Edificios:** Se observan logotipos corporativos en edificios marrón (**HWT** e **IBM**) y un logotipo rojo en un edificio negro (**Central Equity**).
*   **Infraestructura de Transporte:** Un cartel legible indica "**Flinders Street**", sugiriendo una estación de tren.
*   **Estructura Distintiva:** Una aguja o torre metálica con forma de antena que domina el skyline.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/osint-002.png' | relative_url }}" alt="Imagen del reto" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## 3. Metodología e Investigación

### Fase 1: Localización Geográfica
El nombre "Flinders Street" nos lleva directamente a **Melbourne, Australia**. La estación Flinders Street es un punto neurálgico de la ciudad. Mediante **Google Earth**, se validó la perspectiva desde los andenes, confirmando que la disposición de los edificios marrón e industriales coincide plenamente con la realidad.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/Osint-002-localizar.png' | relative_url }}" alt="Localización en Google Earth" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

### Fase 2: Identificación de la Estructura Más Alta
Aunque la aguja del **Arts Centre Melbourne** es muy prominente, se procedió a comparar su altura con el edificio negro adyacente:
*   **Arts Centre Melbourne (Antena):** 162 metros.
*   **Central Equity Tower (Edificio negro):** 167 metros.

Tras consultar fuentes arquitectónicas, se confirma que el edificio de Central Equity supera en altura a la antena del centro de artes.

---

## 4. Hallazgos (Intelligence Findings)

| Categoría | Información Identificada |
| :--- | :--- |
| **Ciudad** | Melbourne, Australia |
| **Punto de Captura** | Estación Flinders Street |
| **Estructura más alta** | Central Equity Tower |
| **Altura Confirmada** | 167 metros |
| **Coordenadas** | -37.82215876715402, 144.96540246070137 |

---

## 5. Conclusión
La investigación concluye que la fotografía fue tomada desde la estación Flinders Street en Melbourne. A pesar de la prominencia visual de la aguja del Arts Centre, la **Central Equity Tower** es la estructura de mayor altura en el encuadre con **167 metros**.

---

## Referencias
*   [Ejercicio original - Gralhix](https://gralhix.com/list-of-osint-exercises/osint-exercise-002/)

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
