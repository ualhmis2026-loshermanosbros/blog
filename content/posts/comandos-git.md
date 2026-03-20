---
title: "Guía Completa: Git, Hugo y Despliegue en GitHub Pages"
date: 2026-03-20
author: "Los Hermanos Bros"
description: "Documentación completa de nuestra metodología de desarrollo para HMIS."
layout: "single"
draft: false
---

Bienvenidos a la documentación oficial de **Los Hermanos Bros**. En esta entrada vamos a explicar detalladamente todas las herramientas y metodologías que hemos utilizado para construir y desplegar este blog estático para nuestra asignatura.

---

## 1. Control de Versiones con Git
Para el desarrollo colaborativo, **Git** ha sido nuestra herramienta principal. Nos permite llevar un registro de los cambios y trabajar en equipo sin pisarnos el código.

### Configuración Inicial
Antes de empezar a hacer commits, es necesario identificarse:
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@correo.com"
```

### Flujo de Trabajo (El día a día)
Estos son los comandos que utilizamos constantemente para subir nuestros avances:
1. `git pull`: Descarga los últimos cambios del repositorio (vital antes de empezar a programar).
2. `git status`: Nos muestra qué archivos hemos modificado en local.
3. `git add .`: Prepara todos los archivos modificados para ser guardados.
4. `git commit -m "Mensaje descriptivo"`: Guarda una "foto" de nuestro código con una explicación de lo que hemos hecho.
5. `git push origin main`: Sube nuestros commits a GitHub para que el resto del equipo pueda verlos.

---

## 2. Generador de Sitios Estáticos (SSG): Hugo
En lugar de programar cada página HTML a mano o usar un gestor pesado como WordPress, hemos optado por **Hugo**, un motor SSG ultrarrápido.

### ¿Cómo funciona nuestro entorno?
* **Contenido en Markdown:** Escribimos nuestras entradas en archivos `.md` simples y limpios (como este mismo post).
* **Diseño en Layouts:** Utilizamos el tema *PaperMod*, que proporciona las plantillas CSS y HTML base.
* **Compilación:** Al ejecutar el comando `hugo` en la terminal, el motor une nuestro Markdown con las plantillas y genera una carpeta `public/` llena de archivos HTML estáticos y ligeros.

---

## 3. Despliegue en GitHub Pages
Para que el blog sea accesible desde cualquier parte del mundo de forma gratuita, lo hemos alojado en **GitHub Pages**.

### Pasos que seguimos para el despliegue:
1. **Ajuste de la URL:** Configuramos el archivo `hugo.toml` para que la `baseURL` apunte a nuestro repositorio oficial (`https://usuario.github.io/repo/`).
2. **Generación del sitio:** Ejecutamos Hugo en local para generar la carpeta de producción.
3. **Publicación:** Subimos el contenido generado a nuestro repositorio. GitHub Pages detecta automáticamente el HTML y sirve la página web sin necesidad de configurar servidores, bases de datos ni certificados SSL manualmente.

> **Reflexión final:** La combinación de Git para el control de versiones, Hugo para la generación estática y GitHub Pages para el alojamiento, nos ha proporcionado un flujo de trabajo profesional, rápido y sin costes.