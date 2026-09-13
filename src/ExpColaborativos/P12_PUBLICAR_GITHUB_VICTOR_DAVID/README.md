# P12 - Estabilidad del modelo predictivo frente al Undersampling

**Autores:** Victor Malsam y David Torres  
**Problema #12:** Estabilidad del modelo predictivo frente al Undersampling.

## Objetivo

Analizar hasta qué punto puede reducirse la cantidad de registros de entrenamiento mediante undersampling sin deteriorar de manera relevante el comportamiento predictivo y económico del modelo.

Se comparan cinco escenarios:

- B100: 100% (Baseline)
- U040: 40%
- U010: 10%
- U005: 5%
- U001: 1%

El análisis integra 12 semillas (SEM1 a SEM12).

## Contenido del repositorio

- `R/`: versión final del informe R Markdown y su HTML renderizado.
- `90_RESULTADOS/`: resultados consolidados necesarios para reconstruir el análisis.
- `91_ANALISIS/00_GLOBAL/`: tablas, comparaciones, Wilcoxon y gráficos globales generados por el Rmd.
- `PARAMS_CORRIDAS/`: `PARAM.yml` de las 60 corridas formales (12 semillas x 5 escenarios).
- `P12 - Informe de Control y Análisis.pdf`: informe de control y análisis.

## Reproducir el análisis

Abrir:

`R/P12_informe_control_v11_SEM1_SEM12_ANALISIS_COMPLETO.Rmd`

y ejecutar **Knit** desde la carpeta del proyecto o desde la subcarpeta `R`.

El Rmd localiza automáticamente las carpetas `90_RESULTADOS` y `91_ANALISIS` y reconstruye las tablas y gráficos globales.

## Alcance de este paquete

Este repositorio publica los resultados consolidados y el análisis final.  
Se incluye una semilla completa como ejemplo de ejecución. No se publican los notebooks de las restantes semillas ni los scripts auxiliares de automatización y exportación.

## Notebooks de ejecución

Para evitar duplicar notebooks con la misma estructura de ejecución, se incluye como ejemplo completo la **SEM1 (semilla 198427)** en los cinco escenarios del experimento:

- **B100** — Baseline 100%
- **U040** — Undersampling 40%
- **U010** — Undersampling 10%
- **U005** — Undersampling 5%
- **U001** — Undersampling 1%

Estos notebooks permiten observar el procedimiento utilizado para ejecutar cada escenario, entrenar el modelo y generar los resultados.

El experimento completo fue realizado sobre **12 semillas (SEM1–SEM12)**. Los resultados consolidados de todas las semillas se encuentran en `90_RESULTADOS/`, mientras que los parámetros y registros de cada corrida se encuentran en `PARAMS_CORRIDAS/`.

Los notebooks restantes no se incluyen para evitar redundancia, dado que corresponden a la repetición del mismo procedimiento experimental sobre las demás semillas.
