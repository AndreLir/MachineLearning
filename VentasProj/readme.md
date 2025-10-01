# 🛒 Análisis y Predicción de Ventas en Tiendas
![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange) ![Python](https://img.shields.io/badge/Python-3.10-blue) ![Status](https://img.shields.io/badge/Status-Active-success) ![License](https://img.shields.io/badge/License-MIT-lightgrey)  

Este proyecto se centra en el **análisis exploratorio de datos de ventas** y en la **implementación de un modelo de predicción de series temporales** utilizando **Facebook Prophet** para estimar ventas futuras en base a datos históricos de tiendas.

---

## 🎯 Objetivo

El objetivo principal es:

> **Comprender los patrones de ventas y construir un modelo predictivo robusto que permita anticipar el comportamiento de ventas**, apoyando la toma de decisiones en gestión de inventario, planeación estratégica y marketing.

---

## 🔎 Enfoque Metodológico

El flujo de trabajo del proyecto siguió las etapas típicas de **Ciencia de Datos aplicada a series temporales**:

1. **Análisis Exploratorio de Datos (EDA):**  
   Identificación de correlaciones clave, tratamiento de valores faltantes y análisis de patrones temporales y estacionales.

2. **Preprocesamiento de Datos:**  
   Limpieza del dataframe de información de tiendas (`store_info_df`), principalmente en columnas de competencia y promociones (`Promo2`).

3. **Modelado Predictivo con Prophet:**  
   Entrenamiento de modelos con y sin inclusión de días festivos para capturar la estacionalidad anual, mensual y semanal.

4. **Evaluación de Modelos:**  
   Comparación mediante **Mean Absolute Error (MAE)** y **Mean Absolute Percentage Error (MAPE)** con validación cruzada.

---

## 📌 Hallazgos Clave del EDA

- **Correlaciones principales:**
  - 📈 Ventas y Clientes: fuerte correlación positiva.  
  - 📊 Ventas y Promociones (`Promo`): impacto directo y positivo en las ventas.  
  - 🔎 Variables como `CompetitionDistance` mostraron correlaciones más bajas.  

- **Patrones temporales:**
  - 🎄 **Estacionalidad Anual:** picos en diciembre por la temporada navideña.  
  - 📅 **Patrones Mensuales:** mayor actividad a inicios y finales de mes.  
  - 📆 **Patrones Semanales:** ventas más altas los lunes, más bajas los domingos.  

- **Características de tienda:**
  - 🏬 Tipo de Tienda **'b'** con ventas promedio más altas.  
  - 💡 Promociones no solo aumentan ventas, también desplazan la distribución hacia valores superiores.  

---

## 📈 Resultados del Modelo Prophet

Se evaluaron dos configuraciones para la **Tienda 10**:

| Modelo                           | MAE (~) | MAPE (~) |
|----------------------------------|---------|----------|
| **Sin días festivos**            | 636.74  | 10.73 %  |
| **Con festivos estatales**       | 609.04  | 10.29 %  |

> ✅ Incluir festivos estatales mejoró ligeramente la precisión, mostrando que estos eventos tienen un efecto cuantificable en las ventas.

---

## 🏁 Conclusión e Implicaciones

El proyecto logró demostrar un **flujo de trabajo completo de predicción de ventas**:  

- El **EDA** reveló relaciones clave (clientes, promociones y estacionalidad).  
- **Facebook Prophet** resultó efectivo para modelar series temporales con estacionalidad y eventos especiales.  
- El modelo con festivos estatales presentó un mejor desempeño, resaltando la importancia de **incorporar variables externas relevantes**.  

### 🚀 Próximos pasos recomendados:
- Optimizar hiperparámetros de Prophet.  
- Incluir variables adicionales (`StoreType`, `Assortment`, `CompetitionDistance`, etc.) como regresores.  
- Ampliar la evaluación a más tiendas para validar la robustez del modelo.  

En conjunto, este enfoque sienta las bases para una **herramienta estratégica de planificación de ventas, inventarios y marketing**.  

---
📂 Parte del repositorio: *Proyectos de Ciencia de Datos aplicados a Retail*.
