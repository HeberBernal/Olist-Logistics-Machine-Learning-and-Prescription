## 📦Olist Logistics: Predictive & Prescriptive Analysis

Este proyecto representa la **Fase 2** de un análisis integral de la cadena de suministro de **Olist** (Brasil). Tras consolidar una "Fuente Única de Verdad" en la Fase 1 (ETL), este módulo aplica Machine Learning para predecir tiempos de entrega y generar recomendaciones estratégicas basadas en hallazgos estadísticos.

---

## 🚀 Objetivo del Proyecto
Desarrollar un modelo de regresión capaz de estimar el tiempo de entrega (`delivery_time`) y utilizar la importancia de las variables para prescribir acciones que optimicen la operación logística, mejorando la precisión de la promesa al cliente.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Librerías de ML:** Scikit-Learn (Random Forest Regressor)
* **Manipulación de Datos:** Pandas, Numpy
* **Visualización:** Matplotlib, Seaborn
* **Metodología:** Análisis Predictivo y Prescriptivo

---

## 📊 Metodología y Preparación
El modelo procesó un dataset de **110,189 registros** con la siguiente estructura de datos:

| Etapa | Descripción |
| :--- | :--- |
| **Feature Selection** | `weight`, `price`, `freight_value` y `category_encoded` |
| **Imputación** | Mediana para dimensiones físicas (evita sesgos) |
| **Data Split** | 80% Entrenamiento / 20% Validación |
| **Algoritmo** | Random Forest Regressor (100 estimators) |

---

## 🤖 Desempeño del Modelo
Tras el entrenamiento, el bosque de decisión arrojó las siguientes métricas de control:

| Métrica | Resultado | Interpretación |
| :--- | :--- | :--- |
| **MAE** | **5.11 días** | Error promedio en la predicción de entrega. |
| **$R^2$** | **0.19** | Variabilidad explicada por atributos del producto. |

> **Diagnóstico Pro:** El bajo $R^2$ es un hallazgo clave; demuestra que en la logística de Olist, la **geografía** (distancia) tiene un impacto mayor que las características físicas del objeto.
---

## 💡 Insights y Análisis Prescriptivo
A partir del análisis de **Importancia de Variables**, donde el costo del flete y el peso resultaron ser los mayores predictores, se proponen las siguientes acciones de negocio:

1. **Ajuste Dinámico de SLA:** Implementar un margen de seguridad de **+5 días** (basado en el MAE) en la promesa de entrega para productos pesados, reduciendo la tasa de insatisfacción.
2. **Auditoría de Rutas Críticas:** Investigar zonas con alto costo de flete que no se traducen en entregas rápidas para renegociar contratos con transportistas locales.
3. **Estrategia de Centros de Distribución:** Incentivar el almacenamiento de productos de alto peso en regiones cercanas a los puntos de mayor demanda para minimizar el tiempo de transporte de larga distancia.
---
**Autor:** Heber Job Bernal Monarrez  
*Data Analyst & Biomedical Researcher*
