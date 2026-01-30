---
layout: default
title: "Ejercicio OSINT #007 – Ubicación de una fotografía"
date: 2024-12-09
tags: [gralhix, osint, geolocalizacion, analisis-visual, investigacion]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación OSINT #007</h1>
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/estructura1.png' | relative_url }}" alt="Imagen del reto" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

## 1. Objetivo del Reto
El objetivo de esta investigación es triple: identificar la ubicación exacta de una fotografía, determinar el año en que fue tomada y recuperar el enlace visible en un cartel publicitario dentro de la escena.

---

## 2. Análisis Visual y Puntos de Interés
La imagen presenta un entorno urbano con elementos arquitectónicos distintivos y cartelería publicitaria de gran formato. Los puntos clave para la investigación son:

*   **Arquitectura:** Diseño de edificios y pavimentación característicos.
*   **Publicidad:** Un cartel de gran tamaño a la derecha de la imagen con texto parcialmente legible.
*   **Mobiliario Urbano:** Disposición de calles y elementos de señalización.

---

## 3. Metodología e Investigación

### Fase 1: Localización Geográfica
Para identificar la ubicación, utilicé **Google Lens** para analizar las estructuras visibles en la imagen. Los resultados mostraron coincidencias con una zona concreta de **Lisboa**.

Después, verifiqué la localización en **Google Maps**, comparando edificios, disposición de la calle y elementos visuales. Finalmente, confirmé el punto exacto utilizando las coordenadas proporcionadas por la búsqueda inversa.

**Respuesta:** Lisboa (38.767649, -9.096185)

<div style="display: flex; justify-content: center; gap: 1rem; margin: 2rem 0; flex-wrap: wrap;">
  <img src="{{ '/assets/img/estructura2.png' | relative_url }}" alt="Verificación 1" style="width: 45%; max-width: 400px; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
  <img src="{{ '/assets/img/estructura3.png' | relative_url }}" alt="Verificación 2" style="width: 45%; max-width: 400px; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

### Fase 2: Determinación de la Fecha
Para determinar el año, revisé el historial de **Street View** en Google Maps. Al comparar versiones antiguas de la calle, pude identificar el año en el que el cartel y la escena coincidían exactamente con la imagen del reto.

La versión correspondiente a **2019** mostraba todos los elementos en su lugar, lo que permite fechar la fotografía con precisión.

**Respuesta:** 2019

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/estructura4.png' | relative_url }}" alt="Historial Street View" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

### Fase 3: Recuperación del Enlace Publicitario
El cartel no era legible en la imagen principal, así que utilicé Street View histórico para revisar capturas anteriores de la misma calle. En una versión antigua, el cartel aparecía completo y el enlace era claramente visible. Esto permitió recuperar la URL original sin ambigüedades.

**Respuesta:** [www.tutankamon.pt](http://www.tutankamon.pt)

---

## 4. Hallazgos (Intelligence Findings)

| Categoría | Información Identificada |
| :--- | :--- |
| **Ubicación** | Lisboa, Portugal |
| **Coordenadas** | 38.767649, -9.096185 |
| **Año de Captura** | 2019 |
| **Enlace del Cartel** | www.tutankamon.pt |

---

## 5. Conclusión
Mediante el uso de herramientas de búsqueda inversa y el análisis de datos históricos de Street View, se ha logrado reconstruir el contexto completo de la imagen. La investigación confirma que la toma se realizó en Lisboa durante el año 2019, vinculada a una campaña publicitaria de una exhibición sobre Tutankamón.

---

## Referencias
*   [Ejercicio original - Gralhix](https://gralhix.com/list-of-osint-exercises/osint-exercise-007/)

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
