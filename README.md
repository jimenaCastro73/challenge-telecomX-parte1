# Análisis de Churn de Clientes - Challenge Telecom X

Este repositorio contiene el proceso completo de **Extracción, Transformación y Carga (ETL)** y **Análisis Exploratorio de Datos (EDA)** realizado para afrontar el desafío de la alta tasa de evasión (churn) de clientes en la empresa ficticia "Telecom X".

## 🎯 Objetivo del Proyecto

El objetivo principal es procesar, limpiar y analizar un conjunto de datos de clientes para identificar patrones y características clave de los usuarios que cancelan su servicio. El resultado es un conjunto de datos limpios y un análisis inicial que servirá como base para que un equipo de Ciencia de Datos construya modelos predictivos y entienda las causas raíz del problema.

## 🚀 Metodología

El proyecto se desarrolló siguiendo los siguientes pasos, basados en una metodología de análisis de datos estándar:

1.  **Extracción:** Conexión a una API para obtener los datos de los clientes en formato JSON.
2.  **Exploración Inicial:** Uso de `pandas` para cargar los datos y realizar una primera revisión de su estructura, tipos de datos, valores ausentes y estadísticas descriptivas.
3.  **Limpieza y Transformación (ETL):**
    *   Manejo de valores nulos y datos inconsistentes.
    *   Corrección de tipos de datos para facilitar el análisis (ej. convertir columnas de texto a numéricas o de fecha).
    *   Creación de nuevas columnas (ingeniería de características) para enriquecer el análisis.
4.  **Análisis y Visualización:**
    *   Análisis de las variables para entender su relación con la evasión de clientes.
    *   Uso de `matplotlib` y `seaborn` para crear visualizaciones (gráficos de barras, histogramas, etc.) que comuniquen de forma clara los hallazgos principales.

## 🛠️ Tecnologías Utilizadas

*   **Lenguaje:** Python
*   **Bibliotecas de Análisis:**
    *   **Pandas:** Para la manipulación y limpieza de datos.
    *   **Matplotlib y Seaborn:** Para la visualización de datos.
    *   **Numpy:** Para operaciones numéricas eficientes.
*   **Entorno de Desarrollo:** Google Colaboratory.

## 📁 Estructura del Repositorio
