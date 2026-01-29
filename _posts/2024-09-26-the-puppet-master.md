---
layout: default
title: "The Puppet Master – HackTheBox"
date: 2024-09-26
tags: [hackthebox, osint, investigacion, vehiculos]
---

<div class="post-hero">
  <h1 style="margin: 0;">Informe de Investigación: The Puppet Master</h1>
</div>

## 1. Evaluación Inicial
La imagen muestra un vehículo militar blindado con ruedas, camuflaje en tonos arena y una estructura robusta típica de los transportes de personal protegidos (MRAP). La presencia de ruedas en lugar de orugas, el frontal inclinado y el diseño del casco permiten descartar otros modelos más comunes como el RG-31 o el Mowag Piranha. Estos detalles sugieren que podría tratarse de un vehículo australiano o empleado por fuerzas aliadas en entornos desérticos.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/Militar.jpg' | relative_url }}" alt="Evaluación inicial del vehículo" style="max-width: 40%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

---

## 2. Identificación del Vehículo
Para confirmar la hipótesis inicial, utilicé Google Lens para realizar una búsqueda inversa. Entre los resultados aparecieron múltiples publicaciones y foros donde se mencionaba el **Bushmaster Protected Mobility Vehicle**. Uno de los posts más relevantes hacía referencia a la fábrica de Thales en Bendigo, Australia, donde se producen estos vehículos. Esto coincide con las características visuales observadas.

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/Militar2.jpg' | relative_url }}" alt="Búsqueda inversa e identificación" style="max-width: 40%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

**Primera flag:** `Bushmaster`

---

## 3. Fabricante del Vehículo
Una vez identificado el modelo, consulté fuentes abiertas para verificar el fabricante. La información más completa y accesible se encuentra en bases de datos públicas y en Wikipedia, donde se indica que el Bushmaster fue diseñado y producido por **Thales Australia**, subsidiaria del grupo francés Thales.

**Segunda flag:** `Thales Australia`

---

## 4. Año de Entrada en Servicio
En la misma ficha técnica se detalla que el Bushmaster entró en servicio en **1997**, manteniéndose operativo hasta la actualidad en varios ejércitos, principalmente el australiano.

**Tercera flag:** `1997`

---

## 5. País de Origen
El vehículo fue diseñado y fabricado en **Australia**, lo cual ya se intuía desde la información del fabricante y se confirma en todas las fuentes consultadas.

**Cuarta flag:** `Australia`

---

## 6. Capacidad de Pasajeros
La capacidad estándar del Bushmaster es de **9 pasajeros más 1 conductor**, lo que lo convierte en un transporte de personal blindado de tamaño medio, adecuado para despliegues tácticos y misiones de protección.

**Quinta flag:** `9 passengers and 1 driver`

---

## Conclusión
Este reto combina identificación visual, verificación cruzada y consulta de fuentes OSINT fiables. El Bushmaster es un vehículo ampliamente documentado, lo que facilita confirmar cada flag mediante análisis estructurado y contrastado.

**Flag final del reto:** `HTB{c0mb1n1ng_r34l_w0rld_4nd_s3lf_c0nt41n3d_OSINT!}`

<div style="text-align: center; margin: 2rem 0;">
  <img src="{{ '/assets/img/Militar3.jpg' | relative_url }}" alt="Misión cumplida" style="max-width: 100%; height: auto; border-radius: 8px; border: 1px solid var(--border-color);">
</div>

<section style="text-align: center; margin-top: 3rem;">
  <a href="{{ '/retos' | relative_url }}" class="btn-primary">← Volver a Writeups</a>
</section>
