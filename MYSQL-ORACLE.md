# GUIA MYSQL - ORACLE

# DDL -> Lenguaje de definición de datos

## Estructura

```mysql
Create database (nombreBaseDatos); 🡪 Crear base de datos

Use (nombreBaseDatos); 🡪 Usar base de datos 

Create table (nombreTabla); 🡪 Crear la tabla

Drop database(nombreBaseDatos); 🡪 Borrar base de datos
```

### Dentro de tabla
```mysql
(nombreColumna)(tipoColumna)(cantidadDeCaracteres) PRIMARY KEY;

(nombreColumna)(tipoColumna)(cantidadDeCaracteres)(restricción);
```

### Tablas con foreign key

1. Se declara las PK:

    ```mysql
    PRIMARY KEY (nombres de columnas que sean FK y PK)
    ```

2. Columnas que vayan a ser FK (deben tener el mismo nombre o nombre similar pero con las mismas caracteristicas de la columna):

    ```mysql
    (nombreColumna)(tipoColumna)(cantidadDeCaracteres)(restricción);
    ```

3. Atributos que vayan a ser FK (deben tener el mismo nombre o nombre similar pero con las mismas caracteristicas del atributo):
    
    ```mysql
    (nombreColumnaPK)(tipoColumnaPK)( cantidadDeCaracteresPK)
    ```
4. Se crea la FK con la columna anteriormente declarada, se pone una referencia a la columna donde está situada la PK, poner la columna de la PK y por ultimo "on delete cascade on update cascade":
    
    ```mysql
    FOREIGN KEY (nombre columna declarada en esta tabla) REFERENCES (nombreTablaReferenciada)(nombreColumnaDeTablaReferenciada) on delete cascade on update cascade.
    ```
Cuando una tabla tiene dos PK en conjunto (porque es débil), hay dos PK que van juntas por lo que se declara exactamente igual pero con la diferencia explicada en el siguiente ejemplo:

```mysql
PRIMARY KEY (nombrePKyFK1, nombrePKyFK2, nombrePKyFK3)
```

## Edición de las tablas
```mysql
RENAME TABLE (nombreTabla) TO (nombreNuevoTabla) 🡪 Para cambiar el nombre de una tabla por otro

Show tables; 🡪 Nos muestra las tablas creadas
Desc  (nombreTabla); 🡪 Obtenemos la información de la tabla nombrada
Drop table (nombreTabla); 🡪 Eliminar la tabla nombrada
ALTER TABLE (nombreTabla) 🡪Encabezado para hacer cambios en la tabla nombrada

```

