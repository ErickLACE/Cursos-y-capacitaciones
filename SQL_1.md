# CRUD Create Read Update Delete  (operaciones básicas en bases de datos)
Antes de comenzar entra al siguiente link que sirve para ejecutar la sintaxis SQL en linea https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all

La siguiente tabla llamada Customers contiene 7 columnas CustomerID, CustomerName, ContactName, Adress, City, PostalCode, Country, si deseamos añadir una nueva fila que contenga estos datos, debe tener 7 elementos, se logra mediante el comando INSERT INTO

### INSERT INTO customers VALUES(100, "Alberto Perez", "Alberto Perez", "chimalhuacan 52", "ecatepunk", 09872, "Tangamandapio" )

Si quisieramos añadir nuevamente valores a una fila, pero que SQL asigne un valor secuencial a CustomerID se hace de la siguiente forma(No escribir nada en "CustomerID"), a esta operación suele llamarse llaves unicas o valores foraneos, valores unicos, funciona para algunos valores que pueden estar repetidos

### INSERT INTO customers( CustomerName, ContactName, Adress, City, PostalCode, Country) VALUES( "Alberto Perez", "Alberto Perez", "chimalhuacan 52", "ecatepunk", 09872, "Tangamandapio" )

Se pueden agregar mas de 1 fila de manera simultanea, cabe mencionar que utilizar rutinas de identación ayuda a mantener el orden en nuestros programas cuando son muy largos
### INSERT INTO 
###     customers( CustomerName, ContactName, Address, City, PostalCode, Country) 
### VALUES
###     ( "Alberto Lopez", "Alberto Perez", "chimalhuacan 52", "ecatepunk", 09872, "Tangamandapio" ),
###     ( "Alberto Rosado", "Beto", "Marte 52", "ecatepunk", 09994, "Nezayork" );

es posible cambiar valores a un valor que se encuentra en una fila, por ejemplo en la tabla Orders cambiamos el valor asignado en ShipperID a 6, hay que especificar que el cambio se hace sobre OrderID=10248 ya que de no especificar, el comando cambiará todos los valores en esa columna
### UPDATE Orders SET ShipperID =6 WHERE orderID=10248;
### UPDATE Orders SET ShipperID =6, EmployeeID=6 WHERE orderID=10248;

Con el siguiente comando pueden eliminarse todos los elementos de una tabla
## DELETE FROM Products

Podemos eliminar todos las filas en donde Supplier tenga valor 1, entre otras mezclas como vimos en los anteriores Quertys

### DELETE FROM Products WHERE SupplierID = 1; 
### DELETE FROM Products WHERE SupplierID = 4 AND CategoryID = 1; 



