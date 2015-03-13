Esta aplicación fue creada para gestionar la distribución de alimentos del FEGA en una Asociación Social. La aplicación se puede utilizar para otras gestiones con pequeñas modificaciones.
Proporciono un archivo con la documentación del mismo y un manual de uso, aunque el manual está adaptado para la Asociación, o sea con el logo de esa asociación.
La aplicación está funcionando con PHP5, HTML4, CSS3 y MySQL.
Funciona perfectamente sobre un servidor Linux con Apache y MySQL, proporcionado por la última versión de XAMPP.
También funciona en un servidor Windows, pero debido a un error, que no he conseguido solucionar la exportación a EXCEL no funciona.
Esta aplicación está diseñada para el navegador Google Chrome (o Chromium) y se recomienda su uso para utilizar la misma.

Versión 1.1 Mejoras
<ul>
<li>Nueva estadísticas de la cantidad de alimentos según la fase que le indiques</li>
<li>Resuelto el problema al crear un PDF con el listado de los usuarios, el error producía que solo se crease una página de los usuarios.</li>
<li>Se ha ordenado el listado en PDF por cod_grupo y no por cod_usuario</li>
<li>Resuelto el error al modificar un dato, este producía que subiese un dato un archivo aunque no hubiese sido indicado a la base de datos</li>
<li>Resuelto el error que se producía al poner un DNI/Pasaporte que no se comprobase si existía el mismo DNI dentro de la familia al modificar, pero este lo comprobada dentro del mismo familiar también lo que impedía que se modificase, se ha solucionado indicando que no buscase dentro del mismo usuario.</li>
</ul>
Versión 1.2 Mejoras
<ul>
<li>Solucionado el problema al guardar excel en Windows (La solución se encuentra en la <a href='http://code.google.com/p/distribucion-alimentos/wiki/Instalacion#Instalación_en_windows:'>WIKI</a>)</li>
<li>Solucionado el problema al subir un backup.</li>
</ul>