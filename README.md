# Diplomatura-ciencia-de-
# Predicción de compra de boletos turísticos

Proyecto grupal (Grupo N°13) de la Diplomatura en Ciencia de Datos.

## Objetivo
Predecir la probabilidad de que un cliente compre un boleto turístico el próximo mes, para dirigir las campañas de marketing solo a los clientes con más chances de compra y reducir costos.

## Qué hice
- Análisis exploratorio y limpieza de datos (valores faltantes, outliers, one-hot encoding, normalización).
- Creación de variables, por ejemplo tiempo desde la última compra.
- Manejo de clases desbalanceadas (16% compra / 84% no compra) con ponderación de clases y validación cruzada estratificada.
- Comparación de 6 modelos: Baseline, Regresión Logística, Árbol de Decisión, Random Forest, XGBoost y LightGBM.
- Ajuste del umbral de decisión (0.35) para equilibrar precisión y recall.
- Segmentación de clientes por probabilidad de compra (baja, media, alta) y propuesta de acciones de marketing para cada segmento.

## Herramientas
Python, pandas, scikit-learn, XGBoost, LightGBM, matplotlib

## Resultados
| Modelo | F1-score | AUC |
|---|---|---|
| Baseline | 0.000 | 0.500 |
| Regresión Logística | 0.440 | 0.710 |
| Árbol de Decisión | 0.858 | 0.938 |
| Random Forest | 0.930 | 0.928 |
| LightGBM | 0.941 | 0.998 |
| **XGBoost** | **0.977** | **1.000** |

El mejor modelo fue **XGBoost**. Con el umbral en 0.35 alcanzó una precisión de 0.98 y un recall de 0.98.

## Variables más influyentes
- Frecuencia de compra previa y tiempo desde la última compra
- Interacción con campañas anteriores y visitas a la página web
- Tipo de destino (nacional/internacional) y estacionalidad

## Aplicación al negocio
Se armó una simulación ilustrativa (con valores de ejemplo, no datos reales) que compara una campaña sin modelo contra una campaña segmentada por probabilidad de compra.

## Limitaciones y mejoras
- Faltan datos de varias temporadas para mejorar la robustez.
- El modelo debería reentrenarse si cambia la estructura de los datos.
- Se podrían probar series temporales o integrar el modelo con herramientas de marketing automatizado.

## Archivos
- `Diplomatura-Ciencia-de-Datos.ipynb`: código completo del análisis y los modelos.
