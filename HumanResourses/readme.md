# 📊 Análisis y Predicción de Deserción Laboral

Este proyecto se centra en el **análisis exploratorio** y la **construcción de un modelo predictivo** para identificar los factores clave que influyen en la deserción de empleados dentro de una organización.

---

## 🎯 Objetivo

El objetivo principal es:

> **Comprender por qué los empleados dejan la empresa y desarrollar una herramienta predictiva que ayude a identificar a los empleados en riesgo de deserción**, permitiendo a la organización implementar estrategias de retención proactivas y efectivas.

---

## 🔎 Enfoque Metodológico

El proyecto sigue un flujo de trabajo típico de **Ciencia de Datos**:

1. **Análisis Exploratorio de Datos (EDA):**  
   Comprensión de la distribución de los datos, correlaciones entre variables y visualización de patrones asociados a la deserción.

2. **Preprocesamiento de Datos:**  
   Codificación de variables categóricas, tratamiento de datos redundantes y preparación para el modelado.

3. **Modelado Predictivo:**  
   Entrenamiento y evaluación de modelos de clasificación (Regresión Logística y XGBoost), con atención al **desbalance de clases**.

4. **Evaluación y Optimización del Modelo:**  
   Uso de métricas como **F1-score**, **Precision**, **Recall** y **ROC-AUC**.  
   Optimización del modelo XGBoost mediante **RandomizedSearchCV** y ajuste de umbral de decisión.

5. **Interpretación del Modelo:**  
   Aplicación de **SHAP values** para entender la importancia y contribución de cada característica en las predicciones.

---

## 📌 Hallazgos Clave

Los factores más influyentes en la deserción identificados por el análisis y el modelo XGBoost fueron:

- **Horas Extra (OverTime):** Asociadas con mayor probabilidad de deserción.  
- **Ingreso Mensual (MonthlyIncome):** Ingresos bajos incrementan el riesgo.  
- **Nivel de Opción de Acciones (StockOptionLevel):** Bajos niveles aumentan la probabilidad de salida.  
- **Antigüedad en la Empresa (YearsAtCompany):** Los primeros años son críticos para la retención.  
- **Edad (Age):** Los empleados más jóvenes muestran mayor deserción.  
- **Rol de Trabajo (JobRole):** El rol de *Sales Representative* presentó la tasa más alta de deserción.  
- **Satisfacción y Relación con el Gerente:** Una menor satisfacción general y menor tiempo con el gerente actual también influyen.

---

## 📈 Resultados del Modelo (XGBoost Optimizado)

| Métrica                  | Valor Aproximado |
|--------------------------|------------------|
| **Accuracy**             | ~0.87            |
| **F1-score (Deserción)** | ~0.61            |
| **ROC-AUC**              | ~0.86            |

> ✅ El modelo optimizado alcanzó un buen **equilibrio entre precisión y sensibilidad**, lo que lo hace útil para identificar empleados en riesgo.

---

## 🏁 Conclusión e Implicaciones

El análisis y modelo desarrollado proporcionan una **herramienta valiosa para la gestión del talento**:

- Identificación proactiva de empleados en riesgo.  
- Estrategias de retención enfocadas en:  
  - Políticas de horas extra.  
  - Revisión de estructura salarial.  
  - Programas de desarrollo temprano de carrera.  
  - Fortalecimiento de la relación gerente–empleado.  

En conjunto, esta solución puede mejorar la **retención de talento** y la **eficiencia organizacional**.

---
📂 Parte del repositorio: *Proyectos de Ciencia de Datos aplicados a Recursos Humanos*.
