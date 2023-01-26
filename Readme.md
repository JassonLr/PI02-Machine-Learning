![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)
​
# Proyecto individual 2
​
¡Bienvenidos al segundo proyecto! Durante estos días estarán poniendo en práctica sus habilidades en el campo de la predicción de datos. Deberán usar cierta métrica para medir la performance del/los modelo/s la cual, a su vez, será usada para elegir los mejores modelos.

## Información relevante
​
Este proyecto es una instancia de evaluación, por lo cual es INDIVIDUAL y OBLIGATORIO para los alumnos de Data Science de Henry. Se disponibilizará un Google Form y pueden cargarse los resultados las veces que quieran. Es obligatorio que todos disponibilicen el código utilizado, para validar los modelos construidos.
​
## Mercado inmobiliario
​
El mercado inmobiliario y cómo los precios de los inmuebles han cambiado constantemente debido a la creciente demanda en las ciudades. La falta de certeza en la valorización real del sector dificulta tomar decisiones para invertir o vender una propiedad. Sin embargo, es importante poder estimar adecuadamente el valor de una propiedad para entender si es una buena oportunidad de compra o venta.

## Descripción del problema
​
Usted ha sido contactado para el área de Machine Learning de una importante empresa inversora dentro del rubro de la inmobiliaria en Estados Unidos. 
​
El Team Lider le propone dos predicciones posibles, de las cuales puede elegir cuál realizar (o ambas si así lo quiere):
​
1. Implementar un modelo de clasificación con aprendizaje supervisado que permita clasificar el precio de las propiedades en venta, utilizando los datos que se han puesto a su disposición.
​
Para esto debe crear la columna `category_price`, en la cual se consideran las categorías
   * 'low': Para precios entre 0 y 999 dólares (debe tomar valor 1 en el archivo con las predicciones).
   * 'medium': Para precios entre 1000 y 1999 dólares (debe tomar valor 0 en el archivo con las predicciones).
   * 'high': Para precios desde 2000 dólares en adelante (debe tomar valor 0 en el archivo con las predicciones). 
​
    Considerando esta categorización, el objetivo es predecir si una propiedad pertenece a la categoría de precios bajos (low).
​
2. Implementar un modelo de clasificación con aprendizaje no supervisado, utilizando clustering que agrupe las propiedades por segun las **3 categorias** a las que pueden pertenecer. Para ello, solo usaran el dataset de test provisto, eliminando previamente las caracteristicas que presenten nulos.
​
## Entrega
​
 Deben tener el código en un script .py o Jupyter Notebook .ipynb, para entrega del  proyecto en el cual se deben utilizar técnicas de EDA, Feature Engineering y, de ser posible, un pipeline de Machine Learning para procesar los datos. Es necesario incluir comentarios y explicaciones claras en el script o Notebook para que cualquier persona pueda entender el razonamiento y pasos aplicados. También se recomienda dedicar tiempo a organizar y crear un README adecuado para el repositorio. Es obligatorio generar un archivo .csv con las predicciones, con una sola columna llamada "pred" y el nombre del archivo debe ser el usuario de GitHub del entregador. El formulario de entrega debe incluir al menos un modelo (supervisado o no supervisado) y se pueden entregar varias veces.

## Métrica a utilizar
​
Como método de evaluación del desempeño, dependerá del modelo que usted decida implementar.
​
1. Para el modelo de aprendizaje supervisado, se utilizará la métrica `Accuracy` para las propiedades de precio bajo (low) a partir de la matriz de confusión (Confusion Matrix).

$$ Accuracy=\frac{TP+TN}{P+N}$$

siendo $TP$ los verdaderos positivos (las propiedades de precio 'low' que realmente lo son), $TN$ verdaderos negativos (las propiedades que realmente NO son de precio 'low') y $P+N$ población total.

Como métrica adicional para verificar el desempeño de su modelo, también se utilizará la métrica de precisión (Recall) para las propiedades baratas.

$$ Recall=\frac{TP}{TP+FN}$$

​
Donde $TP$ son los verdaderos positivos (las propiedades de precio 'low' que realmente lo son) y $FN$ los falsos negativos (las propiedades de precio 'low' que fueron marcadas incorrectamente).

