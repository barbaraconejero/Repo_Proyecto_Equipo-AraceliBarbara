# Ficha técnica de la base de datos

**Nombre del dataset:** base_tripadvisor_visualización_cocina_asiática.csv  
**Fuente:** TripAdvisor (2024), obtenida mediante webscraping.  
**Cobertura geográfica:** Santiago, Región Metropolitana de Chile.  
**Número total de registros:** 163 restaurantes.  
**Año de levantamiento:** 2024  
**Formato del archivo:** CSV  

## Características de los datos

El conjunto de datos contiene información sobre restaurantes, cafeterías y bares de Santiago con sus respectivos ratings, ubicación y oferta vegana o vegetariana. La base fue obtenida mediante webscraping en TripAdvisor y posteriormente se le agregó la variable de origen geográfico para detallar el tipo de cocina.

Para la visualización final se trabajó únicamente con las variables relacionadas con el origen geográfico y el rating.

## Variables incorporadas

| Variable | Descripción |
|-----------|-------------|
| Origen geográfico | Variable creada para detallar el tipo de cocina de cada restaurante (por ejemplo, tailandesa, coreana, japonesa, india, china o fusiones). |
| Rating | Calificación promedio de cada restaurante según TripAdvisor (valores numéricos de 1 a 5). |

## Observaciones

- Algunas entradas corresponden a cocinas fusionadas, es decir, combinaciones de más de un tipo de cocina asiática (por ejemplo, tailandesa-japonesa o china-fusión), lo que refleja que algunos restaurantes no se ajustan a un único origen geográfico.  
- También existen casos de fusiones entre cocina asiática y otros tipos, como europea o latinoamericana.  
- A la base se agregaron manualmente algunos restaurantes que no aparecían en el webscraping inicial, principalmente vinculados a la oferta vegana dentro de la categoría de restaurantes asiáticos.

