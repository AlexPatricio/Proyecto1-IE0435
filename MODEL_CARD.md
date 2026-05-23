# Model Card – Proyecto 1 IE0435

## Model name + version
Support Vector Machine (SVM) – Kernel Lineal  
Versión: 1.0 (modelo exportado en `B88639_Alex_Víquez.joblib`)

---

## Intended use / Out-of-scope
- **Uso previsto**: Clasificación de imágenes vectorizadas (128×128 píxeles) para identificar muestras limpias vs. con impurezas.  
- **Fuera de alcance**: No está diseñado para imágenes naturales complejas, objetos múltiples ni escenarios fuera del dataset académico.

---

## Data summary
- Dataset grupal construido a partir de matrices de cada estudiante.  
- Imágenes procesadas en escala de grises, redimensionadas y vectorizadas.  
- Variaciones mínimas de iluminación y cámara según condiciones de captura.  
- Consolidación realizada en el notebook `OneDataSet.ipynb`.

---

## Labeling process
- Etiquetado manual por estudiantes:  
  - `0` → muestra limpia  
  - `1` → muestra con impureza  
- Herramienta: notebooks de procesamiento (`ProcesadorDeImagenes.ipynb`).  
- Calidad: consistente, aunque puede existir ruido en casos límite.

---

## Metrics
- División de datos: `train_test_split` (entrenamiento/prueba).  
- Métricas: accuracy, precision, recall, f1-score.  
- Resultados principales:  
  - **SVM Lineal** → 100.00 %  
  - Árbol de Decisión → 99.08 %  
  - Random Forest → 94.50 %  
  - KNN k=3 → 90.83 %  
  - KNN k=7 → 87.16 %  
  - SVM RBF → 83.49 %  
  - Naive Bayes → 77.06 %  
  - KNN k=5 → 70.64 %  
  - Árbol de Decisión (max_depth=5) → 66.06 %

---

## Ethical / Safety notes
- Posibles sesgos por iluminación y fondos en las imágenes.  
- Dependencia de la calidad de cámara utilizada por cada estudiante.  
- Dataset pequeño → riesgo de sobreajuste y baja generalización.

---

## Limitations
- No maneja objetos pequeños con oclusión.  
- Sensible a imágenes borrosas (blur).  
- Dataset reducido y balance limitado entre clases.  
- No probado en condiciones reales de producción.

---

## Reproducibility
- **Comandos principales**:
  ```python
  !pip install scikit-learn pandas numpy
  from sklearn.svm import SVC
  model = SVC(kernel='linear')
  model.fit(X_train, y_train)
---
## Exportación: 
- Modelo guardado con joblib.dump() en carpeta modelo/.
---
## Hardware usado 
- Google Colab (CPU estándar).
