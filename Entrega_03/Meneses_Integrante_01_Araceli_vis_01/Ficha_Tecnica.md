
# Ficha técnica de la base de datos

Nombre del dataset: Tripadvisor_database_limpia.csv  
Fuente: TripAdvisor (2024), obtenida mediante webscraping.  
Cobertura geográfica: Santiago, Región Metropolitana de Chile.  
Número total de registros: 163 restaurantes.  
Año de levantamiento: 2024  
Formato del archivo: CSV  

## Características de los datos

El conjunto de datos contiene información sobre restaurantes, cafeterías y bares de Santiago con oferta vegana, vegetariana o plant-based. La base fue obtenida mediante webscraping en TripAdvisor y posteriormente limpiada manualmente para eliminar duplicados, corregir valores vacíos y estandarizar los nombres de comunas.

Para la visualización final se trabajó únicamente con las variables relacionadas con la localización y el conteo de restaurantes, con el fin de mostrar la distribución de la oferta vegana y vegetariana por comuna.

## Variables incorporadas

| Variable | Descripción |
|-----------|-------------|
| Nombre | Nombre del restaurante registrado en TripAdvisor. Se utilizó solo para contabilizar la cantidad de locales por comuna. |
| Comuna | Comuna donde se ubica cada restaurante dentro de la Región Metropolitana. Es la variable principal de la visualización. |
| Cantidad | Total de restaurantes agrupados por comuna. Esta variable fue creada a partir del conteo con value_counts() en pandas. |

## Observaciones

- Se detectó un registro sin información en la columna Comuna correspondiente al restaurante “Mamma Lucia”. Este fue verificado manualmente en Google Maps y clasificado en la comuna de Colina.  
- Se estandarizaron los nombres de comunas para evitar duplicidades (por ejemplo, “Ñuñoa” en lugar de “Nunoa”).  
- La base no presenta valores nulos en las columnas utilizadas para la visualización.  
- El gráfico final representa el número de restaurantes por comuna, ordenados de mayor a menor, mostrando la concentración de la oferta vegana y vegetariana en el cono oriente de Santiago.  
- Los datos corresponden al estado de TripAdvisor al primer semestre de 2024.
