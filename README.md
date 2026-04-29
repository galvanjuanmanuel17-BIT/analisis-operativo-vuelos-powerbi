# Análisis Operativo de Vuelos con Power BI

Proyecto académico de Data Warehouse y Power BI orientado al análisis operativo de vuelos.

## Objetivo del proyecto
El objetivo de este proyecto fue diseñar una solución de análisis basada en un enfoque de Data Warehouse para estudiar información operativa de vuelos y facilitar la obtención de insights a partir de un modelo estrella explotado en Power BI.

## Problema de negocio
A partir de un conjunto de datos de operaciones de vuelos, se buscó estructurar la información de manera analítica para poder responder preguntas vinculadas a:
- volumen de vuelos
- arribos y partidas
- demoras operativas
- rutas más frecuentes
- comportamiento por día y horario
- desempeño según distintas dimensiones de análisis

## Dataset
El proyecto trabaja con un dataset de vuelos correspondiente a operaciones de julio de 2024.

En el repositorio se incluyen:
- una versión **cruda** del dataset original
- una versión **procesada**, adaptada para facilitar el armado del modelo estrella y el análisis en Power BI

## Modelado de datos
Se trabajó con un enfoque dimensional, organizando la información en un **modelo estrella**.

### Componentes principales del modelo
- **Tabla de hechos**: operaciones de vuelos
- **Dimensiones**: tiempo, ruta, aeropuerto, código de vuelo y otros atributos relevantes para el análisis operativo

Este enfoque permitió estructurar los datos de una manera más adecuada para el análisis OLAP y la construcción del dashboard.

## Transformaciones realizadas
Sobre el dataset original se realizaron adecuaciones y agregados para facilitar el modelado analítico, entre ellas:
- revisión y preparación general de los datos
- incorporación de columnas auxiliares
- organización de atributos útiles para el análisis dimensional
- preparación de la información para su explotación en Power BI

> Nota: no se desarrolló un proceso ETL formal con scripts SQL, sino una preparación de datos orientada al modelado y análisis dentro del entorno de trabajo utilizado.

## Dashboard en Power BI
El dashboard fue desarrollado en Power BI con foco en el análisis operativo de vuelos.

Entre los principales elementos analizados se encuentran:
- cantidad total de vuelos
- cantidad de arribos y partidas
- demora promedio
- análisis por ruta
- análisis temporal
- visualización por diferentes filtros de negocio

## Archivos del repositorio
```text
analisis-operativo-vuelos-powerbi/
├── README.md
├── powerbi/
│   └── Data_Warehouse_Graficos.pbix
├── data/
│   ├── raw/
│   │   └── dataset_raw.xlsx
│   └── processed/
│       ├── dataset_processed.xlsx
│       └── README.md
└── images/
    ├── dashboard_principal.png
    ├── dashboard_kpis.png
    └── modelo_estrella.png
