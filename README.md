# Análisis de Cancelación de Clientes (Churn) en Telecomunicaciones

## Descripción del Proyecto

La cancelación de clientes (customer churn) es uno de los principales desafíos para las empresas de telecomunicaciones. Retener clientes existentes suele ser más económico que adquirir nuevos, por lo que predecir el churn se convierte en un problema clave de negocio.

Este proyecto analiza datos de clientes de una empresa de telecomunicaciones con el objetivo de identificar los factores que influyen en la cancelación del servicio y construir un modelo de **Machine Learning** capaz de predecir qué clientes tienen mayor riesgo de abandonar la compañía.

El objetivo es generar **insights accionables** que ayuden a las empresas a diseñar estrategias de retención más efectivas y reducir la pérdida de clientes.

---

## Problema de Negocio

Las empresas de telecomunicaciones suelen enfrentar altos niveles de rotación de clientes. Identificar de forma temprana a los clientes con mayor probabilidad de cancelar su servicio permite implementar acciones preventivas como:

* ofertas personalizadas
* incentivos de contrato
* intervenciones de soporte al cliente

Al anticipar el churn, las empresas pueden **reducir pérdidas de ingresos y mejorar la satisfacción del cliente**.

---

## Descripción del Dataset

El conjunto de datos contiene información de clientes que incluye datos demográficos, suscripciones a servicios, detalles de facturación y características del contrato.

Principales tipos de variables:

* Datos demográficos del cliente
* Información de cuenta
* Detalles del servicio de internet
* Información de facturación y pagos
* Características del contrato

La variable objetivo es:

**Churn**

* **1 → Cliente canceló el servicio**
* **0 → Cliente permanece en la compañía**

Distribución de clases:

* **73% clientes retenidos**
* **27% clientes que cancelaron**

Esto indica un **desbalance moderado de clases**, algo común en problemas de churn.

---

## Flujo del Proyecto (Pipeline de Data Science)

El proyecto sigue un flujo estándar de análisis de datos y machine learning:

### 1. Limpieza de Datos

* manejo de valores faltantes
* conversión de variables a tipos de datos adecuados
* estandarización de variables categóricas

### 2. Análisis Exploratorio de Datos (EDA)

* análisis de la distribución del churn
* exploración de patrones de comportamiento del cliente
* identificación de posibles variables relevantes

### 3. Ingeniería de Características

* transformación de variables
* codificación de variables categóricas para el modelo

### 4. Entrenamiento del Modelo

Se utilizó un modelo de **Random Forest Classifier**, debido a su buen desempeño en datasets estructurados y su capacidad para identificar variables importantes.

### 5. Evaluación del Modelo

El modelo fue evaluado utilizando métricas comunes de clasificación:

* Accuracy
* Precision
* Recall
* Matriz de Confusión

---

## Resultados del Modelo

Modelo utilizado: **Random Forest Classifier**

Accuracy aproximada: **80%**

El modelo demuestra una capacidad razonable para distinguir entre clientes que cancelan el servicio y aquellos que permanecen en la empresa.

El análisis de la **matriz de confusión** muestra que el modelo logra identificar una proporción significativa de clientes con riesgo de churn manteniendo un equilibrio aceptable en las predicciones.

---

## Importancia de Variables

El modelo identificó las siguientes variables como las más influyentes para predecir el churn:

1. Total Charges (Cargos Totales)
2. Tenure (Antigüedad del cliente)
3. Monthly Charges (Cargos mensuales)
4. Cuentas Diarias
5. Método de Pago (Electronic Check)
6. Tipo de Servicio de Internet (Fibra Óptica)

Estas variables tienen un impacto importante en la probabilidad de cancelación del cliente.

---

## Principales Insights

Del análisis se desprenden varias conclusiones relevantes:

* Los clientes con **poca antigüedad** tienen mayor probabilidad de cancelar el servicio.
* Los **cargos mensuales altos** se asocian con mayor riesgo de churn.
* Los clientes que utilizan **electronic check como método de pago** presentan mayor tasa de cancelación.
* La **duración del contrato** está fuertemente relacionada con la retención de clientes.

Estos patrones sugieren que **la estructura de precios y el tipo de contrato influyen significativamente en la fidelización del cliente**.

---

## Recomendaciones de Negocio

Con base en el análisis, las empresas de telecomunicaciones podrían considerar las siguientes estrategias:

**Programas tempranos de retención**
Enfocar esfuerzos de retención en clientes con poca antigüedad.

**Optimización de precios**
Revisar estructuras de precios que puedan estar asociadas a mayor churn.

**Incentivos en métodos de pago**
Promover métodos de pago alternativos para reducir el riesgo asociado a ciertos tipos de pago.

**Programas de fidelización mediante contratos**
Ofrecer beneficios o descuentos por contratos de mayor duración.

---

## Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Estructura del Repositorio

data/ → dataset utilizado en el análisis
notebooks/ → notebook principal del análisis
images/ → visualizaciones y gráficos
README.md → documentación del proyecto

---

## Autor

**Magaly Anabel Hernández**

Aspirante a Data Analyst / Data Scientist enfocada en análisis de datos, machine learning y toma de decisiones basada en datos.

---

## Mejoras Futuras

Posibles extensiones de este proyecto:

* probar otros modelos de machine learning (XGBoost, Logistic Regression)
* optimización de hiperparámetros
* segmentación de clientes según probabilidad de churn
* desarrollo de un dashboard de churn para usuarios de negocio

---

## Conclusión

Este proyecto demuestra cómo el análisis de datos y el machine learning pueden utilizarse para identificar patrones de cancelación de clientes y apoyar la toma de decisiones en empresas de telecomunicaciones.

Al combinar análisis exploratorio, modelado predictivo e interpretación de resultados, es posible desarrollar estrategias proactivas para **reducir el churn y mejorar la retención de clientes**.
