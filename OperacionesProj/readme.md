# 🩺 Clasificación de Condiciones Pulmonares con CNN
![Deep Learning](https://img.shields.io/badge/Deep--Learning-red) ![Python](https://img.shields.io/badge/Python-3.10-blue) ![Status](https://img.shields.io/badge/Status-Experimental-yellow) ![License](https://img.shields.io/badge/License-MIT-lightgrey)  

Este proyecto se centra en el **desarrollo de un modelo de clasificación de imágenes médicas** utilizando **redes neuronales convolucionales (CNN)** para diagnosticar automáticamente diferentes condiciones pulmonares (COVID-19, Normal, Neumonía Vírica, Neumonía Bacteriana) a partir de radiografías de tórax.

---

## 🎯 Objetivo

El objetivo principal es:  

> **Desarrollar un modelo de apoyo al diagnóstico clínico** capaz de diferenciar entre varias condiciones pulmonares a partir de radiografías de tórax, explorando el potencial de las arquitecturas de aprendizaje profundo para aplicaciones médicas.

---

## 🔎 Enfoque Metodológico

El proyecto siguió las siguientes etapas:

1. **Selección de Modelo Pre-entrenado:**  
   Uso de **ResNet50** como base, congelando la mayoría de sus capas y añadiendo capas densas personalizadas para la clasificación.

2. **Preprocesamiento de Datos:**  
   Aplicación de **técnicas de aumento de datos** (data augmentation) para mejorar la generalización.

3. **Entrenamiento del Modelo:**  
   Ajuste del modelo sobre un conjunto de datos de radiografías de tórax multiclase.

4. **Evaluación del Modelo:**  
   Uso de métricas de **precisión, recall y matriz de confusión** para analizar el desempeño por clase.

---

## 📌 Hallazgos Clave

- **Precisión general:** ~62.5%.  
- **COVID-19 (Clase 0):** recall del **100%**, aunque precisión del 59%.  
- **Normal, Neumonía Vírica y Bacteriana:** desempeño más variable, con valores de precisión y recall entre 40% y 67%.  
- La **matriz de confusión** evidencia que el modelo aún confunde algunas clases entre sí.  

Estos resultados muestran un **desempeño desigual entre clases**, destacando que el modelo es especialmente sensible a detectar COVID-19, pero menos robusto al distinguir entre tipos de neumonía.

---

## 📈 Resultados del Modelo (ResNet50 + Capas Densas)

| Clase                 | Precision | Recall |
|------------------------|-----------|--------|
| **COVID-19 (0)**      | ~0.59     | **1.00** |
| **Normal (1)**        | ~0.40-0.60| ~0.50   |
| **Neumonía Vírica (2)**| ~0.45-0.67| ~0.55   |
| **Neumonía Bacteriana (3)** | ~0.50-0.65| ~0.40-0.60 |

> ⚠️ El modelo muestra **potencial**, pero aún necesita mejoras antes de ser considerado para uso clínico real.

---

## 🏁 Conclusiones e Implicaciones

- El modelo desarrollado **puede servir como herramienta de apoyo** al diagnóstico médico.  
- La **precisión actual (62.5%)** es insuficiente para uso clínico directo.  
- El rendimiento por clase indica que **COVID-19 es más fácilmente identificable** que otras patologías.  
- Se requieren mejoras significativas en generalización y diferenciación de clases similares.  

### 🚀 Recomendaciones para mejorar:
- Ampliar y diversificar el conjunto de datos.  
- Ajustar hiperparámetros (learning rate, optimizadores, batch size).  
- Usar técnicas adicionales de regularización (**dropout, L2**).  
- Probar otras arquitecturas CNN pre-entrenadas (DenseNet, EfficientNet) o diseñar arquitecturas personalizadas.  
- Evaluar con métricas clínicas clave (**sensibilidad y especificidad**).  

En general, este proyecto demuestra el **potencial del Deep Learning en radiología**, pero también subraya la necesidad de **validación rigurosa y datos de calidad** antes de la aplicación en entornos médicos reales.

---
📂 Parte del repositorio: *Proyectos de Deep Learning aplicados a Imágenes Médicas*.
