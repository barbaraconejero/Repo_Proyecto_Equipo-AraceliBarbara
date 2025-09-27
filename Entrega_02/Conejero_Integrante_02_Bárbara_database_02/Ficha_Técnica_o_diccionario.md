# Ficha técnica base de datos base de datos TripAdvisor
## Fuente de los datos
Los datos fueron obtenidos de TripAdvisor, un sitio web público que recopila reseñas, calificaciones y datos de restaurantes, bares, cafeterías y otros negocios gastronómicos a nivel mundial. Se eligió esta fuente por su amplio catálogo de establecimientos en Santiago y porque permite filtrar locales según tipo de cocina, incluyendo opciones veganas.

## Metodología de la construcción de la base
Se utilizó webscraping para descargar automáticamente la información disponible de cada local en TripAdvisor. Posteriormente, se realizó un proceso manual de limpieza y estandarización, que incluyó: verificación de la comuna de cada local mediante Google Maps, confirmación de que los negocios seguían activos, homogeneización de variables y descarte de información irrelevante. La base final se organizó en 11 columnas homogéneas, permitiendo comparaciones consistentes entre locales y comunas.

## Alcance de los datos
La base incluye únicamente restaurantes, bares y cafeterías con opciones veganas ubicados en Santiago, Chile, considerando la información disponible hasta agosto de 2025. Contiene registros de nombre del local, descripción, tipo de establecimiento, dirección, comuna, nivel de precio, termómetro vegano, tipo de cocina, consumo, ranking general y ranking dentro de Santiago. Excluye locales cerrados permanentemente o sin información mínima.

Desde un alcance analítico, la base permite explorar la distribución geográfica de la oferta vegana, concentración de locales por comuna, relación entre tipo de cocina y opciones veganas, comparación de niveles de precio y patrones de visibilidad según ratings y premios. No permite análisis de ventas ni cambios históricos detallados en menús.

## Características de los datos
La base está en formato CSV con codificación UTF-8, con un total de 164 registros. Contiene variables textuales (nombre del negocio, descripción, tipo de cocina), categóricas (tipo de local, comuna, tipo de consumo) y numéricas (ranking, rating, nivel de precio). Todos los datos están estandarizados, las columnas homogenizadas y la información verificada para asegurar consistencia. La cobertura geográfica se limita a Santiago y temporalmente incluye datos hasta agosto de 2025.

## Variables incorporadas 
- Nombre del negocio: nombre oficial.

- Descripción: escrita por cada restaurante y en el caso de no tener eso fue señalado.

- Tipo: tipo de local, es decir, restaurante, bar o cafetería.

- Dirección: dirección con calle y número.

- Comuna: comuna de Santiago donde se ubical el local.

- Nivel de precio: TripAdvisor tiene la categorízación de rango de precio según signo de pesos. Siendo un $ la opción más económica, $$-$$$ la intermedia y $$$ la más cara.

    Según lo que averiguamos no hay una estandarización de esta simbología, ya que es algo que varia de país a país, así que decidimos traducir esa simbología en niveles de precio quedando de la siguiente forma:

        - $ : Económico
        - $$ - $$$: Gama media
        - $$$: Más caro


- Termómetro vegano: es la forma en la que medidmos si el local es apto para vegetarianos, tiene opciones veganas e incluso si tiene opciones sin gluten.

- Tipo de cocina: si es de algún país en específico o si es una fusión.

- Consumo: si el local permite comer en el lugar (Servicio de mesa), permite llevar la comida (Comida para llevar) y si es que hace entregas a domicilio (Entrega a domicilio).

- Ranking: el ranking que hacen los usuarios de la aplicación desde el 1 al 5. Siendo 1 la más baja y 5 la más alta. Se consideran aspectos de atención, calidad del servicio, ambiente, entre otros.

- Ranking en Santiago: en qué posición está ubicado cada tipo de local según los registros del sitio.

## Otras observaciones
Puede haber un sesgo en qué tan completa es esta radiografía ya que se incluyen únicamente los que son reseñados o registrados en el sitio, es decir, que pueden escaparse locales que no estén en TripAdvisor.

Muchos locales no tenían descripción al igual que muchos no tenían el Traveller´s Choice Award razón la que se decidió eliminar esta categoría, sumado al hecho de que no nos parecía imprescindible. 

En cuanto al horario si bien es un factor interesante no lo incluimos porque no estaba incluido en todos los locales y porque nos parecía un mejor parámetro si está abierto durante la semana o fin de semana.