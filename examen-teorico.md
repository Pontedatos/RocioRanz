# Examen de Periodismo de Datos

## Rocío Ranz Sánchez, 5º Periodismo y Humanidades, grupo 63

### Preguntas específicas: Bloque C

**1. ¿Cómo creamos un directorio? Si quisiéramos crear dos directorios, ¿podríamos hacerlo de una sola vez? Razona tu respuesta**

En primer lugar debemos tener en cuenta que un directorio es un contenedor virtual en el que se almacenan archivos. Para crear un directorio es necesario introducir el comando <code>mkdir</code>. Encontramos también el indicador <code>-p</code>, que indicará al comando <code>mkdir</code> que cree el directorio principal primero si no existe ya. 

Por otro lado, **sí se puede crear más de un directorio a la vez**. Para crear más de un directorio al mismo nivel únicamente tendríamos que separarlos con espacios, es decir: <code>mkdir primero segundo tercero</code>. Si, en vez de al mismo nivel, quisiéramos crearlos anidados (unos dentro de otros), necesitaríamos del comando <code>-p</code>, que indicaría cuál es el directorio principal que contendrá a los demás. Quedaría así: <code>-p mkdir primero/segundo/tercero</code>. 

Comprobamos que funciona y vemos que cuando mandamos crear carpetas, podemos hacer varias de una vez puesto que si lo hiciéramos por separado simplemente escribiríamos los mismos comandos, solo que uno detrás de otro. Por ello, tiene sentido que se pueda crear a la vez simplemente dejando el espacio.

**2. ¿Cómo vemos los archivos y directorios ocultos al listar un directorio?**

Para visualizar todos los archivos que contiene un directorio utilizamos el comando <code>ls</code>. Teniendo esto en cuenta, para visualizar archivos y directorios ocultos necesitaremos esto y algo más. Es por ello que, para listar los archivos y directorios ocultos se emplea el comando <code>ls -a</code>. Si queremos que esta lista ofrezca más detalle, entonces usaremos <code>ls -la</code>. Los archivos y directorios ocultos contienen configuraciones o datos a los que acceden los programas de ese usuario. No están destinados a ser editados por el usuario, solo por la aplicación Por eso están ocultos de la vista normal del usuario.

**Resumiendo:**

<code>ls</code>: listamos archivos y directorios

<code>ls -a</code>: listamos archivos y directorios ocultos.

<code>ls -la</code>: listamos archivos y directorios ocultos con detalle.

**3. ¿En qué se diferencian las rutas absolutas de las relativas? Pon ejemplos de ambas.**

Llamamos ruta (o path) al lugar donde se localiza un fichero o archivo dentro de nuestro sistema de ficheros, como si fuera su dirección. Existen dos tipos de ruta que debemos diferenciar para aplicar los comandos:

**Ruta absoluta**: se indica toda la ruta del archivo incluyendo el directorio raíz. Por ejemplo, <code>/cygdrive/c/Users/User/...</code>

**Ruta relativa**: se indica la ruta a partir de donde estamos en ese momento situados. No se incluye el directorio raíz. Por ejemplo, si estamos en la ruta <code>/cygdrive/c/Users/User/...</code> (tras hacer pwd la terminal nos lo indicará) y queremos acceder a la carpeta 'practicas-periodismo-de-datos', directamente escribiremos: <code>cd practicas-periodismo-de-datos</code>. Porque ya hemos hecho todo el recorrido de la ruta absoluta para llegar hasta Desktop, el lugar previo a practicas-periodismo-de-datos. 

Otro ejemplo más sencillo: mi ruta absoluta de las prácticas de la asignatura es: <code>/cygdrive/c/Users/User/practicas-periodismo-de-datos</code>. Imaginemos que yo quisiera dirigirme a la carpeta contenida dentro llamada 'practica-4'. Estando ya dentro de la carpeta de las prácticas: <code>cd /cygdrive/c/Users/User/practicas-periodismo-de-datos</code> ya no necesitaría otra ruta absoluta que fuese <code>/cygdrive/c/Users/User/practicas-periodismo-de-datos/practica-4</code> para acceder. Podría simplemente utilizar la ruta relativa: <code>cd practica-4</code> y ya estaría dentro de la carpeta a la que buscaba acceder.


**4. ¿Qué función tiene la almohadilla en Markdown y en un programa de la shell? Razona tu respuesta.**

El mismo carácter cumple con funciones distintas según se trate de Markdown o del programa de la shell.

