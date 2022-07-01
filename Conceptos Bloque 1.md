 # Tipos de Sistemas Gestores de Bases de Datos #

 ## Diferencias entre el modelo lógico y el conceptual

El modelo conceptual es independiente del DBMS que se vaya a utilizar. El lógico depende de un tipo de
SGBD en particular.
El modelo lógico está más cerca del modelo físico, el que utiliza internamente el ordenador.
El modelo conceptual es el más cercano al usuario, el lógico es el encargado de establecer el paso entre
el modelo conceptual y el modelo físico del sistema.

## **Tipos de Sistemas Gestores de Bases de Datos**
Algunos ejemplos de modelos conceptuales son:

-Modelo Entidad Relación
-Modelo RM/T
-Modelo UML
Ejemplos de modelos lógicos son:

-Modelo relacional
-Modelo Codasyl
-Modelo Jerárquico
A continuación se comentarán los modelos lógicos más importantes.

### Modelo jerárquico.
Era utilizado por los primeros SGBD, desde que IBM lo definió para su IMS (Information Management System, Sistema Administrador de Información) en 1970. Se le llama también modelo en árbol debido a que utiliza una estructura en árbol para organizar los datos.
La información se organiza con un jerarquía en la que la relación entre las entidades de este modelo siempre es del tipo padre / hijo. De esta forma hay una serie de nodos que contendrán atributos y que se relacionarán con nodos hijos de forma que puede haber más de un hijo para el mismo padre (pero un hijo sólo tiene un padre).
Los datos de este modelo se almacenan en estructuras lógicas llamadas segmentos. Los segmentos se relacionan entre sí utilizando arcos.
La forma visual de este modelo es de árbol invertido, en la parte superior están los padres y en la inferior los hijos.
Este esquema está en absoluto desuso ya que no es válido para modelar la mayoría de problemas de
bases de datos.
### Modelo en red (Codasyl).
Es un modelo que ha tenido una gran aceptación (aunque apenas se utiliza actualmente). En especial se
hizo popular la forma definida por Codasyl a principios de los 70 que se ha convertido en el modelo en
red más utilizado.
El modelo en red organiza la información en registros (también llamados nodos) y enlaces. En los
registros se almacenan los datos, mientras que los enlaces permiten relacionar estos datos. Las bases de
datos en red son parecidas a las jerárquicas sólo que en ellas puede haber más de un padre.
En este modelo se pueden representar perfectamente cualquier tipo de relación entre los datos (aunque
el Codasyl restringía un poco las relaciones posibles), pero hace muy complicado su manejo.
### Modelo relacional.
En este modelo los datos se organizan en tablas cuyos datos se relacionan. Es el modelo más popular y se
describe con más detalle en los temas siguientes que veremos.
### Modelo de bases de datos orientadas a objetos.
Desde la aparición de la programación orientada a objetos (POO u OOP) se empezó a pensar en bases
de datos adaptadas a estos lenguajes. La programación orientada a objetos permite cohesionar datos y
procedimientos, haciendo que se diseñen estructuras que poseen datos (atributos) en las que se
definen los procedimientos (operaciones) que pueden realizar con los datos. En las bases orientadas a
objetos se utiliza esta misma idea.
A través de este concepto se intenta que estas bases de datos consigan arreglar las limitaciones de las
relacionales. Por ejemplo el problema de la herencia (el hecho de que no se puedan realizar relaciones
de herencia entre las tablas), tipos definidos por el usuario, disparadores (triggers) almacenables en la
base de datos, soporte multimedia...
Se supone que son las bases de datos de tercera generación (la primera fue las bases de datos en red y
la segunda las relacionales), lo que significa que el futuro parece estar a favor de estas bases de datos.
Pero siguen sin reemplazar a las relacionales, aunque son el tipo de base de datos que más está
creciendo en los últimos años.
Su modelo conceptual se suele diseñar en UML y el lógico actualmente en ODMG (Object Data
Management Group, grupo de administración de objetos de datos, organismo que intenta crear
estándares para este modelo).
### Bases de datos objeto-relacionales.
Tratan de ser un híbrido entre el modelo relacional y el orientado a objetos. El problema de las bases de
datos orientadas a objetos es que requieren reinvertir capital y esfuerzos de nuevo para convertir las
bases de datos relacionales en bases de datos orientadas a objetos. En las bases de datos objeto
relacionales se intenta conseguir una compatibilidad relacional dando la posibilidad de integrar mejoras
de la orientación a objetos.
Estas bases de datos se basan en el estándar SQL 99. En ese estándar se añade a las bases
relacionales la posibilidad de almacenar procedimientos de usuario, triggers, tipos definidos por el
usuario, consultas recursivas, bases de datos OLAP, tipos LOB,...
Las últimas versiones de la mayoría de las clásicas grandes bases de datos relacionales (Oracle, SQL
Server, Informix, ...) son objeto relacionales.
### Bases de datos NoSQL.
Bajo este nombre se agrupan las bases de datos (con arquitecturas muy diversas) pensadas para grabar
los datos de manera veloz para así poder atender a miles y miles de peticiones. Es decir, es el modelo
de las bases de datos que se utilizan en los grandes servicios de Internet (como twitter, Facebook,
Amazon,…).
La idea es que los datos apenas necesitan validarse y relacionarse y lo importante es la disponibilidad de
la propia base de datos. El nombre NoSQL, hace referencia a que este modelo de bases de datos rompe
con el lenguaje SQL (el lenguaje de las bases de datos relacionales, las bases de datos dominantes
hasta la actualidad) para poder manipular los datos con lenguajes de otro tipo. 