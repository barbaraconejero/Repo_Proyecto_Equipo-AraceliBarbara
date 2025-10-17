# Documentación individual

## 1. Explicación del proceso de visualización

El proceso de visualización fue realizado en base a la base de datos de los restaurantes de TripAdvisor. Ambas consideramos que esta base de datos, por la cantidad numérica y variedad de variables, ofrecía la posibilidad de insights interesantes.

En un principio pensé mi subhistoria en una tendencia que había palpado a priori cuando estaba realizando la base de datos, la cual era una mayor cantidad de restaurantes asiáticos dentro de la oferta gastronómica vegana. Para ello agregué dos variables: la de **origen geográfico**, que determinaría el tipo de cocina, además de la variable de **tipo de local**, según si era restaurante, cafetería, bar, entre otros.

El problema fue que, al pasar esta información al gráfico de Python, los datos mostraban lo contrario, de manera que mi subhistoria por los datos se caía. Pero me di cuenta de que, si bien no había una muestra amplia de restaurantes asiáticos veganos, estos tenían en general un buen rating según la aplicación de TripAdvisor. Ahí es cuando decidí cambiar la historia con el fin de hacer un análisis y descubrir qué relación existía entre cierto tipo de cocina y la valoración que tenía en la app.

Lo que descubrí fue que la oferta asiática, ya sea cocina tailandesa, coreana, japonesa, india, china o fusiones (entre ellas o que incluyen algún tipo de cocina asiática), es ampliamente valorada por los santiaguinos.

Pero para llegar a esa conclusión, tuve que pasar primero por la creación de un gráfico de barras que me refutó mi hipótesis inicial (la que indidcaba mayor número de restaurantes asiáticos), después por un pictograma que terminé descartando porque la variable de orige geográfico, tanto para el eje x como para el y, quedaba muy largo y poco entendible. Hasta que finalmente revisitandi la librería de Altair llegué a la deicisión de que una gráfico de barras que resaltara los valores más altos.

El procedimiento en Google Colab fue el siguiente:

1. Se cargó la base de datos `base_tripadvisor_visualización_cocina_asiática.csv` utilizando la librería `pandas`.
2. Se calculó el **promedio de ratings por origen geográfico** para tener un valor representativo de cada categoría.
3. Se definió un **valor de referencia de 4.5** para resaltar aquellos orígenes geográficos con rating superior a este número.
4. Finalmente, se creó un **DataFrame adicional con el umbral** y se prepararon las columnas necesarias para el gráfico con `Altair`.

El gráfico se tituló **"Rating promedio por origen geográfico"** y se exportó en formato `.html` (interactivo) y `.jpg` (estático).

---

## 2. Base de datos utilizada

- **Nombre:** base_tripadvisor_visualización_cocina_asiática.csv  
- **Fuente:** Webscraping de TripAdvisor (2024)  
- **Número total de registros:** 180 restaurantes de la Región Metropolitana

---

## 3. Preguntas que responde la visualización

La visualización final permite abordar las siguientes preguntas derivadas del reportaje grupal:

- ¿Cuál es el rating promedio por origen geográfico?  
- ¿Qué orígenes geográficos destacan sobre el umbral de referencia (4.5)?  
- ¿Existen diferencias significativas entre las calificaciones de distintos países o regiones?  
- ¿Qué patrones o tendencias se pueden identificar en la cocina asiática?  
- ¿Qué áreas podrían considerarse de referencia o modelo para restaurantes de alta calificación?  

Aunque el gráfico no muestra directamente la oferta vegana, **contextualiza la gastronomía en Santiago** al mostrar qué tipos de cocina destacan según la percepción de los usuarios.
