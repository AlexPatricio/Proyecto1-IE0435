# Proyecto 1 – IE0435 Inteligencia Artificial Aplicada a la Ingeniería Eléctrica

Este repositorio contiene los entregables del **Proyecto 1**, cuyo objetivo es aplicar modelos clásicos de clasificación sobre un dataset grupal de imágenes procesadas para identificar granos de arroz como impurezas en un entorno de producción simulado.

---

## Objetivo general

Desarrollar un flujo completo de procesamiento, construcción de dataset y entrenamiento de modelos de clasificación utilizando técnicas clásicas de aprendizaje automático.

---

## Contenido del repositorio
- `ProcesadorDeImagenes.ipynb` → Notebook de preprocesamiento digital de imágenes (conversión a escala de grises, redimensionamiento y vectorización).  
- `OneDataSet.ipynb` → Consolidación del dataset grupal a partir de las matrices de todos los participantes.  
- `modelTrainer.ipynb` → Entrenamiento, comparación y selección del mejor modelo de clasificación.  
- `modelo/B88639_Alex_Víquez.joblib` → Modelo final exportado.  
- `DATASET.md` → Documentación del dataset grupal.  
- `MODEL_CARD.md` → Ficha técnica del modelo seleccionado.  
- `LICENSE` → Licencia MIT del proyecto.  
- `README.md` → Este documento explicativo.
---
## Extructura del repositorio

```
Proyecto1-IE0435/
├── README.md
├── DATASET.md
├── MODEL_CARD.md
├── OneDataSet.ipynb
├── modelTrainer.ipynb
├── ProcesadorDeImagenes.ipynb
└── modelo/
    └── B88639_Alex_Víquez.joblib
```
---

## Modelos probados
Se entrenaron y evaluaron los siguientes modelos clásicos usando `scikit‑learn`:
- Árbol de Decisión  
- Naive Bayes  
- K‑Nearest Neighbors (KNN)  
- Support Vector Machine (SVM)

---

## Evaluación y resultados
- División de datos: entrenamiento y prueba mediante `train_test_split`.  
- Métricas: accuracy, precision, recall y f1‑score.  
- Resultados principales:  
  - Árbol de Decisión:  99.08 % accuracy  
  - Naive Bayes:  77.06 % accuracy  
  - KNN (k = 3):  90.83 % accuracy  
  - SVM lineal:  100 % accuracy  


El modelo con mejor desempeño fue **SVM lineal**, alcanzando la mayor precisión en el conjunto de prueba.


---

## ▶️ Cómo reproducir el proyecto
1. Abrir los notebooks en **Google Colab**.  
2. Instalar dependencias:
   ```python
   !pip install scikit-learn pandas numpy
3. Ejecutar OneDataSet.ipynb para generar el dataset grupal.
4. Ejecutar modelTrainer.ipynb para entrenar y comparar modelos.
5. El mejor modelo se guarda automáticamente en la carpeta modelo/.

---
## Autor
Alex Patricio Víquez Víquez
Carné: B88639
IE0435- InteligenciaInteligencia Artificial Aplicada a la Ingeniería Eléctrica
Escuela de Ingeniería Eléctrica de la Universidad de Costa Rica
