# Deteccion de Churn de Clientes - Aprendizaje Supervisado

## Descripcion del Problema

Implementacion de modelos supervisados para predecir el abandono (churn) de clientes
a partir de metricas RFM (Recencia, Frecuencia, Monetario) y variables de comportamiento
de compra. El dataset contiene 200 clientes con 43 variables cada uno.

Variable objetivo: churn (1 = cliente perdido, 0 = activo)
Tasa de churn: ~29%

## Estructura del Repositorio

    datos_clientes.csv          # Dataset original
    taller_churn_ml.ipynb       # Notebook principal
    README.md                   # Este archivo

## Metodologia

1. EDA - Analisis univariado, bivariado, matriz de correlacion y variables categoricas
2. Preprocesamiento - Imputacion mediana, One-Hot Encoding, StandardScaler, split 80/20
3. Modelos - Arbol de Decision, SVM (RBF), Random Forest
4. Evaluacion - Accuracy, Precision, Recall, F1-Score, AUC-ROC, validacion cruzada CV-5

## Resultados

| Modelo            | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|-------------------|----------|-----------|--------|----------|---------|
| Arbol de Decision | 1.0000   | 1.0000    | 1.0000 | 1.0000   | 1.0000  |
| SVM (RBF)         | 1.0000   | 1.0000    | 1.0000 | 1.0000   | 1.0000  |
| Random Forest     | 1.0000   | 1.0000    | 1.0000 | 1.0000   | 1.0000  |

## Nota sobre los Resultados

Los tres modelos obtuvieron metricas perfectas (1.0), lo que sugiere
overfitting dado el tamano reducido del dataset (200 registros).
En un escenario real se recomienda usar un dataset mas grande y
aplicar tecnicas como regularizacion mas agresiva o validacion cruzada
con mas folds.

## Tecnologias

- Python
- scikit-learn
- pandas, numpy, matplotlib, seaborn

## Equipo

- Luis Sebastian Arias Loaiza
- Christian David Guerra Castro
- Angelo Daniel Guevara Salazar
- Cristian Paul Quintana Velasquez

## Como ejecutar

    pip install pandas numpy matplotlib seaborn scikit-learn
    jupyter notebook taller_churn_ml.ipynb
