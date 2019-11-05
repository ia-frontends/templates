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
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-28M54NEml3w4GDTE" width="100%" style="max-width: 651.625px;" viewBox="0 0 651.625 568.8609390258789"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M337.3046875,66L337.3046875,91L337.80468749999994,116.50000152587894" marker-end="url(#arrowhead87)" style="fill:none"></path><defs><marker id="arrowhead87" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M293.5976491713951,208.811713197274L165.8984375,277.5187530517578L166.39843750000003,306.8859413146973" marker-end="url(#arrowhead88)" style="fill:none"></path><defs><marker id="arrowhead88" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M382.0117238521852,208.81171212193595L508.7109375,277.5187530517578L509.2109375,303.01875381469756" marker-end="url(#arrowhead89)" style="fill:none"></path><defs><marker id="arrowhead89" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M166.39843750000003,377.4937522888183L165.8984375,405.8609390258789L165.8984375,430.8609390258789" marker-end="url(#arrowhead90)" style="fill:none"></path><defs><marker id="arrowhead90" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M509.2109375,381.36093978881865L508.7109375,405.8609390258789L508.7109375,430.8609390258789" marker-end="url(#arrowhead91)" style="fill:none"></path><defs><marker id="arrowhead91" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M508.7109375,476.8609390258789L508.7109375,501.8609390258789L508.7109375,526.8609390258789" marker-end="url(#arrowhead92)" style="fill:none"></path><defs><marker id="arrowhead92" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M165.8984375,476.8609390258789L165.8984375,501.8609390258789L165.8984375,526.8609390258789" marker-end="url(#arrowhead93)" style="fill:none"></path><defs><marker id="arrowhead93" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="A" transform="translate(337.3046875,43)" style="opacity: 1;"><rect rx="0" ry="0" x="-44.2734375" y="-23" width="88.546875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-34.2734375,-13)"><foreignObject width="68.546875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Sitio Web</div></foreignObject></g></g></g><g class="node" id="B" transform="translate(337.3046875,184.2593765258789)" style="opacity: 1;"><polygon points="68.259375,0 136.51875,-68.259375 68.259375,-136.51875 0,-68.259375" rx="5" ry="5" transform="translate(-68.259375,68.259375)"></polygon><g class="label" transform="translate(0,0)"><g transform="translate(-42.84375,-13)"><foreignObject width="85.6875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Producción?</div></foreignObject></g></g></g><g class="node" id="C" transform="translate(165.8984375,341.68984603881836)" style="opacity: 1;"><polygon points="35.303906250000004,0 70.60781250000001,-35.303906250000004 35.303906250000004,-70.60781250000001 0,-35.303906250000004" rx="5" ry="5" transform="translate(-35.303906250000004,35.303906250000004)"></polygon><g class="label" transform="translate(0,0)"><g transform="translate(-6.2265625,-13)"><foreignObject width="12.453125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Si</div></foreignObject></g></g></g><g class="node" id="D" transform="translate(508.7109375,341.68984603881836)" style="opacity: 1;"><polygon points="39.171093750000004,0 78.34218750000001,-39.171093750000004 39.171093750000004,-78.34218750000001 0,-39.171093750000004" rx="5" ry="5" transform="translate(-39.171093750000004,39.171093750000004)"></polygon><g class="label" transform="translate(0,0)"><g transform="translate(-10.5234375,-13)"><foreignObject width="21.046875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Ño</div></foreignObject></g></g></g><g class="node" id="G" transform="translate(165.8984375,453.8609390258789)" style="opacity: 1;"><rect rx="0" ry="0" x="-145.8984375" y="-23" width="291.796875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-135.8984375,-13)"><foreignObject width="271.796875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Cambiar variable a: isProduction = true</div></foreignObject></g></g></g><g class="node" id="F" transform="translate(508.7109375,453.8609390258789)" style="opacity: 1;"><rect rx="0" ry="0" x="-146.9140625" y="-23" width="293.828125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-136.9140625,-13)"><foreignObject width="273.828125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Mantener variable: isProduction = false</div></foreignObject></g></g></g><g class="node" id="H" transform="translate(508.7109375,549.8609390258789)" style="opacity: 1;"><rect rx="0" ry="0" x="-74.4140625" y="-23" width="148.828125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-64.4140625,-13)"><foreignObject width="128.828125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">No optimizar nada</div></foreignObject></g></g></g><g class="node" id="I" transform="translate(165.8984375,549.8609390258789)" style="opacity: 1;"><rect rx="0" ry="0" x="-135.8515625" y="-23" width="271.703125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-125.8515625,-13)"><foreignObject width="251.703125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Optimizar imagenes, css y javascript</div></foreignObject></g></g></g></g></g></g></svg></div>
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
