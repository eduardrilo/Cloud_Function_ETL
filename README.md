EXPLICACIÓN ARCHIVOS:

1. main: Codigo python que configura la cuenta de servicio, el nombre del bucket, el nombre de la tabla, el punto de entrada del evento, instala la api de google, toma la data del bucket y la carga en la memoria. Al final hay un control de error por carga y limpieza,
2. requirements: Instalación de las dependencias de Google, para hacer funcionar los servicios, tambien se instalan las librerias de python correspondientes.
3. bigquery: Seteo de la fecha, borrado de tabla anterior y carga de nuevos datos. Control de filas insertadas y errores. Breve query para insertar los daots en la tabla correspondiente. Control de error al finalizar la insercion de datos.
4. storage: Se descarga el archivo y se ubica en el bucket correspondiente. Control de error si es que hay problemas en la descarga. Se carga el archivo como dataframe y se torna la tabla correspondiente. Ultimo control de error si es que hay un problema con la generacióno del dataframe.
5. utility: Limpieza de data, cambio de nombre de columnas, se añade nueva columna, se eliminan otras, se ajustan formatos, parseo de campo conversation_id, todos los numeros mayores a 1, eliminar espacios vacios de la columna Fecha. Funcion para remover acentos, convertir los Nan como texto vacio, dejar todo tipo de dato como string. Por utlimo, control de error para la limpieza.
