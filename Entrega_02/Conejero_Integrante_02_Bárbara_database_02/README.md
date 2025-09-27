# Documentación base de datos TripAdvisor
## 1. Proceso de limpieza de datos
El proceso de limpieza fue manual, ya que si bien con la ayuda de Webscrapper se pudo obtener gran parte de la información, aún así hubo algunos datos que no se descargaron por igual de todos los locales, esa información variaba entre puntuación, descripción del restaurante y el termómetro vegano.

Adicionalmente se hizo una búsqueda manual de la comuna de los locales, ya que TripAdvisor en la mayoría de los casos solo entregaba la dirección.

Como último paso manual y relacionado con lo anterior, se hizo una limpieza por Google Maps, local por local, para saber si el negocio seguía funcionando o si había cerrado temporalmente.

Una vez limpiada la base de datos se orderaron los datos que había entregado TripAdvisor ( Nombre del local, Rango de precio, Dirección, Rating, Ranking en Santiago, Descripción, Horario,Traveller´s Choice Award, Información sobre el tipo de cocina o consumo y si ofrecían opciones veganas ) en 11 columnas homogéneas (descartándose algunos datos que no se consideraban relevantes):
- Nombre del negocio

- Descripción

- Tipo

- Dirección

- Comuna

- Nivel de precio

- Termómetro vegano

- Tipo de cocina

- Consumo

- Ranking

- Ranking en Santiago

## 2. Fuentes de datos utilizadas y razones de selección
### Fuente de datos
TripAdvisor: es un sitio web que proporciona reseñas, calificaciones y datos de restaurantes bares, cafeterías, panoramas y hoteles a nivel mundial.

La elegimos porque permite acceder a un gran catálogo de ofertas de restaurantes y filtrar según ciudad y tipo de cocina (en este caso vegana o con opciones veganas). Además su acceso es público y gratuito.

## 3. Preguntas que se pueden responder con la base de datos limpia
La base permite responder preguntas relevantes para el reportaje, como: 
- ¿Existe relación entre el nivel de precio de los restaurantes y qué tan veganos son?

- ¿Qué tipos de cocina ofrecen más opciones veganas?

- ¿Cómo se distribuen georgráficamente los restaurantes con mayor reconocimiento respecto a la oferta vegana?

Además de las ya planteadas para la investigación general:
- ¿Cómo ha crecido la oferta de restaurantes veganos en Santiago en los últimos años?

- ¿En qué sectores de Santiago se concentra la oferta gastronómica vegana?

- ¿Cuántos restaurantes no veganos han incorporado opciones veganas en sus menús?

- ¿Existe relación entre la inclusión de platos vegetarianos como estándar en restaurantes y la apertura de espacio para que lo vegano ocupe el lugar que antes tuvieron las opciones vegetarianas?