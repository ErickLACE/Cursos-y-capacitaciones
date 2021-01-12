
# Manupulación de las bases de datos
Query (Query son las intrucciones que se dan mediante el código). Antes de comenzar entra al siguiente link que sirve para ejecutar la sintaxis SQL en linea https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all. Para comentar dentro de la sintaxis de SQL se utiliza --

Seleccionamos todos "*" los elementos contenidos en la tabla Poducts al concluir una sentencia es necesario terminar con un ; para que las sentencias no se mezclen entre sí
### SELECT * FROM [Orders]


Vamos a "personalizar" las tablas, por ejemplo la tabla Orders contiene las columnas OrderID, CustomerID, EmployeeID..., pediremos una tabla  que solo contenga las columnas OrderID y EmployeeID
### SELECT  OrderID, CustomerID FROM Orders;

Como vimos antes las columnas ya tienen un nombre, este puede ser cambiado de la siguiente forma

### SELECT  OrderID AS "Orden ID", CustomerID AS "Cliente ID" FROM Orders;

Podemos filtrar datos, por ejemplo la tabla Customers tiene una columna llamada Country, y contiene varios paises, podemos filtrar todas las filas que contienen a Mexico de la siguiente manera

###SELECT  * FROM Customers WHERE Country = "Mexico";

Si tu filtro contiene texto deberás usar comillas ""

Ahora combinamos lo anterior pidiendo una columna en específico llamda CustomerName utiliando el filtro llamado Mexico

###SELECT  CustomerName FROM Customers WHERE Country = "Mexico";

El filtro no solo funciona para elegir, tambien para excluir, podemos pedir todos los demas paises excluyendo a Mexico usando un signo de admiración

###SELECT  CustomerName AS "Nombre del cliente" FROM Customers WHERE Country != "Mexico";
