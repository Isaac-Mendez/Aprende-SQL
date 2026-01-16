El modelo entidad-relación es un modelo de datos abstracto, que nos permite representar de manera conceptual una base de datos

Antes de crear una base de datos también hay que cumplir unas ciertas fases que tenemos:

- Recogida de información: Aquí lo que hacemos es recoger todas la información necesaria
- Modelo entidad-relacion: Después toda esa información lo que hacemos es diseñar el diagrama 
- Modelo relacional: Pasamos a un modelo donde se pueda entender ya para crear las tablas 
- Normalización: Es como ordenar esas tablas con una serie de reglas 
- Codificación: Ya es crear la tabla en SQL

Para resumir hay que pasarla por 3 proceso que son: 
- Conceptual: Es donde pensamos el proyecto
- Modelo lógico: Hacemos los diagramas y realizamos la lógica 
- Modelo físico: donde codificamos 

## 2.2. Entidad: representación gráfica, atributos y tipos de claves

- Entidades
Podemos diferenciar las entidades porque están creadas en un rectángulo, además tiene que ser un nombre único 

- Atributos
  Son los datos que tiene una entidad

- Clave primaria 
  La que permite identificar una fila de manera única

- Atributo multivaluado
  Un atributo que se repite varias veces 

- Atributo derivado:
  Atributo que puede ser calculado por otros atributos 


## 2.3. Relación: representación gráfica, atributos, grado y cardinalidad

- Relacion

Se utiliza para conectar las entidades y su diseño es un rombo ademas de esto la palabra que se utilizar para conectar siempre es un verbo como "Tiene"

## 2.4. Diagrama entidad-relación

## Cardinalidad
 Numero de participaciones que tiene la entidades aquí nos podemos encontrar 3 participaciones 
- 1:1 Cuando las participaciones tiene una como mínimo y una como máximo de cada lado 

- 1:N Cuando de un lado tiene relacion de un lado y del otros la relaciones son muchas 

- M:N Cuando es muchas con muchas de ambos lados 

## Participaciones

La participación es lo que se pone encima de la relacion y tiene que ser el máximo de cada lado 

## Entidades fuertes y débiles

- Entidad fuerte: 
 Esta entidad tiene existencia por si misma y no depende de otra 

- Entidad Débil: 
 Depende de una relacion fuerte para existir, no tiene existencia por si sola 

## Tipos de correspondencias en las relaciones: binaria, reflexiva y otros

- Relación unaria o reflexiva: 
 Es una relacion que hace menciona a sigo misma 

- Relación binaria o de grado 2:
 Cuando hace mencion a otra entidad y la otra enntidad hace mención a ella 

- Relaciones ternarias o de grado 3:
 Cuando hay 3 entidades 

- Relación N-aria: 
 Cuando tenemos mas de 3 entidades 

# 2.5. Modelo entidad-relación extendido

Hasta ahora solo hemos visto entidades relacion solo de forma binarias pero no de una forma dinámica para esto tenemos el modelo entidad-relacion extendido 

## Generalización/especialización

Estos dos conceptos lo podemos definir de la siguiente manera: 

- Generalización: 
  Es cuando la entidad comparte atributos generales ósea que lo puede utilizar cualquier que comparta ese atributo 
- Especificación: Es cuando la entidad tiene atributos mas específicos 
