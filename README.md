# Hacking y Ciberseguridad

## Metodologías de Hacking Ético

Las metodologías son importantes porque nos facilitan la realización de un conjunto de actividades en un **orden** determinado y estableciendo una prioridad adecuada para intentar garantizar el éxito y alcanzar un objetivo final.

Esto es muy importante a la hora de realizar un hacking ético, ya que en el camino nos encontraremos con muchas técnicas, herramientas y fases, es por esto fundamental que sigamos un orden, el output de una fase se corresponde con el input de la siguiente, al seguir un orden nos aseguramos el tener éxito al finalizar el ejercicio. De esta manera nos aseguramos de tener en mente una estructura que nos diga que fases vamos a seguir, que herramientas vamos a utilizar, en que orden vamos a utilizarlas, en que vamos a priorizar cuando obtengamos resultados específicos, etc.

### Principales Metodologías

* OSSTMM (Open Source Security Testing Methodology Manual): https://www.isecom.org/OSSTMM.3.pdf

* The Penetration Testing Execution Standard (PTES): http://www.pentest-standard.org/index.php/Main_Page

* ISSAF (Information Systems Security Assessment Framework)

* OTP (OWASP Testing Project)

Estas son las metodologías principales, pero, es importante que sepamos que seguir un metodología al pie de la letra no es útil si no se adapta a nuestro estilo propio de trabajo, siempre debemos buscar algo que se adapte a nosotros y que podamos integrar a nuestro día a día, de lo contrario podemos abrumarnos al ver lo extenso que puede llegar a ser un documento de alguna de estas metodologías, es importante tener un equilibrio entre el documento formal y la practicidad.

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