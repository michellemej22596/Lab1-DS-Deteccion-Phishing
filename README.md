# Detección de Phishing Basada en Análisis de URLs
Por Silvia Illescas y Michelle Mejía

## Descripción

Este proyecto implementa un sistema de clasificación de URLs para la detección de sitios **phishing** utilizando técnicas de *Machine Learning*.
El enfoque se basa exclusivamente en el análisis estructural y estadístico de las URLs, sin necesidad de acceder al contenido de las páginas web.

Se desarrolló un flujo completo que incluye exploración de datos, ingeniería de características, preprocesamiento, selección de variables, división de datos y entrenamiento de modelos de clasificación.

---

## Objetivo

Clasificar URLs como:

-  Legítimas
-  Phishing

Utilizando modelos supervisados y evaluando su desempeño con métricas relevantes en el contexto de ciberseguridad.

---

## Metodología

### Exploración de datos
- Análisis de balance de clases.
- Visualización de distribución.
- Análisis de correlación.

### Ingeniería de características
Se derivaron 15 características basadas en la estructura de la URL, incluyendo:

- Longitud total de la URL
- Número de subdominios
- Conteo de dígitos y caracteres especiales
- Ratio de dígitos
- Número de parámetros
- Entropía de Shannon
- Entropía relativa
- Entropía de caracteres no alfanuméricos

### Preprocesamiento
- Conversión de variable categórica (`status`) a binaria.
- Eliminación de duplicados.
- Limpieza y validación de datos.

### Selección de características
- Eliminación de columnas constantes.
- Análisis de correlación.
- Evaluación de importancia de variables.

### División de datos
- 📘 55% Entrenamiento
- 📙 15% Validación
- 📕 30% Prueba

---

## Modelos Implementados

- Regresión Logística (Baseline)
- Random Forest

---

## Métricas de Evaluación

Se utilizaron las siguientes métricas:

- Matriz de confusión
- Precisión (Precision)
- Recall
- Curva ROC
- AUC

El modelo **Random Forest** presentó mejor desempeño general, con mayor capacidad de discriminación entre URLs legítimas y phishing.

---

## Resultados

El modelo final demostró:

- Alta capacidad de detección de ataques (recall elevado).
- Buen balance entre precisión y recall.
- AUC superior a 0.90 en datos de prueba.

Esto indica una adecuada capacidad de generalización en datos no vistos.

---

## Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Conclusión

El análisis estructural de URLs combinado con técnicas de Machine Learning permite desarrollar modelos efectivos para la detección de phishing.

Si bien el modelo presenta un desempeño sólido, siempre existe un riesgo residual, por lo que su implementación en entornos reales debería complementarse con estrategias adicionales de seguridad.
