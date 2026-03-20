# 🛢️ OilyGiant: Optimización de Extracción Petrolera y Análisis de Riesgo

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-F7931E.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Visualization-11557c.svg)

## 📌 Descripción del Proyecto
En el sector de extracción de hidrocarburos, la decisión de dónde perforar nuevos pozos conlleva inversiones de capital masivas y un alto grado de incertidumbre geológica. Este proyecto se desarrolla para la compañía de extracción **OilyGiant**, con el objetivo estratégico de identificar la región más rentable y segura para la apertura de 200 nuevos pozos petrolíferos.

A partir de un presupuesto operativo de 100 millones de dólares y datos de exploración de tres regiones distintas, el reto principal trasciende la simple predicción de volumen; exige cuantificar la rentabilidad esperada y **mitigar el riesgo financiero** asociado a cada zona geográfica.

## 🎯 Objetivo de Negocio
* Seleccionar la mejor región para desarrollar 200 pozos de extracción.
* Garantizar un margen de riesgo de pérdida financiera **estrictamente inferior al 2.5%**.
* Maximizar el retorno de inversión (ROI) estimado.

## ⚙️ Metodología y Herramientas
1. **Análisis Exploratorio de Datos (EDA):** Limpieza y preparación de tres bases de datos geológicas (100,000 registros cada una), eliminando variables no predictivas.
2. **Modelado Predictivo:** Entrenamiento y validación de modelos de **Regresión Lineal** para pronosticar el volumen de reservas de crudo en pozos individuales (División 75:25).
3. **Cálculo de Punto de Equilibrio:** Determinación del volumen mínimo de producción (111.1 mil barriles) para evitar pérdidas operativas.
4. **Evaluación de Riesgos (Bootstrapping):** Simulación de 1,000 escenarios de extracción para modelar la distribución de las ganancias, calcular intervalos de confianza (95%) y determinar la probabilidad de pérdidas.

## 📊 Resultados Técnicos

| Región | RMSE (Error Medio) | Volumen Predicho (Promedio) | Beneficio Promedio Proyectado | Riesgo de Pérdida |
| :--- | :---: | :---: | :---: | :---: |
| **Región 0** | 37.76 | 92.40 mil barriles | $4,278,475 USD | 5.50% ❌ |
| **Región 1** | **0.89** | 68.71 mil barriles | **$5,113,627 USD** | **0.90%** ✅ |
| **Región 2** | 40.15 | 94.77 mil barriles | $4,025,756 USD | 7.40% ❌ |

*(Nota: En la carpeta `images/` de este repositorio se encuentran los gráficos de dispersión de predicciones y los histogramas de la simulación de Bootstrapping).*

## 💡 Conclusión y Recomendación Estratégica
El análisis demuestra que basarse únicamente en el promedio general de reservas es engañoso y altamente riesgoso, ya que ninguna región supera el punto de equilibrio de forma natural sin la intervención de un modelo predictivo.

El algoritmo logró un desempeño excepcional en la **Región 1**, alcanzando un margen de error casi nulo (RMSE de 0.89). Al someter estas predicciones a la simulación de Bootstrapping, la Región 1 fue la única en cumplir con las estrictas condiciones de negocio de OilyGiant:
* Proyecta el **mayor beneficio neto** (+$5.11 millones USD).
* Reduce el riesgo operativo a **0.90%**, blindando el capital de la compañía contra la incertidumbre geológica.

**Recomendación:** Se aprueba y recomienda destinar el presupuesto de 100 millones de dólares para el desarrollo de infraestructura exclusivamente en la Región 1 (`geo_data_1.csv`).

## 🚀 Cómo ejecutar este proyecto
1. Clona este repositorio: `git clone https://github.com/joseariasduran/oilygiant-risk-analysis.git`
2. Instala las dependencias requeridas: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Ejecuta el Jupyter Notebook principal para reproducir el análisis paso a paso y generar las visualizaciones.

---
**Autor:** José Arias Durán  
**Contacto:** [LinkedIn] | [GitHub](https://github.com/joseariasduran)
