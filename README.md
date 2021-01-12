# Aprendiendo bases de datos
-- esto es un comentario que no afecta al Query (Query son las intrucciones que se dan mediante el código).
-- Antes de comenzar entra al siguiente link que sirve para ejecutar la sintaxis SQL en linea .
--https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all 
SELECT * FROM [Orders]
-- Seleccionamos todos "*" los elementos contenidos en la tabla Poducts
-- al concluir una sentencia es necesario terminar con un ; para que las sentencias no se mezclen entre sí


--Vamos a "personalizar" las tablas, por ejemplo la tabla Orders contiene las columnas OrderID, CustomerID, EmployeeID...
--pediremos una tabla  que solo contenga las columnas OrderID y EmployeeID
SELECT  OrderID, CustomerID FROM Orders;
