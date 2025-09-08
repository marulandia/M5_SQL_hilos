Descripción:

Este script genera el esquema mydb en MySQL para administrar clientes, proveedores, hilos y ventas. Incluye la creación de tablas, carga de datos de ejemplo y consultas para practicar DDL y DML.

Tablas principales
-Clientes: datos de los clientes.
-Proveedores: empresas que surten hilos.
-Hilos: inventario de hilos (color, cantidad, código).
-Ventas: cabecera de ventas con cliente y fecha.
-Proveedores_has_Hilos: tabla puente (relación muchos-a-muchos).
-Ventas_has_Hilos: detalle de ventas (qué hilos y cuántos).


Relaciones
-Un cliente puede tener muchas ventas.
-Una venta contiene varios hilos.
-Un hilo puede ser surtido por varios proveedores.

Contenido del script
-Creación de tablas con claves primarias, foráneas y restricciones (CHECK, UNIQUE).
-Inserción de datos de ejemplo: 5 clientes, 3 proveedores, 12 hilos, 7 ventas y detalles.
-Consultas SELECT con JOIN, GROUP BY, HAVING.

Notas:
El script está diseñado para MySQL 8.0+ (los CHECK funcionan desde 8.0.16).
Las claves foráneas están con ON DELETE CASCADE, por lo que al borrar un cliente, proveedor o hilo, se eliminan también sus relaciones.

Hecho por: María Eugenia Martínez
