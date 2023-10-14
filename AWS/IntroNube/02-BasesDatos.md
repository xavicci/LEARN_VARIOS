https://aws.amazon.com/es/getting-started/decision-guides/databases-on-aws-how-to-choose/
Existen 7 principales clases de bases de datos.

• BD relacionales : Los datos están organizados en un conjunto de tablas que están relacionados entre si
	○ MYSQL
	○ Oracle
	○ PostgresSQL
	○ MariaSB
	○ SQL server

	○ Por ejemplo una tabla de usuarios que esté relacionada con otra tabla que contenga la cantidad de tarjetas que tenga registrada en un servicio

• BD Clave/valor  Key/Value
	Utiliza un modelo de llave - valor para almacenar los datos. Los almacena como un conjunto  de pares. 
	○ Es una base de datos NO relacional
	○ Se usa comúnmente como tabla de transacciones

• BD en memoria
	○ Utiliza la memoria para almacenar los datos , es de naturaleza NO relacional
	○ Se usa mucho para que la agilidad o velocidad de lectura de datos sea mucho más rápida que cuando está en un disco duro

• BD documentales
	○ Mongo es la más famosa
	○ Se usa para guardar JSON (Java Script Objet notation (fundamentado en texto, y es muy liviano. Se usa, sobre todo, para transmitir datos entre un servidor y una aplicación web )) de información muy grandes 

• BD columnaer
	○ Es relacional y está optimizada para almacenar los datos en columnas para mejorar el desempeño
	○ Se usa para data warehousing (Los data warehouses pueden: Almacenar grandes cantidades de datos en una base de datos central – y en un formato estándar. Integrar datos de diferentes fuentes y estandarizarlos, de modo que se faciliten el análisis y los reportes. )
	○ Separa cada columna por aparte 
	○ Aplica compresión en las columnas para que sea más eficiente

• BD Grafos
	○ Representa la información en forma de vértices y aristas 
	○ Sirve para identificar relaciones fuertes y conocer quien más usuario y que tipo de red de contactos cercanos usan o tienen alguna app o servicio

• BD Series de Tiempo
	○ Sirve para hacer timestamps para saber cuándo cambió el valor de un objeto en el tiempo.
	○ Sirve para hacer monitoreos a través del tiempo - PROMETEUS es una de las BD más conocidas de la nube