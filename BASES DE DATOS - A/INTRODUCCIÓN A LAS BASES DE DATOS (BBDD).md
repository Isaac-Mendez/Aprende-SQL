La definición de base de datos básicamente es una serie de datos que están agrupados y organizados para su fácil consulta.

# 1.1. Evolución histórica de las BBDD

La base de datos no es una novedad de la sociedad moderna; desde los sumerios ya se empleaba gestión de datos, colocando en tablas la recogida de trigo y el registro de transportes con animales.

## 1900 - 1950

Incluso en épocas tan duras como la Segunda Guerra Mundial los datos jugaron un papel importante; en ese periodo se desarrolló la máquina de Turing como concepto de máquina lógica y se usaron sistemas con tubos de vacío.

## Años 60

En estos años se creó el sistema de batch processing, lo que supuso un cambio de paradigma: ya no era necesario depender constantemente de la máquina para procesar tareas.

## Años 70

En esta década Edgar F. Codd publicó el modelo relacional; a partir de ello surgieron sistemas como Oracle y el modelo entidad-relación, que facilita el diseño de bases de datos.

## Años 80

En los años 80 se trabajó en la estandarización y se consolidó un lenguaje universal: SQL.

## Años 90

A principios de los 90 las bases de datos ya estaban popularizadas en las empresas, lo que impulsó el desarrollo de sistemas gestores de bases de datos (SGBD).

Aquí Microsoft creó Microsoft Access.

## Años 2000 y adelante

Debido a limitaciones de los modelos tradicionales, surgieron conceptos como el TAD (Tipo Abstracto de Datos), relacionado con la programación orientada a objetos.

# 1.2. Ventajas e inconvenientes de las BBDD

## Ventajas

- La información almacenada en la base de datos se guarda de forma independiente, reduciendo la redundancia de los datos.
- A partir de una pequeña cantidad de datos se puede extraer mucha información útil.
- Se asegura la integridad de los datos y resultados coherentes.
- Posibilidad de una alta seguridad.

## Desventajas

- El mantenimiento debe hacerlo personal cualificado.
- La inversión inicial es mayor que en otras soluciones, como el papel.
- Se requiere bastante memoria en el equipo.

# 1.3. Almacenamiento de la información

En el almacenamiento de una base de datos utilizamos ficheros —también llamados archivos—; éstos se guardan de manera binaria siguiendo una estructura lógica determinada.

## Tipos de ficheros

Estos se pueden identificar según el tipo de acceso que permitan.

- Fichero de texto plano: se caracteriza por tener un registro continuo; para acceder a él suele ser necesario recorrer todo el contenido de principio a fin.
- Fichero indexado: se divide en dos partes: índice y registro; con el índice se accede directamente al registro correspondiente.
- Fichero de acceso directo: se prescinde del recorrido secuencial y se accede directamente a la dirección física del registro.
- Otros: aquí se incluyen, por ejemplo, ficheros hash que usan algoritmos de mapeo.

## Operaciones básicas de un fichero

- Abrir (open): prepara el fichero para operaciones de lectura y escritura.
- Cerrar (close): cierra el fichero.
- Leer (read): lee el contenido del fichero.
- Escribir (write): escribe en el fichero.
- Posicionarse (seek): posiciona el puntero para la operación de lectura o escritura.
- Fin de fichero (eof): marca el fin del fichero.

## Conceptos clave de las BBDD

Conceptos que se utilizan en la base de datos:

- Datos: Expresan información concreta sobre algo específico. Ejemplo: la edad es un dato.
- Tipo de datos: Indica la clase de dato; por ejemplo, la edad es un tipo de dato numérico.
- Campo: Identificador o atributo; ejemplo: nombre, apellido, edad.
- Tabla: Conjunto formado por varios campos y registros; ejemplo: la tabla "persona" con los atributos nombre, apellidos, edad, donde cada registro es una persona.
- Registro: También llamado tupla; es la agrupación de los datos de una fila. Ejemplo: Isaac, Méndez, 31.
- Campo clave: Es el dato que se usa para identificar un registro de manera única.
- Consulta: También llamada query; sirve para consultar, agregar, actualizar o eliminar datos, entre otras operaciones.
- Índice: Estructura que agrupa o referencia campos clave para facilitar su localización.
- Vista: Estructura que engloba campos de una o varias tablas.
- Informe: Listado que organiza campos y registros en un formato que facilita su lectura.
- Script: Conjunto de comandos o funciones que se pueden ejecutar dentro de la base de datos.
- Procedimiento: Similar a una función, pero no necesariamente devuelve un valor.

