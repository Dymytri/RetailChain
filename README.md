# RetailChain
¿Cuántas filas devuelve cada consulta y por qué son distintas? Explicá con ejemplos concretos de los datos qué filas se eliminaron con UNION.
Con UNION devuelve 11 filas, mientras que con UNION ALL devuelve 14 filas. Los productos con ID 103, 104 y 106, al estar duplicados, en UNION se ignoran y en UNION ALL se contemplan.

¿Por qué UNION ALL es más eficiente que UNION? ¿Qué operación adicional realiza UNION internamente que consume más recursos?
UNION ALL es mas eficiente porque no compara registros para buscar duplicados, solo arma todo como esta. UNION, al contrario, compara registros para eliminar duplicados.

¿En qué casos de negocio usarías cada uno? Dá al menos dos ejemplos reales distintos a los del ejercicio.
Utilizaria UNION para crear una lista de productos disponibles en una tienda, una lista de clientes registrados como compradores o una lista de mails para generar una difusion.
Utilizaria UNION ALL para ver la cantidad de ventas por cliente de diferentes sucursales o la cantidad de stock disponible de distintos productos de varias tiendas de ropa.

¿Qué pasa si las columnas de ambas consultas no coinciden en número o tipo? ¿Qué error genera SQL?
SQL advierte a traves de un error que para utilizar UNION debemos tener igual numero y tipo de columnas en las target list.
