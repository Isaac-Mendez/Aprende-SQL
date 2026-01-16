El modelo entidad-relación es un modelo de datos abstracto que nos permite representar de manera conceptual una base de datos.

Antes de crear una base de datos hay que seguir unas fases:

- Recogida de información: aquí recopilamos toda la información necesaria.
- Modelo entidad-relación: con esa información diseñamos el diagrama.
- Modelo relacional: lo transformamos a un modelo entendible para crear las tablas.
- Normalización: organizamos las tablas según una serie de reglas.
- Codificación: creamos las tablas en SQL.

Para resumir, hay que pasar por 3 procesos:

- Conceptual: donde pensamos el proyecto.
- Modelo lógico: hacemos los diagramas y definimos la lógica.
- Modelo físico: donde codificamos.

## 2.2. Entidad: representación gráfica, atributos y tipos de claves

- Entidades Se representan con un rectángulo y deben tener un nombre único.
    
- Atributos Son los datos que tiene una entidad.
    
- Clave primaria Permite identificar una fila de manera única.
    
- Atributo multivaluado Un atributo que puede repetirse varias veces.
    
- Atributo derivado Atributo que puede ser calculado a partir de otros atributos.
    

## 2.3. Relación: representación gráfica, atributos, grado y cardinalidad

- Relación Se utiliza para conectar las entidades y se representa con un rombo; además, la palabra que conecta suele ser un verbo como "tiene".

## 2.4. Diagrama entidad-relación

## Cardinalidad

Número de participaciones de las entidades; encontramos 3 tipos:

- 1:1 Cuando la participación es como mínimo y como máximo una en cada lado.
- 1:N Cuando en un lado la relación es uno y en el otro son muchas.
- M:N Cuando en ambos lados hay muchas participaciones.
## Participaciones

La participación es lo que se coloca sobre la relación y debe ser la máxima de cada lado.

## Entidades fuertes y débiles

- Entidad fuerte: Esta entidad tiene existencia por sí misma y no depende de otra.
    
- Entidad débil: Depende de una relación fuerte para existir; no tiene existencia por sí sola.
    

## Tipos de correspondencias en las relaciones: binaria, reflexiva y otros

- Relación unaria o reflexiva: Es una relación que se refiere a sí misma.
    
- Relación binaria o de grado 2: Cuando se refiere a otra entidad y la otra entidad se refiere a ella.
    
- Relaciones ternarias o de grado 3: Cuando hay 3 entidades.
    
- Relación n-aria: Cuando tenemos más de 3 entidades.
    

# 2.5. Modelo entidad-relación extendido

Hasta ahora solo hemos visto entidades relacionadas solo de forma binaria; para modelar relaciones más dinámicas existe el modelo entidad-relación extendido.

## Generalización/especialización

Estos dos conceptos se pueden definir de la siguiente manera:

- Generalización: Es cuando la entidad comparte atributos generales, es decir, que pueden ser utilizados por cualquiera que comparta esos atributos.
- Especialización: Es cuando la entidad tiene atributos más específicos.

## Inclusiva vs exclusiva o total vs parcial

Vamos a definir cada una de ellas y cómo se combinan entre sí.

- Inclusiva: Se puede decir que es cuando el ejemplar del supertipo puede pertenecer a varios subtipos.

Ejemplo: Un futbolista puede ser defensa, delantero o portero.

- Exclusiva: Es cuando el ejemplar del supertipo solo puede pertenecer a uno de los subtipos; se diferencia por la línea que hay en los subtipos.
    ![[Pasted image 20260116193856.png]]

Ejemplo: Cuando la persona solo puede ser jugador o árbitro, pero no ambos.

Observación importante: estas dos no se pueden combinar porque sería incoherente.

Luego tenemos la totalidad y la parcialidad:

- Total: Los ejemplares tienen que estar sí o sí en alguno de los subtipos. Esto se identifica por la esfera que está encima del triángulo.

![[Pasted image 20260116194400.png]]

Ejemplo: las personas deben ser masculinas o femeninas.

- Parcial Cuando el ejemplar podría no pertenecer a ninguno de los subtipos.

Ejemplo:

Si el supertipo es vehículo y hay dos subtipos: cuatro ruedas y cuatro cilindros, hay vehículos que no tienen cuatro cilindros pero siguen siendo vehículos.

Estas categorías se pueden combinar quedando de la siguiente manera:

- Total parcial
- Total exclusiva
- Inclusiva parcial
- Inclusiva total




