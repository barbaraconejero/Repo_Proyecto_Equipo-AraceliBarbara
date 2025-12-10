
# Ficha técnica de las bases de datos

## 1. Gráfico oferta según comunas
Nombre del dataset: Tripadvisor_database_limpia.csv  
Fuente: TripAdvisor (2024), obtenida mediante webscraping.  
Cobertura geográfica: Santiago, Región Metropolitana de Chile.  
Número total de registros: 163 restaurantes, bares y cafeterías.
Año de levantamiento: 2025 
Formato del archivo: CSV  

### Características de los datos

El conjunto de datos contiene información sobre restaurantes, cafeterías y bares de Santiago con oferta vegana, vegetariana o plant-based. La base fue obtenida mediante webscraping en TripAdvisor y posteriormente limpiada manualmente para eliminar duplicados, corregir valores vacíos y estandarizar los nombres de comunas.

Para la visualización final se trabajó únicamente con las variables relacionadas con la localización y el conteo de restaurantes, con el fin de mostrar la distribución de la oferta vegana y vegetariana por comuna.

### Variables incorporadas

| Variable | Descripción |
|-----------|-------------|
| Nombre | Nombre del restaurante registrado en TripAdvisor. Se utilizó solo para contabilizar la cantidad de locales por comuna. |
| Comuna | Comuna donde se ubica cada restaurante dentro de la Región Metropolitana. Es la variable principal de la visualización. |
| Cantidad | Total de restaurantes agrupados por comuna. Esta variable fue creada a partir del conteo con value_counts() en pandas. |

### Observaciones

- Se detectó un registro sin información en la columna Comuna correspondiente al restaurante “Mamma Lucia”. Este fue verificado manualmente en Google Maps y clasificado en la comuna de Colina.  
- Se estandarizaron los nombres de comunas para evitar duplicidades (por ejemplo, “Ñuñoa” en lugar de “Nunoa”).  
- La base no presenta valores nulos en las columnas utilizadas para la visualización.  
- El gráfico final representa el número de restaurantes por comuna, ordenados de mayor a menor, mostrando la concentración de la oferta vegana y vegetariana en el cono oriente de Santiago.  
- Los datos corresponden al estado de TripAdvisor al primer semestre de 2024.

## 2. Gráfico ranking restaurantes veganos
Nombre del dataset: Tripadvisor_database_limpia.csv  
Fuente: TripAdvisor (2024), obtenida mediante webscraping.  
Cobertura geográfica: Santiago, Región Metropolitana de Chile.  
Número total de registros: 152 restaurantes.
Año de levantamiento: 2025 
Formato del archivo: CSV  

### Características de los datos

El conjunto de datos contiene información únicamente sobre restaurantes, ya que se uso como punto de referencia la muestra de 3.950 restaurantes que Tripadvisor contempla en su ranking, siendo las cafeterías y bares excluidas de este ranking. La base fue obtenida mediante webscraping en TripAdvisor y posteriormente limpiada manualmente para eliminar duplicados, corregir valores vacíos y estandarizar los nombres de comunas.

Para la visualización final se trabajó con las variables de rating, ranking en Santiago y tipo de local.

### Variables incorporadas

| Variable | Descripción |
|-----------|-------------|
| Nombre | Nombre del restaurante registrado en TripAdvisor. Se utilizó para contabilizar la cantidad de locales veganos dentro del ranking. |
| Rating | Evaluación que los usuarios le entregan a cada restaurante en una escala de 1 a 5. |
| Ranking en Santiago | Se utilizó como medida de referencia para saber en qué posición estaba cada restaurante de la muestra total de 3.950 que están en el ranking. |
| Tipo de local | Se utilizó para limpiar la base e identificar únicamente restaurantes. |

### Observaciones
- El gráfico permite identificar un fenómeno clave: los restaurantes veganos no solo están representados en el ranking, sino que algunos ocupan lugares destacados, con varios de ellos ubicados dentro del top 10 general. Esto se observa inmediatamente porque existen marcas en el extremo derecho del eje, donde el rango es más competitivo.

- La gran mayoría está dentro del top 200, a pesar que representan alrededor del 4% de la muestra. Lo que puede llevar a conclusiones de que más que la cantidad lo que importa es la calidad.

- Dentro de los restaurantes veganos también están contemplados los "no tradicionalmente veganos" que, en general, corresponden a restaurantes de cadena. Lo que puede indicar que los restaurantes nuevos han tenido que adoptar estas opciones para ser más competitivos dentro del mercardo gastronómico.

