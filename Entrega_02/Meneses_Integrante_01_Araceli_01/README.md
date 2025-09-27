# Documentación base de datos INAPI 
## 1. Proceso de limpieza de datos
El proceso de limpieza se realizó de manera manual, dado que los informes de INAPI contienen miles de registros anuales sin clasificar por rubro. Los pasos fueron:

Descarga de informes (2009–2025) desde el portal oficial de INAPI.

Filtrado preliminar con función de búsqueda (Ctrl+F) de las palabras clave: vegano, vegetariano, veggie y plant based.

Extracción de coincidencias: se copiaron los resultados que contenían esas palabras en su nombre o descripción de marca.

Depuración manual: se revisó en internet cada marca para determinar si efectivamente correspondía al rubro alimentario vegano/vegetariano.

Ejemplo: se descartaron marcas de ropa vegana o cosméticos cruelty free, ya que no pertenecen a la industria alimentaria.

Se mantuvieron restaurantes, productores de alimentos, tiendas especializadas, servicios de delivery y marcas de productos procesados veganos.

Estandarización de variables: se construyeron cinco columnas homogéneas:

- Nombre de la marca.

- Año de registro.

- Tipo de negocio (producto/servicio/ambos).

- Estado de tramitación.

- Región del solicitante.

- Consolidación en un archivo Excel único que integra todas las observaciones entre 2009 y 2025.

Este procedimiento fue lento y artesanal, pero necesario para lograr un dataset enfocado únicamente en la industria alimentaria vegana.

## 2. Fuentes de datos utilizadas y razones de selección
Instituto Nacional de Propiedad Industrial (INAPI):

Es la institución oficial que concentra todas las solicitudes y registros de marcas en Chile.

Permite acceder a series históricas desde 2009.

Su acceso es público y gratuito, lo que garantiza transparencia y replicabilidad del proceso.

Se descartaron otras fuentes (encuestas de consumo, catálogos comerciales, directorios privados), porque no ofrecían un panorama longitudinal ni desagregado en el tiempo.

## 3. Preguntas que se pueden responder con la base de datos limpia
3.⁠ ⁠Preguntas que se pueden responder con la base de datos limpia

La base permite responder preguntas relevantes para el reportaje, como:

¿Existe una tendencia de crecimiento en el registro de marcas veganas en Chile entre 2009 y 2025?

Permite identificar los años con mayor explosión de registros y contextualizar el auge del rubro.

¿Qué tipo de negocios veganos predominan en los registros?

Contrastar entre marcas que ofrecen productos (ej. snacks, hamburguesas vegetales), servicios (restaurantes, delivery) o ambos.

¿Qué regiones concentran mayor número de registros de marcas veganas?

Permite mapear si la tendencia se concentra en la Región Metropolitana o si hay crecimiento en regiones.

¿Cómo se relaciona el aumento en registros con hitos sociales o culturales en Chile?

Ejemplo: incremento a partir de 2020, que puede asociarse con mayor conciencia ambiental, el impacto de la pandemia y el auge de nuevas tendencias alimentarias.

¿Cuál es la foto actual de la industria vegana/vegetariana en comparación con su evolución histórica?

Esta base, cruzada con la principal (directorio actual de restaurantes y tiendas), permite dar contexto histórico y mostrar que el boom actual es parte de un proceso de crecimiento sostenido.