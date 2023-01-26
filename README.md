# Machine Learning   

##  Proyecto de Clasificación de precios de propiedades inmobiliarias en Estados Unidos

El mercado inmobiliario y cómo los precios de los inmuebles han cambiado constantemente debido a la creciente demanda en las ciudades. La falta de certeza en la valorización real del sector dificulta tomar decisiones para invertir o vender una propiedad. Sin embargo, es importante poder estimar adecuadamente el valor de una propiedad para entender si es una buena oportunidad de compra o venta.

##  Descripcion del problema

### Utilizando técnicas de aprendizaje supervisado y no supervisado para predecir la categoría de precios de las propiedades en venta.

El problema presentado en el proyecto es la necesidad de clasificar el precio de las propiedades inmobiliarias en venta en Estados Unidos para una empresa inversora. Se proponen dos posibles soluciones:

1. Usando un modelo de clasificación con aprendizaje supervisado para predecir si una propiedad pertenece a la categoría de precios bajos. Para esto, se sugiere crear una columna "category_price" con las categorías "low", "medio" y "high" y utilizar el conjunto de datos proporcionados para entrenar el modelo.

2. Usar un modelo de clasificación con aprendizaje no supervisado usando clustering para agrupar las propiedades por las 3 categorías de precios. Se sugiere utilizar solo el conjunto de datos de prueba provistos y eliminar las características con valores nulos antes de aplicar el algoritmo de clustering.

Las ideas clave del problema son: clasificación de precios de propiedades inmobiliarias, aprendizaje supervisado y no supervisado y utilización de técnicas de clustering.

##  Entrega

El problema presentado es la necesidad de entregar un proyecto de análisis de utilizando datos técnicos de EDA, Feature Engineering y, de ser posible, un pipeline de Machine Learning. Se requiere que el código sea entregado en un script .py o Jupyter Notebook .ipynb con comentarios y explicaciones claras para que cualquier persona pueda entender el razonamiento y los pasos aplicados. También se recomienda crear un README adecuado para el repositorio. Es obligatorio generar un archivo .csv con las predicciones y se pueden entregar varias veces.

### En el análisis exploratorio de datos para Machine Learning aprendizaje supervisado se tomo en cuenta:

  * Entender las características del conjunto de datos, como el número de registros, las columnas, los tipos de datos y la presencia de valores faltantes.
  * Use gráficos y estadísticas para explorar la distribución y la relación entre las características y la variable objetivo.
  * Identificar patrones y tendencias en los datos que pueden influir en el rendimiento del modelo.
  * Probar diferentes técnicas de preprocesamiento, como la codificación de variables categóricas, la normalización de variables numéricas y la eliminación de características irrelevantes.

la solución para el análisis exploratorio de datos se incluye los siguientes pasos:

  * Usar pandas para cargar y explorar el conjunto de datos.
  * Use matplotlib y seaborn para generar gráficos que ilustren la distribución y las relaciones entre las características y la variable objetivo.
  * Utilizando técnicas de preprocesamiento, como la codificación de variables categóricas y la eliminación de características irrelevantes, para preparar el conjunto de datos para el entrenamiento del modelo.
  * Use scikit-learn para dividir el conjunto de datos en conjuntos de entrenamiento y prueba y para entrenar un modelo.

### Para la solucion del Proyecto usamos un Modelo de Clasificacion con Aprendizaje Supervisado

Implementamos un modelo de aprendizaje supervisado con árbol de decisión y train_test_split para procesar los datos. El modelo se entrena con el conjunto de datos de entrenamiento y se evalúa en el conjunto de datos de prueba y se genera un archivo .csv con las predicciones del modelo.

Las ideas clave del problema son: entrega de un proyecto de análisis de datos, técnicas de EDA, Feature Engineering, pipeline de Machine Learning, modelo de aprendizaje supervisado, arbol de decisión, train_test_split y generación de un archivo .csv con las predicciones. 

Todo eso esta en los comentarios del codigo donde explica a detalle
