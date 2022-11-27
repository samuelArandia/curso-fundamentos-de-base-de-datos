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


### Diagrama Físico Normalización 

La normalización como su nombre lo indica nos ayuda a dejar todo de una forma normal. Esto obedece a las 12 reglas de Codd y nos permiten separar componentes en la base de datos:

    Primera forma normal (1FN): Atributos atómicos (Sin campos repetidos)
    Segunda forma normal (2FN): Cumple 1FN y cada campo de la tabla debe depender de una clave única.
    Tercera forma normal (3FN): Cumple 1FN y 2FN y los campos que NO son clave, NO deben tener dependencias.
    Cuarta forma normal (4FN): Cumple 1FN, 2FN, 3FN y los campos multivaluados se identifican por una clave única.
La normalización en las bases de datos relacionales es uno de esos temas que, por un lado es sumamente importante y por el otro suena algo esotérico. Vamos a tratar de entender las formas normales (FN) de una manera simple para que puedas aplicarlas en tus proyectos profesionales.

Primera Forma Normal (1FN)
Esta FN nos ayuda a eliminar los valores repetidos y no atómicos dentro de una base de datos.

Formalmente, una tabla está en primera forma normal si:

    Todos los atributos son atómicos. Un atributo es atómico si los elementos del dominio son simples e indivisibles.
    No debe existir variación en el número de columnas.
    Los campos no clave deben identificarse por la clave (dependencia funcional).
    Debe existir una independencia del orden tanto de las filas como de las columnas; es decir, si los datos cambian de orden no deben cambiar sus significados.

Se traduce básicamente a que si tenemos campos compuestos como por ejemplo “nombre_completo” que en realidad contiene varios datos distintos, en este caso podría ser “nombre”, “apellido_paterno”, “apellido_materno”, etc.

También debemos asegurarnos que las columnas son las mismas para todos los registros, que no haya registros con columnas de más o de menos.

Todos los campos que no se consideran clave deben depender de manera única por el o los campos que si son clave.

Los campos deben ser tales que si reordenamos los registros o reordenamos las columnas, cada dato no pierda el significado.

Segunda Forma Normal (2FN)
Esta FN nos ayuda a diferenciar los datos en diversas entidades.

Formalmente, una tabla está en segunda forma normal si:

    Está en 1FN
    Sí los atributos que no forman parte de ninguna clave dependen de forma completa de la clave principal. Es decir, que no existen dependencias parciales.
    Todos los atributos que no son clave principal deben depender únicamente de la clave principal.

Lo anterior quiere decir que sí tenemos datos que pertenecen a diversas entidades, cada entidad debe tener un campo clave separado. Por ejemplo:

