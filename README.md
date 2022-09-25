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


### 
