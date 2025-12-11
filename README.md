# Restauración de Patrones con PCA y SVD

Esta tarea de Computacón Científica implementa técnicas de **Análisis de Componentes Principales (PCA)** y **Descomposición en Valores Singulares (SVD)** para la restauración y reconocimiento de patrones digitales (imágenes). El objetivo principal es reconstruir o "limpiar" imágenes que presentan ruido o datos faltantes, utilizando un modelo estadístico pre-calculado.

## Descripción

La restauración de imágenes mediante PCA/SVD se basa en la proyección de los datos (imágenes ruidosas) sobre un subespacio de menor dimensión generado a partir de patrones limpios. Al reconstruir la imagen utilizando solo los componentes principales más significativos, se preserva la estructura esencial del patrón y se descarta el ruido, el cual suele residir en los componentes de menor varianza.

Este repositorio contiene el código fuente en Python (Jupyter Notebook) para realizar este proceso, junto con los archivos de datos necesarios con los parámetros del modelo entrenado.

## Estructura del Repositorio

- **`Restauración_de_Patrones_Digitales.ipynb`**:  
  Archivo central de la Tarea. El cuaderno de Jupyter que contiene:
  - Carga de librerías y datos.
  - Implementación de los algoritmos de reconstrucción usando PCA/SVD.
  - Visualización de los patrones originales, ruidosos y restaurados.
  
- **`mu.npy`**:  
  Archivo de NumPy que almacena el **vector media ($\mu$)** calculado a partir del conjunto de entrenamiento de patrones limpios. Es esencial para centrar los datos antes de aplicar PCA.

- **`densities.npy`**:  
  Archivo de NumPy que contiene la información de densidad o los componentes principales (autovectores/valores singulares) necesarios para la proyección y reconstrucción.

- **`pattern/`**:  
  Carpeta que contiene las imágenes o patrones utilizados para las pruebas y validación del algoritmo.

- **`descripcion proyecto.txt`**:  
  Archivo de texto con detalles adicionales o notas sobre el alcance del proyecto.

## Librerías usadas en la Tarea

* [NumPy](https://numpy.org/) (para manipulación de matrices y carga de archivos `.npy`)
* [Matplotlib](https://matplotlib.org/) (para visualizar las imágenes)
* [Jupyter Notebook](https://jupyter.org/) (para ejecutar el código)
