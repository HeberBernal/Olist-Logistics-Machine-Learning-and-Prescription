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

## 📊 Metodología y Preparación de Datos
El modelo se entrenó utilizando una muestra final de **110,189 registros**, aplicando las siguientes etapas:
1. **Feature Engineering:** Selección estratégica de variables críticas: `product_weight_g`, `price`, `freight_value` y categorías de producto.
2. **Tratamiento de Datos:** Imputación de valores nulos en dimensiones físicas mediante la mediana para garantizar la integridad del entrenamiento.
3. **Data Splitting:** División de datos en 80% entrenamiento y 20% validación.

---

## 🤖 Modelado: Random Forest Regressor
Se seleccionó el algoritmo de **Random Forest** por su robustez ante valores atípicos y su capacidad para capturar relaciones no lineales entre el peso físico del producto y el costo del flete.

### **Resultados Técnicos:**
* **Error Medio Absoluto (MAE):** 5.11 días.
* **Precisión del Modelo ($R^2$):** 0.19.

> **Diagnóstico:** El $R^2$ de 0.19 indica que las características intrínsecas del producto explican una quinta parte de la variabilidad. El resto de la varianza está fuertemente ligada a factores geográficos (distancia origen-destino), lo que marca la hoja de ruta para futuras optimizaciones geoespaciales.

---

## 💡 Insights y Análisis Prescriptivo
A partir del análisis de **Importancia de Variables**, donde el costo del flete y el peso resultaron ser los mayores predictores, se proponen las siguientes acciones de negocio:

1. **Ajuste Dinámico de SLA:** Implementar un margen de seguridad de **+5 días** (basado en el MAE) en la promesa de entrega para productos pesados, reduciendo la tasa de insatisfacción.
2. **Auditoría de Rutas Críticas:** Investigar zonas con alto costo de flete que no se traducen en entregas rápidas para renegociar contratos con transportistas locales.
3. **Estrategia de Centros de Distribución:** Incentivar el almacenamiento de productos de alto peso en regiones cercanas a los puntos de mayor demanda para minimizar el tiempo de transporte de larga distancia.

---

## 📈 Visualizaciones
*(Aquí puedes incluir la imagen de tu gráfica de importancia de variables)*
`![Importancia de Variables](nombre_de_tu_grafica.png)`

---
**Autor:** Heber Job Bernal Monarrez  
*Data Analyst & Biomedical Researcher*
