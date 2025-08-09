# TelecomX Customer Churn Analysis

## Descripción del Proyecto

Este proyecto presenta un análisis completo de **abandono de clientes (churn)** para TelecomX, una empresa de telecomunicaciones. El objetivo es identificar patrones, factores de riesgo y desarrollar estrategias para reducir la tasa de abandono de clientes mediante técnicas de análisis de datos y visualización.

### Objetivos Principales

- **Análisis Exploratorio de Datos (EDA)** comprehensive de la base de clientes
- **Identificación de factores** que influyen en el churn de clientes
- **Visualizaciones estratégicas** para comunicar insights clave
- **Recomendaciones accionables** para reducir el abandono de clientes
- **Cuantificación del impacto económico** del churn

## Estructura del Proyecto

```
Challenge_TelecomX_2/
├── README.md                                  # Documentación del proyecto
├── requirements.txt                           # Dependencias del proyecto
├── TelecomX_Data.json                         # Dataset principal (7,267 clientes)
├── telecom_churn_analysis_fbeltran.ipynb      # Notebook Parte 1: Análisis Exploratorio
├── telecom_churn_ml_prediction.ipynb          # Notebook Parte 2: Machine Learning
├── example/                                   # Directorio de ejemplos
└── .git/                                      # Control de versiones Git
```

## 📊 Dataset

### Características del Dataset

- **Tamaño**: 7,267 registros de clientes
- **Formato**: JSON con estructura anidada
- **Características**: 20+ variables incluyendo datos demográficos, servicios contratados y estado de churn

### Variables Principales

- **Demográficas**: CustomerID, Gender, SeniorCitizen, Partner, Dependents
- **Servicios**: PhoneService, MultipleLines, InternetService, OnlineSecurity, etc.
- **Contractuales**: Contract, PaymentMethod, PaperlessBilling
- **Financieras**: MonthlyCharges, TotalCharges, tenure
- **Target**: Churn (Yes/No)

## Configuración del Entorno

### Requisitos Previos

```bash
# Python 3.7+
# Jupyter Notebook o JupyterLab
```

### Instalación Rápida de Dependencias

```bash
# Instalar todas las dependencias desde el archivo requirements.txt
pip install -r requirements.txt
```

## Flujo del Proyecto

### Parte 1: Análisis Exploratorio (`telecom_churn_analysis_fbeltran.ipynb`)

- Carga y limpieza de datos
- Análisis exploratorio de datos (EDA)
- Visualizaciones y insights
- Identificación de patrones de churn

### Parte 2: Machine Learning (`telecom_churn_ml_prediction.ipynb`)

- Preparación de datos para ML
- Entrenamiento de 7 modelos predictivos
- Evaluación con métricas completas
- Análisis de importancia de variables
- Recomendaciones estratégicas basadas en IA

## Resultados Principales

### Métricas Clave

- **Tasa de Churn Global**: 26.5%
- **Impacto Económico Anual**: ~$2.8M en pérdidas
- **Clientes en Riesgo**: 1,927 clientes activos
- **Potencial de Ahorro**: ~$700K anuales con 25% de reducción

### Factores de Alto Riesgo

| Factor                      | Tasa de Churn | Impacto |
| --------------------------- | ------------- | ------- |
| Contratos mes a mes         | 42.7%         | Alto    |
| Pago con cheque electrónico | 45.3%         | Alto    |
| Clientes nuevos (≤12 meses) | 47.4%         | Crítico |
| Servicio Fiber Optic        | 30.9%         | Medio   |
| Sin servicios adicionales   | 35.0%         | Medio   |

### Perfil Financiero

- **Clientes que abandonan**: $74.44 promedio mensual, 17.6 meses tenure
- **Clientes que permanecen**: $61.27 promedio mensual, 37.6 meses tenure

## Recomendaciones Estratégicas

### 🟥 Acciones Inmediatas (0-3 meses)

1. **Migración de Pagos**: Incentivar el cambio desde cheque electrónico
2. **Campañas de Retención**: Focalizar en contratos mes a mes
3. **Descuentos Dirigidos**: Para clientes con alta probabilidad de churn

### 🟨 Acciones a Medio Plazo (3-12 meses)

1. **Sistema de Alerta Temprana**: Implementar scoring de riesgo de churn
2. **Programa de Onboarding**: Mejorar experiencia primeros 12 meses
3. **Optimización de Precios**: Rebalancear tarifas vs servicios

### 🟩 Acciones a Largo Plazo (12+ meses)

1. **Modelo Predictivo**: Machine Learning para predicción de churn
2. **Programa de Lealtad**: Incentivos por permanencia a largo plazo
3. **Segmentación Avanzada**: Estrategias personalizadas por segmento

## Visualizaciones Incluidas

- **Distribución de Churn** por categorías demográficas
- **Análisis de Supervivencia** por tenure
- **Heatmaps de Correlación** entre variables
- **Gráficos de Barras** para factores de riesgo
- **Distribuciones** de variables financieras
- **Dashboard Ejecutivo** con métricas clave

## Características Técnicas

### Procesamiento de Datos

- **ETL Robusto**: Manejo de datos faltantes y inconsistencias
- **Limpieza Inteligente**: Corrección automática de valores erróneos
- **Validación de Calidad**: Verificación de integridad de datos

### Funciones Principales

- `safe_float_conversion()`: Conversión segura de tipos de datos
- `calculate_churn_metrics()`: Cálculo de métricas de negocio
- `generate_risk_segments()`: Segmentación por nivel de riesgo

### Modelos de Machine Learning

- **Logistic Regression**: Modelo lineal con interpretabilidad
- **Random Forest**: Ensemble de árboles con alta precisión
- **Gradient Boosting**: Boosting secuencial optimizado
- **K-Nearest Neighbors**: Clasificación por proximidad
- **Support Vector Machine**: Clasificador de margen máximo
- **Decision Tree**: Árbol interpretable con reglas claras
- **Naive Bayes**: Clasificador probabilístico eficiente

## Metodología

1. **Extracción**: Carga y parseo del JSON original
2. **Transformación**: Limpieza y normalización de datos
3. **Análisis Exploratorio**: Estadísticas descriptivas y univariadas
4. **Análisis Bivariado**: Relaciones entre variables y churn
5. **Visualización**: Creación de gráficos estratégicos
6. **Insights**: Identificación de patrones y oportunidades
7. **Recomendaciones**: Desarrollo de estrategias accionables
