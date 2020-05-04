# Práctica: Módulo Deep Learning - Bootcamp KeepCoding - BIG DATA & MACHINE LEARNING

# Deep Learning

En este práctica se utilizan y comparan distintas **redes neuronales** sobre datos numércios para ser capaces de predecir el precio de
viviendas de Airbnb. Así mismo se trabaja con redes neuronales **convolucionales** para el tratamiento de imágenes y finalmente
se combinan datos numéricos e imágenes para predecir el precio de viviendas Airbnb. El código está desarrollado en Python.

Estas técnicas se utilizan tanto para resolver un problema de regresión como de clasificación

Conceptos tratados en esta práctica:

- Librerías **numpy**, **pandas**, **Sklearn** y **Keras** de Python 
- División de datos en train y test
- Limpieza y procesamiento de datos
- Generación de nuevas características
- Análisis exploratorio de variables de tipo numérico. Datos estadísticos, distribuciones
- Tratamiento de outliers
- Análisis exploratorio de variables de tipo categórico
- Análisis exploratorio de variables de tipo booleano
- Codificación de variables categóricas
- Análisis de correlación
- Estandarización y normalización
- Modelado con redes neuronales usando solo datos numéricos
     - Redes neuronales con varias capas densas
     - Redes neuronales con regularización de tipo L1 y Dropout
- Modelado con redes convolucionales usando solo imágenes     
     - Descarga de imágenes partiendo de URLs
     - Construcción de dataset de imágenes
     - Redes neuronales con varias capas convolucionales
     - Regularización MaxPooling2D, BatchNormalizacion y Dropout
     - Modelado usando VGG16, RestNet50 e InceptionV3 con finetunning
- Modelado con redes neuronales combinando datos numéricos e imágenes tanto para un problema de regresión como de clasificación


## Enunciado

El objetivo de la práctica es abordar un problema de Deep Learning realista siguiendo la metodología y buenas prácticas explicadas durante las clases teóricas. 

**Tarea : Implementar un algoritmo predictivo que sea capaz de estimar el precio de las viviendas Airbnb utilizando para ello datos de distintos tipos y técnicas de Deep Learning (redes neuronales profundas).**

Se realizará primero un modelado solo con datos numéricos, posteriormente un modelado con redes convolucionales usando solo imágenes y finalmente se combinaran ambos timpos de datos en un único modelo predicitivo. Se resolverá como un problema de regresión y como un problema de clasificación


## Conjunto de datos

El conjunto de datos escogido es [éste](https://public.opendatasoft.com/explore/dataset/airbnb-listings/export/?disjunctive.host_verifications&disjunctive.amenities&disjunctive.features&q=Madrid&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJ5QXhpcyI6Imhvc3RfbGlzdGluZ3NfY291bnQiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiJyYW5nZS1jdXN0b20ifV0sInhBeGlzIjoiY2l0eSIsIm1heHBvaW50cyI6IiIsInRpbWVzY2FsZSI6IiIsInNvcnQiOiIiLCJzZXJpZXNCcmVha2Rvd24iOiJyb29tX3R5cGUiLCJjb25maWciOnsiZGF0YXNldCI6ImFpcmJuYi1saXN0aW5ncyIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUuaG9zdF92ZXJpZmljYXRpb25zIjp0cnVlLCJkaXNqdW5jdGl2ZS5hbWVuaXRpZXMiOnRydWUsImRpc2p1bmN0aXZlLmZlYXR1cmVzIjp0cnVlfX19XSwidGltZXNjYWxlIjoiIiwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZX0%3D&location=16,41.38377,2.15774&basemap=jawg.streets), extraído de Airbnb mediante técnicas de scraping. Dentro de las opciones recomiendo utilizar el extract (“Only the 14780 selected records”), ya que minimiza el tiempo de ejecución y evita problemas de memoria en equipos con menos prestaciones.

## Estructura del proyecto

**data**

*airbnb_listings.csv*: Es el dataset original de airbnb, la versión reducida. Está comprimido como .zip ya que excede el tamaño permitido por Github

*airbnb_cleaned*: Es el dataset ya limpio y preparado. El el resultado de los primeros 5 puntos de la práctica y fue también el obtenido en el módulo de Machine Learning

*airbnb_segun_img*: Este esl el dataset limpio y ordenado según las imágenes que tenemos y como se haya realizado la carga de estas. Se usará cuando se combinen datos numéricos e imágenes para el modelo. Este archivo se obtiene en el punto 8.2 de la práctica

imagenes

Son todas las imágenes descargas partiendo del campo "Picture URL" que está en el dataset de airbnb. El nombre de cada archivo coinicide con el ID del anuncio de airbnb. La descarga de estas imágenes se realiza en el punto 8.1 de la práctica

datasetImagenes

X.pickle: es el dataset ya preparado extraido desde las imágenes, contiene una estructura (1271x50x50x3)

Y.pickle: es el dataset con los precios extraidos a partir del ID de las imágenes y buscando en el dataset de airbnb

Estos dos archivos se obtienen en el punto 8.2

     
    
     

