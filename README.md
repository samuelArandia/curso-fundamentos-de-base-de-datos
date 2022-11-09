# Curso de fundamientos de base de datos 

### Historia

Antiguamente se usaban tablillas de arcilla, eran poco transportables y generaban problemas.

Luego se usó el pergamino, era más portátil y liviano, pero era basado en materia animal o vegetal, se descomponía.
    
Los chinos llegaron a una revolución con el papel, tenía una gran ventaja de portabilidad, pero era fácilmente destruible.
    
Muchos siglos después, específicamente en el siglo 20, con el microfilm, fue una tecnología que puede almacenar datos de manera infinita y vivir miles de años. Su desventaja es la modificación de información, es muy complejo.
    
Los medios digitales incluyen los discos duro, cd’s, etc. Se guardaba información en formato de bits y bytes.
    
La nube fue una gran revolución, tiene muchas ventajas frente a los otros medios de almacenamiento, gracias a su fácil acceso desde cualquier parte del mundo.


Tipos de bases de datos

Relacionales

    SQL server
    MariaDB
    Oracle
    PostgreSQL
    Mysql
    
![imagen](https://user-images.githubusercontent.com/83564327/191741202-7cde56f0-ed68-43ff-bee3-a4b787bcdcb2.png)
    

No relacionales

    Cassandra
    Elasticsearch
    Neo4j
    MongoDB
    
![imagen](https://user-images.githubusercontent.com/83564327/191741253-f3cdbce9-0b9b-4685-90cf-118459a1ac28.png)
    
![imagen](https://user-images.githubusercontent.com/83564327/191741297-f9de9bc6-abaa-4cef-9ae3-f79395be5d1b.png)

Servicios

Auto administrados: Son las bases de datos que instalamos en nuestro pc, nos encargamos de la parte de mantenimiento, updates, etc. Nosotros no encargamos de ese la actulizaciones 

Administrados: No los llevamos nosotros, los ofrecen las nubes como Amazon, googles, azure.

### Historia de las base de datos relaciones 

Las bases de datos surgen de la necesidad de conservar la información más allá de lo que existe en la memoria RAM.

Las bases de datos basadas en archivos eran datos guardados en texto plano, fáciles de guardar pero muy difíciles de consultar y por la necesidad de mejorar esto nacen las bases de datos relacionales. Su inventor Edgar Codd dejó ciertas reglas para asegurarse de que toda la filosofía de las bases de datos no se perdiera, estandarizando el proceso.

12 reglas de la CODD O los dos mandamientos (https://www.mindmeister.com/es/1079684487/las-12-reglas-de-codd-del-modelo-relacional?fullscreen=1#) 

### Etidades y atributos 

### ¿Qué es una entidad?

Una entidad es algo similar a un objeto (programación orientada a objetos) y representa algo en el mundo real, incluso algo abstracto. Tienen atributos que son las cosas que los hacen ser una entidad y por convención se ponen en plural.Las entidades se escriben en Plural y están representadas por un conjunto de atributos

Estas pueden ser:
• Concreta: Persona, empleado, casa, auto, etc …
• Abstracta: cta bancaría, empresa, curso
• Multivaluados: puede tener varios valores (teléfonos, hijos, discos duros)
• Compuestos: desde los cuales se desprenden más atributos
• Llave: aquel que identifica la entidad y no se puede repetir y existen dos tipos:
-Natural: Son inherentes del Objeto (Cedula, No. Serie)
-Artificial: No es inherente al objeto y se asigna arbitrariamente
• Derivados: es aquel que se obtiene de un atributo definido (fecha Nac = edad)

Ejemplo de entidad en bases de datos

En la imagen puedes observar como ejemplo que la enidad Laptops posee diferentes atributos como color, pantalla, año, modelo, etc.

![imagen](https://user-images.githubusercontent.com/83564327/192128813-780b6a0d-b30f-47c3-a9d7-f8500264c028.png)

### ¿Qué es un atributo?

Son las características o propiedades que describen a la entidad (se encierra en un óvalo). Los atributos se componen de:

Los atributos compuestos son aquellos que tienen atributos ellos mismos.

Los atributos llave son aquellos que identifican a la entidad y no pueden ser repetidos. Existen:

Naturales: son inherentes al objeto como el número de serie
Clave artificial: no es inherente al objeto y se asigna de manera arbitraria.

### Tipos de entidades

Entidades fuertes: son entidades que pueden sobrevivir por sí solas.

Entidades débiles: no pueden existir sin una entidad fuerte y se representan con un cuadrado con doble línea.

Identidades débiles por identidad: no se diferencian entre sí más que por la clave de su identidad fuerte.

Identidades débiles por existencia: se les asigna una clave propia.

Cómo representar las entidades en bases de datos

Existen varios tipos de notaciones para los modelos entidad relacionamiento. Chen es uno de los más utilizados para diagramar lógicamente la base de datos. Aquí te mostramos un ejemplo.

![imagen](https://user-images.githubusercontent.com/83564327/192128838-5b72ecdb-f0bf-4252-a72d-21e4368a040b.png)
![imagen](https://user-images.githubusercontent.com/83564327/192128930-c0e4c61e-b0b4-40de-8b4f-76eec0d19551.png)


### Relaciones 

Las relaciones nos permiten ligar o unir nuestras diferentes entidades y se representan con rombos. Por convención se definen a través de verbos.

Las relaciones tienen una propiedad llamada cardinalidad y tiene que ver con números. Cuántos de un lado pertenecen a cuántos del otro lado:

### Cardinalidad: 1 a 1

![imagen](https://user-images.githubusercontent.com/83564327/200380544-1144271b-b161-4e98-bcfa-d16ce81d1cc4.png)

### Cardinalidad: 0 a 1

![imagen](https://user-images.githubusercontent.com/83564327/200380806-8828ae1e-21b1-4ea4-8b17-9022a11e7377.png)

    
### Cardinalidad: 1 a N

![imagen](https://user-images.githubusercontent.com/83564327/200380995-bfc70e2a-d49a-45d1-a638-1bd43e124114.png)

### Cardinalidad: 0 a N

![imagen](https://user-images.githubusercontent.com/83564327/200381121-112bb878-1bb0-44ff-8019-d814232d1fbc.png)


![imagen](https://user-images.githubusercontent.com/83564327/200378595-d391f01f-9141-4184-aebf-212c7242de16.png)

### Cardinalidad: N A N 

![imagen](https://user-images.githubusercontent.com/83564327/200642554-c1e72297-a737-46ee-b9f1-b2fc078d4433.png)

### Diagrama Entidad relación

![imagen](https://user-images.githubusercontent.com/83564327/200712947-22391d50-ecac-4e4c-8074-e1e9893c9ca9.png)


### Digrama Físico: Tipo de datos y constraints 

Para llevar a la práctica un diagrama debemos ir más allá y darle detalle con parámetros como:

Tipos de dato:

    Texto: CHAR(n), VARCHAR(n), TEXT
    Números: INTEGER, BIGINT, SMALLINT, DECIMAL(n,s), NUMERIC(n,s)
    Fecha/hora: DATE, TIME, DATETIME, TIMESTAMP
    Lógicos: BOOLEAN

![imagen](https://user-images.githubusercontent.com/83564327/200714188-cd03e31a-d13a-4348-af6c-eea3d4c3f697.png)

Constraints (Restricciones)

    NOT NULL: Se asegura que la columna no tenga valores nulos
    UNIQUE: Se asegura que cada valor en la columna no se repita
    PRIMARY KEY: Es una combinación de NOT NULL y UNIQUE
    FOREIGN KEY: Identifica de manera única una tupla en otra tabla
    CHECK: Se asegura que el valor en la columna cumpla una condición dada
    DEFAULT: Coloca un valor por defecto cuando no hay un valor especificado
    INDEX: Se crea por columna para permitir búsquedas más rápidas
![imagen](https://user-images.githubusercontent.com/83564327/200715369-3f0261b9-7e7d-47b5-8efe-5bc3f49646c4.png)


### Diagrama Físicoñ Normalización 

La normalización como su nombre lo indica nos ayuda a dejar todo de una forma normal. Esto obedece a las 12 reglas de Codd y nos permiten separar componentes en la base de datos:

    Primera forma normal (1FN): Atributos atómicos (Sin campos repetidos)
    Segunda forma normal (2FN): Cumple 1FN y cada campo de la tabla debe depender de una clave única.
    Tercera forma normal (3FN): Cumple 1FN y 2FN y los campos que NO son clave, NO deben tener dependencias.
    Cuarta forma normal (4FN): Cumple 1FN, 2FN, 3FN y los campos multivaluados se identifican por una clave única.

![imagen](https://user-images.githubusercontent.com/83564327/200717562-18b099bd-0215-4ce3-bc13-82c68c68f5c4.png)

![imagen](https://user-images.githubusercontent.com/83564327/200718861-5d0db6eb-ace7-4efe-a3ce-107480ac2dc8.png)

![imagen](https://user-images.githubusercontent.com/83564327/200719444-fd5ccdeb-aac0-4866-a2f6-d6064367e427.png)
![imagen](https://user-images.githubusercontent.com/83564327/200719463-7e9e2aff-97f5-4980-9003-48e87fd17253.png)


