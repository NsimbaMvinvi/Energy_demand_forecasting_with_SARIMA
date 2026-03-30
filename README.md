# Pronóstico de Demanda Eléctrica con SARIMA

## Objetivos del Análisis
Este proyecto desarrolla un modelo de series temporales para pronosticar la demanda eléctrica horaria en California con un horizonte de corto plazo de hasta **24 horas**.

Desde una perspectiva de negocio, el objetivo es ayudar a la empresa encargada de la generación y distribución de energía a **optimizar su operación**, alineando la oferta energética con la demanda esperada.

Los objetivos específicos del análisis fueron:
- Comprender el comportamiento histórico de la demanda energética.
- Preparar una serie temporal limpia y consistente.
- Detectar patrones de tendencia y estacionalidad.
- Construir un modelo base para comparación.
- Implementar un modelo **SARIMA** para mejorar la precisión.
- Evaluar el desempeño del modelo mediante métricas como **MAPE** y **RMSE**.
- Analizar los residuales para validar la calidad del modelo.

## Datos Utilizados
El análisis utiliza datos reales de demanda eléctrica horaria del estado de **California, Estados Unidos**.

Características principales:
- **Variable temporal:** `period`
- **Variable objetivo:** `value` (demanda energética)
- **Nivel original:** sub-regiones energéticas (`subba`)
- **Transformación:** agregación de sub-regiones para obtener una única serie temporal estatal

Procesamiento realizado:
- Conversión de fechas a formato `datetime`
- Ordenamiento cronológico
- Identificación de datos faltantes
- Interpolación lineal de valores ausentes
- Detección y tratamiento de outliers mediante el método de Tukey

## Tecnologías y Librerías

### Tecnologías
- Python
- Jupyter Notebook

### Librerías
- **pandas** – manipulación de datos
- **numpy** – operaciones numéricas
- **matplotlib** – visualización
- **seaborn** – análisis exploratorio
- **statsmodels** – ACF, PACF, ADF y modelos SARIMA/SARIMAX
- **scikit-learn** – métricas de evaluación

## Archivo Principal
- **`pronostico_demanda_electricidad_sarima.ipynb`**  
Contiene todo el flujo del proyecto:
- Carga y limpieza de datos  
- Análisis exploratorio  
- Identificación de estacionalidad  
- Modelado base  
- Implementación de SARIMA  
- Evaluación y análisis de residuales  

## Notas Adicionales

### Contexto de Negocio
Una correcta estimación de la demanda energética es crítica para la operación:

- **Sobreestimación de la demanda:**
  - Generación excesiva de energía
  - Costos por desperdicio o almacenamiento innecesario

- **Subestimación de la demanda:**
  - Fallos en el suministro eléctrico
  - Impacto negativo en clientes residenciales e industriales

Por lo tanto, mejorar la precisión del pronóstico permite:
- Reducir costos operativos
- Aumentar la eficiencia energética
- Garantizar estabilidad en el suministro

### Hallazgos Técnicos
- Se identificó una **estacionalidad diaria clara (24 horas)**.
- El modelo SARIMA logró mejorar el desempeño frente al modelo base.
- Los residuales muestran ligera sobreestimación, indicando margen de mejora.

### Mejoras Futuras
- Incorporar variables exógenas (temperatura, festivos, tipo de día)
- Optimizar hiperparámetros del modelo
- Evaluar modelos alternativos (Prophet, XGBoost, LSTM)

---