## 3. Visualización mapa de oferta gastronómica vegana en Santiago con datos de TripAdvisor
Nombre del dataset: restorants
Fuente: TripAdvisor (2024), obtenida mediante webscraping.
Cobertura geográfica: Santiago, Región Metropolitana de Chile. 
Número total de registros: 180 restaurantes, bares y cafeterías.
Año de levantamiento: 2025
Formato del archivo: CSV

### Características de los Datos: 
El conjunto de datos contiene información sobre restaurantes, cafeterías y bares en Santiago que ofrecen opciones veganas o vegetarianas. La base fue obtenida mediante webscraping desde TripAdvisor y posteriormente limpiada manualmente para eliminar duplicados, corregir valores vacíos y estandarizar nombres de comunas. 

Para la visualización final, se trabajó únicamente con las variables relacionadas con la localización y el conteo de restaurantes, con el objetivo de mostrar la distribución de la oferta vegana y vegetariana por comuna. 

### Variables incorporadas
| Variable  | Descripción |
|-----------|-------------|
| **Dirección** | Dirección completa de cada restaurante. Utilizada para identificar la ubicación de cada local. |
| **Latitud** | Coordenada geográfica (latitud) del restaurante. |
| **Longitud** | Coordenada geográfica (longitud) del restaurante. |

### Observaciones 
- Se estandarizaron las direcciones y nombres de las comunas para evitar duplicidades en los registros.
- Los datos fueron obtenidos directamente de TripAdvisor a través de webscraping y reflejan la oferta gastronómica vegana y vegetariana disponible en Santiago al primer semestre de 2024.

 ## 4. Gráfico INAPI 
 Nombre del dataset: BASE DE DATO MARCAS VEGGIES Y HAMBURGUESAS (1).csv
 Fuente: MARCAS REGISTRADAS EN INAPI DESDE 2009 - 2025
 Cobertura geográfica: Nacional (Chile)
 Número total de registros: De categoría alimentación vegana: 74. Categoría hamburguesas: 141.
 Año de levantamiento: 2025
 Formato del archivo: CSV

 ### Características de los Datos:
El conjunto de datos contiene información sobre marcas registradas en INAPI entre los años 2009 y 2025 de productos alimentarios veganos y hamburguesas. Cada registro representa una marca de producto o servicio en el mercado con las siguientes características, como año de lanzamiento y su clasificación como "VEGGIE" o "BURGER". 


 ### Variables incorporadas
Variable          | Descripción |
|-------------------|-------------|
| **Año**           | Año de registro de la marca. |
| **Marca**         | Nombre de la marca o producto. |
| **VEGGIE**        | Indicador de si el producto es vegano/vegetariano |
| **BURGER**        | Indicador de si el producto o servicio es de hamburguesas
 ### Observaciones 
Las palabras clave que se utilizaron para filtrar los datos en el registro de inscripción de marca en INAPI de 2009 a 2025 fueron para categoría vegano ("veggie", "vegan", "vegetariano", "plant-based") y para categoría hamburguesas ("burger" y "hamburguesa"). 

 ## 5. Gráfico tipos de cocina por comuna
Nombre del dataset: Tripadvisor_database_limpia.csv  
Fuente: TripAdvisor (2024), obtenida mediante webscraping.  
Cobertura geográfica: Santiago, Región Metropolitana de Chile.  
Número total de registros: 163 restaurantes, bares y cafeterías.
Año de levantamiento: 2025 
Formato del archivo: CSV 

Características de los datos
El conjunto de datos contiene información sobre el tipo de cocina que predomina en cada comuna. Se usó la misma base de ofertas por comunas pero se usó solo la información de las comunas de Santiago Centro, Providencia, Las Condes y Vitacura. Se tomaron en cuentas las variaciones y fusiones de cocinas existentes de cada restaurante hasta determinar categorías macro de tipo de cocina.

| Variable | Descripción |
|-----------|-------------|
| Nombre | Nombre del restaurante registrado en TripAdvisor. Se utilizó solo para contabilizar la cantidad de locales por comuna. |
| Comuna | Comuna donde se ubica cada restaurante dentro de la Región Metropolitana. En este caso se consideró solo las comunas de Santiago Centro, Providencia, Las Condes y Vitacura. |
| Tipo de cocina| Tipo de cocina predominante según las categorías de “otras” (cocina contemporánea, saludable, fusiones), “asiática” (china, japonesa, coreana, tailandesa, india)“italiana” (pizzería, pastas) “mediterránea” (española, griega) y “latinoamericana” (chilena, caribeña, peruana). |

### Observaciones

- El principal hallazgo tiene que ver con la variedad de cocinas. Si bien había una cierta tendencia en algunas comunas sobre otras, en general, todas presentaban gran variedad culinaria. Lo que reafirma nuestra hipótesis de que lo vegano ha encontrado un lugar en todos los tipos de restaurantes.
