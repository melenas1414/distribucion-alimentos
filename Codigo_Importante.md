# Introducción #

Distinto código a tener en cuenta por su dificultad.


# Detalles #
## 1 crearbackup.php ##

Este código realiza lo siguiente:
<ol>
<li>Se genera primero el head de un archivo sql.</li>
<li>Luego va generando una variable con los insert de cada tabla por medio del siguiente<br>
código, la etiqueta <i><code>&lt;tabla&gt;</code></i> se cambia por cada tabla:<br>
<pre><code>$file.="--\n<br>
-- Volcado de datos para la tabla `&lt;tabla&gt;`\n<br>
--\n";<br>
$consulta="select * from &lt;tabla&gt;";<br>
$sql=buscar($consulta);<br>
while ($row = mysql_fetch_row($sql))<br>
{<br>
$file.="insert into &lt;tabla&gt; values (";<br>
for($i=0; $i&lt; count($row); $i++) {<br>
if ($i+1==count($row))<br>
{<br>
$file.="'".$row[$i]."');\n";<br>
}<br>
else<br>
$file.="'".$row[$i]."',";<br>
}<br>
}<br>
</code></pre>
</li>
<li>Al terminar la variable se imprime con un echo y automáticamente te lo descarga.</li>
</ol>
## 2 reordenar.php ##
Este código permite realizar un reordenado de los usuarios que han sido eliminados, el propio
archivo está comentado y permite un fácil entendimiento del mismo, se puede encontrar en el anexo 5 (de la <a href='http://code.google.com/p/distribucion-alimentos/downloads/detail?name=Proyectodistribuciondealimentos.pdf&can=2&q='>documentación</a>) dentro del código de todas los archivos php.
## 3 subirbackup.php ##
Este código permite respaldar una base de datos, para ello primero llama al procedimiento de
MySQL restore y luego lee cada línea del archivo sql subido, que se encuentra en la carpeta
backups, y las va ejecutando en MySQL.