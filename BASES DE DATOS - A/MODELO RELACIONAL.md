
## 3.1. Terminología del modelo relacional

En este modulo lo que haremos es pasar de entidad relación que es un formato mas de diagrama a un modelo relacional que es un formato escrito donde ya se puede leer para realizar las tablas 
en este nuevo modelo la terminología se cambia un poco por lo que hay que estar pendiente para no confundirnos 

Terminología: 

- Tupla:  Son los registros o las filas. 

* Atributos: Son los títulos de las columnas, ejemplos nombre. Esto en ER era los campos

- Dominio: Es el tipo de datos que tiene el atributo ejemplo; Edad es un tipo numérico

 - Grado: El es numero de atributos que tiene una relación

- Cardinalidad: el numero de registro de la relación

- BD relacional: Conjunto de relaciones normalizadas 


## 3.3. Atributos y dominio de los atributos

Cada atributo tiene su dominio que tiene que ser de un solo valor ejemplo un dominio no puede tener caracteres y tipo numérico

Ademas no puede a ver dos atributos no pueden tener el mismo nombre también si una entidad tiene 4 atributos no puede a ver un registro con 5 atributos 

## 3.4. Concepto y tipos de clave: candidatas, primarias, ajenas, alternativas

Como ya comentamos antes un registro se tiene que identificar de manera única por mínimo un atributo o por varios, a esto de decimos clave primaria. Una clave primaria puede tener dos categorías que son: 

- Clave simple: Que es una registro que se identifica con un atributos 
- Clave compuesta: Que es cuando el registro se identifica por varios atributos compuesto.

- Clave primaria: 
Puede ser de un atributo o compuesto, tiene que ser único, no puede ser un null  la entiedad tiene varios  el programador sera el que decida quien sera la clave primaria        

 - Clave candidata:
Las los atributos que optan por ser la clave primarias 
- Claves alternativas:
Son las que no son elegidas para ser claves primarias pero que podria ser claves primaria 
- Claves ajenas (o foráneas):
Son claves primarias de otra tabla 

# 3.5. Valores nulos

Los valores nulos se supone que no se utilizan pero en la practicas si que utilizan, estos no se puede confundir con 0 por que 0 si es un valor por lo que podemos decir que un null es ausencia de valor 

## 3.6. Reglas de integridad: de entidad y referencial

en esto ya hicimos mención anteriormente y dijimos que hay dos regla de integridad que hay que cumplir uno que le correspondia al sisteme de base de datos y la otra a usurios, aqui detallemos estas regla de integridad

Reglas de la integridad de la entidad: 
- Niguna clave primaria puede ser null
- Despues de la modificación se hará una modificación

Reglas de la integridad referencial:

Aqui tenemos 3 reglas: 
- La clave foránea tiene que concidir con la clave primaria o ser nula
- La modificaciones no puede violentar la integridad de lo contrario se tiene que modificar o rechazar 
- Si la clave forania es nula la partificipacion o es obligatoria 

# Restringido

Una clave primaria no puede ser borrada si es clave forenea en otra tabla 

# Transmisión en cascada

Si borramos una clave primaria que sea una clave foreane en otras pues esta se borrar en todas las tablas que este puesta 

# Puestas a nulos

Si borramos la clave primaria en donde este como clave forenea alli quedara un null 

## 3.7. Traducción del modelo entidad-relación al modelo relacional

En este apartado ya entramo a la transformacion de modelo ER a un modelo Relacional, recordemo que la terminologia cambia un poco porque la entidades seran tablas los atributos sera atributos de esas tablas, tambien la palabra clave, para a ser las clave primaria de esa tabla y los atributos son columnas de esa tabla y los atributos derivados tambien son columnas de esas tablas 

Recordemos que los modelo entidad-relacion tenemos 3 casos que se pueden pasar 

- De 1 a 1
- De 1 a N
- De M a N

En base a estos casos podemos cambiar el modelo Entidad-Relacion a un modelo relacional 

- Cuando las participaciones son (1,1) y (1,1):

![[Pasted image 20260117120248.png]]

Este se  las participaciones es de uno a uno se puede elegir cual sera la clave primaria de la tabla según te convenga, lo normas es que se haga en una sola tabla pero también lo puede hacer en dos tablas sin problema 

Ejemplo:

Entidad_AB(Atributo_PK,AtributoA2,AtributoB1_FK, AtributoB2);

Entidad_A(Atributo_PK,AtributoA2,A, AtributoB1_FK)
Entiudad_B(AtributoB1_PK, AtributoB2)


- Cuando las participaciones son (0,1) y (1,1):

![[Pasted image 20260117121815.png]]

Esto se hacen en dos tablas y siempre la tabla 0,1 hereda la clave primaria de 1,1

Ejemplo:

Entidad_A(AtributosA1_PK, AtributosA2,AtributosB1_FK)
Entidad_B(AtributosB1_PK, AtributosB2)

- Y, por último, cuando las participaciones son (0,1) y (0,1):
![[Pasted image 20260117123221.png]]

Aquí pasa algo curioso y es que como las participaciones son 0,1 y 0,1 puedes se crea una tercera tabla pero en esta tercera que lleve las claves de las dos tabla una como clave primaria y si no que las dos claves son foránea


Ejemplo:

Entidad_A(AtributosA1_PK, AtributosA2)
Entidad_B(AtributosB1_PK, AtributosB2)
Entidad_AB(AtributosA1_FK, AtributosB2_FK)

- Cuando las participaciones son (1,1) y (1,n):
![[Pasted image 20260117125212.png]]
Este facil ya que se crea una dos tabla donde 1,n hereda de 1,1

Ejemplo: 

Entidad_A(AtributosA1_PK, AtributosA2)
Entidad_B(AtributosB1_PK, AtributosB2, AtributoA1_FK)

- Cuando las participaciones son (0,1) y (1,n):
![[Pasted image 20260117125908.png]]
Esta se podria decir que es la mas complicada ya se crea un tercera tabla con las clave primarias de hablas y en esta tabla se tiene que elegir una de estas claves como primaria es igual que 0,1 y 0,1 pero aqui las dos no son foranera si no una si es primaria y la que tiene que ser clave primaria siempre es 1,n

Ejemplo: 

Entidad_A(AtributosA1_PK, AtributosA2)
Entidad_B(AtributosB1_PK, AtributosB2)
Entidad_AB( AtributosB1_PK_FK,AtributosA1_FK)

- 3.7.3. Caso de cardinalidad tipo N:M
![[Pasted image 20260117131711.png]]

Esta es simple se crea una tercera tabla donde esta tercera tabla tiene las dos clave primaria haciendo una clave compuesta 