La normalización es un conjunto de reglas y restricciones que se aplican al modelo relacional para mejorar la calidad de los datos. Entre estas mejoras tenemos:

- Eliminación de redundancia en los atributos
- Prevención de problemas de interrelación entre atributos
- Eliminación de inconsistencias en los datos
- Garantía de la integridad referencial
- Permite modificaciones
- Permite la inserción de nuevos tipos de datos

Primero conoceremos las dependencias que tienen estos datos y luego veremos cómo separarlas en formas normales.

Existen cuatro tipos de dependencia:

- Dependencia funcional: Es cuando un atributo depende directamente de la clave primaria.

Ejemplo: tenemos una tabla alumno con: codigo_estudiante, nombre, apellido, edad. Aquí nombre tiene una dependencia funcional con codigo_estudiante, ya que por medio de este se puede obtener el nombre del alumno.

- Dependencia funcional completa : Es igual que la anterior, pero en este caso la clave primaria está compuesta por varios atributos.
    
- Dependencia funcional transitiva: Es cuando un atributo depende de otro atributo no clave, y este a su vez depende de un atributo clave.
    
- Dependencia parcial: Es cuando un atributo no depende de todos los atributos que conforman la clave. Ejemplo: si la clave está formada por dos atributos, el atributo dependerá de uno de ellos, no de ambos.
    

## 4.2. Las formas normales

Ya que conocemos las dependencias, ahora aplicaremos las formas normales. Estas formas se implementan de forma consecutiva, es decir, una detrás de la otra; si una no está aplicada no se puede continuar con la siguiente.

Hay 5 formas normales, pero nosotros veremos 3 de ellas:

# 4.3. Primera forma normal (1FN)

Para que una relación esté en primera forma normal debe cumplir los siguientes requisitos:

- El orden de las filas es irrelevante
- El orden de las columnas es irrelevante
- No puede haber filas repetidas
- En cada intersección entre fila y columna solo debe haber un valor
- Todas las filas deben ser regulares

# 4.4. Segunda forma normal (2FN)

En la segunda forma normal deben cumplirse los siguientes parámetros:

- Estar en primera forma normal.
- Todos los atributos no clave deben tener una dependencia funcional completa con respecto a la clave  (elimina dependencias parciales).

## 4.5. Tercera forma normal (3FN)

En la tercera forma normal deben cumplirse los siguientes parámetros:

- Estar en segunda forma normal.
- No deben existir atributos con dependencia transitiva respecto a atributos no clave (elimina dependencias transitivas).