En los **archivos de configuración de la <code>shell</code>**, sirve para introducir comentarios. La almohadilla (<code>#</code>) que aparece al principio de línea significa que esa línea está comentada y que no va a ser interpretada por la shell. Pueden quedar varias líneas comentadas y son útiles para documentar los pasos que vas dando a lo largo de tu shell script (o guión de shell).

En **Markdown** equivale al elemento <code>h1</code> de HTML o "encabezamiento de primer nivel". Es decir, las almohadillas se utilizan para crear encabezados. Estos pueden ser de distintos tamaños si se siguen agregando almohadillas, de modo que, a mayor número de almohadillas, menor tamaño del encabezamiento (por ejemplo, dos almohadillas, ##,  darían lugar a un encabezamiento de segundo nivel) Asimismo, para usarlo, se debe añadir uno por cada nivel.


**5. ¿Qué es una API. Pon algún ejemplo.**

Las siglas API se refieren a *Access Programming Interface*, es decir, interfaz de programación de acceso. API se refiere a los códigos para comunicarse con la web, o todo el conjunto de protocolos y códigos necesarios para componer y hacer funcionar el *software* de una app. Por ejemplo: HTTP es una API. HTTP, como sabemos, es un protocolo de control de transmisión. Es una de las API más conocidas pero existen muchas más. Aunque HTTP sea universal, cada recurso tiene la suya propia. Véase: Facebook, que hace pocos años se vio obligado a crear una API de código abierto (modelo de *software* basado en la colaboración abierta), para hacer frente a ciertos tipos de publicidades dañinas. 

**6. ¿Qué es Markdown?**

Markdown es un lenguaje. Como hemos aprendido, se trata de una lengua para la edición de textos en aplicaciones informáticas. Markdown surge de la necesidad de "facilitar" el formato HTML de las páginas web, pues este era muy difícil de leer. Será entonces un conversor de HTML puesto que aportará una sintaxis muy simple (por supuesto, no pretende ser un sustituto, simplemente una herramienta o complemento que acerque la sintaxis). Al ser un "traductor" (o conversor, como lo hemos llamado antes), en Github, por ejemplo, se muestra como HTML pero el archivo fuente, que nosotros hemos editado, sigue siendo Markdown. 

**7. ¿Que significa TSV?**

TSV significa *Tab Separated Values*, es decir, valores separados por tabuladores. Se refiere a un formato de textos que almacena los caracteres (o datos) dentro de una forma tabular, en una tabla. Como hemos aprendido, el formato CSV (*Comma separated values* o valores separados por comas) de texto es heredero de TSV ya que ambos guardan los datos en tablas. Por ejemplo: Excel visualiza los datos en formato CSV pues es una herramienta para ver tablas. 

### Preguntas obligatorias:
**1. ¿Quién es Philip Meyer?**

Philip Meyer es un periodista conocido por sus investigaciones acerca de precisión y calidad en el periodismo. Es conocido por haber ejercido la profesión en el periódico *Detroit Free Press*, en el que, en 1967, tras unos disturbios en la ciudad de Detroit, utilizó un ordenador central para demostrar que cualquier tipo de persona podría haber asistido a esa manifestación, es decir, gente con estudios universitarios tenía las mismas posibilidades de haber provocado los altercados que aquellos que no hubiesen acabado la secundaria. Para llevar a cabo este estudio realizó una encuesta con la que pretendía encontrar las causas de los disturbios. Trabajaría con un equipo de dos psicólogos, una programadora informática y 50 entrevistadores. La encuesta llevaría 3 semanas y seguiría el método utilizado por la Universidad de los ángeles para hacer, en 1965, un informe sobre las revueltas en Watts. Él mismo hablaría de que intentó convertir el periodismo en una ciencia. Este caso, junto con el de la CBS, dio lugar al llamado *Computer Assited Reporting* o periodismo asistido por ordenador. 

**2. ¿Quién fue Florence Nightingale?**

Florence Nightingale fue una enfermera, escritora y estadística. Ha sido considerada la pionera de la enfermería moderna y la creadora del primer modelo conceptual de enfermería. Especialmente importante, y razón por la que la estudiamos en esta asignatura, fue su aportación al Periodismo de Datos, pues su trabajo fue visionario en la estadística médica. En el hospital en el que trabajaba en Turquía fue capaz de crear directrices sobre cómo registrar la mortalidad y las enfermedades en los hospitales militares. Estos datos fueron claves para conocer las cifras de muertos y las causas de estas muertes. Crearía un "diagrama de rosas" (imagen incluida más abajo) fácil de comprender que mostraba el fuerte descenso de las muertes tras el trabajo de la Comisión Sanitaria. 

![Diagrama-de-rosas-Florence-Nightingale](https://i0.wp.com/www.thehistorypress.co.uk/media/2034/nightingale-mortality.jpg?w=1220&ssl=1)

### Pregunta de desarrollo

**¿Qué es el periodismo de datos? ¿Cómo se relaciona con la visualización de datos?**

Llamamos periodismo de datos a la rama del periodismo que, combinando diferentes campos como la informática, la estadística, el diseño... etc crea noticias e historias que analizan y estudian en profundidad diferentes tipos de datos específicos. Como hemos estudiado, su origen se encuentra en el periodismo de precisión, así como en el *Computer Asisted Reporting*, que ya hemos mencionado cuando hablábamos de Philip Meyer. El periodismo de datos moderno, del que bebemos actualmente, nace en 2006-2008 con una combinación de factores: abundancia de software de código abierto, HTML5 y Open Data.

Esta rama se compone de tres saberes específicos: el periodismo, por supuesto, capaz de crear las narraciones que se nos vienen a la cabeza cuando pensamos en noticias, reportajes o crónicas, pero también los datos y la visualización, ambos fundamentales. Los datos son aquellos saberes específicos en los que nos apoyamos, ya sean cantidades, cifras, mapas... Todos ellos son precisos y se puede acceder a partir de diferentes herramientas. También es necesario recordar que cuando hablamos de datos no nos estamos refiriendo únicamente a aquellos que, a priori, se presentan estructurados o preparados. También podemos estar hablando de registros electrónicos en los que podemos encontrar datos no estructurados que necesitaríamos tratar: imágenes, vídeos, música... incluso páginas web no estructuradas. 

Pero lo que une a ambos es la visualización. Esta visualización va mucho más allá del producto final (una infografía por ejemplo). La visualización se refiere a todos las técnicas estadísticas, análisis, y programas informáticos que consiguen que seamos capaces de pensar hipótesis o conclusiones hasta llegar a historias de un gran volumen de datos. Por lo tanto, la visualización de datos es la relación fundamental que hace que el periodismo de datos pueda existir, puesto que se trata de la materialización de los datos, aquella que nos permite tratarlos, conocerlos y acercarlos a quien nos lea. 