## Tipos de BBDD

En este punto organizaremos las bases de datos según cómo están estructuradas internamente:

- Jerárquicas: Se organizan como un árbol donde el nodo principal tiene mayor jerarquía y las ramificaciones dependen de él.
- En red: Se organizan en una red de nodos conectados entre sí, donde cada nodo puede relacionarse con varios pares.
- Relacionales: Formadas por tablas que están relacionadas entre sí.
- Orientadas a objetos: Organizadas por objetos que pertenecen a una clase.

# 1.4. Sistemas gestores de bases de datos (SGBD)

Los sistemas de bases de datos están diseñados para facilitar al usuario la administración de los datos.

## Funciones, componentes y tipos

En esta primera parte vemos que las funciones de la base de datos tienen 3 tipos:

- Definición: Aquí especificamos los tipos de datos, la estructura de la base de datos y establecemos restricciones.
- Construcción: Es el proceso de almacenamiento de los datos.
- Manipulación: Es la gestión de los datos y la realización de consultas sobre los datos almacenados.

## Según su capacidad y ponencia

En este apartado podemos decir que hay dos:

- SGBD ofimáticos: Son los domésticos, utilizados por pequeñas empresas (por ejemplo, Excel).
- SGBD corporativos: Son los utilizados por grandes empresas (por ejemplo, Oracle).

## Licencia de uso

Aquí tenemos dos categorías:

- Licencia comercial: En esta licencia una empresa posee los derechos del software y el usuario no puede modificar el código ni acceder a él.
- Licencia pública: En esta licencia el usuario tiene acceso al código, puede modificarlo y también comercializarlo.

## Ejecutivo de SGBD

Los SGBD son sistemas que brindan al usuario herramientas para manipular los datos y realizar tareas, teniendo en cuenta su seguridad.

Entre las herramientas que ofrecen los SGBD para garantizar seguridad e integridad tenemos las siguientes:

- Creación y especificación de los datos: creación de la estructura requerida en cada unidad.
- Manipulación de los datos en la base de datos: operaciones de inserción, eliminación y consulta de datos.
- Recuperación de los datos: realización de copias de seguridad.

## Tipos de usuarios en la base de datos

Aquí tenemos dos categorías:

- Informáticos: pueden diseñar la base de datos, además de añadir y consultar datos.
- No informáticos: no acceden directamente a la base de datos; su interacción es mediante formularios.

## Administración de la Base de Datos (BDA) — funciones y responsabilidades

La BDA se refiere al rol del administrador de la base de datos, que realiza funciones como:

- Definir estatura (tamaño) 
- Definir espacio en memoria.
- Modificar los parámetros anteriores.
- Asignar permisos a otros usuarios.
- Establecer restricciones.

## Tipos de lenguajes de BBDD

Tenemos 4 tipos de lenguajes en la base de datos, cada uno para tareas distintas:

- DDL: se utiliza para crear la estructura de datos.
- DML: se utiliza para manipular los datos, como insertar, actualizar y eliminar.
- DCL: permite controlar los permisos.
- TCL: administra las transacciones en la base de datos; usa COMMIT para guardar y ROLLBACK para deshacer lo realizado.

## Diccionario de datos; conceptos, contenido, tipos y uso

Es el lugar donde se deposita la información referente a la base de datos. Además, el diccionario de datos ofrece información sobre la estructura lógica y física de la base de datos.

Por otro lado, tenemos dos tipos de diccionario de datos:

- off-line: su función es mantener el diccionario.
- on-line: funciona como un compilador.

# 1.5. ANSI/X3/SPARC. Estándares y niveles

