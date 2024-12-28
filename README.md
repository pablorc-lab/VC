# Visión por computador

Prácticas de la asignatura Visión por Computador de la Escuela Técnica Superior de Ingeniería Informática (ETSIIT), perteneciente al grado de Ingeniería Informática, curso 24/25.
 

## Importante
Para utilizar correctamente las imágenes ubicadas en la carpeta `images`, es fundamental asegurarse de que esta se encuentre en la siguiente ruta dentro de nuestro Google Drive: 

`/content/drive/My Drive/`

Esto garantizará que el acceso a los archivos sea correcto y sin errores durante la ejecución del código en Google Colab.

Además, debemos descargar el dataset indicado en `https://www.kaggle.com/competitions/spr-x-ray-age/data` y almacenarlo en nuestro `/content/drive/My Drive/Colab Notebooks` 

## Práctica 1: Procesamiento de Imágenes
La práctica se centra en implementar filtros de convolución para comprender cómo se aplican en imágenes, particularmente en el cálculo de las derivadas, lo que incluye trabajar con gradientes para detectar bordes y transiciones. También se busca utilizar técnicas de filtrado lineal para identificar patrones y elementos clave, demostrando cómo estas técnicas permiten interpretar la estructura y contenido visual de una imagen. Con un enfoque práctico en procesamiento de imágenes, se trabajan transformaciones matemáticas y análisis visual, incluyendo la implementación de filtros básicos como Sobel o Laplaciano para derivadas, la exploración de cómo estos resultados ayudan a identificar características importantes como bordes o texturas, y el uso de convoluciones como base para técnicas más avanzadas de visión por computador.

### Detectar bordes
<img src="images/zebra.jpg" alt="Zebra" width="450px">
<img src="assets/p1_magnitud.png" alt="Zebra magnitud" width="450px">
<img src="assets/p1_laplacian.png" alt="Zebra laplaciana" width="450px">

### Imagen híbrida
<img src="images/einstein.bmp" alt="Einstein" width="200px"> <img src="images/marilyn.bmp" alt="Marilyn" width="200px">

<img src="assets/p1_hybrid.png" alt="Zebra laplaciana" width="450px">

### Unión de imágenes
<img src="assets/p1_manzana.png" alt="Manzana" width="250px"> <img src="assets/p1_naranja.png" alt="Naranja" width="250px"> 

<img src="assets/p1_reconstruccion.png" alt="Zebra laplaciana" width="400px">

---

## Práctica 2: Redes Neuronales Convolucionales y Explicabilidad
Esta práctica se enfoca en el desarrollo y mejora de modelos de redes neuronales convolucionales (CNN) para tareas de clasificación y regresión, utilizando el conjunto de datos CIFAR100 y el SPR X-Ray Age Prediction Challenge, junto a la biblioteca de **fastai** o **pythorch**. El objetivo principal es entrenar y optimizar redes profundas mediante técnicas como la creación de modelos desde cero y la mejora de arquitecturas preexistentes, experimentando con diferentes configuraciones de capas, funciones de activación y técnicas de regularización. También se trabaja con **transfer learning** y **fine-tuning** usando modelos preentrenados como **ResNet50**, adaptándolos para nuevas tareas de predicción. Finalmente, se incorpora el concepto de **IA explicable** al aplicar Grad-CAM para visualizar y comprender las decisiones tomadas por los modelos, ayudando a interpretar qué áreas de una imagen influyen en las predicciones, lo cual es esencial para mejorar la transparencia y confiabilidad de los modelos de visión por computadora.

---
## Práctica 3 : Extracción (y Emparejamiento) de Características y Registrado de Imágenes
La práctica consiste en implementar un detector de esquinas Harris para identificar puntos de interés en una imagen. Se deben calcular las derivadas de la imagen, obtener los términos de la matriz de segundo momento, y luego calcular el valor de Harris para cada píxel. Tras aplicar la supresión de no máximos y establecer un umbral adecuado, se seleccionan los puntos de interés. Para cada uno, se calcula la orientación principal y se genera una lista de keypoints con las coordenadas y características como el tamaño y la orientación. El resultado final incluye la visualización de los puntos detectados y el mapa de respuestas de Harris.

Además, en el ejercicio 2 se realiza el emparejamiento de keypoints entre dos imágenes utilizando descriptores SIFT, HOG y LBP. Finalmente, en el ejercicio 3, se lleva a cabo la creación de un panorama o mosaico mediante la estimación de homografías entre las imágenes emparejadas, utilizando RANSAC para una estimación robusta y transformando las imágenes a sus posiciones correctas en un lienzo.

### Detectar bordes en una imágen
<img src="images/p3_harris.png" alt="Harris" width="450px">

### Imagen híbrida
<img src="images/p3_sift1.png" alt="sift1" width="300px"> <img src="images/p3_sift2.png" alt="sift2" width="300px">

<img src="assets/p3_matches.png" alt="matches" width="450px">

### Crear un panorama dada imágenes con distintas perspectivas
<img src="assets/p3_mosaico.png" alt="mosaico" width="400px">