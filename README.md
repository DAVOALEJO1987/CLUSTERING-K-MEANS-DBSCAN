# Análisis del proceso de ML no supervisado de clasificación, K-MEANS & DBSCAN

# Introducción 
La predicción climática ha sido históricamente un reto debido a la naturaleza caótica y altamente no lineal de los sistemas atmosféricos. En décadas anteriores, los enfoques basados en inteligencia artificial enfrentaban limitaciones por la escasez de datos, baja capacidad computacional y modelos incapaces de captar relaciones complejas. Además, el análisis estadístico convencional no podía manejar el volumen ni la variedad de datos meteorológicos generados a escala global. Con el avance del Big Data y la computación en la nube, hoy es posible procesar millones de registros meteorológicos multivariables en tiempo real. En este contexto, las técnicas de aprendizaje automático no supervisado, como K-Means, DBSCAN y t-SNE, permiten descubrir patrones ocultos, segmentar condiciones climáticas y detectar eventos extremos sin requerir etiquetas previas. Estos métodos han mejorado significativamente la precisión y comprensión del comportamiento climático, facilitando aplicaciones prácticas en predicción estacional, planificación agrícola y sistemas de alerta temprana con una precisión superior a enfoques tradicionales.

![image](https://github.com/user-attachments/assets/ed2d0c35-1c9d-44e0-9eb8-780d22f08303)

# Estructura del código 
El código fuente del notebook "Actividad_3_ML_no_supervisado.ipynb" esta conformado or las siguientes secciones: 

1. Análisis de Estadística descriptiva, EDA del conjunto de datos
2. Optimización del dataset y Vizualización de distribución
3. Aprendizaje Automatico No Supervizado
4. Clustering con K-Means
5. Clustering con DBSCAN
6. Clustering K-Means con PCA
7. Clustering con t-SNE
8. Clustering con Silhouette Score
9. Análisis de Resultados

El código fuente implementa un flujo completo de aprendizaje automático no supervisado aplicado a un conjunto de datos meteorológicos de la ciudad de Basilea. Este análisis comienza con la carga de datos desde un repositorio en línea y continúa con un exhaustivo proceso de preprocesamiento: se identifican y tratan valores nulos (rellenando con la mediana), se eliminan duplicados y se corrigen formatos de fecha. Además, se detectan valores atípicos mediante visualizaciones tipo boxplot para cada variable numérica.

Posteriormente, el código desarrolla un Análisis Exploratorio de Datos (EDA), presentando estadísticas descriptivas y gráficos de distribución para comprender el comportamiento de las variables climáticas. A partir de estos datos depurados, se procede a la fase de modelado no supervisado utilizando algoritmos de clustering K-Means y DBSCAN. Para K-Means, se aplica el método del codo para determinar el número óptimo de clusters, mientras que para DBSCAN se evalúa la densidad de puntos.

Finalmente, el código utiliza técnicas de reducción de dimensionalidad como PCA y t-SNE para visualizar los resultados de los clusters en un espacio bidimensional. Este enfoque permite identificar patrones climáticos ocultos y segmentar condiciones meteorológicas, aportando valor a aplicaciones como la predicción climática, 

Referencia [https://www.kaggle.com/datasets/hrhuynguyen/2d-spatial-dataset/data]


planificación agrícola o análisis de riesgos. 
