# 📊 Análisis de Deserción de Clientes en Telecom (Parte 1)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458)
![Plotly](https://img.shields.io/badge/Library-Plotly-informational)
![Seaborn](https://img.shields.io/badge/Library-Seaborn-green)

## 📌 Descripción del Proyecto
En la industria, la retención de clientes es crítica. Este proyecto analiza un conjunto de datos de una compañía que brinda servicios de internet, teléfonico, etc., para identificar patrones de comportamiento en los clientes que abandonan el servicio (**Churn**). 

## ❓ Problemática
La empresa enfrenta una pérdida constante de usuarios y desconoce las causas raíz. Se busca responder:
1.  ¿Qué tipo de contratos favorecen la fuga?
2.  ¿En qué momento del ciclo de vida del cliente ocurre el abandono?
3.  ¿Influyen los métodos de pagos?

## 🛠️ Tecnologías Utilizadas
* **Python:** Lenguaje principal para el análisis.
* **Pandas:** Limpieza y manipulación de datos (ETL).
* **Plotly Express:** Visualizaciones interactivas (Sunburst, Boxplots).
* **Seaborn & Matplotlib:** Gráficos estadísticos estáticos.

---

## 🔍 Análisis y Hallazgos Clave

### 1. La Influencia del Tipo de Contrato
El análisis revela que la flexibilidad contractual es el factor #1 de riesgo.

> **[INSERTA TU GRÁFICO DE BARRAS AQUÍ]**
> *Ruta sugerida: `img/grafico_contratos.png`*

* **Insight:** Los clientes con contrato **"Mes a Mes"** representan la gran mayoría de los abandonos. Los contratos a largo plazo (1 o 2 años) generan una lealtad casi total.

### 2. La "Zona de Peligro" (Antigüedad)
Utilizando Boxplots, analizamos la distribución de la permanencia (*Tenure*) de los usuarios.

> **[INSERTA TU GRÁFICO BOXPLOT AQUÍ]**
> *Ruta sugerida: `img/boxplot_tenure.png`*

* **Insight:** La fuga es un problema de *Onboarding*. La mediana de antigüedad de los clientes que se van es de apenas **10 meses**. Si un cliente supera los primeros 2 años, la probabilidad de abandono cae drásticamente.

### 3. El Efecto "Adherencia" (Stickiness)
Se descubrió una relación entre la cantidad de servicios contratados y la fidelidad.
* **Insight:** Los clientes que contratan "paquetes" (Internet + Seguridad + TV) tienden a quedarse más tiempo que aquellos que tienen un solo servicio.

---

## 🧹 Limpieza de Datos (Data Cleaning)
Antes del análisis, se realizaron los siguientes pasos de pre-procesamiento:
* Conversión de la columna `TotalCharges` a numérica (manejo de cadenas vacías).
* Mapeo de variables categóricas (0/1 a "No/Sí") para mejorar la legibilidad de los gráficos.
* Creación de variables sintéticas como `Total_Servicios` para medir la adherencia.

## 🚀 Conclusiones y Recomendaciones
Basado en los datos, se sugiere a la gerencia:

1.  **Migración de Contratos:** Crear incentivos agresivos para mover a clientes "Mes a Mes" hacia contratos anuales.
2.  **Foco en el Primer Año:** Implementar un programa de fidelización intensivo durante los primeros 12 meses (La "Zona de Peligro").
3.  **Revisión de Métodos de Pago:** Investigar fallos o fricciones en el pago con "Cheque Electrónico", ya que presenta una tasa de abandono anormalmente alta.

## 🔮 Próximos Pasos
* Implementar un modelo de **Machine Learning (Regresión Logística / Random Forest)** para predecir la probabilidad de fuga futura.
* Segmentar a los clientes de alto valor (LTV) para priorizar su retención.

---
*Proyecto realizado por DAO Estudiante*