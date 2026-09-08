# StreamView Analytics

## Descripción

StreamView Analytics es una solución de visualización de datos orientada al análisis de un catálogo cinematográfico. El proyecto busca transformar información de películas en indicadores y visualizaciones que permitan identificar patrones de presencia, popularidad y oportunidades financieras para apoyar la priorización de contenidos.

## Objetivo

Desarrollar una solución visual que permita analizar el catálogo cinematográfico e identificar contenidos y características relevantes para la toma de decisiones.

## Fuente de datos

El proyecto utiliza el dataset:

Netflix Movies Detailed up to 2025

Entre las principales variables utilizadas se encuentran:

- show_id
- title
- genres
- country
- language
- release_year
- popularity
- rating
- budget
- revenue

## Análisis exploratorio

El análisis exploratorio permitió revisar la calidad de los datos, identificar valores faltantes y detectar patrones relacionados con género, país, popularidad, valoración y variables financieras.

Entre los principales hallazgos se encuentran:

- El catálogo contiene 16.000 películas.
- Drama presenta la mayor presencia dentro del catálogo.
- La mayor cantidad de títulos de un género no implica necesariamente mayor popularidad.
- Algunos títulos concentran niveles de popularidad considerablemente superiores al promedio.
- La información financiera presenta una cobertura limitada.

## Dashboard

El dashboard fue desarrollado en Looker Studio.

Incluye:

- Indicadores KPI.
- Filtros por género, país, idioma y año.
- Comparaciones por género.
- Comparación por país.
- Análisis de popularidad y valoración.
- Ranking de películas.
- Análisis exploratorio de presupuesto, ingresos y ROI.

## Estructura del proyecto

```text
data/
notebooks/
dashboard/
images/
docs/
src/
README.md

StreamView_Analytics/
│
├── data/
│   └── netflix_movies_detailed_up_to_2025.csv
│
├── notebooks/
│   └── 01_EDA_Data_Movies_CORREGIDO.ipynb
│
├── dashboard/
│   ├── Looker_Studio_Link.txt
│   └── dashboard_streamview.pdf
│
├── images/
│   ├── dashboard_completo.png
│   ├── catalogo_popularidad.png
│   └── oportunidades_financieras.png
│
├── docs/
│   ├── Informe_Ejecutivo.pdf
│   └── Presentacion.pptx
│
├── src/
│
└── README.md