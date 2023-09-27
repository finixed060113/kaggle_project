# Kaggle_Project

![portada](https://github.com/Ironhack-Data-Madrid-Enero-2021/W7-Kaggle_competition/blob/main/images/PORTADA.jpg)

## Descripción

Este proyecto tiene como objetivo principal realizar un Análisis Exploratorio de Datos (EDA) detallado y construir un modelo predictivo para predecir el precio de los diamantes en función de sus características. El conjunto de datos utilizado contiene información variada sobre los diamantes, como su peso en quilates, claridad, color, corte, entre otros atributos.

Durante el EDA, se llevaron a cabo procesos de limpieza y exploración de datos para comprender la distribución de las características, identificar posibles correlaciones y detectar patrones que puedan influir en el precio de los diamantes. Además, se tomaron decisiones importantes sobre cómo tratar los valores atípicos y se seleccionaron las características más relevantes para el modelo de predicción.

En la etapa de ajuste de modelo, se eligió un algoritmo adecuado y se realizaron preprocesamientos de datos específicos para construir un modelo de regresión capaz de predecir los precios de los diamantes con precisión. El modelo se evaluó utilizando métricas de evaluación de regresión y se realizaron ajustes iterativos para mejorar su rendimiento.

Variables:

-id: only for test & sample submission files, id for prediction sample identification

-price: price in USD

-carat: weight of the diamond

-cut: quality of the cut (Fair, Good, Very Good, Premium, Ideal)

-color: diamond colour

-clarity: a measurement of how clear the diamond is

-x: length in mm

-y: width in mm

-z: depth in mm

-depth: total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43--79)

-table: width of top of diamond relative to widest point (43--95)

## EDA (Análisis Exploratorio de Datos)

Limpieza de datos (manejo de valores faltantes, duplicados, etc.).
Resumen estadístico de las variables.
Visualización de datos (gráficos, histogramas, diagramas de dispersión, etc.).
Identificación de patrones o tendencias en los datos.
Análisis de correlaciones entre variables.

### Decisiones Tomadas

Durante la fase de preparación de datos, se tomaron varias decisiones clave que afectaron la calidad y el contenido de los datos utilizados en este proyecto de predicción del precio de los diamantes:

Valores Faltantes: Se realizó una verificación exhaustiva de valores faltantes en el conjunto de datos y se confirmó que no había valores nulos en ninguna de las características. Esto garantiza que los datos estén completos y listos para su análisis.

Valores Atípicos: Se optó por mantener los valores atípicos en el conjunto de datos en lugar de eliminarlos o transformarlos. Esto se hizo con la intención de no perder información valiosa que podría ser relevante para la predicción del precio de los diamantes. Los valores atípicos se considerarán en la construcción del modelo.

Codificación de Variables Categóricas: Para la variable "cut", se utilizó una codificación mediante mapeo, que asignó valores numéricos a las categorías. En el caso de las variables "color" y "clarity", se optó por la codificación one-hot, creando columnas binarias para cada categoría. Esta elección se basó en la naturaleza de las variables y se hizo para permitir que el modelo capture de manera efectiva la influencia de estas categorías en el precio.

Estas decisiones se tomaron después de un análisis cuidadoso de los datos y se consideraron apropiadas para este proyecto específico. Cada decisión se tomó con el objetivo de preparar los datos de manera que sean adecuados para el ajuste de modelos de predicción y permitan la exploración de relaciones significativas entre las características y el precio de los diamantes.



### Resultados del Modelo

En esta sección, se presentan los resultados clave del modelo de Árbol de Decisión II que se ajustó para predecir el precio de los diamantes en función de sus características. Estas métricas proporcionan una evaluación del rendimiento del modelo en los conjuntos de prueba y entrenamiento:
![MODELO]("")

MAE (Error Absoluto Medio):

Conjunto de Prueba: El MAE en el conjunto de prueba es aproximadamente 0.1171, lo que indica que, en promedio, las predicciones del modelo tienen un error absoluto promedio de alrededor del 11.71% en relación con los valores reales.
Conjunto de Entrenamiento: El MAE en el conjunto de entrenamiento es aproximadamente 0.1075.
MSE (Error Cuadrático Medio):

Conjunto de Prueba: El MSE en el conjunto de prueba es aproximadamente 0.0257, lo que significa que el modelo tiene un error cuadrático medio de alrededor del 2.57% en relación con los valores reales.
Conjunto de Entrenamiento: El MSE en el conjunto de entrenamiento es aproximadamente 0.0208.
RMSE (Raíz del Error Cuadrático Medio):

Conjunto de Prueba: El RMSE en el conjunto de prueba es aproximadamente 0.1603, lo que representa la raíz cuadrada del MSE.
Conjunto de Entrenamiento: El RMSE en el conjunto de entrenamiento es aproximadamente 0.1443.
R2 (Coeficiente de Determinación):

Conjunto de Prueba: El R2 en el conjunto de prueba es aproximadamente 0.9748, lo que significa que el modelo es capaz de explicar alrededor del 97.48% de la variación en el precio de los diamantes en el conjunto de prueba.
Conjunto de Entrenamiento: El R2 en el conjunto de entrenamiento es aproximadamente 0.9799.
Estos resultados indican que el modelo de Árbol de Decisión II es altamente efectivo para predecir el precio de los diamantes en función de sus características. Aunque el rendimiento en el conjunto de prueba es ligeramente inferior al conjunto de entrenamiento, las métricas siguen siendo muy favorables, lo que sugiere que el modelo generaliza bien a datos no vistos. El R2 cercano a 1 y los errores bajos son indicativos de un buen ajuste del modelo.  

### Recursos Adicionales
https://www.kaggle.com/competitions/diamonds-part-may-23/overview

