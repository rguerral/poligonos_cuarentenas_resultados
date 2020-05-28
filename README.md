# poligonos_cuarentenas_resultados

Poligonos de las zonas en cuarentena actualizados a diario.

## csvs/
En la carpeta /csvs se almacenan un archivo diario con las zonas/comunas en cuarentena activas.
* Desde el 17-03-2020 (20200317.csv) hasta el 22-04-2020 (20200422.csv) se construyen las tablas manualmente a partir de la información entregada por el ministerio. Para estas tablas se utilizan poligonos de comunas extraidos de la BCN (https://www.bcn.cl/siit/mapas_vectoriales).
* A partir del 24-04-2020(20200424.csv) las tablas se construyen de forma automática a partir de la información publicada en \* . La carpeta se actualiza de forma diaria a las  12:00 P.M., generando un nuevo archivo correspondiente a las cuarentenas del día. Los nombres de los archivos tienen dos fechas: la primera corresponde a la fecha de obtención del dato y la segunda a la fecha de la ultima actualización del sitio.

\* https://www.google.com/maps/d/u/0/viewer?mid=1cdg89HnDuW_y4-aenjiJ-hBfO5rRGNF3&hl=es-419&ll=-33.53677990899952%2C-70.54145458367657&z=11

## resultados/
* cuarentenas_por_dia/: contiene el archivo consolidado de las cuarentenas (la concatenación de las tablas en csvs/)

Los siguientes resultados están solo para la Región Metropolitana:
* poligonos_cuarentenas_manzanas/: contiene la asignación de manzanas censales a los poligonos de cuarentena.
* zonas_en_poligonoscuarentena/: contiene la asignación de zonas censales a los poligonos de cuarentena.
* poblacion_en_cuarentena/: contiene la población en cuarentena por día a nivel de comunas y para el total de la RM.
