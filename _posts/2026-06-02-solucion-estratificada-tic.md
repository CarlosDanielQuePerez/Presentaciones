---
layout: post
title: "Solución Estratificada"
theme: league
background: '#2c3e50'
slides:
  - title: "1.1 Solución Estratificada de Problemas en TIC"
    slide-data: "### Descripción<br>Consiste en la división metodológica de las infraestructuras tecnológicas en capas (hardware, sistema operativo, red, aplicaciones) para aislar fallos y optimizar la administración de recursos.<br><br>### Características<br>• Enfoque modular y jerárquico.<br>• Facilita el diagnóstico al segmentar la complejidad del sistema.<br>• Permite aplicar soluciones específicas en la capa afectada sin alterar el resto."
     
  - title: "1.1 Solución Estratificada en TIC"
    slide-data: "### Casos de Uso<br>• Auditorías de rendimiento en servidores empresariales.<br>• Diseño de arquitecturas de red complejas y resolución de problemas de conectividad.<br><br>### Ejemplos<br>• El modelo OSI/TCP-IP para solucionar la pérdida de paquetes de datos en la red.<br>• Análisis de logs divididos por capas (aplicación vs. base de datos)."

  - title: "1.1.a Virtualización por Interpretación Pura"
    slide-data: "### Descripción<br>Técnica clásica donde un software (emulador) traduce y ejecuta instrucción por instrucción del código del sistema invitado en tiempo real para adaptarlo al hardware anfitrión.<br><br>### Características<br>• Alta portabilidad (permite ejecutar software de arquitecturas completamente distintas).<br>• Desempeño considerablemente lento debido a la sobrecarga de traducción constante.<br>• Aislamiento total del entorno emulado."

  - title: "1.1.a Interpretación Pura"
    slide-data: "### Casos de Uso<br>• Preservación de software heredado (legacy) y sistemas antiguos.<br>• Desarrollo y pruebas de software para arquitecturas de hardware que aún no están físicamente disponibles.<br><br>### Ejemplos<br>• <b>Bochs</b>: Emulador de arquitectura x86.<br>• Emuladores de consolas retro (NES en procesadores modernos)."

  - title: "1.1.b Virtualización por Recompilación Dinámica"
    slide-data: "### Descripción<br>Evolución de la interpretación pura. Analiza bloques de código en tiempo de ejecución, los traduce a código nativo del anfitrión y los guarda en un búfer (caché) para reutilizarlos.<br><br>### Características<br>• Mucho más rápida que la interpretación pura gracias al almacenamiento en caché.<br>• Consume más memoria RAM temporal para almacenar el código recompilado."

  - title: "1.1.b Recompilación Dinámica"
    slide-data: "### Casos de Uso<br>• Ejecución de aplicaciones multiplataforma con rendimiento cercano al nativo.<br>• Entornos de ejecución virtualizados que requieren optimización sobre la marcha.<br><br>### Ejemplos<br>• <b>QEMU</b>: Utiliza recompilación dinámica para emular diferentes CPU.<br>• <b>Máquina Virtual de Java (JVM)</b>: Mediante su compilador JIT (Just-In-Time)."

  - title: "1.1.c Virtualización por Hipervisión (Bare Metal)"
    slide-data: "### Descripción<br>Tipo de virtualización (Hipervisor Tipo 1) donde el software se instala directamente sobre el hardware físico de la máquina, actuando como el propio sistema operativo subyacente.<br><br>### Características<br>• Rendimiento óptimo de nivel empresarial (acceso directo al hardware).<br>• Alta disponibilidad, escalabilidad y gestión eficiente de recursos físicos.<br>• Mayor seguridad al no depender de un sistema operativo anfitrión intermedio."

  - title: "1.1.c Hipervisión (Bare Metal)"
    slide-data: "### Casos de Uso<br>• Despliegue de nubes privadas y públicas en centros de datos.<br>• Consolidación de servidores empresariales para reducir costos de hardware físico.<br><br>### Ejemplos<br>• <b>VMware ESXi</b><br>• <b>Proxmox VE</b> / KVM<br>• <b>Microsoft Hyper-V Server</b>"
---

{% for slide in page.slides %}
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
  <h1>{{ slide.title }}</h1>
  <div>{{ slide.slide-data }}</div>
</section>
{% endfor %}