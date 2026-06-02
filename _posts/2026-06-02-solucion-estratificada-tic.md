---
layout: slide
title: "Solución TIC"
theme: league
---

# 1.1 Solución Estratificada de Problemas en TIC

### Descripción
Consiste en la división metodológica de las infraestructuras tecnológicas en capas (hardware, sistema operativo, red, aplicaciones) para aislar fallos y optimizar la administración de recursos.
      
### Características
* Enfoque modular y jerárquico.
* Facilita el diagnóstico al segmentar la complejidad del sistema.
* Permite aplicar soluciones específicas en la capa afectada sin alterar el resto.

---

# 1.1 Solución Estratificada en TIC

### Casos de Uso
* Auditorías de rendimiento en servidores empresariales.
* Diseño de arquitecturas de red complejas y resolución de problemas de conectividad.
      
### Ejemplos
* El modelo OSI/TCP-IP para solucionar la pérdida de paquetes de datos en la red.
* Análisis de logs divididos por capas (aplicación vs. base de datos).

---

# 1.1.a Virtualización por Interpretación Pura

### Descripción
Técnica clásica donde un software (emulador) traduce y ejecuta instrucción por instrucción del código del sistema invitado en tiempo real para adaptarlo al hardware anfitrión.
      
### Características
* Alta portabilidad (permite ejecutar software de arquitecturas completamente distintas).
* Desempeño considerablemente lento debido a la sobrecarga de traducción constante.
* Aislamiento total del entorno emulado.

---

# 1.1.a Interpretación Pura

### Casos de Uso
* Preservación de software heredado (legacy) y sistemas antiguos.
* Desarrollo y pruebas de software para arquitecturas de hardware que aún no están físicamente disponibles.
      
### Ejemplos
* **Bochs**: Emulador de arquitectura x86.
* Emuladores de consolas de videojuegos retro (como reproducir código de NES en un procesador moderno).

---

# 1.1.b Virtualización por Recompilación Dinámica

### Descripción
Evolución de la interpretación pura. En lugar de traducir instrucción por instrucción cada vez, analiza bloques de código del sistema invitado en tiempo de ejecución, los traduce a código nativo del anfitrión y los guarda en un búfer (caché) para reutilizarlos.
      
### Características
* Mucho más rápida que la interpretación pura gracias al almacenamiento en caché.
* Consume más memoria RAM temporal para almacenar el código recompilado.

---

# 1.1.b Recompilación Dinámica

### Casos de Uso
* Ejecución de aplicaciones multiplataforma con rendimiento cercano al nativo.
* Entornos de ejecución virtualizados que requieren optimización sobre la marcha.
      
### Ejemplos
* **QEMU**: Utiliza recompilación dinámica para emular diferentes CPU con excelente velocidad.
* **Máquina Virtual de Java (JVM)**: Mediante su compilador JIT (Just-In-Time).

---

# 1.1.c Virtualización por Hipervisión (Bare Metal)

### Descripción
Tipo de virtualización (Hipervisor Tipo 1) donde el software de virtualización se instala directamente sobre el hardware físico de la máquina, actuando como el propio sistema operativo subyacente.
      
### Características
* Rendimiento óptimo y de nivel empresarial (acceso casi directo al hardware).
* Alta disponibilidad, escalabilidad y gestión eficiente de recursos físicos.
* Mayor seguridad al no depender de un sistema operativo anfitrión intermedio.

---

# 1.1.c Hipervisión (Bare Metal)

### Casos de Uso
* Despliegue de nubes privadas y públicas en centros de datos.
* Consolidación de servidores empresariales para reducir costos de hardware físico.
      
### Ejemplos
* **VMware ESXi**
* **Proxmox VE** / KVM
* **Microsoft Hyper-V Server** (versión core dedicada)