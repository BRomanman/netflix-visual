# StreamView Analytics — EP1 (Data_Movies)

Proyecto ADY1104 – Visualización de Datos. Evaluación Parcial I (semana 5).
Consultora de Visual Analytics para StreamView Analytics — análisis del catálogo de películas.

## Estructura

```
project/
├── data/
│   ├── netflix_movies_detailed_up_to_2025.csv   # dataset original (sin modificar)
│   └── movies_clean.csv                         # dataset tras limpieza documentada
├── notebooks/
│   └── 01_EDA_Data_Movies.ipynb                 # limpieza + EDA completo, con gráficos
├── images/                                      # gráficos exportados en PNG (para informe/PPT/dashboard)
├── dashboard/                                   # (siguiente etapa: EP2)
├── src/                                         # (scripts reutilizables, si se agregan)
└── README.md
```

## Hallazgos de calidad de datos más relevantes

1. **`duration` está 100% vacía** en el extracto de `Data_Movies` (16.000/16.000 filas). El diccionario
   de datos del caso la describe como texto tipo "120 min", pero no contiene ningún valor utilizable.
   Se excluye del análisis y se declara como limitación.
2. **`rating` no es una clasificación por edad.** Coincide exactamente con `vote_average` en el 100% de
   las filas. No corresponde a los valores esperados (TV-MA, PG-13, R...) del diccionario del caso.
   Se excluye de cualquier segmentación por clasificación etaria.
3. **`budget`/`revenue` en 0 en 69.7% / 64.7% de las filas** — se recodifican a NaN (dato no informado,
   no presupuesto real de $0). Solo el **22.1%** del catálogo tiene ambos datos disponibles; los KPIs
   financieros y el ROI se calculan únicamente sobre ese subconjunto, declarando el alcance parcial
   (Regla de Negocio #9 del caso).
4. Sin duplicados por `show_id`. Nulos moderados en `director` (0.8%), `cast` (1.3%), `country` (2.9%)
   y `genres` (0.7%), excluidos fila a fila solo del análisis puntual que los usa.

Ver el notebook `01_EDA_Data_Movies.ipynb` para el detalle completo, código y gráficos.
