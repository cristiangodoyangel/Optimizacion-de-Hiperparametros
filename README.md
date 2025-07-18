# 🧠 Clasificación y Optimización de Hiperparámetros - Medical Cost Dataset

Este proyecto implementa un pipeline completo de *Machine Learning* aplicado a un problema de clasificación utilizando el **Medical Cost Personal Dataset**, con enfoque en preprocesamiento, modelado y optimización de hiperparámetros.

---

## 📁 Dataset

- **Nombre:** Medical Cost Personal Dataset
- **Fuente:** Kaggle
- **Objetivo:** Clasificar si el costo médico de una persona será *alto o bajo* (usando la mediana como umbral)

---

## 🧪 Flujo de Trabajo

### 🔍 1. Exploración Inicial
- Revisión de estructura del dataset (`head`, `describe`, `info`)
- Verificación de valores nulos ✅
- Identificación de outliers (`bmi`, `charges`) mediante boxplots y método IQR

### 🧼 2. Preprocesamiento
- Imputación:
  - Numéricas: mediana
  - Categóricas: moda
- Codificación One-Hot para variables categóricas
- Escalado de características numéricas (`StandardScaler`)
- Integración con `ColumnTransformer`

### 🤖 3. Modelado Inicial
- Modelos evaluados:
  - Regresión Logística
  - K-Nearest Neighbors (KNN)
  - Árbol de Decisión
- Evaluación con **validación cruzada (cv=5)**

### 🧠 4. Optimización de Hiperparámetros
- `GridSearchCV` para Regresión Logística
- `RandomizedSearchCV` para Árbol de Decisión
- Comparación de resultados y mejora significativa en métricas

### 📊 5. Evaluación Final
- Separación train/test (80/20)
- Métricas evaluadas:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC-AUC
- Visualizaciones:
  - Matriz de confusión
  - Curva ROC

---

## ✅ Conclusiones

- Los modelos base mejoraron tras la optimización de hiperparámetros.
- La Regresión Logística optimizada mostró mejor equilibrio entre interpretabilidad y rendimiento.
- El uso de pipelines y `ColumnTransformer` permitió reproducibilidad y escalabilidad.
- El proyecto refuerza buenas prácticas en problemas de clasificación realistas con datos tabulares.

---

## 🛠️ Stack Tecnológico

- Python 3
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

## 📌 Versión

`v1.0.0` - Primera versión completa del proyecto

---

## 📂 Repositorio

Incluye:

- Notebook con todo el análisis (`.ipynb`)
- Dataset (`insurance.csv`)
- README con documentación
