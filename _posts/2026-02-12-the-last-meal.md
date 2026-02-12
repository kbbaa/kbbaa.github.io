---
layout: default
title: "The Last Meal – UK OSINT"
date: 2026-02-12
tags: [uk-osint, osint, investigacion, geolocalizacion]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación: The Last Meal</h1>
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/bigjohn1.png' | relative_url }}" alt="Big John's establishment" style="max-width: 80%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

En este ejercicio se nos proporciona una imagen de un establecimiento de comida rápida perteneciente a la cadena Big John’s, ubicado en el Reino Unido. Este primer dato ya es relevante, ya que nos permite acotar la investigación a un área geográfica concreta.

---

## 1. Análisis inicial de la imagen
En la fotografía observamos varios elementos clave que nos permiten avanzar en la geolocalización:
- **La señalización vial** y el estilo de los carteles comerciales confirman que nos encontramos en territorio británico.
- **La presencia de un cartel verde** de dirección indica que estamos ante una carretera principal del Reino Unido.
- Además, se aprecia claramente la **referencia a la A41**, una vía importante que atraviesa varias ciudades de la región de West Midlands.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/bigjohn.png' | relative_url }}" alt="Señalización A41" style="max-width: 80%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## 2. Confirmación del área geográfica
Con la información visual disponible, podemos reducir aún más el área de búsqueda. La combinación de:
- la carretera **A41**,
- el estilo de la zona,
- y la presencia de un **Big John’s con drive-thru**,

nos lleva directamente a la zona de **West Bromwich**, muy próxima a Wolverhampton.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/bigjohn2.png' | relative_url }}" alt="Área geográfica" style="max-width: 80%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## 3. Verificación mediante mapas
Para validar la localización exacta, recurrimos a herramientas cartográficas como Google Maps. Al buscar “Big John’s A41” o “Big John’s West Bromwich”, aparecen varias sucursales, ya que se trata de una franquicia con múltiples locales.

Sin embargo, la combinación de elementos visuales —gasolinera cercana, señalización de velocidad, diseño del edificio y disposición de la carretera— nos permite identificar sin duda el establecimiento correcto.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/bigjohn3.png' | relative_url }}" alt="Google Maps verification" style="max-width: 80%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## 4. Confirmación final y obtención del código postal
Una vez localizada la sucursal exacta, solo queda consultar su ficha en Google Maps para obtener el dato solicitado: el código postal asociado al establecimiento.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/bigjohn4.png' | relative_url }}" alt="Final confirmation" style="max-width: 80%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

**FLAG 🚩** `osintuk{B709RL}`

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
