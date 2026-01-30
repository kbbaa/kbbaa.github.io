---
layout: default
title: "Ejercicio OSINT #003 – Presidente"
date: 2025-05-23
tags: [gralhix, osint, geolocalizacion, turquia, investigacion-oficial]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación OSINT #003</h1>
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/president1.jpg' | relative_url }}" alt="Imagen del reto" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

## 1. Objetivo del Reto
Identificar la ubicación exacta donde se encuentran los presidentes en la imagen proporcionada y determinar las coordenadas precisas del punto donde se saludan los funcionarios.

---

## 2. Análisis Visual y Puntos de Interés
La imagen muestra a dos presidentes caminando sobre una alfombra ceremonial blanca y azul hacia la entrada de un complejo gubernamental, lo que sugiere un entorno oficial de alto nivel. Los elementos clave identificados son:

*   **Entorno Arquitectónico:** Grandes columnas y una estructura monumental.
*   **Protocolo:** Alfombra ceremonial con colores específicos (blanco y azul).
*   **Sujetos:** Dos figuras de autoridad en un acto oficial.

---

## 3. Metodología e Investigación

### Fase 1: Identificación del Lugar
Para confirmar la ubicación, realice una búsqueda inversa de imágenes. Los resultados mostraron múltiples publicaciones que identificaban el lugar como el **Complejo Presidencial de Turquía (Cumhurbaşkanlığı Sarayı)**, en Ankara.

Entre ellas, destacaba una publicación de X (Twitter) que documentaba una visita reciente del presidente de Somalia al mismo complejo, coincidiendo plenamente con la arquitectura y el protocolo visibles en la imagen.

**Respuesta:** Complejo Presidencial (Cumhurbaşkanlığı Sarayı), Ankara, Turquía.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/president2.png' | relative_url }}" alt="Búsqueda inversa e identificación" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

### Phase 2: Localización Exacta
Para determinar el punto exacto donde los presidentes se dan la mano, utilicé **Google Earth Pro**. Mediante imágenes históricas y ajustes de perspectiva, localicé la entrada principal del complejo presidencial.

Los elementos arquitectónicos —columnas, distribución del pavimento, alfombra ceremonial y disposición del acceso— coincidieron perfectamente con la escena original. Esto permitió identificar con precisión el punto exacto dentro del recinto.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/president3.png' | relative_url }}" alt="Localización exacta en Google Earth" style="max-width: 75%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## 4. Hallazgos (Intelligence Findings)

| Categoría | Información Identificada |
| :--- | :--- |
| **Lugar** | Complejo Presidencial (Cumhurbaşkanlığı Sarayı) |
| **Ciudad / País** | Ankara, Turquía |
| **Coordenadas Exactas** | 39°55'52"N 32°47'58"E |

---

## 5. Conclusión
La investigación confirma que la imagen fue capturada en el Complejo Presidencial de Turquía en Ankara. La correspondencia arquitectónica y el análisis de fuentes abiertas (X/Twitter) permitieron validar tanto el complejo como las coordenadas geográficas precisas del evento oficial.

---

## Referencias
*   [Ejercicio original - Gralhix](https://gralhix.com/list-of-osint-exercises/osint-exercise-003/)

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
