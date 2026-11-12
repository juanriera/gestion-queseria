# La gestión industrial de la quesería

**Autor:** Juan Riera  
**Año:** 2026  
**Licencia:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es)

---

## Sobre el libro

*La gestión industrial de la quesería* es un libro de texto para el módulo profesional **MP 5148 "Gestión Industrial de la Quesería"**, del Curso de Especialización FP Superior en Tecnología y Gestión Quesera (RD 1092/2024).

El libro aborda la gestión industrial de la producción quesera desde tres ángulos complementarios (gestión técnica, gestión económica y mejora continua), e incluye algunas ideas sobre la calidad, seguridad alimentaria y gestión medioambiental. 

Se estructura en 20 capítulos, organizados en cuatro partes:

- **Parte I — Gestión técnica:** el precio de la leche, el balance de materia, el rendimiento quesero, las pérdidas y los indicadores de productividad y eficiencia de los equipos.
- **Parte II — Gestión económica:** los costes de producción, el escandallo y el presupuesto anual.
- **Parte III — Mejora continua:** organización y análisis estadístico de datos de producción, visualización, gráficos de control, capacidad del proceso y grupos de mejora.
- **Parte IV — Calidad, seguridad alimentaria y medio ambiente:** APPCC, certificaciones y gestión medioambiental.

El hilo conductor puede resumirse en tres verbos: **medir** (parte I), **valorizar** (parte II) y **mejorar** (parte III).

---

## Contenido adicional

- **Fichas de diagnóstico en tecnología quesera** es una relación de fichas con  algunos de los principales problemas en la tecnología quesera que dan lugar a defectos en el queso. Se indican posibles causas y acciones para su corrección. El libro está basado en McSweeney(2007): *Cheese Problems Solved*, CRC Press LLC.
- **Introducción a la tecnologia quesera.pdf** es un pequeño documento que trata de manera muy resumida los principales conceptos que deben formar parte de la enseñanza y aprendizaje de la tecnología quesera.
- **La mejora continua en la producción quesera** es una compilación de contenidos que se propone como referencia para la parte III del módulo de Gestión Industrial de la Quesería, cuyo contenido oficial puede verificarse en el RD citado más arriba. Existe una versión web de este documento que incluye detalle del código R y Python utilizado en los ejemplos (https://juanriera.github.io/master-queseria/)
- **Manual de costes y rendimiento quesero** es un resumen del capítulo de costes y rendimiento del libro, estructurado para facilitar su utilización en el aula. Utiliza varios de los ejemplos que se incluyen en las hojas de cálculo adjuntas.
- La carpeta **`recursos`** contiene varias hojas de cálculo utilizadas en estos documentos como ejemplos y modelos de cálculo:
  - `01-pecio-leche.xlsx`: Hoja Excel con un ejemplo de cálculo del precio de la leche según lo explicado en el capítulo 3 del libro.
  - `02-fab_queso_sim.csv`: Registros diarios simulados de recepción de leche y fabricación de queso durante un año completo. Incluye fecha, kilos y litros de leche recibida, composición analítica (MG y proteína), datos  de cuba y kilogramos y composición del queso producido.
  - `03-fab_queso.xlsx`: Hoja Excel con el cálculo de un balance de materia utilizando tablas dinámicas. Se corresponde con el ejemplo del capítulo 4 del libro.
  - `04-balance_materia_semanal.csv`: Un balance de materia semanal a partir de las entradas de leche y datos de fabricación, para su exploracion con la hoja de cálculo.
  - `05-ejemplo-std-tecnico.xlsx`: Hoja de cálculo con un modelo de estándar técnico para comprender el ejemplo del capítulo 5 del libro .
  - `06-analisis-desviaciones-rendimientos_2x2.xlsx`: Un ejemplo en hoja de cálculo para analizar las desviaciones de rendimiento y consumo de materia respecto a un estándar. Se corresponde con el ejemplo del capítulo 5 (apdo 5.7).

Los archivos CSV usan separador `;` y decimal `,` (formato europeo), codificación ISO-8859-1, compatibles con Excel en español y con `read_csv2()` de R.

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
