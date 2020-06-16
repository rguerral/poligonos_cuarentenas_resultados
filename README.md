# poligonos_cuarentenas_resultados

## resultados
### (a) cuarentenas_por_dia
Cuarentenas activas por día. Cada cuarentena tiene asociada un póligono en el formato "\[(x1,y1), (x2,y2), ...\]" donde x_i e y_i corresponden a las latitudes y longitudes de sus vertices.

### (b) shape_cuarentenas
Archivo geojson con la geometría/poligono de cada cuarentena. Análogo a la columna *geo* del resultado **(a)**. **Los nombres de los póligonos cruzan con los del resultado (a)**. Para obtener la geometria de cada cuarentena recomeindo usar el geojson en vez de la columna *geo*. Es más fácil de cargar.

### (c) manzanas_en_poligonoscuarentena
Contiene la asignación de manzanas censales a las cuarentenas. Tiene 3 asignaciones: 
(1) InFull: listado de manzanas censales cuya área está contenidas completamente en una cuarentena
(2) InPartial: listado de manzanas censales que tienen al menos un punto de su interior contenido en una cuarentena
(3) InArea0.25: listado de manzanas censales que tienen al menos el 25\% de su área contenida en una cuarentena.
En la carpeta *plots_asignacion* se puede ver graficamente cada asignacion. **Recomiendo usar InArea0.25**.
**Los nombres de los póligonos cruzan con los del resultado (a)**

### (d) zonas_en_poligonoscuarentena
Contiene la asignación de zonas censales a los poligonos de cuarentena. Tamién hay 3 asignaciones, analogas a las **manzanas_en_poligonoscuarentena**. PD: Las zonas censales de RM tienen 11 digitos y las de Region de Valpariso 10 digitos.
**Los nombres de los póligonos cruzan con los del resultado (a)**

### (e) poblacion_en_cuarentena:  
Contiene la cantidad de personas en cuarentena por día a nivel de comunas (para todo Chile) y para el total de la RM. Para calcularlo se el dato usan la poblacion de las manzanas censales (Censo2017) contenidas en cada cuarentena (InArea0.25) .

## csvs
En la carpeta /csvs se almacenan un archivo diario con las zonas/comunas en cuarentena activas.
* Desde el 17-03-2020 (20200317.csv) hasta el 22-04-2020 (20200422.csv) se construyen las tablas manualmente a partir de la información entregada por el ministerio. Para estas tablas se utilizan poligonos de comunas extraidos de la BCN (https://www.bcn.cl/siit/mapas_vectoriales).
* A partir del 24-04-2020(20200424.csv) las tablas se construyen de forma automática a partir de la información publicada en \* . La carpeta se actualiza de forma diaria a las  12:00 P.M., generando un nuevo archivo correspondiente a las cuarentenas del día. Los nombres de los archivos tienen dos fechas: la primera corresponde a la fecha de obtención del dato y la segunda a la fecha de la ultima actualización del sitio.

\* https://www.google.com/maps/d/u/0/viewer?mid=1cdg89HnDuW_y4-aenjiJ-hBfO5rRGNF3&hl=es-419&ll=-33.53677990899952%2C-70.54145458367657&z=1
