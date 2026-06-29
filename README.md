# La gestión industrial de la quesería

**Autor:** Juan Riera  
**Año:** 2026  
**Licencia:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es)

---

## Sobre el libro

*La gestión industrial de la quesería* es un libro de texto para el módulo profesional **MP 5148 "Gestión Industrial de la Quesería"**, del Curso de Especialización FP Superior en Tecnología y Gestión Quesera (RD 1092/2024).

El libro aborda la gestión industrial de la producción quesera desde tres ángulos complementarios:

- **Parte I — Gestión técnica:** el precio de la leche, el balance de materia, el rendimiento quesero, las pérdidas y los indicadores de productividad y eficiencia de los equipos.
- **Parte II — Gestión económica:** los costes de producción, el escandallo y el presupuesto anual.
- **Parte III — Mejora continua:** organización y análisis estadístico de datos de producción, visualización, gráficos de control, capacidad del proceso y grupos de mejora.
- **Parte IV — Calidad, seguridad alimentaria y medio ambiente:** APPCC, certificaciones y gestión medioambiental.

El hilo conductor puede resumirse en tres verbos: **medir** (parte I), **valorizar** (parte II) y **mejorar** (parte III).

---

## Contenido del repositorio

Además del libro en formato PDF, este repositorio contiene los archivos de datos utilizados en los ejemplos y ejercicios del libro:

- `01-pecio-leche.xlsx`: Hoja Excel con un ejemplo de cálculo delo sprecios dla leche según lo explicado en el capítulo 3 del libro.
- `02-fab_queso_sim.csv`: Registros diarios simulados de recepción de leche y fabricación de queso durante un año completo. Incluye fecha, kilos y litros de leche recibida, composición analítica (MG y proteína), datos de cuba y kilogramos y composición del queso producido.
- `03-fab_queso.xlsx`: Hoja Excel con el cálculo de un balance de materia utilizando tablas dinámicas. Se correspnde con el capítulo 4 del libro.
- `04-balance_materia_semanal.csv`: Un balance de materia semanal a partir de las entradas de leche y datos de fabricación, para su exploracion con la hoja de cálculo.
- `05-ejemplo-std-tecnico.xlsx`: Hoja de cálculo con un modelo de estándar técnico para comprender el ejemplo del libro del capítulo 5.
- `06-analisis-desviaciones-rendimientos.xlsx`: Un ejemplo en hoja de cálculo para analizar las desviaciones respecto al estándar. Se corresponde con el ejemplo del capítulo 5 (apdo 5.7).

Los archivos CSV usan separador `;` y decimal `,` (formato europeo), codificación ISO-8859-1, compatibles con Excel en español y con `read_csv2()` de R.

Tanto los CSV como las hojas de cálculo están en la carpeta `recursos/`

---

## Uso con R

```r
library(tidyverse)

datos <- read_csv2(
  "02-fab_queso_sim.csv",
  locale = locale(decimal_mark = ",", grouping_mark = ".", encoding = "ISO-8859-1")
)
```

---

## Contacto

[talamera.com](https://talamera.com)
