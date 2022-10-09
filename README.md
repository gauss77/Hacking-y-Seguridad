# Hacking y Ciberseguridad

## Metodologías de Hacking Ético

Las metodologías son importantes porque nos facilitan la realización de un conjunto de actividades en un **orden** determinado y estableciendo una prioridad adecuada para intentar garantizar el éxito y alcanzar un objetivo final.

Esto es muy importante a la hora de realizar un hacking ético, ya que en el camino nos encontraremos con muchas técnicas, herramientas y fases, es por esto fundamental que sigamos un orden, el output de una fase se corresponde con el input de la siguiente, al seguir un orden nos aseguramos el tener éxito al finalizar el ejercicio. De esta manera nos aseguramos de tener en mente una estructura que nos diga que fases vamos a seguir, que herramientas vamos a utilizar, en que orden vamos a utilizarlas, en que vamos a priorizar cuando obtengamos resultados específicos, etc.

### Principales Metodologías

* OSSTMM (Open Source Security Testing Methodology Manual): https://www.isecom.org/OSSTMM.3.pdf

* The Penetration Testing Execution Standard (PTES): http://www.pentest-standard.org/index.php/Main_Page

* ISSAF (Information Systems Security Assessment Framework)

* OTP (OWASP Testing Project)

Estas son las metodologías principales, pero, es importante que sepamos que seguir una metodología al pie de la letra no es útil si no se adapta a nuestro estilo propio de trabajo, siempre debemos buscar algo que se adapte a nosotros y que podamos integrar a nuestro día a día, de lo contrario podemos abrumarnos al ver lo extenso que puede llegar a ser un documento de alguna de estas metodologías, es importante tener un equilibrio entre el documento formal y la practicidad.

## Metodología Básica

- ``Definición del alcance del test de penetración``: fase en la cual participa el cliente, es en donde se definen los requerimientos.
- ``Recopilación de información:`` Se divide en 3 sub fases: recopilación pasiva de información, recopilación semi pasiva de información y recopilación activa de información.
- ``Identificación y análisis de vulnerabilidades``
- ``Explotación de las vulnerabilidades:`` Se divide en 3 sub fases: explotación ed vulnerabilidades en host, explotación de vulnerabilidades en aplicaciones web y explotación de vulnerabilidades en redes.
- ``Post-explotación``
- ``Elaboración de un documento de informe``

### Definición del alcance del test de penetración

Antes de realizar cualquier acción debemos ``discutir con el cliente las tareas`` que llevará a cabo el analista durante el test de penetración, así como los ``roles y responsabilidades`` de ambos.

También es importante ``asegurar mediante un contrato firmado`` que las acciones que se llevaran a cabo son en representación del cliente.

Debemos analizar las políticas del la organización las cuales definen el uso que pueden hacer los usuarios de los sistemas e infraestructura de la organización.

Es importante definir un procedimiento en el caso de que se localice una intrusión por parte de un tercero.

### ¿Cómo es un informe real de hacking ético o auditoria de seguridad?

Debemos tener en cuenta que los informes de un hacking ético y auditoria de seguridad dependen mucho de la organización que los realiza y del tipo de auditoria que se ha llevado a cabo, No todas las auditorias son completas y siguen todas las fases antes mencionadas, en algunas ocasiones se centran en fases o entornos específicos dentro de la infraestructura tecnológica de una organización. Todo esto se debe concretar en la fase de definición del alcance.

- ``Recursos para la elaboración de un informe de hacking ético o auditoria de seguridad``: 
  - https://github.com/juliocesarfort/public-pentesting-reports. Recopilación de informes de auditorias reales de diferentes empresas.
  - https://pentestreports.com/templates/. Plantillas para la elaboración de informes de hacking ético.
  - https://github.com/hmaverickadams/TCM-Security-Sample-Pentest-Report

## Recopilación pasiva de información

Una de las primeras fases es la de recopilación de información, esta fase podemos dividirla en 3 sub fases: recopilación pasiva de información, recopilación semi pasiva de información y recopilación activa de información, el objetivo de estas 3 fases es tratar de obtener toda la información posible sobre nuestro objetivo, si estamos realizando un test sobre una organización determinada, entonces en esta fase nuestro objetivo es obtener toda la información que podamos sobre la infraestructura tecnológica de la organización de manera que facilite las siguientes fases del proceso de hacking ético. Todas las fases se van construyendo en base a los hallazgos de la fase anterior.

