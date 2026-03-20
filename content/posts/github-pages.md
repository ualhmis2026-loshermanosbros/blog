---
title: "Despliegue del Blog en GitHub Pages"
date: 2026-03-20
author: "Los Hermanos Bros"
description: "Cómo publicar tu sitio estático Hugo de forma gratuita."
summary: "Pasos detallados para hacer pública nuestra web utilizando el servicio de GitHub Pages."
draft: false
---

Una vez que tenemos nuestro blog listo en local, el siguiente paso en la asignatura **HMIS** es hacerlo público. Para ello, hemos elegido **GitHub Pages**.

### ¿Qué es GitHub Pages?
Es un servicio de alojamiento de sitios estáticos que toma archivos HTML, CSS y JavaScript directamente de un repositorio en GitHub y los publica en una URL tipo `usuario.github.io`.

### Pasos para el despliegue con Hugo:

1. **Generar los archivos:** Ejecutamos el comando `hugo` en la terminal. Esto crea la carpeta `/public`.
2. **BaseURL:** Es vital configurar el archivo `hugo.toml` con la URL final (ej: `https://tu-usuario.github.io/tu-repo/`).
3. **Subida de archivos:** * Podemos subir solo la carpeta `public` a una rama llamada `gh-pages`.
   * O mejor aún, usar **GitHub Actions** para que GitHub compile Hugo automáticamente cada vez que hagamos un `push`.

### Beneficios para el equipo
* **Gratuito:** No tiene costes de servidor.
* **Integrado:** Todo el historial de cambios está en el mismo lugar que el código.
* **Rápido:** Al ser contenido estático, la velocidad de carga es excelente.

¡Ya podéis visitar nuestra web online!