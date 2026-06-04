---
layout: post
title: "Tarea 997: Pizza as a Service 2.0"
theme: league
background: '#1a1a1a'
slides:
  - title: "Modelos de Servicio en la Nube"
    slide-data: |
      ### Tarea #997
      Explicación de los modelos IaaS, PaaS y SaaS usando la analogía de la Pizza.
      
      **Alumno:** [Carlos Daniel Que Pérez]
      **Fecha:** 04 de Junio de 2026

  - title: "IaaS: Infraestructura"
    slide-data: |
      ### Descripción
      Es como si te rentaran la cocina y el horno. Tú pones los ingredientes y haces todo el trabajo.
      
      ### Ventajas y Desventajas
      * **Ventaja:** Tienes control total de los servidores.
      * **Desventaja:** Tú eres responsable de las actualizaciones y la seguridad.

  - title: "IaaS: Casos y Ejemplos"
    slide-data: |
      ### Casos de Uso
      * Cuando necesitas mucha potencia o configuraciones muy especiales.
      
      ### Ejemplos
      * **Amazon EC2** (AWS).
      * **Google Compute Engine** (GCP).

  - title: "PaaS: Plataforma"
    slide-data: |
      ### Descripción
      Es como pedir pizza a domicilio. Ellos ponen la pizza y el horno; tú solo pones la mesa y los refrescos.
      
      ### Ventajas y Desventajas
      * **Ventaja:** Te olvidas de configurar servidores, solo subes tu código.
      * **Desventaja:** Estás limitado a lo que el proveedor te ofrezca.

  - title: "PaaS: Casos y Ejemplos"
    slide-data: |
      ### Casos de Uso
      * Ideal para desarrolladores que quieren lanzar apps rápido sin complicaciones.
      
      ### Ejemplos
      * **Heroku**.
      * **Google App Engine**.

  - title: "SaaS: Software"
    slide-data: |
      ### Descripción
      Es como ir a un restaurante. No haces nada, solo llegas y te comes la pizza que ya está lista.
      
      ### Ventajas y Desventajas
      * **Ventaja:** No instalas nada, todo funciona desde el navegador.
      * **Desventaja:** No puedes cambiar nada del funcionamiento interno.

  - title: "SaaS: Casos y Ejemplos"
    slide-data: |
      ### Casos de Uso
      * Herramientas listas para el usuario final.
      
      ### Ejemplos
      * **Google Drive / Gmail**.
      * **Slack** o **Netflix**.

  - title: "Resumen: Pizza as a Service"
    slide-data: |
      ### ¿Quién hace qué?
      * **On-Premise:** Tú haces todo en casa.
      * **IaaS:** Te dan el equipo, tú cocinas.
      * **PaaS:** Te traen la pizza, tú pones la mesa.
      * **SaaS:** Vas al restaurante y te sirven todo.
---

<style>
  .reveal h1 { font-size: 1.8em !important; color: #f1c40f !important; }
  .reveal h3 { font-size: 1.2em !important; color: #e67e22 !important; text-align: left; }
  .reveal p, .reveal li { font-size: 0.8em !important; text-align: left; }
</style>

{% for slide in page.slides %}
<section data-background="{{ page.background }}">
  <h1>{{ slide.title }}</h1>
  <div class="slide-content">
      {{ slide.slide-data | markdownify }}
  </div>
</section>
{% endfor %}