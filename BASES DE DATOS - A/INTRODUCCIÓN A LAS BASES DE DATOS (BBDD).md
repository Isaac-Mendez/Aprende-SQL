
La definición de base de datos básicamente es una serie  de datos que están agrupados y acomodados para su fácil consulta

# 1.1. Evolución histórica de las BBDD

La base de datos no es una novedad de la sociedad moderna ya que desde los sumerios ya utilizaban gestión de bases de datos donde en tablas colocaban la recogidas de trigo y traslaciones con animales 

## 1900 - 1950

También en las peores época como pudo ser la segunda guerra mundial los datos jugaron un papel importante ya que para esas épocas se creo la maquina de turing que es la primera maquina lógica utilizando un sistema de tubos de vacío 

## Años 60 

En estos años se creo el sistema de (batchprocessing) y esto era un cambio de paradigma ya que con la creación de este sistema ya no había que estar pudiente de la maquina 

## Años 70 

En este año el señor Edgar Frank publica el modelo relacional y de allí se crea la BBDD Oracle y aparece el entidad-relación que facilita el diseño de BBDD

## Años 80 

Pues aquí se decide estandarizarlo y se creo un lagunaje universal que en este caso es SQL 

## Años 90 

A principio de los 90 ya las BBDD ya están popularizadas por todas las empresas entonces empezaron a crear los sistema de gestión de bases de datos (SGBD) 

Aquí Microsoft creo Microsotf Acces

## Años 2000 y adelante

Debido a las limitaciones que daba las bases de datos se creo el TAD que es: Tipo Abstracto de datos que básica mente es programación orientada a objeto 

# 1.2. Ventajas e inconvenientes de las BBDD

## Ventajas 

- La información que se guarda en la base de datos se guarda de forma independiente y de esta manera se reduce la refundación de la información
- Mediante la información que se guarda se puede sacar la mayor información partiendo de una pequeña cantidad de datos 
- Se asegura la integridad de los datos y resultados coherente 
- Posible de una gran seguridad 
## Desventajas 

- El mantenimiento lo tiene que hacer alguien que sepa 
- La inversión inicial es mayor que otras como el papel 
- Se necesita bastante memoria en la computadora 

# 1.3. Almacenamiento d e la información

En el almacenamiento de una base de datos utilizamos ficheros que también podemos decirle archivos, esto lo guarda de una manera binaria siguiendo una estructura logia determinada 

## Tipos de ficheros 

Estos se puede identificar según  el acceso que tenga.

- Fichero de texto plano: Este se caracteriza por tener un registro continuo ósea que para acceder a el se tiene que recorrer todo el registro para de principio a fin 


- Fichero indexado: Este se divide en dos forma: índice y registro; con esto si se tiene el índice se lleva al registro directamente 

- Fichero de acceso directo:  En este se prescinde del registro por lo que se va directo a la dirección física del registro 

- Otros:  Aquí conseguimos otros como los ficheros hash que un algoritmo de encriptación

## Operaciones básicas de un fichero


- Abrir (Open): prepara el fichero para su posterior operación Lectura y escritura  
- Cerrar(Close): Cierra el fichero 
- Leer(read): Lee el fichero
- Escritura(write): Escribe en el fichero
- Posicionarse(seek): posiciona el puntero para su operación ósea la escritura o lectura 
- Fin de fichero(eof): Marca el fin de fichero

## Conceptos clave de las BBDD

Conceptos que se utiliza en la base de datos: 

- Datos: Expresa una información concreta de algo especifico. Ejemplo la edad es un dato
- Tipo de datos: Es el tipo de dato que esta escrito un ejemplo es que edad es un tipo de dato numerico
- Campo:  El campo un identificador o un atributo ejemplo; nombre, apellido, edad. 
- Tabla: La tabla esta creada por varios campos y registro ejemplo; se crea la tabla persona con los atributos; nombre, apellidos, edad y cada registros es una persona
- Registro: también se le dice dupla y es la agrupación de los datos de una fila ejemplo: Isaac, Mendez, 31
- Campo clave: Es el datos que se toma para identificar el registro de manera única
- Consulta: También se le llama query y se utiliza para consultar datos, agregar datos actualización de datos, eliminación de datos y otros 
- índice: Es una estructura que agrupa los campo claves para poderlo ubicar mas fácil
- Vista: Es una estructura que engloba todos los campos de una tabla o de otras 
- informe: es un listado que agrupa campos y registro en un formato que facilita su lectura 
- Script: son funciones que se puede hacer dentro de la base de batos 
- Procedimiento: Es parecido al la función pero no devuelve nada  

## Tipos de BBDD

En este punto organizaremos las bases de datos según como están organizadas por dentro:

- Jerárquicas: Esta se organizan como fuera un árbol de pero al inversa donde el primero es el que tiene mas poderes y todas las ramificaciones depende de esta principal 

- En Red: Esta esta organizada por red unidas por nudos donde cada nudos esta relacionados con el de la par 

- Relaciones: Esta esta formada por tablas que están relacionadas entre si 

- Orientada a objeto: Esta esta organizadas por objetos que pertenecen a una clase  

# 1.4. Sistemas gestores de bases de datos (SGBD)

Los sistema de base de datos están creados para facilitar al usuarios la administración de dichos datos 

## Funciones componente y tipos

En esta primera parte vemos que las funciones de la base de datos tiene 3 tipos: 

- Definición: Aquí especificamos los tipos de datos, la estructuración de base de datos y ponemos restricciones

- Construcciones: Es el proceso de almacenamiento de los datos 

- Manipulación: Es la manipulación de los datos y las consultas de los datos almacenados 