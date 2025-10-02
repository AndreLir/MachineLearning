# 📝 Análisis de Sentimientos con Machine Learning

![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange) ![Python](https://img.shields.io/badge/Python-3.10-blue) ![Status](https://img.shields.io/badge/Status-Active-success) ![License](https://img.shields.io/badge/License-MIT-lightgrey)

Este proyecto se centra en la **clasificación de opiniones positivas y negativas** utilizando técnicas de **aprendizaje supervisado**. Se implementaron y compararon modelos de **Naive Bayes** y **Regresión Logística** para evaluar su desempeño en un conjunto de reseñas desbalanceado.

---

## 🎯 Objetivo

El objetivo principal es:

> **Desarrollar un modelo de Machine Learning capaz de analizar automáticamente opiniones de usuarios y clasificarlas en positivas o negativas, con énfasis en el tratamiento de datos desbalanceados para mejorar la detección de reseñas negativas.**

---

## 🔎 Enfoque Metodológico

El proyecto sigue un flujo de trabajo típico en **Procesamiento de Lenguaje Natural (NLP)** y **Ciencia de Datos**:

1. **Análisis Exploratorio de Datos (EDA):**

   * Distribución de opiniones positivas y negativas.
   * Identificación de desbalance de clases.
   * Limpieza y preprocesamiento del texto (tokenización, stopwords, lematización).

2. **Representación del Texto:**

   * Vectorización con **Bag of Words** y **TF-IDF**.

3. **Modelado Predictivo:**

   * Entrenamiento de **Naive Bayes** y **Regresión Logística**.
   * Evaluación en un dataset con alta desproporción de clases.

4. **Evaluación del Modelo:**

   * Métricas utilizadas: **Accuracy**, **Precision**, **Recall**, **F1-score**.
   * Comparación de desempeño entre modelos.

5. **Optimización y Consideraciones:**

   * Análisis del impacto del **desbalance de clases**.
   * Discusión de técnicas futuras (re-sampling, ajuste de umbral, embeddings).

---

## 📌 Hallazgos Clave

* Ambos modelos obtienen **alto rendimiento en la detección de opiniones positivas** (f1 > 0.95).
* El desempeño en la **detección de opiniones negativas** es bajo (recall = 0.25), lo que confirma la dificultad del desbalance.
* La **Regresión Logística supera levemente a Naive Bayes** en precisión y métricas globales.

---

## 📈 Resultados del Modelo

| Modelo             | Accuracy | F1 (Positivo) | F1 (Negativo) | Macro F1 |
| ------------------ | -------- | ------------- | ------------- | -------- |
| **Naive Bayes**    | 0.91     | 0.95          | 0.34          | 0.65     |
| **Reg. Logística** | 0.92     | 0.96          | 0.36          | 0.66     |

> ✅ La Regresión Logística ofrece un desempeño ligeramente superior, aunque ambos modelos presentan limitaciones para detectar sentimientos negativos.

---

## 🏁 Conclusión e Implicaciones

El análisis confirma que los modelos de **Machine Learning tradicionales** funcionan bien para clasificar reseñas positivas, pero **presentan limitaciones frente al desbalance de clases** al analizar reseñas negativas.

* **Regresión Logística** es la opción más sólida en este escenario, aunque la diferencia frente a Naive Bayes es mínima.
* Para una aplicación más robusta, se recomienda:

  * Rebalanceo de clases (SMOTE, oversampling).
  * Ajuste de umbrales de decisión.
  * Uso de **embeddings modernos (BERT, Word2Vec, FastText)** para capturar mejor los matices del lenguaje.

En conjunto, este proyecto sienta las bases para la **automatización del análisis de opiniones de usuarios**, con aplicaciones en atención al cliente, marketing digital y monitoreo de la reputación de marca.

---

📂 Parte del repositorio: *Proyectos de Machine Learning aplicados a Procesamiento de Lenguaje Natural (NLP).*

