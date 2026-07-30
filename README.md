# Customer Churn Prediction
## Descripción del proyecto

La pérdida de clientes (Customer Churn) es uno de los principales desafíos para las empresas que ofrecen servicios por suscripción. Cada cliente que abandona la compañía representa una disminución de ingresos y un aumento en los costos de adquisición de nuevos clientes.

En este proyecto se desarrolla un flujo completo de análisis de datos y Machine Learning para identificar los factores asociados al abandono de clientes y construir un modelo capaz de predecir qué clientes presentan un mayor riesgo de churn.

El proyecto combina limpieza de datos, análisis exploratorio (EDA), modelado predictivo y visualización de resultados mediante Power BI.

## Problema de negocio

Retener clientes suele ser considerablemente más económico que adquirir nuevos. Por este motivo, contar con un modelo capaz de identificar clientes con alta probabilidad de abandono permite implementar campañas de retención antes de que el cliente deje de utilizar el servicio.

El objetivo principal consiste en comprender el comportamiento de los clientes, detectar los factores más influyentes en el abandono y construir un modelo predictivo que ayude a la toma de decisiones.

## Objetivos del proyecto

- Comprender la estructura del conjunto de datos.
- Realizar la limpieza y transformación de la información.
- Analizar las variables relacionadas con el abandono de clientes.
- Construir y comparar diferentes modelos de Machine Learning.
- Seleccionar el modelo con mejor desempeño.
- Obtener conclusiones e insights de negocio que permitan reducir el churn.

## Dataset

El proyecto utiliza el dataset Telco Customer Churn, que contiene información demográfica de los clientes, los servicios contratados, información de facturación y el estado final de abandono.

|Atributo	|Descripción|
| ----------| ----------:|
|customerID|	Identificador único del cliente|
|gender|	Género del cliente|
|SeniorCitizen|	Indica si el cliente es adulto mayor|
|Partner|	Indica si el cliente posee pareja|
|Dependents|	Indica si el cliente posee dependientes|
|tenure|	Cantidad de meses que el cliente permanece en la empresa|
|PhoneService|	Servicio telefónico contratado|
|MultipleLines|	Cantidad de líneas telefónicas|
|InternetService|	Tipo de servicio de Internet|
|OnlineSecurity|	Servicio de seguridad en línea|
|OnlineBackup|	Servicio de respaldo en línea|
|DeviceProtection|	Protección de dispositivos|
|TechSupport|	Soporte técnico|
|StreamingTV|	Servicio de televisión por streaming|
|StreamingMovies	Servicio de películas por streaming|
|Contract|	Tipo de contrato|
|PaperlessBilling|	Facturación electrónica|
|PaymentMethod|	Método de pago|
|MonthlyCharges|	Cargo mensual del cliente|
|TotalCharges|	Cargo total acumulado|
|Churn	|Indica si el cliente abandonó la empresa|

## Metodología
### 1. Comprensión de los datos

Se realizó un análisis inicial del conjunto de datos para conocer:

- Dimensiones del dataset.
- Tipos de datos.
- Valores únicos.
- Valores nulos.
- Consistencia de la información.

### 2. Limpieza y transformación de datos

Durante esta etapa se realizaron las siguientes tareas:

- Eliminación de registros con valores vacíos.
- Conversión de tipos de datos.
- Estandarización de variables categóricas.
- Corrección de inconsistencias.
- Codificación mediante One-Hot Encoding.
- Preparación del dataset para Machine Learning.

### 3. Análisis Exploratorio de Datos (EDA)

Se analizaron tanto variables categóricas como numéricas mediante:

- Distribución de frecuencias.
- Comparación entre clientes con y sin churn.
- Estadísticos descriptivos.
- Diagramas de barras.
- Boxplots.
- Interpretación de resultados desde una perspectiva de negocio.

Los principales hallazgos mostraron que el abandono de clientes está fuertemente asociado con:

- Contratos mensuales (Month-to-month).
- Baja antigüedad del cliente (tenure).
- Servicio de Internet por fibra óptica.
- Cargos mensuales elevados.
- Ausencia de soporte técnico y seguridad en línea.

### 4. Preparación para Machine Learning

Antes del entrenamiento de los modelos se realizaron las siguientes tareas:

- Selección de variables predictoras y variable objetivo.
- Transformación de variables categóricas.
- Separación entre variables independientes (X) y variable objetivo (y).
- División del conjunto de datos en entrenamiento y prueba (Train-Test Split).
- Escalado de variables numéricas para la Regresión Logística.

### 5. Modelos de Machine Learning

Se entrenaron y evaluaron tres algoritmos de clasificación:

- Regresión Logística.
- Árbol de Decisión.
- Random Forest.

La comparación entre modelos se realizó utilizando las siguientes métricas:

- Accuracy.
- Precision.
- Recall.
- F1-Score.
- ROC-AUC.

### Comparación de modelos
|Modelo	Accuracy|	ROC-AUC|
| -------------| --------: |
|Regresión Logística|	80.38%	0.8357|
|Árbol de Decisión|	71.50%	0.6382|
|Random Forest|	78.75%	0.8119|

### Modelo seleccionado

La Regresión Logística obtuvo el mejor desempeño general, logrando el mayor Accuracy y ROC-AUC, además de ofrecer una excelente capacidad de interpretación de los resultados.

## Principales Insights

El análisis permitió identificar varios factores asociados al abandono de clientes:

- Los contratos Month-to-month presentan la mayor tasa de churn.
- Los clientes con menor antigüedad poseen una mayor probabilidad de abandonar la empresa.
- Los clientes con servicio de Fibra Óptica muestran un mayor riesgo de churn.
- La ausencia de Soporte Técnico y Seguridad en Línea incrementa significativamente la probabilidad de abandono.
- Los contratos de mayor duración favorecen la retención de clientes.

Estos resultados permiten orientar estrategias comerciales enfocadas en la fidelización y retención de clientes.

### Dashboard

Como complemento del análisis, se desarrolló un dashboard interactivo en Power BI, donde se resumen los principales indicadores del proyecto.

El dashboard incluye:

- Resumen general de clientes.
- Tasa de abandono.
- Perfil de clientes.
- Análisis por contratos.
- Análisis por servicios.
- Métodos de pago.
- Variables numéricas.
- Principales hallazgos del proyecto.

imágenes del dashboard

### Tecnologías utilizadas
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Power BI
- Git
- GitHub

## Conclusiones

En este proyecto se desarrolló un flujo completo de Machine Learning, desde la comprensión y preparación de los datos hasta la construcción y evaluación de modelos predictivos.

El análisis exploratorio permitió identificar las variables con mayor influencia sobre el abandono de clientes, mientras que la comparación entre modelos demostró que la Regresión Logística fue la alternativa con mejor desempeño para este conjunto de datos.

Los resultados obtenidos pueden servir como apoyo para la toma de decisiones dentro de una empresa, permitiendo identificar clientes con mayor riesgo de abandono y diseñar estrategias de retención más efectivas.


