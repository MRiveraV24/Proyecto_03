# Segmentación de Clientes para Productos Financieros Personalizados

## Introducción
Este proyecto tiene como objetivo segmentar clientes de una empresa financiera para ofrecer un nuevo producto con límites de crédito personalizados. Los directivos necesitan determinar la cantidad óptima de grupos de clientes y cómo asignar nuevos clientes a estos grupos. Para lograrlo, se utilizaron datos históricos de clientes y técnicas avanzadas de análisis de datos.

---

## Contexto
La empresa busca mejorar la personalización de sus productos financieros mediante la segmentación de clientes. En lugar de adoptar un enfoque generalizado, se pretende dividir a los clientes en grupos más pequeños y homogéneos basados en características clave que la empresa ya monitorea. Esta estrategia permitirá diseñar ofertas adaptadas a las necesidades específicas de cada grupo.

---

## Objetivo
Los objetivos específicos de este proyecto son:

- Determinar el número óptimo de segmentos de clientes.
- Identificar las características clave que diferencian a cada grupo.
- Desarrollar un modelo que asigne nuevos clientes a los segmentos adecuados.
- Proporcionar una comprensión profunda de los datos para optimizar campañas de marketing dirigidas.

---

## Conjunto de Datos
El análisis se realizó sobre un conjunto de datos con las siguientes características:

- **Variables disponibles:**
  - Salario mensual (ingreso en pesos mexicanos).
  - Crédito tipo 1 (indica si posee un producto financiero específico; 1 = sí, 0 = no).
  - Crédito tipo 2 (similar a crédito tipo 1; 1 = sí, 0 = no).
  - Límite de tarjeta de crédito.
  - Años como cliente.
  - Interés previo en el producto (1 = sí, 0 = no).
- **Tamaño inicial:** 500 registros.
- **Tamaño final tras limpieza:** 486 registros.
- **Datos adicionales:** Se incluyó un conjunto de 50 nuevos clientes para validar el modelo.

---

## Metodología
El proyecto siguió las siguientes etapas:

1. **Exploración de Datos:**
   - Análisis descriptivo para comprender la distribución y correlaciones entre variables.
   - Identificación de valores atípicos y análisis de correlación.
   - Hallazgos clave: correlación positiva entre el límite de crédito y los años como cliente.

2. **Preprocesamiento de Datos:**
   - Limpieza de valores atípicos.
   - Escalado de variables numéricas para normalizar los datos.

3. **Modelado:**
   - Algoritmo principal: **K-means clustering**.
   - Selección del número óptimo de clusters mediante el método del codo.
   - Uso de Análisis de Componentes Principales (PCA) para reducir la dimensionalidad y facilitar la visualización.
   - Aplicación de K-means sobre los componentes principales.

4. **Evaluación:**
   - Métricas utilizadas:
     - Índice de silueta.
     - Índice Calinski-Harabasz.
     - Índice Davies-Bouldin.

5. **Validación:**
   - El modelo fue aplicado a un conjunto de datos de 50 nuevos clientes para asignarlos a los segmentos identificados.

---

## Resultados

- **Segmentos Identificados:** Se agruparon los clientes en 4 segmentos bien diferenciados.
- **Características de los Clusters:**
  - **Grupo 0 y Grupo 3:** Clientes con salarios y límites de tarjeta bajos, y baja contratación de productos financieros.
  - **Grupo 1 y Grupo 2:** Clientes con límites de crédito más altos, mayor antigüedad y contratación de productos financieros.
- **Validación del Modelo:** Los nuevos clientes fueron asignados exitosamente a los clusters, validando la robustez del modelo.
- **Visualización:** Diagramas de dispersión mostraron la separación clara entre los clusters tras aplicar PCA.
- **Métricas:** Los índices de silueta, Calinski-Harabasz y Davies-Bouldin confirmaron la calidad de la segmentación.

---

## Conclusiones

- La segmentación en 4 grupos permitirá personalizar las ofertas de productos financieros.
- El modelo puede ser utilizado para asignar nuevos clientes a segmentos adecuados de forma precisa.
- Grupos 0 y 3 requieren campañas de marketing específicas para aumentar la contratación de productos.
- La reducción de dimensionalidad con PCA mejoró la interpretabilidad y visualización de los datos.
- Se recomienda integrar este modelo en las estrategias de marketing y ventas para optimizar resultados.

---

## Herramientas

- **Python:** Lenguaje principal.
- **Pandas:** Manipulación y análisis de datos.
- **NumPy:** Operaciones numéricas.
- **Matplotlib y Seaborn:** Visualización de datos.
- **Scikit-learn:** Modelado de clustering (K-means, PCA) y métricas de evaluación.
- **Plotly:** Gráficos interactivos.
- **Yellowbrick:** Visualización de selección de clusters óptimos.
- **SciPy:** Análisis jerárquico de clústeres (dendrogramas).

---
