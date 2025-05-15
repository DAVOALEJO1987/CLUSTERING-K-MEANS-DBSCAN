# Análisis del proceso de ML no supervisado de clasificación, K-MEANS & DBSCAN

# Introducción 
La predicción climática ha sido históricamente un reto debido a la naturaleza caótica y altamente no lineal de los sistemas atmosféricos. En décadas anteriores, los enfoques basados en inteligencia artificial enfrentaban limitaciones por la escasez de datos, baja capacidad computacional y modelos incapaces de captar relaciones complejas. Además, el análisis estadístico convencional no podía manejar el volumen ni la variedad de datos meteorológicos generados a escala global. Con el avance del Big Data y la computación en la nube, hoy es posible procesar millones de registros meteorológicos multivariables en tiempo real. En este contexto, las técnicas de aprendizaje automático no supervisado, como K-Means, DBSCAN y t-SNE, permiten descubrir patrones ocultos, segmentar condiciones climáticas y detectar eventos extremos sin requerir etiquetas previas. Estos métodos han mejorado significativamente la precisión y comprensión del comportamiento climático, facilitando aplicaciones prácticas en predicción estacional, planificación agrícola y sistemas de alerta temprana con una precisión superior a enfoques tradicionales.

![image](https://github.com/user-attachments/assets/ed2d0c35-1c9d-44e0-9eb8-780d22f08303)

# Estructura del código 
El código fuente del notebook "Actividad_3_ML_no_supervisado.ipynb" esta conformado por las siguientes secciones: 

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

Finalmente, el código utiliza técnicas de reducción de dimensionalidad como PCA y t-SNE para visualizar los resultados de los clusters en un espacio bidimensional. Este enfoque permite identificar patrones climáticos ocultos y segmentar condiciones meteorológicas, aportando valor a aplicaciones como la predicción climática, planificación agrícola o análisis de riesgos, tecnologia de aprendizaje para maquinas generadoras de agua WATERGEN. 

Referencia [https://www.kaggle.com/datasets/hrhuynguyen/2d-spatial-dataset/data]

# Uso del codigo  
Para el uso integral del codigo se recomenda ir ejecutando cada sección del mismo:

![image](https://github.com/user-attachments/assets/88cd44a7-f903-401e-8951-15f1b31eab2f)

En caso de ayuda enviar un email a: david.narvaez@uees.edu.ec 

# Insight principales 
# 📈 Interpretación del Silhouette Score en K-Means y DBSCAN
Durante la implementación de los algoritmos de clustering K-Means y DBSCAN, se utilizó el Silhouette Score como métrica para evaluar la calidad de los clusters formados. Esta métrica mide qué tan similar es un objeto a su propio cluster (cohesión) en comparación con otros clusters (separación).

El rango del Silhouette Score va de -1 a 1:

- Valores cercanos a +1 indican que los objetos están bien agrupados y lejos de otros clusters.
- Valores cercanos a 0 sugieren que los puntos se encuentran en los límites entre clusters.
- Valores negativos indican que los puntos podrían estar asignados incorrectamente.

En este estudio, se obtuvo un Silhouette Score de 0.2567 para K-Means con k=4, lo que sugiere una segmentación moderadamente coherente, con cierta separación entre grupos pero también zonas de solapamiento. Este valor positivo indica que los puntos están más cerca de su propio centroide que de otros clusters, aunque no de forma óptima.

En comparación, DBSCAN arrojó un score de 0.1264 (excluyendo puntos considerados ruido), lo cual refleja una menor definición de los clusters formados.

🔍 Conclusión: De los métodos aplicados, K-Means obtuvo el mejor rendimiento según el Silhouette Score, siendo más efectivo para agrupar los datos climáticos de Basilea.

![image](https://github.com/user-attachments/assets/ecda7792-99ab-4bff-b558-988aef35c5a5)

# 📈 Interpretación del t-SNE

El análisis de clustering no supervisado visualizado mediante t-SNE permite identificar con mayor claridad la distribución no lineal de los datos agrupados por el modelo K-Means con k=4. A diferencia de PCA, t-SNE preserva las relaciones de vecindad local y revela una separación más evidente entre los grupos, ideal para interpretar patrones complejos.

Cluster 2 (verde) destaca por tener la mayor radiación solar (2.92) y el mayor brillo solar (10.68), acompañado de temperatura media positiva (1.32), lo que lo asocia directamente con días veraniegos soleados. Estos registros son ideales para actividades al aire libre, agricultura estacional o planificación de generación solar.

Cluster 1 (naranja) presenta alta precipitación (1.23) y temperatura media muy baja (-10.01), además de baja radiación y sol, lo que sugiere condiciones de invierno extremo con eventos lluviosos o nevadas. Este tipo de cluster sería útil para alertas meteorológicas, logística invernal y planificación de energía térmica.

Cluster 3 (rojo) es un grupo intermedio pero seco: alta exposición solar (8.51), baja humedad (0.56) y temperatura fría (-8.16), compatible con días despejados de invierno o altitudes elevadas.

Cluster 0 (azul) presenta condiciones más equilibradas: radiación y sol moderados, temperatura baja (-1.61) y humedad alta (0.94). Este grupo representa condiciones más típicas, ni extremas ni secas, lo que puede ser útil para operaciones estándar o predicción del clima predominante.

![image](https://github.com/user-attachments/assets/28dac114-4e05-4130-a337-35b3924019b2)
