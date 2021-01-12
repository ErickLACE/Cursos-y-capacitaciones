
# Manupulación de las bases de datos
Query (Query son las intrucciones que se dan mediante el código). Antes de comenzar entra al siguiente link que sirve para ejecutar la sintaxis SQL en linea https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all. Para comentar dentro de la sintaxis de SQL se utiliza --

Seleccionamos todos "*" los elementos contenidos en la tabla Poducts al concluir una sentencia es necesario terminar con un ; para que las sentencias no se mezclen entre sí
### SELECT * FROM [Orders]


Vamos a "personalizar" las tablas, por ejemplo la tabla Orders contiene las columnas OrderID, CustomerID, EmployeeID..., pediremos una tabla  que solo contenga las columnas OrderID y EmployeeID
### SELECT  OrderID, CustomerID FROM Orders;

Como vimos antes las columnas ya tienen un nombre, este puede ser cambiado de la siguiente forma

### SELECT  OrderID AS "Orden ID", CustomerID AS "Cliente ID" FROM Orders;

Podemos filtrar datos, por ejemplo la tabla Customers tiene una columna llamada Country, y contiene varios paises, podemos filtrar todas las filas que contienen a Mexico de la siguiente manera

### SELECT  * FROM Customers WHERE Country = "Mexico";

Si tu filtro contiene texto deberás usar comillas ""

Ahora combinamos lo anterior pidiendo una columna en específico llamda CustomerName utiliando el filtro llamado Mexico

### SELECT  CustomerName FROM Customers WHERE Country = "Mexico";

El filtro no solo funciona para elegir, tambien para excluir, podemos pedir todos los demas paises excluyendo a Mexico usando un signo de admiración

### SELECT  CustomerName AS "Nombre del cliente" FROM Customers WHERE Country != "Mexico";

Podemos filtrar intervalos de valores numéricos usando desigualdades, en el lenguaje de Query se le llama operadores relacionales < ,<=, >, >= 
### SELECT * FROM Products WHERE Price >= "20";

Similarmente, podemos elegir datos anteriores o posteriores a una fecha, mientras esta esté registrada en una columna

### SELECT * FROM Orders WHERE OrderDate >= "1997-01-01";

Es posible utilizar filtros para mas de una columna de manera simultanea, por ejemplo en la tabla products tenemos las columnas SupplierID y Price,
pedimos los valores en donde SupplierID sea igual a 1 pero tambien en donde Price sea mayor que 20 con el comando AND

### SELECT * FROM Products WHERE SupplierID = 1 AND Price <= 20

Del mismo modo podemos pedir que nos dé los productos en donde SupplierID sea igual a 1 o que Price sea mayor que 20 

### SELECT * FROM Products WHERE SupplierID = 1 OR Price <= 20

La diferencia entre AND y OR radica en qué, AND se utiliza para obtener los datos que cumplen obligatoriamente las condiciones impuestas, con el comando OR 
pedimos los datos que contengan una u otra condición

Cuando necesitamos muchos elementos asociados a los datos por ejemplo que contenga mas de un país, es tedioso utilizar repetidas veces AND y OR, podemos
escribir un Query que contenga a varios de ellos a la vez utilizando IN, por ejemplo de la tabla Customers, tomamos las filas que contengan a Germany, OK y Mexico

### SELECT CustomerName AS "Nombre", Country AS "País" FROM Customers WHERE Country IN ("Germany",  "UK", "Mexico");

También podemos obtener todos los datos y excluir a los anteriores paises con NOT IN

### SELECT CustomerName AS "Nombre", Country AS "País" FROM Customers WHERE Country NOT IN ("Germany",  "UK", "Mexico");

Tenemos por otra parte la tabla Products, si de ella quisieramos tomar precios que se encuentren dentro de un intervalo, por ejemplo [20,40]

### SELECT * FROM Products WHERE Price >= 20 AND Price <= 40;

Se hace lo mismo con un solo comando, BETWEEN, es de utilidad al ser mas directo

### SELECT * FROM Products WHERE Price BETWEEN 20 AND 40;

Memorizar muchos nombres por ejemplo clientes es a veces imposible, sin embargo podemos recordar cosas como su giro, por ejemplo "tacos" o "gourmet", podemos rastrear
algun dato que contenga ciertas palabras utilizando LIKE, este comando está relacionado con un signo de porcentaje %, podemos rastrear clientes que contengan la palabra gourmet de la siguiente forma

SELECT * FROM Customers WHERE CustomerName LIKE "%Gourmet%";

si la palabra que buscamos se encuentra al inicio utilizamos gourmet% si sabemos que la oración que buscamos se inicia con "gour" y termina con "met" se escribe gour%met etc etc.

### SELECT * FROM Customers WHERE CustomerName LIKE "Gourmet%";










