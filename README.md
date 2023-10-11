# DATA SCIENCE - PROYECTO INDIVIDUAL Nº2

En este proyecto, abarcaremos una serie de pasos para desarrollar un proceso de **`Data Analytics`** sobre un dataset de accidentes aéreos, para posteriormente disponibilizar un **`Dashboard Interactivo`** utilizando **`Power BI`**.

## Contexto

Planteamos la necesidad de analizar datos históricos de **`accidentes aéreos`** a los efectos de identificar patrones, tendencias y factores que ayuden a mejorar la seguridad en la aviación civil. 

## Dataset

El [dataset] en cuestión posee información acerca de vuelos que han sufrido un siniestro a lo largo de todo el mundo desde 1908 hasta 2021. El mismo cuenta con 5008 filas (representando cada fila un accidente aéreo) y 18 columnas (atributos de cada vuelo).

## Objetivo

El propósito del trabajo fue describir las características de vuelos siniestrados a los efectos de analizar los siguientes **`KPI's`** propuestos:

- Disminución en un 10% de la **`tasa anual de mortalidad de la tripulación`** (Tripulación fallecida/Número de accidentes en una década);
- Reducción en un 5% de la **`tasa anual de mortalidad`** (Personas fallecidas/Personas a bordo);
- Disminución de la **`cantidad de accidentes`** para el país con mayor cantidad de siniestros: Estados Unidos.

## ETL  

Para realizar los procesos de ETL se utilizó **`Python`** con librerías de Numpy, Pandas, Matplotlib y Seaborn, entre otras.

## Exportación a MySQL

Una vez finalizadas las transformaciones necesarias sobre el archivo csv, se procedió a ingestar el dataframe resultante en MySQL a través de python estableciendo la conexión correspondiente con la librería **`mysql-connector-python`**.
A través del código en cuestión, se creó la base de datos **`air_flights`** y la tabla contenedora del dataframe **`air_accidents`**

## EDA

A los efectos de poder entender los datos presentados, se realizaron una serie de análisis y estudios sobre las variables del dataset a los efectos de poder encontrar relaciones entre los datos y comprender la relevancia de los mismos.
Dentro de los análisis efectuados se encuentran: 
- Distribuciones de frecuencias y estadísticas de las variables numéricas;
- Análisis e identificación de outliers en variables de interés (total_aboard y total_fatalities);
- Identificación de variables categóricas y sus valores; 
- Análisis de accidentes, tasa de mortalidad, tasa de supervivencia y seguridad en vuelos por: país, aerolínea, aeronave, marca de aeronave y categoría de vuelo;
- Análisis temporales por hora, día, mes y año.

## Dashboard e insights

El dashboard consta de 1 portada y 4 páginas navegables a través de botones.

Se destaca que dentro de cada página del mismo, en la esquina superior derecha, se puede encontrar el botón de información que redirecciona a este repositorio de Github.

## Conclusiones

- La tasa de mortalidad de la tripulación, no presenta cambios muy significativos a la baja, al contrario, se puede notar un aumento durante los últimos 10 años, esto debido a que al mismo tiempo que las muertes de la tripulación bajaron, tambien bajaron los accidentes pero en mayor medida porcentual, lo que se cree es que sea debido a que los aviones que sufren los accidentes son cada vez más grandes y llevan consigo a mayor cantidad de tripulación.

- La Tasa anual de mortalidad, oscila entre el 50% y el 100% para la mayoría de los años. La misma si bien presenta tendencia en algunos períodos, no podemos decir que tenga una marcada tendencia a la baja. Es importante en su lugar, estar por debajo del target de tasa conforme al KPI indicado por lo que se sugiere revisarlo año a año.

- Por último es destacable la tendencia anual de accidentes para Estados Unidos y Rusia, el cual pese a tener la mayor cantidad de accidentes históricos, mantiene una marcada tendencia a la baja en los últimos años, en concordancia con la tendencia mundial. 
