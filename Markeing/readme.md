# 📊 Segmentación de Clientes y Análisis de Características con Machine Learning  

![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange) ![Python](https://img.shields.io/badge/Python-3.10-blue) ![Status](https://img.shields.io/badge/Status-Completed-success) ![KMeans](https://img.shields.io/badge/Model-KMeans-yellow) ![Autoencoder](https://img.shields.io/badge/Model-Autoencoder-red)  

---

## 📌 Resumen del Proyecto

Este proyecto aborda la **segmentación de clientes** utilizando técnicas de *Machine Learning*, con el objetivo de **identificar grupos distintivos basados en patrones de comportamiento y características crediticias**.  

Se emplearon dos enfoques principales:  
- 🔹 **K-Means tradicional** aplicado directamente sobre los datos.  
- 🔹 **Autoencoder + K-Means** → reducción de dimensionalidad previa con un autoencoder y posterior clustering.  

Ambos métodos se comparan para evaluar mejoras en la segmentación.  

---

## 🧭 Flujo de Trabajo

### 1. 🔎 Análisis Exploratorio de Datos (EDA)
- Carga y visualización inicial del dataset.  
- Eliminación de la columna `CUST_ID` por irrelevante.  
- Estadísticas descriptivas de variables.  
- Imputación de valores nulos en `MINIMUM_PAYMENTS` y `CREDIT_LIMIT` con la media.  
- Eliminación de duplicados.  
- Visualización de correlaciones.  
- Histogramas y diagramas de caja → identificación de distribuciones sesgadas y outliers.  

---

### 2. 🛠️ Preprocesamiento de Datos
- **Escalado con StandardScaler** para normalizar variables numéricas.  
- Preparación del dataset para K-Means y entrenamiento del autoencoder.  

---

### 3. 📊 Clustering con K-Means (Datos Originales Escalados)
- Determinación de clústeres con el **método del codo** → `k = 6`.  
- Evaluación con métricas internas:  
  - Silhouette Score  
  - Davies-Bouldin Index  
  - Calinski-Harabasz Index  
- Visualización en 2D con **PCA**.  
- Perfiles de los clústeres → segmentos de clientes identificados:  

| Clúster | Perfil Identificado |
|---------|----------------------|
| 1 | Compradores Frecuentes a Plazos |
| 2 | Compradores de Alto Gasto |
| 3 | Usuarios de Anticipos en Efectivo |
| 4 | Clientes de Baja Actividad |
| 5 | Clientes Premium de Alto Gasto |
| 6 | Usuarios Intensivos de Anticipos en Efectivo |

---

### 4. 🤖 Reducción de Dimensionalidad con Autoencoder
- Implementación con **TensorFlow/Keras**.  
- Reducción de 17 → 10 dimensiones.  
- Arquitectura con capas densas (encoder + decoder).  
- Función de pérdida: **Mean Squared Error (MSE)**.  
- Guardado de pesos entrenados.  
- Extracción
