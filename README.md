# Segmentación de Clientes para Productos Financieros Personalizados 

## Introducción

Este proyecto se enfoca en segmentar clientes de una empresa financiera para ofrecer un nuevo producto con límites de crédito diferenciados. Los directivos necesitan ayuda para determinar la cantidad óptima de grupos de clientes y cómo asignar nuevos clientes a estos grupos. Este análisis utiliza datos históricos de clientes para crear una segmentación útil y práctica.

## Contexto

La empresa financiera busca mejorar la forma en que ofrece sus productos a los clientes. En lugar de un enfoque general, desean dividir a sus clientes en grupos más pequeños y homogéneos para ofrecer límites de crédito personalizados. Esto requiere un análisis de datos que determine la mejor manera de segmentar a los clientes. La segmentación se basa en características clave de los clientes que la institución financiera ya rastrea.

## Objetivo

El objetivo principal de este proyecto es segmentar a los clientes en grupos usando técnicas de análisis de datos. Específicamente, se busca:
•	Determinar el número óptimo de segmentos de clientes.
•	Identificar las características clave que diferencian a cada grupo de clientes.
•	Desarrollar un modelo que pueda asignar nuevos clientes a los segmentos adecuados.
•	Ofrecer una mejor comprensión de los datos de los clientes para campañas de marketing dirigidas.

## Conjunto de datos

El análisis se basa en una base de datos que contiene información sobre clientes existentes. Los datos incluyen las siguientes variables:
•	Salario mensual: Ingreso mensual del cliente en pesos mexicanos.
•	Crédito tipo 1: Indica si el cliente tiene un producto financiero específico (1 = sí, 0 = no).
•	Crédito tipo 2: Similar al crédito tipo 1 (1 = sí, 0 = no).
•	Límite de TC: Límite de crédito de la tarjeta del cliente.
•	Años siendo cliente: Tiempo que el cliente ha tenido relación comercial con la institución financiera.
•	Previamente se ofreció el producto: Indica si el cliente mostró interés en una versión anterior del producto (1 = sí, 0 = no).
•	El conjunto de datos inicial consta de 500 registros, después de limpiar los datos atípicos quedan 486 registros.
•	Se utilizó un conjunto de datos adicional de 50 nuevos clientes para validar el modelo.

## Metodología

Se utilizó una combinación de técnicas de análisis exploratorio de datos, preprocesamiento, modelado y evaluación para la segmentación de clientes.
•	Exploración de Datos: Se realizó un análisis descriptivo para entender la distribución y correlación de las variables. Se identificaron valores atípicos y se visualizaron las distribuciones de los datos. Se encontraron correlaciones entre el límite de crédito y el tiempo como cliente.
•	Preprocesamiento de datos: Los datos fueron limpiados, se eliminaron valores atípicos y se escalaron las variables numéricas.
•	Modelado: Se aplicó el algoritmo de K-means para agrupar a los clientes en segmentos. Se utilizó el método del codo para determinar el número óptimo de clusters. Adicionalmente se aplicó el Análisis de Componentes Principales (PCA) para reducir la dimensionalidad y visualizar los datos en dos componentes principales. Se repitió el proceso de K-means sobre los componentes principales.
•	Evaluación: Se utilizaron métricas como el análisis de silueta, el índice Calinski-Harabasz y el índice Davies-Bouldin para evaluar la calidad de la segmentación.
•	Aplicación a nuevos datos: El modelo entrenado se aplicó a un conjunto de datos de 50 nuevos clientes para predecir su pertenencia a los segmentos identificados.

## Resultados

•	Se identificaron 4 grupos de clientes basados en sus características.
•	La segmentación basada en K-means y PCA muestra que los datos se agrupan en 4 clusters bien diferenciados, lo que se visualizó mediante diagramas de dispersión.
•	Se observó una correlación positiva entre el límite de crédito y el tiempo como cliente, lo que sugiere que los clientes con más tiempo tienden a tener límites de crédito más altos.
•	Los grupos de clientes varían en sus salarios, límites de crédito, y el uso de productos financieros ofrecidos.
•	Los grupos 0 y 3 se caracterizan por tener clientes con salarios y limites de tarjeta bajos, así como poca contratación de los productos financieros ofrecidos.
•	Los grupos 1 y 2 se caracterizan por tener límites de crédito más altos, mayor tiempo como clientes y mayor contratación de productos financieros ofrecidos.
•	El modelo se validó con 50 nuevos clientes, los cuales fueron asignados a los 4 clusters con base en sus características.
•	El análisis de silueta, Calinski-Harabasz y Davies-Bouldin indicaron una buena agrupación y separación de los clusters.

## Conclusiones

•	La segmentación de clientes en 4 grupos permite a la empresa personalizar sus ofertas de productos financieros.
•	El modelo puede ser utilizado para asignar nuevos clientes a los segmentos adecuados y ofrecer productos de forma mas personalizada.
•	Los grupos 0 y 3 requieren campañas de marketing mejor orientadas para promover la contratación de los distintos productos financieros ofrecidos por la empresa.
•	Los hallazgos sugieren que la empresa puede optimizar sus estrategias de marketing y ventas enfocándose en las características de cada segmento de clientes.
•	El uso de PCA permitió reducir la complejidad de los datos y facilitar la visualización de los grupos.

## Herramientas

Las principales herramientas utilizadas en este proyecto son:
•	Python: Lenguaje de programación principal.
•	Pandas: Para manipulación y análisis de datos.
•	NumPy: Para operaciones numéricas.
•	Matplotlib y Seaborn: Para visualización de datos.
•	Scikit-learn: Para modelado de clustering (K-means, PCA), escalado de datos y métricas de evaluación.
•	Plotly: Para la creación de gráficos interactivos.
•	Yellowbrick: Para visualización de la selección del numero optimo de clusters.
•	SciPy: Para el análisis jerárquico de clústeres (dendrogramas).



