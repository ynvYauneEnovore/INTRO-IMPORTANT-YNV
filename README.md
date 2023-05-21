<h1>Suvida a Producción Docker</h1>
<h2> <span>Desarrollador: Yovan R. Yaune Enovore</span></h2>
![Logo](https://github.com/ynvYauneEnovore/personal-port/blob/main/public/img/ynv.png](https://www.docker.com/wp-content/uploads/2021/09/Moby-run.png.webp)

<p>Este repositorio contiene una colección de comandos útiles para trabajar con Docker. El objetivo principal es proporcionar una referencia práctica y guías para desarrolladores y administradores de sistemas que deseen utilizar Docker en sus proyectos.</p>

<h2>Estructura del repositorio</h2>

<ul>
  <li><code>/production</code>: Directorio que contiene archivos con ejemplos de comandos de Docker y su descripción.</li>
</ul>

<h2>Uso del repositorio</h2>

<pre><code>git clone https://github.com/ynvYauneEnovore/production-docker-laravel.git</code></pre>

<p>Explora los diferentes directorios para encontrar los comandos que necesitas.</p>

<p>Dentro de cada archivo, encontrarás una descripción detallada del comando y su uso correspondiente.</p>

<h2>Contribución</h2>

<p>¡Tu contribución es bienvenida! Si deseas agregar nuevos comandos, ejemplos o mejorar la documentación existente, puedes seguir estos pasos:</p>

<ol>
  <li>Haz un fork de este repositorio.</li>
  <li>Crea una rama con un nombre descriptivo para tu contribución.</li>
  <li>Realiza los cambios y mejoras en tu rama.</li>
  <li>Envía un pull request para revisar tus cambios.</li>
</ol>

<h2>Subida a un repositorio de Docker</h2>

<p>Para subir una imagen de Docker a un repositorio de Docker, puedes seguir estos pasos:</p>

<pre><code>docker build -t nombre-repositorio/nombre-imagen:etiqueta .
docker login
docker tag nombre-imagen:etiqueta nombre-repositorio/nombre-imagen:etiqueta
docker push nombre-repositorio/nombre-imagen:etiqueta</code></pre>

<h2>Integración con Git para implementar un contenedor Docker en producción</h2>

<p>Para implementar un contenedor Docker en producción mediante la integración con Git, puedes seguir estos pasos:</p>

<ol>
  <li>Configura un repositorio de Git para tu proyecto.</li>
  <li>Crea un archivo de configuración de implementación (por ejemplo, <code>docker-compose.yml</code> o <code>Dockerfile</code>) que describa la configuración del contenedor Docker.</li>
  <li>Crea un archivo de configuración de Git Hooks para automatizar la implementación. Por ejemplo, puedes crear un archivo <code>post-receive</code> en el directorio <code>.git/hooks/</code> con el siguiente contenido:</li>
</ol>

<pre><code>#!/bin/sh
git --work-tree=/ruta-al-proyecto --git-dir=/ruta-al-repositorio checkout -f
docker-compose -f /ruta-al-proyecto/docker-compose.yml up -d</code></pre>

<p>Asegúrate de cambiar <code>/ruta-al-proyecto</code> y <code>/ruta-al-repositorio</code> con las rutas correspondientes en tu entorno.</p>

<ol start="4">
  <li>Configura los permisos de ejecución para el archivo de configuración de Git Hooks:</li>
</ol>

<pre><code>chmod +x .git/hooks/post-receive</code></pre>

<p>Ahora, cada vez que realices un <code>git push</code> a tu repositorio, el contenedor Docker se implementará automáticamente en tu entorno de producción.</p>

<h2>Licencia</h2>

<p>Este proyecto se encuentra bajo la Licencia MIT.

<h2>Contacto</h2>

<p>Si tienes alguna pregunta o sugerencia, no dudes en ponerte en contacto conmigo. Puedes enviar un correo electrónico a <a href="mailto:yovanuxf@gmail.com">yovanuxf@gmail.com</a>.</p>

![Logo](https://github.com/ynvYauneEnovore/personal-port/blob/main/public/img/ynv.png)
