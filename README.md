# Microproyecto 3 — Azure Machine Learning
**Predicción de Abandono de Clientes (Customer Churn)**

> Computación en la Nube — Universidad Autónoma de Occidente  
> Estudiante: Marlon Valencia Velosa

## Descripción

Solución de Machine Learning para predecir qué clientes de **RetailCo S.A.S.** tienen alta probabilidad de abandonar la plataforma, usando **Azure Machine Learning Designer**.

## Resultados del Modelo

| Métrica | Valor |
|---------|-------|
| Accuracy | 80.58% |
| AUC | 0.855 |
| Precision | 68.11% |
| Recall | 56.41% |
| F1 Score | 0.617 |

## Pipeline Azure ML

```
Dataset (telco-churn)
    → Select Columns (excluye customerID)
    → Clean Missing Data
    → Edit Metadata (Label: Churn)
    → Normalize Data (MinMax)
    → Split Data (80/20)
    → Two-Class Boosted Decision Tree + Train Model
    → Score Model
    → Evaluate Model
```

## Estructura del Repositorio

```
├── docs/
│   ├── analisis_requerimientos.html   # Sección 1: Análisis
│   ├── propuesta_diseno.html          # Sección 2: Diseño
│   └── informe_final.html             # Informe completo
├── dataset/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv  # Dataset IBM Telco
├── pipeline/                          # Configuración del pipeline
└── demo/                              # Demo de la solución
```

## Tecnologías

- Microsoft Azure Machine Learning Studio
- Azure Blob Storage
- Azure Compute Cluster (Standard_DS2_v2)
- Dataset: [Telco Customer Churn — IBM](https://github.com/IBM/telco-customer-churn-on-icp4d)