### Recopilación pasiva de información

La recopilación pasiva de información como su nombre lo indica consiste en recopilar toda la información que se pueda obtener sobre nuestro objetivo interactuando lo mínimo posible con el.

- Recolección de información sobre un objetivo determinado sin que las actividades realizadas por el analista `sean mínimamente detectadas` por dicho objetivo.

Por ejemplo, no intercambiaremos tráfico de red con el objetivo, es por esto que en esta fase hacharemos mano de recursos OSINT (Open Source Intelligence).

- Difícil de realizar y a menudo proporciona resultados poco concluyentes.

- La manera habitual de recolección pasiva de información es mediante el acceso a la `información almacenada en lugares públicos`

- Raramente se utiliza de manera individual.

## Hacking con buscadores: Google Hacking

Podríamos llegar a pensar, ¿porque ponemos la palabra hacking si tan solo estamos usando el buscador de google para recopilar información?, resulta que todos lo buscadores nos proporcionan alguna herramientas avanzadas, una serie de comandos o palabras clave que nos permiten construir consultas mas avanzadas de las que solemos hacer comúnmente, con esto podemos encontrar información muy específica sobre nuestro objetivo la cual está publicada en internet y que estos buscadores han indexado.

Por lo general se utiliza google ya que es el buscador que mas información indexa, pero también podemos utilizar otros buscadores como Bing, yahoo, duckduckgo, etc.

Algunos de los comandos mas utilizados son:

La sintaxis común de los comandos es `comando` `:` `consulta`

- ``site:`` Nos permite buscar información sobre un dominio en concreto.

Todos los resultados serán de ese dominio en concreto.

Ejemplo: ``site:google.com``

- ``filetype:`` Nos permite buscar información sobre un tipo de archivo en concreto.

Ejemplo: ``site:google.com filetype:pdf``

o ``site:google.com filetype:txt``

Nos devolverá todos los archivos pdf que se encuentren en el dominio google.com

Existen varios, su nombre técnico es ``Google Dorks``.

Podemos usar los comillas dobles ``""`` para hacer una búsqueda exacta de una frase en concreto.

Por ejemplo: ``"index of" / "chat/logs"``

Este tipo de búsqueda, por ejemplo, nos devuelve logs de algunos chats los cuales pueden ser de alguna organización en concreto, tan solo debemos usar el comando ``site:`` para buscar información sobre ese dominio en especifico, y podríamos encontrar chats que de alguna forma se han dejado públicos en internet, lo cual puede ser un punto de entrada para un ataque.

Por ejemplo: ``"index of" / "chat/logs" site:google.com``

Un dork muy típico es buscar dumps o volcados de bases de datos sql de alguna organización, esto se puede hacer de la siguiente manera:

- ``filetype:sql "MySQL dump"``

Podemos reemplazar el comando ``filetype:`` por ``ext:``

- ``ext:sql "MySQL dump"``

- ``ext:sql "MySQL dump" (password|pass|passwd|pwd)``. Nos devuelve los dumps de bases de datos sql que contienen la palabra password, pass, passwd o pwd.

Con este tipo de dork por lo general encontramos resultados en páginas como Github, GitLab, Bitbucket, etc. con archivos en donde se pueden haber dejado volcados de bases de datos con contraseñas, nombres de usuarios, etc.

Si nosotros quisiésemos buscar una aplicación web con una url especifico y queremos buscar una parte de esa url podemos usar el comando ``inurl:``

- ``inurl:index.php?id=``

Con esta búsqueda podemos encontrar un url la cual podemos, por ejemplo, para hacer sql injection.

Por ejemplo: ``website.com/index.php?id=' or '1'=='1'--``

Si no hay una santificación correcta de los valores que recibe el parámetro id, lo que puede pasar es que mediante una sql injection podemos acceder al contenido de la base de datos de esa aplicación web.

Otro dork común es:

- ``site:gov ext:pdf allintitle:restricted``

Esta búsqueda nos devuelve todos los archivos pdf que se encuentran en dominios .gov y que contienen la palabra restricted en el titulo, podríamos encontrar documentos con información que debería ser restringida.

Debemos recordar que la información que recabamos mediante este tipo de herramientas es información que nos sera útil en las fases posteriores.