# Análisis de Churn de Clientes - Challenge Telecom X

Este repositorio contiene el proceso completo de **Extracción, Transformación y Carga (ETL)** y **Análisis Exploratorio de Datos (EDA)** realizado para afrontar el desafío de la alta tasa de evasión (churn) de clientes en la empresa ficticia "Telecom X".

## 🎯 Objetivo del Proyecto

El objetivo principal es procesar, limpiar y analizar un conjunto de datos de clientes para identificar patrones y características clave de los usuarios que cancelan su servicio. El resultado es un conjunto de datos limpios y un análisis inicial que servirá como base para que un equipo de Ciencia de Datos construya modelos predictivos y entienda las causas raíz del problema.

## 🚀 Metodología

El proyecto se desarrolló siguiendo los siguientes pasos, basados en una metodología de análisis de datos estándar:

1.  **Extracción:** Conexión a una API para obtener los datos de los clientes en formato JSON anidado.
2.  **Transformación y Limpieza (ETL):**
    *   **Normalización:** Se aplanó la estructura JSON utilizando `pandas.json_normalize` para crear un DataFrame tabular.
    *   **Manejo de Inconsistencias:** Se corrigieron valores vacíos en la columna `Churn` y espacios en blanco en la columna `Charges.Total`.
    *   **Ajuste de Tipos de Datos:** Se convirtieron columnas a sus tipos de datos correctos (ej. `Charges.Total` a `float64`, y columnas binarias como 'Yes'/'No' a `int64`).
    *   **Ingeniería de Características:** Se crearon las columnas `Cuentas_Diarias` y `NumServices` para enriquecer el análisis.
3.  **Análisis Exploratorio y Visualización (EDA):**
    *   Análisis de la distribución de la variable objetivo (`Churn`).
    *   Visualización de la tasa de churn para las principales variables categóricas (`Contract`, `PaymentMethod`, `InternetService`).
    *   Análisis de la distribución de variables numéricas (`tenure`, `Charges.Monthly`) en relación con el churn utilizando histogramas interactivos.
    *   Cálculo y visualización de una matriz de correlación para cuantificar la relación entre las variables.

## 🛠️ Tecnologías Utilizadas

*   **Lenguaje:** Python
*   **Bibliotecas de Análisis:**
    *   **Pandas:** Para la manipulación, limpieza y análisis de datos.
    *   **NumPy:** Para operaciones numéricas eficientes.
    *   **Matplotlib y Seaborn:** Para la creación de visualizaciones estáticas.
    *   **Plotly Express:** Para la creación de visualizaciones interactivas.
*   **Entorno de Desarrollo:** Google Colaboratory.

## 📁 Estructura del Repositorio

```
├── Analisis_Churn_TelecomX.ipynb       # Notebook principal con todo el proceso de ETL y EDA.
├── data/                               # Carpeta con los datos limpios listos para analizar
└── README.md                           # Este archivo.
```

## ⚙️ Cómo Ejecutar el Proyecto

1.  **Prerrequisitos:** Asegúrate de tener un entorno que pueda ejecutar notebooks de Python (como Google Colab, Jupyter Notebook o VS Code).
2.  **Clonar el Repositorio (Opcional):**
    ```bash
    git clone [URL-DE-TU-REPOSITORIO]
    ```
3.  **Abrir en Google Colab:** La forma más sencilla es abrir el archivo `Analisis_Churn_TelecomX.ipynb` directamente en Google Colab.
4.  **Ejecutar las Celdas:** El notebook está diseñado para ser ejecutado de forma secuencial. Todas las dependencias se cargan y los datos se extraen desde la API directamente en el código.

## 📊 Análisis y Hallazgos Principales

El análisis exploratorio reveló varios factores clave directamente relacionados con la evasión de clientes:

*   **Tipo de Contrato:** Es el predictor más fuerte. Los clientes con contrato **mes a mes** tienen una tasa de churn superior al **40%**, mientras que en los contratos a largo plazo es casi nula.
*   **Antigüedad (Tenure):** Existe una fuerte correlación negativa. La gran mayoría de las cancelaciones ocurren en los **primeros meses** del servicio. Los clientes de larga data son extremadamente leales.
*   **Cargos Mensuales y Servicios:** Los clientes con **cargos mensuales altos**, especialmente aquellos con **Fibra Óptica**, son más propensos a cancelar. Esta tendencia se acentúa si **no tienen contratados servicios de soporte o seguridad**, los cuales actúan como factores de retención.
*   **Método de Pago:** El pago con **cheque electrónico** está asociado a una tasa de churn anormalmente alta (casi 45%), sugiriendo fricción o problemas en este proceso.

## 💡 Recomendaciones Estratégicas

Basado en los hallazgos, se proponen las siguientes acciones para reducir la tasa de churn:

1.  **Fomentar el Compromiso a Largo Plazo:** Crear campañas para migrar a los clientes de "mes a mes" a planes anuales, ofreciendo incentivos claros.
2.  **Fortalecer la Experiencia del Cliente Nuevo:** Implementar un programa de "onboarding" robusto durante los primeros 90 días para asegurar la calidad y el valor percibido desde el inicio.
3.  **Aumentar el Valor de los Planes Premium:** "Blindar" los planes de Fibra Óptica incluyendo servicios de seguridad y soporte técnico por defecto para justificar su alto costo.
4.  **Optimizar la Experiencia de Pago:** Investigar y mejorar el proceso de pago con cheque electrónico e incentivar la adopción de métodos de pago automáticos.

## ✒️ Autor

*   **Jimena Mariel Castro Ramírez**
*   **GitHub:** [jimenaCastro73](https://github.com/jimenaCastro73)

## 👏 Agradecimientos

*   Los datos para este desafío fueron proporcionados por **Alura LATAM**.
*   El dataset original se encuentra en el repositorio de [Ingrid Cristh](https://github.com/ingridcristh/challenge2-data-science-LATAM).
