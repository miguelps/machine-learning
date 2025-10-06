# Machine Learning para Docentes

El contenido se enfoca en los **prerrequisitos esenciales** para abordar, en futuras sesiones, temas más avanzados como **Redes Neurales de Aprendizaje Profundo (DNN)** y **Visión Computacional**. La capacitación se estructura en dos componentes clave para asegurar un aprendizaje integral: **teoría y práctica.**

## Contenido

A continuación, se presenta la lista de temas propuestos y el número de horas asignadas para el desarrollo del curso, conforme a las conversaciones previas.

| Aula  | Tema                                                                                        |
| :---: | :-------------------------------------------------------------------------------------------|
|   1   | Python. Análisis de Componentes Principales.                                                |
|   2   | Python. Regresión y selección de modelos.                                                   |
|   3   | Aprendizaje no supervisado: Agrupamiento *k-means*, Agrupamiento jerárquico *dendrograma.*  |
|   4   | Aprendizaje supervisado: Discriminantes lineales, Máquinas de Vectores de Soporte.          |
|   5   | Árboles de Clasificación y Bosques Aleatorios                                               |
|   6   | Redes neuronales artificiales                                                               |
|   7   | Aprendizaje profundo. Capas convolucionales y capas recurrentes                             |
|   8   | *Transformers*                                                                              |

---

### 1: Reducción de Dimensionalidad

* **Descomposición en Valores Singulares (SVD)**: Es una de las factorizaciones de matrices más importantes. Se utiliza para obtener aproximaciones de bajo rango y para el cálculo de pseudoinversas.
* **Análisis de Componentes Principales (PCA)**: Un uso clave de la SVD es el algoritmo de PCA, que descompone datos de alta dimensión en factores estadísticamente descriptivos.
* **Aplicación**: SVD y PCA se aplican en una amplia variedad de problemas de ciencia e ingeniería.

### 2: Regresión y Selección de Modelos

El **aprendizaje automático** se centra en la optimización. Herramientas de **regresión y selección de modelos** permiten crear modelos interpretables, simples y eficientes. Cuando el modelo ideal no está predefinido, se aplican métodos de optimización para seleccionar el mejor.

### 3: Aprendizaje No Supervisado

El objetivo es agrupar datos sin etiquetas.

* **Agrupamiento K-Means**: Particiona un conjunto de *m* observaciones vectoriales en *k* grupos. El número de particiones (*k*) generalmente es desconocido y debe determinarse.
* **Agrupamiento Jerárquico (Dendrograma)**: Esta técnica agrupa datos según su similitud, creando una jerarquía en forma de árbol. Comienza con cada observación como un grupo separado y las fusiona progresivamente.

\newpage

### 4: Aprendizaje Supervisado

En este tipo de aprendizaje, los datos etiquetados guían el algoritmo de clasificación.

* **Análisis Discriminante Lineal (LDA)**: Una técnica de clasificación estándar cuyo objetivo es encontrar una combinación lineal de características que separe dos o más clases de objetos.
* **Máquinas de Vectores de Soporte (SVM)**: Algoritmo de clasificación que encuentra un hiperplano óptimo para maximizar la distancia entre las clases en un espacio N-dimensional.

### 5: Árboles de Decisión y Bosques Aleatorios

* **Árbol de Decisión**: Estructura jerárquica supervisada que divide los datos para lograr una clasificación y regresión robustas. Al ser supervisado, utiliza datos etiquetados para optimizar las divisiones.
* **Bosques Aleatorios**: Método de aprendizaje en conjunto que crea múltiples árboles de decisión para mejorar la robustez. Es una mejora significativa, ya que los árboles individuales pueden ser sensibles a las variaciones en los datos de entrenamiento.

### 6: Redes Neurales Artificiales (ANN)

Las **Redes Neuronales Artificiales** son sistemas de aprendizaje compuestos por neuronas interconectadas jerárquicamente. El aprendizaje se logra ajustando los "pesos sinápticos" para minimizar una función de costo. El algoritmo de **retropropagación** fue un avance crucial para entrenar estas redes de forma eficiente.

### 7: Aprendizaje Profundo (Deep Learning)

Las **redes neuronales profundas** se componen de múltiples capas de neuronas interconectadas que refinan y optimizan las predicciones o clasificaciones.

* **Redes Neuronales Convolucionales (CNN)**: Ideales para visión por computadora. Detectan características y patrones en imágenes para tareas como detección de objetos y reconocimiento de patrones.
* **Redes Neuronales Recurrentes (RNN)**: Utilizadas para datos secuenciales como series de tiempo o texto. Pueden procesar datos de forma secuencial y son comunes en el procesamiento del lenguaje natural y el reconocimiento de voz. Se identifican por sus bucles de retroalimentación.

### 8: Transformers

* **Transformers**: Arquitectura de red neuronal que ha revolucionado el Procesamiento del Lenguaje Natural (NLP).
* **Mecanismo de Autoatención**: Su principal innovación es la capacidad de capturar dependencias globales entre los elementos de una secuencia de entrada.
* **Ventaja**: Pueden procesar datos en paralelo, lo que los hace altamente eficientes y escalables para el entrenamiento en hardware moderno.

<center>

#### Dr. Cs. Miguel Pari Soto  y  Dr. Cs. Claver Pari Soto

</center>