En su momento se intentó crear un diseño abstracto para estandarizar los sistemas de bases de datos y esta estructura se basa en tres niveles:

- nivel externo o de visión: es el nivel para el usuario; aquí el usuario sólo puede ver lo que se le permite.
    
- nivel conceptual: en este nivel se define la estructura que se va a utilizar en la base de datos y las interrelaciones que existen entre los datos.
    
- nivel interno o físico: en este nivel se organiza el almacenamiento de la base de datos.
    

## 1.6. Modelos de BBDD. Tipos: jerárquico, red, relacional y orientado a objetos

Este punto ya se tocó antes en tipos de datos, pero aquí lo profundizaremos un poco más.

Los modelos de bases de datos organizan el almacenamiento de los datos y también su lógica; los más destacados son los siguientes:

Jerárquico: tiene forma de árbol invertido y utiliza herencia. ![[Pasted image 20260116071743.png]]

En red: este modelo son nodos que se enlazan entre sí; aquí no hay herencia. ![[Pasted image 20260116071939.png]]

Modelo relacional: organiza la información en entidades y duplas o filas para evitar la redundancia.

Modelo entidad-relación (ER): es el que todos conocemos y que hemos venido explicando.

Modelo entidad-relación extendido: es el mismo, pero con menos limitaciones.

Modelo orientado a objetos: en este modelo se utilizan tanto la herencia como los objetos.

## Regla de integridad de los datos

Los SGBD deben garantizar la seguridad de los datos; de lo contrario la base de datos sufrirá pérdida de información. Por ello hay dos reglas de integridad que se deben seguir:

- Regla de integridad del sistema: Asegura que el sistema de gestión de bases de datos elegido funcione correctamente y no presente problemas de seguridad ni de integridad.
    
- Regla de integridad del usuario: El usuario debe operar correctamente el SGBD para evitar pérdida de datos y, en caso de producirse, saber cómo recuperar la información.
    

## Modelo distribuido: ventajas e inconvenientes, técnicas de fragmentación, distribución de datos y esquemas de asignación y replicación de datos

Resumen del módulo: una base de datos distribuida es aquella en la que varias máquinas (nodos) se unen para cumplir un objetivo común. Tiene ventajas y desventajas: ventajas como mayor rapidez y rendimiento; desventajas como posibles vulnerabilidades. También existe el concepto de fragmentación, que es cómo se divide la información: fragmentación horizontal (por filas), vertical (por atributos) y mixta (combinación de ambas).

## 1.7. Bases de datos centralizadas y distribuidas

Base de datos centralizada (BDC)

Una base de datos centralizada es una base de datos localizada que no interactúa con otras bases de datos. Esto conlleva ventajas y desventajas.

Ventajas:

- Seguridad elevada.
- Menos problemas de integridad.
- Rendimiento óptimo al procesar menos datos.
- Posibilidad de aplicar restricciones.

Desventajas:

- Recuperación más complicada.
- No permite compartir tareas entre nodos.
- Si el sistema falla se puede perder toda la información.
- El computador es más costoso que el papel.

Base de datos distribuida (BDD)

Una base de datos distribuida es aquella que se encuentra en una red formada por nodos interconectados; cada nodo está relacionado con los demás y, a la vez, es independiente. Esto presenta ventajas y desventajas.

Ventajas:

- Acceso rápido
- Mejora la comunicación
- Mejor organización
- Al ser en red, las modificaciones (insertar, borrar, etc.) son más rápidas y eficientes
- Bajo coste para crear una red pequeña

Inconvenientes:

- Diseño más complejo
- Aumenta el riesgo de seguridad
- Recuperación más compleja

## Componentes: hardware y software

A nivel de componentes, en una base de datos distribuida se utiliza más hardware, ya que se requieren varios ordenadores; en cuanto al software, se necesita un sistema que coordine la comunicación entre los nodos.

Distribución de los datos

Para distribuir los datos hay cuatro maneras:

- Centralizada: similar al modelo cliente-servidor
- Replicada: se duplica la información
- Particionada: se almacena una porción de los datos en cada nodo
- Híbrida: combina replicación y particionamiento


