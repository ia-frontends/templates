---


---

<h1 id="frontend-config---diego-gutiérrez">Frontend config - Diego Gutiérrez</h1>
<p>A continuación detallo de manera específica, todos los elementos necesarios para iniciar a maquetar un <strong>micrositio</strong> cómodamente. Cabe mencionar que es necesario contar con <strong>software de diseño</strong> algunas <strong>dependencias de Node js</strong>, así como <strong>Gulp 4.</strong></p>
<h1 id="gestión-de-tareas-con---gulp-4">Gestión de tareas con - Gulp 4</h1>
<p>En los micrositios que maqueto, siempre me mantengo en <strong>HTML5, CSS y Javascript</strong>, preprocesando <em>Pug para HTML y SASS para css</em> con Gulp en su versión <em><strong>4.0.1</strong></em>. Independientemente de la tecnología en la que se programe el sitio, a menos de que sea indicado, se trabajará en un entorno diferente como: <em>React o Angular</em> Dicho esto, continuo especificando:</p>
<h3 id="dependencias-para-desarrollo">Dependencias para desarrollo:</h3>
<p>Para trabajar con un micrositio hecho por mi, es necesario contar con los permisos en Mac de escritura en todas las carpetas.* Una ves comprobado los permisos de usuario, procedemos a la instalación de las dependencias con el *<strong>comando de instalación</strong>:</p>
<ul>
<li>“browser-sync”: “^2.26.7”,
<blockquote>
<p>Para montar un servidor local.</p>
</blockquote>
</li>
<li>“gulp”: “^4.0.2”,
<blockquote>
<p>Para gestionar todas las tareas.</p>
</blockquote>
</li>
<li>“gulp-autoprefixer”: “^7.0.1”,
<blockquote>
<p>Para no escribir prefijos de css 3 y navegadores viejos.</p>
</blockquote>
</li>
<li>“gulp-concat”: “^2.6.1”,
<blockquote>
<p>Para concatenar archivos.</p>
</blockquote>
</li>
<li>“gulp-cssnano”: “^2.1.3”,
<blockquote>
<p>Para minificar css.</p>
</blockquote>
</li>
<li>“gulp-header”: “^2.0.9”,
<blockquote>
<p>Para escribir la firma en los archivos.</p>
</blockquote>
</li>
<li>“gulp-if”: “^3.0.0”,
<blockquote>
<p>Gulp if, permite hacer condiciones en la gestión de tareas.</p>
</blockquote>
</li>
<li>“gulp-imagemin”: “^6.1.1”,
<blockquote>
<p>Para optimizar imagenes mediante línea de comando.</p>
</blockquote>
</li>
<li>“gulp-notify”: “^3.2.0”,
<blockquote>
<p>Para notificar cuando se haya ejecutado cualquier tarea de la lista.</p>
</blockquote>
</li>
<li>“gulp-plumber”: “^1.2.1”,
<blockquote>
<p>Para detectar errores dentro de las tareas.</p>
</blockquote>
</li>
<li>“gulp-pretty-html”: “^2.0.10”,
<blockquote>
<p>Para mejorar el aspecto de indentación en los HTML.</p>
</blockquote>
</li>
<li>“gulp-pug”: “^4.0.1”,
<blockquote>
<p>Preprocesar Html con <strong>Pug</strong>.</p>
</blockquote>
</li>
<li>“gulp-sass”: “^4.0.2”,
<blockquote>
<p>Preprocesar CSS con <strong>SASS</strong></p>
</blockquote>
</li>
<li>“gulp-uglify”: “^3.0.2”,
<blockquote>
<p>Para minificar javascript.</p>
</blockquote>
</li>
<li>“node-sass”: “^4.12.0”,
<blockquote>
<p>Para correr <em>Gulp Sass</em></p>
</blockquote>
</li>
<li>“rupture-sass”: “^0.3.0”
<blockquote>
<p>Para hacer media queries.</p>
</blockquote>
</li>
</ul>
<blockquote>
<p>*Si no se cuenta con los permisos correspondientes, se presentarán problemas a la hora de instalar Gulp y sus dependencias.</p>
</blockquote>
<h2 id="instalar-gulp-4-y-trabajar-según-la-etapa-del-proyecto">Instalar Gulp 4 y trabajar según la etapa del proyecto:</h2>
<p>Dentro del archivo <strong>gulpfile.js</strong> encontraremos la variable <code>isProduction</code> con la cual notificaremos al proyecto en que etapa de desarrollo nos encontramos, así, condicionamos su funcionalidad. En el siguiente diagrama se presenta como validamos su uso:</p>
<p><img src="https://static.cinepolis.com/landings/imagenes/diagrama.png" alt="enter image description here"></p>
<h3 id="instalar-dependencias-del-proyecto">Instalar dependencias del proyecto:</h3>
<p>El <strong>comando de instalación</strong> desde teminal es: <strong><code>npm install --save-dev</code></strong>.<br>
Este comando instalará todas las dependencias mencionadas en <strong>package.json</strong></p>
<h3 id="trabajar-con-gulp-en-la-etapa-de-desarrollo">Trabajar con Gulp en la etapa de desarrollo:</h3>
<p>Una ves instalado el proyecto con Gulp, mantenemos la variable: <strong><code>isProduction = false</code></strong> para evitar acabar con la memoria ram de nuestro equipo, ya que es sabido que Gulp, es ejecutado todas las veces en las que se guarda el proyecto.</p>
<p>Para correr el proyecto escribe en terminal: <strong><code>Gulp</code></strong></p>
<h3 id="preparar-los-archivos-con-gulp-en-la-etapa-de-producción">Preparar los archivos con Gulp en la etapa de producción:</h3>
<p>Dentro del archivo <em>gulpfile.js</em> cambiar la variable: <strong><code>isProduction = false</code></strong> a <strong><code>isProduction = true</code></strong><br>
Con ello las imagenes serán optimizadas y los archivos indicados serán minificados y se les agregará la firma del sitio. Pe:</p>
<p><code>/*! Copyright © - 2019 Desarrollado para Ia Interactive */</code><br>
<code>.swiper-container{margin:0 auto;position:relative;overflow:hid...</code></p>
<h1 id="programas">Programas</h1>
<h3 id="diseño-web">Diseño web</h3>
<p>Para gestionar el diseño gráfico de los sites, es necesario contar con:</p>
<ul>
<li><strong>Adobe Photoshop - Ultima versión</strong></li>
<li><strong>Adobe Illustrator - Ultima versión</strong></li>
<li><strong>Sketch - Ultima versión</strong></li>
</ul>
<p>Principalmente para dar seguimiento a los estilos y extraer assets.</p>
<h3 id="frontend">Frontend</h3>
<p>Para gestionar el código de los sites, es necesario contar cualquiera de los 2 softwares:</p>
<ul>
<li>
<p><strong>Visual Studio Code - Ultima versión</strong></p>
<ul>
<li>Con las dependencias:
<ul>
<li>Editorconfig for VS Code.</li>
<li>pug</li>
<li>sass</li>
</ul>
</li>
</ul>
</li>
<li>
<p><strong>Sublime Text - Ultima versión</strong></p>
<ul>
<li>Con las dependencias:
<ul>
<li>Editorconfig for Sublime text 3</li>
<li>Sass language</li>
<li>pug language</li>
</ul>
</li>
</ul>
</li>
</ul>
<p>Cualquiera de los dos funciona muy bien, ya es cuestión de gustos y de vanguardias.</p>
<blockquote>
<p><strong>Nota:</strong> Validar que estos programas tengan acceso completo como administradores, ya que gestionan ciertas carpetas y necesitan de todos los permisos.</p>
</blockquote>
<h1 id="en-resumen">En resumen:</h1>
<p>La lista de programas que se necesitan para maquetar un micrositio o landing:</p>

<table>
<thead>
<tr>
<th>Diseño</th>
<th>Web</th>
</tr>
</thead>
<tbody>
<tr>
<td>Adobe Photoshop - Ultima versión</td>
<td><a href="https://nodejs.org/es/">Node Js</a></td>
</tr>
<tr>
<td>Adobe Illustratir - Ultima versión</td>
<td>Visual Studio Code</td>
</tr>
<tr>
<td>Sketch</td>
<td>Sublime text 3</td>
</tr>
<tr>
<td></td>
<td><strong>Parcel</strong> <em>Opcional</em></td>
</tr>
</tbody>
</table>
