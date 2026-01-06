# 🌦️ Proyecto de Automatización RPA: SENAMHI

## 📋 Descripción del Proyecto
Este proyecto es una solución de **RPA (Robotic Process Automation)** diseñada para extraer, limpiar y consolidar datos meteorológicos históricos desde la plataforma web del [SENAMHI](https://www.senamhi.gob.pe/).

El objetivo principal fue automatizar un proceso manual repetitivo que consumía más de 30 segundos por estación, reduciéndolo a un flujo automático que ahorra un **80% del tiempo operativo** y elimina errores humanos de transcripción.

## 🚀 Desafíos Técnicos Superados
Este script va más allá de una grabación de macros simple. Resuelve problemas complejos de navegación web:
* **Manejo de Iframes Anidados:** El bot navega a través de múltiples capas de la web (Web Principal -> Iframe del Mapa -> Iframe del Popup -> Tabla de Datos).
* **Detección de Cloudflare/Captchas:** Incluye lógica para "escuchar" bloqueos de seguridad. Si detecta una pantalla de verificación de Cloudflare, pausa la ejecución y alerta al usuario en lugar de bloquearse.
* **Interacción con Mapas Dinámicos:** Manipulación de objetos DOM (`leaflet-marker-icon`) para interactuar con mapas geográficos en tiempo real.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** VBA (Visual Basic for Applications).
* **Librería:** Selenium Basic (ChromeDriver).
* **Herramienta:** Microsoft Excel (para consolidación y dashboard).

## ⚙️ Cómo usar este Demo
1.  Descarga el archivo `Excel_Automatizado.xlsm`.
2.  Asegúrate de tener instalado **Selenium Basic** y el **ChromeDriver** actualizado.
3.  Abre el Excel y habilita las Macros.
4.  Ejecuta la macro `Pregunta3_Extraccion_V15_Cloudflare`.

> **⚠️ Nota de Rendimiento:**
> Para efectos de demostración en este portafolio, el bucle de extracción está **limitado a las primeras 3 estaciones**.
> Debido a la arquitectura de seguridad de la web (Iframes + Anti-bot), el script utiliza tiempos de espera (`Waits`) conservadores para garantizar la estabilidad de la conexión.

---
*Desarrollado por [Tu Nombre]*
