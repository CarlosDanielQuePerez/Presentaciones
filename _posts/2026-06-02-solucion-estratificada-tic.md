---
layout: post
title: "Tarea 998: Solución estratificada de problemas en TIC"
theme: league
background: '#2c3e50'
slides:
  - title: "1.1 Solución Estratificada de Problemas en TIC"
    slide-data: |
      ### Descripción
      Consiste en la división metodológica de las infraestructuras en capas (hardware, SO, red, apps) para aislar fallos y optimizar recursos.
      
      ### Características
      * Enfoque modular y jerárquico.
      * Facilita el diagnóstico por segmentos.
      * Soluciones específicas sin alterar el resto.
     
  - title: "1.1 Solución Estratificada en TIC"
    slide-data: |
      ### Casos de Uso
      * Auditorías de rendimiento empresarial.
      * Diseño de redes y resolución de conectividad.
      
      ### Ejemplos
      * Modelo OSI/TCP-IP para pérdida de datos.
      * Análisis de logs divididos por capas.

  - title: "1.1.a Virtualización por Interpretación Pura"
    slide-data: |
      ### Descripción
      Un software traduce instrucción por instrucción del sistema invitado en tiempo real para el hardware anfitrión.
      
      ### Características
      * Alta portabilidad entre arquitecturas.
      * Desempeño lento por sobrecarga constante.
      * Aislamiento total del entorno emulado.

  - title: "1.1.a Interpretación Pura"
    slide-data: |
      ### Casos de Uso
      * Preservación de software legacy.
      * Pruebas para hardware no disponible.
      
      ### Ejemplos
      * **Bochs**: Emulador x86.
      * Emuladores de consolas retro.

  - title: "1.1.b Virtualización por Recompilación Dinámica"
    slide-data: |
      ### Descripción
      Traduce bloques de código en tiempo de ejecución y los guarda en caché para reutilizarlos.
      
      ### Características
      * Más rápida que la interpretación pura.
      * Mayor consumo de memoria RAM por el caché.

  - title: "1.1.b Recompilación Dinámica"
    slide-data: |
      ### Casos de Uso
      * Apps multiplataforma con rendimiento nativo.
      * Entornos optimizados sobre la marcha.
      
      ### Ejemplos
      * **QEMU** y **JVM** (Java Virtual Machine).

  - title: "1.1.c Virtualización por Hipervisión (Bare Metal)"
    slide-data: |
      ### Descripción
      El software se instala directamente sobre el hardware físico (Tipo 1), actuando como sistema base.
      
      ### Características
      * Rendimiento óptimo empresarial.
      * Alta disponibilidad y gestión eficiente.
      * Mayor seguridad sin SO intermedio.

  - title: "1.1.c Hipervisión (Bare Metal)"
    slide-data: |
      ### Casos de Uso
      * Despliegue de nubes públicas/privadas.
      * Consolidación de servidores físicos.
      
      ### Ejemplos
      * **VMware ESXi**, **Proxmox VE** y **Hyper-V**.
---

<style>
  /* Ajuste de Títulos */
  .reveal h1 {
    font-size: 2.0em !important; 
    text-transform: uppercase;
    margin-bottom: 20px !important;
    line-height: 1.1 !important;
  }
  
  /* Ajuste de Subtítulos (Los que antes tenían ###) */
  .reveal h3 {
    font-size: 1.0em !important;
    color: #1abc9c !important;
    margin-top: 20px !important;
    margin-bottom: 10px !important;
    text-transform: none !important;
    text-align: left;
  }

  /* Texto de los párrafos y listas */
  .reveal p, .reveal li {
    font-size: 0.7em !important;
    line-height: 1.3 !important;
    text-align: left;
  }

  .reveal ul {
    margin-left: 1em !important;
  }

  /* Contenedor principal */
  .reveal .slide-content {
    width: 90%;
    margin: 0 auto;
  }
</style>

{% for slide in page.slides %}
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
  <h1>{{ slide.title }}</h1>
  <div class="slide-content">
      {% comment %} 
         AQUÍ ESTÁ EL TRUCO: | markdownify 
         Esto convierte el texto con ### y asteriscos en HTML real
      {% endcomment %}
      {{ slide.slide-data | markdownify }}
  </div>
</section>
{% endfor %}