​
2. Para el modelo de aprendizaje no supervisado, se utilizará la métrica `Silhouette score`.

$$ Silhouette=\frac{b_i-a_i}{max(b_i,a_i)}$$

Dónde $b_i$ es la distancia promedio al grupo más cercano desde el punto i, $a_i$ es la distancia promedio a todos los demás puntos del clúster al que pertenece el punto i. 
​
## Criterios de Evaluacion

El objetivo de este proyecto es crear un repositorio en GitHub con acceso público donde se subirá la solución propuesta en un archivo de Jupyter Notebook (.ipynb) o bien un script de Python (.py) y el archivo de texto plano con valores separados por comas (.csv) con las predicciones. El repositorio debe incluir un análisis exploratorio de los datos (EDA), un modelo de Machine Learning adecuado al problema (clasificación o regresión), o no supervisado en caso de elegir esa vía, y un readme que describa brevemente el problema y la solución propuesta. Es necesario incluir comentarios y fundamentación escrita en Markdown en el Jupyter Notebook o en un documento aparte. Es recomendable utilizar técnicas de división de dataset en train y test, y utilizar Pipelines en la producción del modelo. Es obligatorio

## Archivos provistos
​
Se proveen los siguientes archivos en formato parquet:
 - 'train.parquet': Contiene 346479 registros y 22 dimensiones, el cual incluye la información **numérica** del precio en la columna `price`.
 - 'test.csv': Contiene 38498 registros y 21 dimensiones, el cual no incluye la información del precio. 

 Link al dataset: https://drive.google.com/drive/folders/1nJ9ZMj6E6zh6McC9NwCA6KopfUIOG_1O

 ## Descripción de las dimensiones
- id: Identificador del anuncio. 
- url: Link web del anuncio.
- region: Región de Estados Unidos en donde se encuentra la propiedad.
- region_url: Link web de los anuncios pertenecientes a la región. 
- price: Precio de la propiedad en dólares.
- type: Tipo de propiedad.
- sqfeet: Metros cuadrados de la propiedad.
- beds: Cantidad de dormitorios.
- baths: Cantidad de baños.
- cats_allowed: Si se permiten gatos en la propiedad toma el valor 1, 0 para caso contrario.
- dogs_allowed: Si se permiten perros en la propiedad toma el valor 1, 0 para caso contrario.
- smoking_allowed: Si se permite fumar en la propiedad toma el valor 1, 0 para caso contrario.
- wheelchair_access: Si la propiedad posee acceso para sillas de ruedas toma el valor 1, 0 para caso contrario.
- electric_vehicle_charge: Si la propiedad posee cargador para vehículos eléctricos toma el valor 1, 0 para caso contrario.
- comes_furnished: Si la propiedad viene amueblada toma el valor 1, 0 para caso contrario.
- laundry_options: Opciones de lavandería (w/d in unit: Lavadora/secadora en la propiedad, w/d hookups: conexión para lavadora/secadora, laundry on site: servicio de lavandería en el lugar, laundry in bldg: servicio de lavandería en el edificio, no laundry on sit: sin servicio de lavandería).
- parking_options: Opciones de estacionamiento (off-street parking: zona de estacionamiento, attached garage: garaje incluido, carport: cochera/garaje abierto, detached garage: garaje separado, street parking: estacionamiento delimitado en la calle, no parking: sin estacionamiento, valet parking: estacionamiento con servicio valet).
- image_url: Link web de la imagen de la propiedad en el anuncio. 
- description: Descripción de la propiedad puesta en el anuncio. 
- lat: Latitud.
- long: Longitud.
- state: Código del estado al que pertenece la propiedad.
​
## Sugerncias

- Explorar el dataset y entender el tipo de problema y las variables de salida.
- Considerar qué tipo de modelo es aplicable según el problema y las variables.
- Investigar sobre la métrica aplicada, conociendo sus ventajas y desventajas.
- Revisar que las coordenadas geoespaciales correspondan al lugar correcto.
- Aplicar procesamiento del lenguaje natural (NLP) si hay comentarios en el dataset.
- Utilizar git branching para hacer cambios experimentales sin romper el modelo.
- Aprovechar esta oportunidad para experimentar y disfrutar el proceso de aprendizaje.