![imagen](https://user-images.githubusercontent.com/83564327/200720986-8f0c7948-9ed2-4608-904a-441e18846e9c.png)

En la tabla anterior tenemos por lo menos dos entidades que debemos separar para que cada uno dependa de manera única de su campo llave o ID. En este caso las entidades son alumnos por un lado y materias por el otro. En el ejemplo anterior, quedaría de la siguiente manera:

![imagen](https://user-images.githubusercontent.com/83564327/200721041-5613f8b5-169f-4280-ae06-7f02d2e1fbfa.png)

Tercera Forma Normal (3FN)
Esta FN nos ayuda a separar conceptualmente las entidades que no son dependientes.

Formalmente, una tabla está en tercera forma normal si:

Se encuentra en 2FN
No existe ninguna dependencia funcional transitiva en los atributos que no son clave

Esta FN se traduce en que aquellos datos que no pertenecen a la entidad deben tener una independencia de las demás y debe tener un campo clave propio. Continuando con el ejemplo anterior, al aplicar la 3FN separamos la tabla alumnos ya que contiene datos de los cursos en ella quedando de la siguiente manera.
![imagen](https://user-images.githubusercontent.com/83564327/200721084-4bb2c940-a9c5-4c9a-a92a-783f89950474.png)
![imagen](https://user-images.githubusercontent.com/83564327/200721105-93f8cdbb-7202-4eba-b107-e041c13d02eb.png)

Cuarta Forma Normal (4FN)
Esta FN nos trata de atomizar los datos multivaluados de manera que no tengamos datos repetidos entre rows.

Formalmente, una tabla está en cuarta forma normal si:

    Se encuentra en 3FN
    Los campos multivaluados se identifican por una clave única

Esta FN trata de eliminar registros duplicados en una entidad, es decir que cada registro tenga un contenido único y de necesitar repetir la data en los resultados se realiza a través de claves foráneas.

Aplicado al ejemplo anterior la tabla materia se independiza y se relaciona con el alumno a través de una tabla transitiva o pivote, de tal manera que si cambiamos el nombre de la materia solamente hay que cambiarla una vez y se propagara a cualquier referencia que haya de ella.

![imagen](https://user-images.githubusercontent.com/83564327/200721188-3522a3a2-44d1-4aee-b61d-9781d459ab98.png)
![imagen](https://user-images.githubusercontent.com/83564327/200721204-7a6b7e77-9ff8-4d0a-bd16-84377b073827.png)

De esta manera, aunque parezca que la información se multiplicó, en realidad la descompusimos o normalizamos de manera que a un sistema le sea fácil de reconocer y mantener la consistencia de los datos.

Algunos autores precisan una 5FN que hace referencia a que después de realizar esta normalización a través de uniones (JOIN) permita regresar a la data original de la cual partió.

## Diagrama fisico: normalizacion 

Cuando se tiene 1 a muchos se coloca la llave foranea de muchos en la que tiene uno 

![imagen](https://user-images.githubusercontent.com/83564327/200812990-693e6fd4-729f-413a-a2a5-e0783041f09d.png)
![imagen](https://user-images.githubusercontent.com/83564327/200814100-46cbe80e-dc3f-4ad1-862c-2a59648f522a.png)


### tabla intermedia 

Es obligarotio que tengas las dos claves. Necesitamo una clave 

Claves compuestas: Es un campo id esta dormado por dos id, la combinacion debe ser unica. Pero los id de cada tabla se hacen llave foranea, es decir que pueden tener los dos id

![imagen](https://user-images.githubusercontent.com/83564327/200813410-f351a209-e576-4adc-89f1-807a6d48886b.png)


### Instalación local de un RDBMS (Windows)

Hay dos maneras de acceder a manejadores de bases de datos:

    Instalar en máquina local un administrador de bases relacional.
    Tener ambientes de desarrollo especiales o servicios cloud.

En este curso usaremos MySQL porque tiene un impacto histórico siendo muy utilizado y además es software libre y gratuito. La versión 5.6.43 es compatible con la mayoría de aplicaciones y frameworks.

    Root es el usuario principal que tendrá todos los permisos y por lo tanto en ambientes de producción hay que tener mucho cuidado al configurarlo.


### ¿Qué es RDB y RDBMS?
RDB (relational database)

RDBMS (Relational DataBase Management System) Sistema Manejador de Bases de datos relacionales.

La diferencia entre ambos es que las BBDD son un conjunto de datos pertenecientes ( o al menos en teoría) a un mismo tipo de contexto, que guarda los datos de forma persistente para un posterior uso, y el Sistema de gestión de BBDD o sistema manejador, es el que nos permite acceder a ella, es un software, herramienta que sirve de conexión entre las BBDD y el usuario (nos presenta una interfaz para poder gestionarla, manejarla).

RDBMS

    MySQL
    PostgreSQL
    Etc

Todas toman un lenguaje base, pero cada uno lo apropia, imponiéndole diferentes reglas y características.
![imagen](https://user-images.githubusercontent.com/83564327/200974790-68d6787a-adc4-4bac-9bd9-ccdd91ed6f54.png)


### Cliente Gráfico 

MySQL en escritorio 

### Servicios adminitrativos o cloud 

Hoy en día muchas empresas ya no tienen instalados en sus servidores los RDBMS sino que los contratan a otras personas. Estos servicios administrados cloud te permiten concentrarte en la base de datos y no en su administración y actualización.


## Historia de SQL 

SQL significa Structured Query Language y tiene una estructura clara y fija. Su objetivo es hacer un solo lenguaje para consultar cualquier manejador de bases de datos volviéndose un gran estándar.

Ahora existe el NOSQL o Not Only Structured Query Language que significa que no sólo se utiliza SQLen las bases de datos no relacionales.


## DDL

![imagen](https://user-images.githubusercontent.com/83564327/201223658-cb19c253-a55c-4a47-a359-e3ecc897f221.png)

SQL tiene dos grandes sublenguajes:
DDL o Data Definition Language que nos ayuda a crear la estructura de una base de datos. Existen 3 grandes comandos:

    Create: Nos ayuda a crear bases de datos, tablas, vistas, índices, etc.
    Alter: Ayuda a alterar o modificar entidades.
    Drop: Nos ayuda a borrar. Hay que tener cuidado al utilizarlo.

3 objetos que manipularemos con el lenguaje DDL:

    Database o bases de datos
    Table o tablas. Son la traducción a SQL de las entidades
    View o vistas: Se ofrece la proyección de los datos de la base de datos de forma entendible.



    DML
    o Data Manipulation Language o Lenguaje de Manipulación de Datos
    o Lenguaje procedimental y declarativo  conjunto de instrucciones que apoyarán al proceso de construcción de la BD
    o Las sentencias DML afectan los registros en una tabla. Estas son operaciones básicas que realizamos sobre datos tales como seleccionar algunos registros de una tabla, insertar nuevos registros, eliminar registros innecesarios y actualizar / modificar registros existentes.
    o Opciones DML
     SELECT: para seleccionar registros de tablas
     INSERT: para insertar nuevos registros
     UPDATE: para actualizar y modificar registros
     DELETE: para eliminar registros existentes.

    DDL
    o Data Definition Language o Lenguaje de Definición de Datos
    o Aquí ya se especifica el esquema de la BD, generando un diccionario de datos, las restricciones de integridad y las autorizaciones para que ciertos usuarios no vean cierto contenido.
    o Sentencias DDL son las necesarias para poder modificar la BD, esquema y ESTRUCTURA de las tablas. Son las útiles para el diseño y control de objetos que se encuentran dentro de las BD.
    o Opciones DDL
    CREATE: Crear una nueva base de datos, una tabla o esquema.
    ALTER: Alterar tabla existente, descripción de columnas, etc.
    DROP: Eliminar objetos existentes de la BD.
    o 3 objetos que manipularemos con el lenguaje DDL
    Database
    Tables: traducción a SQL de las entidades
    View : se ofrece la proyección de los datos de la BD de forma entendible

    DCL
    o Lenguaje de Control de Datos
    o Las declaraciones DLC son las encargadas de controlar el acceso de los usuarios a las BD.
    o Opciones DDL
     GRANT:
    • Declaración que permite a los usuarios leer / escribir en objetos que digamos de la BD.
     REVOKE:
    • Es la que ofrece a los usuarios estar sin permiso de lectura / escritura en objetos de la BD.

    TLC
    o Lenguaje de Control de Transacciones
    o Instrucciones que permiten administrar transacciones y tener integridad de datos dentro de las declaraciones SQL. Se gestiona a través de las siguientes declaraciones
     BEGIN Transaction
    • Nos permite abrir una transacción
    COMMIT Transaction
    • Ofrece confirmar una transacción
     ROLLBACK Transaction
    • Devuelve una transacción en caso de error cometido.

![imagen](https://user-images.githubusercontent.com/83564327/201227297-60a7915b-e8d0-4e1f-8343-bab0c6a27054.png)

![imagen](https://user-images.githubusercontent.com/83564327/201227752-e629483a-84eb-4e98-a3bc-33ecfe48f507.png)

PK - Primary Key

NN - Not Null

BIN - Binary (stores data as binary strings. There is no character set so sorting and comparison is based on the numeric values of the bytes in the values.)

UN - Unsigned (non-negative numbers only. so if the range is -500 to 500, instead its 0 - 1000, the range is the same but it starts at 0)

UQ - Create/remove Unique Key

ZF - Zero-Filled (if the length is 5 like INT(5) then every field is filled with 0’s to the 5th digit. 12 = 00012, 400 = 00400, etc. )

AI - Auto Increment

G - Generated column. i.e. value generated by a formula based on the other columns

## CREATE VIEW y DDL ALTER
            INSERT INTO `platziblog`.`people` (`person_id`, `last_name`, `first_name`, `address`, `city`) 
            VALUES ('1', 'Vásquez', 'Israel', 'Calle Famosa Num 1', 'México'),
                       ('2', 'Hernández', 'Mónica', 'Reforma 222', 'México'),
                       ('3', 'Alanis', 'Edgar', 'Central 1', 'Monterrey');
![imagen](https://user-images.githubusercontent.com/83564327/201456797-4dc28fa9-28cd-4b63-8f75-563a079e644b.png)

## DDL(Data definition languaje): Drop 

Está puede ser la sentencia ¡más peligrosa! (????), sobre todo cuando somos principiantes. Básicamente borra o desaparece de nuestra base de datos algún elemento.

![imagen](https://user-images.githubusercontent.com/83564327/201472670-fc5748f1-076c-4544-ae81-9e9741b1cd3a.png)

## DML (Data Manipulation Language) (https://www.w3schools.in/mysql/ddl-dml-dcl/)

DML trata del contenido de la base de datos. Son las siglas de Data Manipulation Language y sus comandos son:

    Insert: Inserta o agrega nuevos registros a la tabla.
    ![imagen](https://user-images.githubusercontent.com/83564327/201486319-e105690d-38ba-4263-9772-8188ffa2fc57.png)

    Update: Actualiza o modifica los datos que ya existen.
    ![imagen](https://user-images.githubusercontent.com/83564327/201487028-3952b41a-9afe-43e6-9310-667a8f3fc3e5.png)

    Delete: Esta sentencia es riesgosa porque puede borrar el contenido de una tabla.
    ![imagen](https://user-images.githubusercontent.com/83564327/201488959-1e89fe31-d62c-4cb8-8b1b-7296847c9ebc.png)

    Select: Trae información de la base de datos.
    ![imagen](https://user-images.githubusercontent.com/83564327/201489070-12caae77-8b44-49fd-af6e-fffab07b1f58.png)

## ¿Qué tan standard es SQL?

La utilidad más grande de SQL fue unificar la forma en la que pensamos y hacemos preguntas a un repositorio de datos. Ahora que nacen nuevas bases de datos igualmente siguen tomando elementos de SQL.

![imagen](https://user-images.githubusercontent.com/83564327/201491511-0c8512d0-b41e-4a21-8f62-9df4e17b34e8.png)

## Tablas independientes, dependientes y tablas transitivas. 


Las tablas transitivas sirven como puente para unir dos tablas. No tienen contenido semántico.
Reverse Engineer nos reproduce el esquema del cual nos basamos para crear nuestras tablas. Es útil cuando llegas a un nuevo trabajo y quieres entender cuál fue la mentalidad que tuvieron al momento de crear las bases de datos.


![imagen](https://user-images.githubusercontent.com/83564327/201494273-e5567d67-27b1-4a20-9f18-f1a676473cfc.png)

![imagen](https://user-images.githubusercontent.com/83564327/201494267-3e289ff3-2f6f-4a43-a4b8-160e0480da90.png)

## ¿Por qué las consultas son tan importantes?

Las consultas o queries a una base de datos son una parte fundamental ya que esto podría salvar un negocio o empresa.
Alrededor de las consultas a las bases de datos se han creado varias especialidades como ETL o transformación de datos, business intelligence e incluso machine learning.

Las consultas en una base de datos juegan un papel muy fundamental, puesto que facilitan de manera considerable los procesos en cualquier empresa.
ETL
La palabra ETL correspondería al acrónimo de:
Extract (Extraer)
Transform (Transformar)
Load (Cargar)
ETL hace parte del proceso de integración de datos, mas aun es un componente muy importante que completa el resultado final en la relación de aplicaciones y sistemas.


## Estructura básica de un Query

Los queries son la forma en la que estructuramos las preguntas que se harán a la base de datos. Transforma preguntas en sintaxis.

El query tiene básicamente 2 partes: SELECT y FROM y puede aparecer una tercera como WHERE.

    La estrellita o asterisco (*) quiere decir que vamos a seleccionar todo sin filtrar campos.

![imagen](https://user-images.githubusercontent.com/83564327/201523918-8913568e-b2ae-45d2-bf85-bcada0e4f401.png)

## SELECT 

Es la primera parte de la estructura que necesitamos para hacer preguntas a la base de datos.
Se encarga de proyectar o mostrar los datos que le pedimos a la base de datos.
Si escribimos "SELECT (*) " estamos seleccionando todos los campos de la tabla que seleccionaremos con FROM .
Si, en cambio, escribimos "SELECT " y luego uno o varios nombres de los campos de la tabla, separados por coma, unicamente recibiremos dichos los datos de dichas columnas.
Por cada campo, podemos agregar un “_AS _ …” (por ejemplo, " titulo AS encabezado ). Esto nos permitira mostrar las columnas con un nombre diferente: en este caso mostrara la columna titulo con el nombre encabezado. Si indicamos " SELECT COUNT (*)", la funcion COUNT contara todas las filas de la tabla (usualmente se usa con algun filtro, para no elegir todas las columnas de la tabla).

El AS tambien se puede usar con la funcion COUNT de la siguiente manera:
  
    SELECT COUNT (*) AS numeroDePosts


![imagen](https://user-images.githubusercontent.com/83564327/201524539-fedf31c9-8aa3-4d6f-8fba-67a1ffa5a27b.png)


## From 

FROM indica de dónde se deben traer los datos y puede ayudar a hacer sentencias y filtros complejos cuando se quieren unir tablas. La sentencia compañera que nos ayuda con este proceso es JOIN.

Los diagramas de Venn son círculos que se tocan en algún punto para ver dónde está la intersección de conjuntos. Ayudan mucho para poder formular la sentencia JOIN de la manera adecuada dependiendo del query que se quiere hacer.

![imagen](https://user-images.githubusercontent.com/83564327/201559553-96d14966-d416-4542-92f6-d13c89dd66bf.png)

![imagen](https://user-images.githubusercontent.com/83564327/201647350-d7394d9b-c5dc-46b3-a3e4-4a2bc4b4d9ae.png)

![imagen](https://user-images.githubusercontent.com/83564327/201559188-f3a82c67-adaf-4361-b045-2a4bce7b8575.png)


            SELECT * FROM usuarios LEFT JOIN posts ON usuarios.id = posts.usuario_id
            WHERE posts.usuario_id IS NULL
            UNION 
            SELECT * FROM usuarios RIGHT JOIN posts ON usuarios.id = posts.usuario_id
            WHERE posts.usuario_id IS NULL;
            
## WHERE 
Es la sentencia que nos ayuda a filtrar tuplas o registros dependiendo de las características que elegimos.

La propiedad LIKE nos ayuda a traer registros de los cuales conocemos sólo una parte de la información.
La propiedad BETWEEN nos sirve para arrojar registros que estén en el medio de dos. Por ejemplo los registros con id entre 20 y 30.
    
    
Un breve resumen del like y uso del %:
– %termina_en
– %en medio%
– inicia_con%

![imagen](https://user-images.githubusercontent.com/83564327/202327745-56888861-132f-430e-9deb-0b6f7829a344.png)

## Utilizando la sentencia WHERE nulo y no nulo
 
El valor nulo en una tabla generalmente es su valor por defecto cuando nadie le asignó algo diferente. La sintaxis para hacer búsquedas de datos nulos es IS NULL. La sintaxis para buscar datos que no son nulos es IS NOT NULL

        SELECT * FROM posts WHERE usuario_id is NULL;
        
        
        
## GROUP BY 
                    SELECT estatus, COUNT(*) posts_quantity 
                    FROM posts GROUP BY  estatus;  

                    SELECT YEAR(fecha_publicacion) AS post_year, COUNT(*) AS post_quantity 
                    FROM  posts 
                    GROUP BY post_year;

                    SELECT MONTHNAME(fecha_publicacion) AS post_months, COUNT(*) AS post_quantity
                    FROM posts
                    GROUP BY post_months;
                    
GROUP BY tiene que ver con agrupación. Indica a la base de datos qué criterios debe tener en cuenta para agrupar.

Aparte de la función COUNT, podemos encontrar las siguientes funciones de agregado:
AVG Calcula el promedio
COUNT Cuenta los registros de un campo
SUM Suma los valores de un campo
MAX Devuelve el maximo de un campo
MIN Devuelve el mínimo de un campo

![imagen](https://user-images.githubusercontent.com/83564327/203461781-a07451ea-d9ec-42fd-be6d-c6ddf257a074.png)

## ORDER BY y HAVING

La sentencia ORDER BY tiene que ver con el ordenamiento de los datos dependiendo de los criterios que quieras usar.

    ASC sirve para ordenar de forma ascendente.
    DESC sirve para ordenar de forma descendente.
    LIMIT se usa para limitar la cantidad de resultados que arroja el query.

HAVING tiene una similitud muy grande con WHERE, sin embargo el uso de ellos depende del orden. Cuando se quiere seleccionar tuplas agrupadas únicamente se puede hacer con HAVING.

                    SELECT MONTHNAME(fecha_publicacion) AS post_month, estatus, COUNT(*) AS post_quality 
                    FROM posts 
                    GROUP BY estatus, post_month
                    HAVING post_month = 'april'
                    ORDER BY post_month;
                    
## El interminable agujero de conejo (Nested queries)

 Los Nested queries significan que dentro de un query podemos hacer otro query. Esto sirve para hacer join de tablas, estando una en memoria. También teniendo un query como condicional del otro.

Este proceso puede ser tan profundo como quieras, teniendo infinitos queries anidados.
Se le conoce como un producto cartesiano ya que se multiplican todos los registros de una tabla con todos los del nuevo query. Esto provoca que el query sea difícil de procesar por lo pesado que puede resultar.

Ejemplos:
                        SELECT new_table_projection.date, COUNT(*) AS post_count
                        FROM (
                        SELECT DATE(MIN(fecha_publicacion)) AS date, YEAR(fecha_publicacion) AS post_year
                        FROM posts
                        GROUP BY post_year
                        ) AS new_table_projection
                        GROUP BY new_table_projection.date
                        ORDER BY new_table_projection.date;
                        .
                        SELECT *
                        FROM posts
                        WHERE fecha_publicacion = (
                        SELECT MAX(fecha_publicacion)
                        FROM posts
                        );

## ¿Cómo convertir una pregunta en un query SQL?

De pregunta a Query

    SELECT: Lo que quieres mostrar
    FROM: De dónde voy a tomar los datos
    WHERE: Los filtros de los datos que quieres mostrar
    GROUP BY: Los rubros por los que me interesa agrupar la información
    ORDER BY: El orden en que quiero presentar mi información
    HAVING: Los filtros que quiero que mis datos agrupados tengan
