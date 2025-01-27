# Clasificación de dígitos con Redes Neuronales

## Descripción del proyecto
Este proyecto utiliza un modelo de red neuronal multicapa (MLP) entrenado con el dataset MNIST para la clasificación de dígitos escritos a mano. La implementación incluye preprocesamiento de datos, entrenamiento, evaluación de métricas y visualización de resultados.
El proyecto ha sido redactado a modo tutorial para facilitar su comprensión, a lo largo del mismo se cuestionan los parámetros y se hacen variaciones en ellos para ver como evoluciona el comportamiento de la red neuronal.

## Objetivos
- Preprocesar y escalar datos de imágenes para garantizar un buen rendimiento del modelo.
- Implementar y entrenar modelos MLP utilizando Keras con TensorFlow.
- Evaluar el rendimiento de los modelos.
- Exploración de hiperparámetros y experimentación.
- Prevención del sobreajuste y optimización de la generalización.
- Visualización de resultados.
- Aplicación práctica del modelo.

## Flujo de trabajo
1. **Carga de datos:** Se carga el dataset MNIST desde la biblioteca de Keras, que incluye imágenes de dígitos de 28x28 píxeles.
   - El dataset MNIST es cargado desde las bibliotecas de Keras, proporcionando conjuntos de datos para entrenamiento (60,000 imágenes) y prueba (10,000 imágenes).
   - Cada imagen es de 28x28 píxeles con valores de intensidad de gris entre 0 (negro) y 255 (blanco). Las etiquetas representan los dígitos del 0 al 9.
3. **Preprocesamiento de datos:**
   - Normalización: Los valores de los píxeles se escalan entre 0 y 1 para facilitar el entrenamiento.
   - Reformateo: Las imágenes 28x28 se transforman en vectores unidimensionales de 784 elementos.
   - One-hot Encoding: Las etiquetas se convierten en vectores binarios, facilitando la clasificación multiclase.
4. **Creación, compilación y entrenamiento del modelo:** Arquitectura de red neuronal multicapa (MLP) diseñada con Keras.
5. **Experimentación y optimización**:
    - Impacto de las neuronas ocultas: Se evalúan configuraciones con distinto número de neuronas, observando los efectos en precisión y pérdida.
    - Modificación de epochs: Se experimenta con el número de epochs para identificar el impacto del sobreajuste.
    - Regularización: Se implementan técnicas como Dropout y L2 regularization para prevenir el sobreajuste.
    - Optimización: Comparación entre Adam, RMSprop y SGD para seleccionar el optimizador más eficiente.
    - Funciones de activación: Evaluación de ReLU, Sigmoid y Tanh para comparar su desempeño.
6. **Evaluación y visualización:**
   - Visualización de curvas de precisión y pérdida durante el entrenamiento.
   - Prueba del modelo con una imagen aleatoria del conjunto de prueba. El modelo predice correctamente el dígito.

## Resultados
Métricas del modelo final
- Precisión en entrenamiento: 93,87%
- Precisión en validación: 95,17%
- Pérdida en entrenamiento: 0.42
- Pérdida en validación: 0.38
