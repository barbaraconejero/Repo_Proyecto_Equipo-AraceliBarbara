# Documentación individual

## 1. Explicación del proceso de visualización

El proceso de visualización comenzó con la exploración de la base de datos que realizamos mediante webscraping en TripAdvisor, que reúne información de 163 restaurantes ubicados en Santiago con opciones veganas, vegetarianas o plant-based.

En un principio, el objetivo de mi visualización era comparar la cantidad de restaurantes 100 % veganos con aquellos locales tradicionales que solo incorporan opciones veganas en su carta, con la intención de observar cómo los negocios gastronómicos han debido adaptarse a esta tendencia alimentaria.

Para ello, intenté crear una nueva columna en Google Colab que clasificara los restaurantes según su “grado de veganismo”. Sin embargo, al revisar la base de datos con más detalle, noté que los valores en la columna “Termómetro vegano” no eran uniformes: las categorías se repetían con ligeras variaciones (“Apto para vegetarianos y opciones veganas”, “Apto para vegetarianos, opciones veganas y opciones sin gluten”, etc.), lo que impedía agrupar los datos de manera confiable sin una limpieza manual extensa.

Debido al tiempo disponible y a la dificultad de validar uno por uno los restaurantes, decidí cambiar el enfoque de la visualización hacia un aspecto más sólido dentro de la base: la distribución geográfica de los locales según comuna. Esta variable estaba completa, permitía un análisis más claro y se relacionaba directamente con una de las preguntas centrales del reportaje con la que hemos ido trabajando en todas las entregas:

¿En qué sectores de Santiago se concentra la oferta gastronómica vegana?

Así, el proceso de visualización se centró en mostrar cuántos restaurantes con opciones veganas o vegetarianas existen en cada comuna de Santiago.

En Google Colab, el procedimiento fue el siguiente:

1. Se cargó la base de datos Tripadvisor_database_limpia.csv utilizando la librería pandas.
2. Se verificó la existencia de datos faltantes en la columna Comuna, encontrándose un caso sin información (“Mamma Lucia”), el cual fue revisado manualmente en Google Maps y clasificado correctamente en la comuna de Colina.
3. Se realizó un conteo de registros por comuna utilizando el método value_counts().
4. Los resultados se almacenaron en un nuevo DataFrame con las columnas Comuna y Cantidad, lo que permitió visualizar cuántos restaurantes hay por zona.
5. Finalmente, se utilizó la librería Altair para construir un gráfico de barras horizontal, donde las comunas se ordenaron de mayor a menor según su número de restaurantes.

El gráfico se tituló “Dónde se concentra la oferta vegana y vegetariana en Santiago” y se exportó en formato .html (interactivo) y .jpg (estático).

Este cambio de enfoque me permitió obtener una visualización más clara, coherente con la hipótesis grupal y con una narrativa visual que evidencia de forma directa la desigualdad territorial del acceso a la alimentación basada en plantas en la capital.

---

## 2. Base de datos utilizada

Nombre: Tripadvisor_database_limpia.csv  
Fuente: Webscraping de TripAdvisor (2024)  
Número total de registros: 163 restaurantes de la Región Metropolitana.

### Motivo de selección
Esta base fue elegida porque ofrece una radiografía actual de la oferta gastronómica vegana en Santiago, con información pública, verificable y comparable entre comunas. Además, su nivel de detalle permite analizar tanto la localización como el tipo de cocina, precio y características de los locales.

### Procesamiento de la base
- Se eliminaron duplicados y filas vacías.  
- Se revisó manualmente la columna “Comuna” para completar valores faltantes.  
- Se estandarizaron los nombres de comunas (por ejemplo, “Ñuñoa” en lugar de variantes como “Nunoa”).  
- Se exportó el archivo limpio en formato .csv para su uso en la visualización.

---

## 3. Preguntas que responde la visualización

La visualización final permite abordar las siguientes preguntas derivadas del reportaje grupal:

- ¿Dónde se concentran los restaurantes veganos y vegetarianos en Santiago?  
- ¿Qué comunas presentan una oferta reducida o nula de opciones basadas en plantas?  
- ¿Qué relación existe entre el nivel socioeconómico de las comunas y la presencia de este tipo de restaurantes?  
- ¿De qué manera la localización de los locales refleja las desigualdades territoriales en torno al acceso a opciones veganas?

Estas preguntas complementan la hipótesis general del proyecto, mostrando que la expansión del veganismo en Santiago no se distribuye de forma uniforme, sino que responde a factores culturales y socioeconómicos que delimitan el mapa gastronómico de la ciudad.
