
## 3.1. Terminología del modelo relacional

En este módulo pasaremos del modelo entidad-relación, que es más gráfico, al modelo relacional, que es un formato escrito donde ya se puede leer para diseñar las tablas. En este nuevo modelo la terminología cambia un poco, por lo que hay que estar pendientes para no confundirnos.

Terminología:

- Tupla: Son los registros o las filas.
- Atributo: Son los títulos de las columnas; por ejemplo: nombre. En ER esto correspondía a los campos.
- Dominio: Es el tipo de datos que tiene el atributo; por ejemplo, Edad es de tipo numérico.
- Grado: Es el número de atributos que tiene una relación.
- Cardinalidad: El número de registros de la relación.
- BD relacional: Conjunto de relaciones normalizadas.

## 3.3. Atributos y dominio de los atributos

Cada atributo tiene su dominio y debe aceptar un solo tipo de valor; por ejemplo, un dominio no puede mezclar caracteres y valores numéricos. Además, no puede haber dos atributos con el mismo nombre; también, si una entidad tiene cuatro atributos no puede haber un registro con cinco atributos.

## 3.4. Concepto y tipos de clave: candidatas, primarias, ajenas, alternativas

Un registro debe identificarse de manera única por al menos un atributo o por varios; a esto lo llamamos clave. Una clave primaria puede ser de dos tipos:

- Clave simple: El registro se identifica con un único atributo.
    
- Clave compuesta: El registro se identifica por varios atributos combinados.
    
- Clave primaria: Puede ser de un atributo o compuesta; debe ser única y no puede ser NULL. Si la entidad tiene varias opciones, el diseñador decidirá cuál será la clave primaria.
    
- Clave candidata: Son los atributos que pueden optar a ser la clave primaria.
    
- Claves alternativas: Son las candidatas que no fueron elegidas como clave primaria, pero que podrían serlo.
    
- Claves ajenas (o foráneas): Son claves primarias de otra tabla.
# 3.5. Valores nulos

Los valores nulos se supone que no se utilizan, pero en la práctica sí se utilizan; no se pueden confundir con 0, ya que 0 sí es un valor. Podemos decir que un null es ausencia de valor.

## 3.6. Reglas de integridad: de entidad y referencial

Ya lo mencionamos anteriormente: hay dos reglas de integridad que hay que cumplir, una corresponde al sistema de base de datos y la otra a los usuarios. A continuación detallamos estas reglas.

Reglas de integridad de la entidad:

- Ninguna clave primaria puede ser null.
- Después de la modificación se debe mantener la integridad de la entidad.

Reglas de integridad referencial:

Aquí tenemos 3 reglas:

- La clave foránea debe coincidir con una clave primaria existente o ser nula.
- Las modificaciones no pueden violar la integridad; en caso contrario, deben corregirse o rechazarse.
- Si la clave foránea es nula, la participación no es obligatoria.

# Restringido

Una clave primaria no puede ser borrada si es clave foránea en otra tabla.

# Transmisión en cascada

Si borramos una clave primaria que sea clave foránea en otras tablas, ésta se borrará en todas las tablas donde esté referenciada.

# Puestas a nulos

Si borramos la clave primaria, allí donde esté como clave foránea quedará un null.

## 3.7. Traducción del modelo entidad-relación al modelo relacional

En este apartado entraremos en la transformación del modelo ER a un modelo relacional. Recordemos que la terminología cambia un poco: las entidades serán tablas, los atributos serán columnas de esas tablas, la clave será la clave primaria de la tabla y los atributos derivados también serán columnas de esas tablas.

Recordemos que en el modelo entidad-relación tenemos 3 casos que se pueden transformar:

- De 1 a 1
- De 1 a N
- De M a N

En base a estos casos podemos convertir el modelo entidad-relación a un modelo relacional.

- Cuando las participaciones son (1,1) y (1,1)

![[Pasted image 20260117120248.png]]

Este es el caso de participaciones uno a uno: se puede elegir cuál será la clave primaria de la tabla según te convenga. Lo normal es que se haga en una sola tabla, pero también se puede hacer en dos tablas sin problema.

Ejemplo:

Entidad_AB(Atributo_PK, AtributoA2, AtributoB1_FK, AtributoB2)

Entidad_A(Atributo_PK, AtributoA2, A, AtributoB1_FK) Entidad_B(AtributoB1_PK, AtributoB2)

- Cuando las participaciones son (0,1) y (1,1):

![[Pasted image 20260117121815.png]]

Esto se hace en dos tablas y siempre la tabla 0,1 hereda la clave primaria de 1,1

Ejemplo:

Entidad_A(AtributosA1_PK, AtributosA2, AtributosB1_FK) Entidad_B(AtributosB1_PK, AtributosB2)

- Y, por último, cuando las participaciones son (0,1) y (0,1):
![[Pasted image 20260117123221.png]]

Aquí ocurre algo curioso: como las participaciones son 0,1 y 0,1, puede crearse una tercera tabla que lleve las claves de las dos tablas, una como clave primaria o ambas como claves foráneas.

Ejemplo:

Entidad_A(AtributosA1_PK, AtributosA2) Entidad_B(AtributosB1_PK, AtributosB2) Entidad_AB(AtributosA1_FK, AtributosB1_FK)

- Cuando las participaciones son (1,1) y (1,n):
![[Pasted image 20260117125212.png]]
Está fácil, ya que se crean dos tablas donde 1,n hereda de 1,1.

Ejemplo:

Entidad_A(AtributosA1_PK, AtributosA2) Entidad_B(AtributosB1_PK, AtributosB2, AtributoA1_FK)

- Cuando las participaciones son (0,1) y (1,n):
![[Pasted image 20260117125908.png]]
Esta se podría decir que es la más complicada: se crea una tercera tabla con las claves primarias de ambas tablas y en esta se debe elegir una de esas claves como primaria. Es similar a 0,1 y 0,1, pero aquí ninguna es foránea exclusivamente; una actúa como primaria y la que debe ser clave primaria siempre es 1,n.

Ejemplo:

Entidad_A(AtributosA1_PK, AtributosA2) Entidad_B(AtributosB1_PK, AtributosB2) Entidad_AB(AtributosB1_PK_FK, AtributosA1_PK_FK)

- 3.7.3. Caso de cardinalidad tipo N:M
![[Pasted image 20260117131711.png]]

Esta es simple: se crea una tercera tabla, donde esta tercera tabla tiene las dos claves primarias formando una clave compuesta.