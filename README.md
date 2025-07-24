
---

## Objetivo

Desarrollar y comparar distintos modelos predictivos para estimar el volumen futuro de violaciones por exceso de velocidad en zonas escolares, utilizando datos históricos abiertos de la Ciudad de Chicago.

---

## Tecnologías y Herramientas

- Python 3.x
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn (Random Forest, XGBoost)
- Facebook Prophet
- Statsmodels (Holt-Winters)
- Jupyter Notebook

---

## Modelos Implementados

| Modelo                  | Frecuencia | Mejor MAPE | Comentario |
|-------------------------|------------|-------------|------------|
| Random Forest           | Tabular    | 45.71%      | Buen R², sensible a extremos |
| XGBoost (Semanal)       | Tabular    | 42.60%      | Preciso y robusto             |
| Holt-Winters (Semanal)  | Semanal    | 0.53%       | Mejor HW, sin sobreajuste     |
| Prophet (Semanal)       | Semanal    | **0.34%**   | ✅ Mejor modelo general        |

---

## Resultados

- **Mejor modelo general:** Prophet con frecuencia semanal desde 2021.
- **Mejor modelo tradicional:** Holt-Winters con estacionalidad semanal (52). ***Este se debe ajustar, aunque dio valores "Buenos" parecen engañosos
- Se identificaron patrones estacionales claros (por semana y año).
- El análisis permite anticipar violaciones futuras y optimizar acciones preventivas.

---

## Conclusiones

- La calidad del preprocesamiento fue clave para el rendimiento de los modelos.
- El análisis de series de tiempo resultó más efectivo que los modelos estructurados.
- La integración de modelos y visualizaciones permitió validar hallazgos desde distintas perspectivas.

---

## Recomendaciones

- Incorporar variables externas (feriados, clima, eventos).
- Automatizar el pipeline de actualización del modelo.
- Desplegar un dashboard para visualización continua de predicciones.

---

## Datos Abiertos

- [Speed Camera Violations - City of Chicago](https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4)

---

## Autor

Bryan Leon  
Maestría en Analítica de Datos  
Proyecto final – Minería de Datos  
Julio 2025

---

