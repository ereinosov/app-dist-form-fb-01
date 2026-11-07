# FORM-FB-01 · Coronel Gómez Khriz Alexander

Aplicaciones Distribuidas (ISR-701), UTEQ, séptimo nivel, paralelo A.

## Tema elegido

**Replicación y tolerancia a fallos en Apache Kafka para la comunicación entre microservicios.**

Pregunta orientadora para TA-IND-01. ¿Cómo influyen la replicación y la configuración de Apache Kafka en la conservación de mensajes, la disponibilidad y la recuperación ante fallos?

La selección también incluye estudios de Kafka Streams para analizar aplicaciones que procesan eventos. Sus resultados deben atribuirse al componente, la versión y las condiciones evaluadas en cada estudio.

## Estado del trabajo

El documento contiene cinco fichas, con tres artículos de revista y dos artículos de congresos ACM, publicados entre 2023 y 2026. Cada resumen propuesto tiene 100 palabras, contadas como unidades separadas por espacios.

Queda pendiente la lectura integral de las dos primeras fuentes. La cobertura bibliográfica disponible se documenta en la sección de verificación.

## Archivos

- `main.tex` contiene la presentación y las cinco fichas.
- `refs.bib` contiene los registros para generar referencias IEEE con `biblatex`.
- `FORM-FB-01_coronel.pdf` es el PDF compilado de las fichas.
- `README.md` recoge las instrucciones de compilación, los enlaces y el estado de verificación.

## Fuentes seleccionadas

| Clave en BibLaTeX | Publicación | Uso propuesto en TA-IND-01 |
|---|---|---|
| `raptis2023survey` | Raptis y Passarella, IEEE Access, vol. 11, pp. 85333–85350, 2023 | Fundamentos de Kafka y organización de la literatura |
| `raptis2024partitioning` | Raptis, Cicconetti y Passarella, Future Generation Computer Systems, vol. 154, pp. 173–188, 2024 | Particionado, configuración de brokers y requisitos de las aplicaciones |
| `henning2024scalability` | Henning y Hasselbring, Journal of Systems and Software, vol. 208, artículo 111879, 2024 | Escalabilidad y recursos de microservicios que procesan eventos |
| `vogel2024recovery` | Vogel et al., DEBS 2024, pp. 171–182 | Recuperación ante fallos y métricas para el análisis crítico |
| `chen2026tuning` | Chen et al., ICPE Companion 2026, pp. 154–159 | Efecto de la configuración en el rendimiento de Kafka Streams |

### 1. Fundamentos de Kafka

A Survey on Networked Data Streaming With Apache Kafka.

- [DOI editorial](https://doi.org/10.1109/ACCESS.2023.3303810)
- [Copia de la publicación en el repositorio del CNR](https://iris.cnr.it/retrieve/e2f4702a-f9a1-4673-b47a-02ff703a2059/prod_490723-doc_204476.pdf)
- Lectura propuesta para identificar los componentes de Kafka y los problemas de investigación relevantes para el informe.

### 2. Particionado y fiabilidad

Efficient topic partitioning of Apache Kafka for high-reliability real-time data streaming applications.

- [DOI editorial](https://doi.org/10.1016/j.future.2023.12.028)
- [Copia de la publicación en el repositorio del CNR](https://iris.cnr.it/retrieve/45b6ccdc-9fec-4de5-9367-9703370a39cc/1-s2.0-S0167739X23004892-main.pdf)
- Lectura propuesta para estudiar cómo se determina el número de particiones y brokers según las necesidades de la aplicación.

### 3. Escalabilidad en microservicios

Benchmarking scalability of stream processing frameworks deployed as microservices in the cloud.

- [DOI editorial](https://doi.org/10.1016/j.jss.2023.111879)
- [Versión de los autores](https://arxiv.org/abs/2303.11088)
- [Copia de la publicación en la Universidad de Southampton](https://eprints.soton.ac.uk/488788/1/1-s2.0-S0164121223002741-main.pdf)
- Lectura propuesta para definir métricas y comparar el consumo de recursos bajo cargas crecientes.

### 4. Recuperación tras fallos

A Comprehensive Benchmarking Analysis of Fault Recovery in Stream Processing Frameworks.

- [DOI editorial](https://doi.org/10.1145/3629104.3666040)
- [Texto completo de la versión de los autores](https://arxiv.org/html/2404.06203v3)
- Dato localizado en la sección 5.2 de esa versión. Los experimentos de eliminación de pods afectan a 1, 2 o 4 trabajadores simultáneamente y repiten los fallos cada cinco minutos.
- Revisar las secciones 4.2 y 6.1 para relacionar el comportamiento observado con Kafka Streams 3.5 y el rebalanceo de las particiones.

### 5. Configuración y rendimiento

Performance Optimization in Stream Processing Systems: Experiment-Driven Configuration Tuning for Kafka Streams.

- [DOI editorial](https://doi.org/10.1145/3777911.3800636)
- [Versión de los autores](https://arxiv.org/abs/2603.04027)
- El abstract editorial informa una mejora de hasta el 23 % en throughput frente a la configuración predeterminada. Revisar las condiciones experimentales antes de emplear la cifra en una ficha.

## Verificación realizada y pendientes

Se consultó el registro de cada DOI mediante la API de Crossref y se cotejaron título, autores, publicación, año, volumen y páginas o identificador de artículo. Los cinco enlaces DOI devolvieron una redirección HTTP 302 hacia IEEE Xplore, Elsevier o ACM, según corresponde.

IEEE Xplore presentó una comprobación de navegador y varias páginas editoriales o repositorios devolvieron HTTP 403 o 401 en la consulta automática. En las dos primeras fuentes se contrastaron los metadatos y el abstract disponible mediante búsqueda académica, con lectura integral pendiente. Se consultaron copias de autores de Henning y Hasselbring, Vogel et al. y Chen et al. disponibles en arXiv. Cada ficha identifica la versión y la localización del dato utilizado.

Los registros consultados de los tres artículos de revista no incluyen número de fascículo. El registro de Journal of Systems and Software utiliza el identificador de artículo 111879, guardado como `eid`. Los artículos de Elsevier corresponden a volúmenes de 2024 aunque sus DOI contienen 2023. Las versiones de autores se enlazan para lectura y el archivo `.bib` cita las publicaciones editoriales.

La cobertura de IEEE Access en Scopus y Web of Science consta en la página de IEEE. El catálogo de la biblioteca de DESY registra esas mismas bases para las dos revistas de Elsevier. [IEEE Access](https://ieeeaccess.ieee.org/about/bibliometrics/), [Future Generation Computer Systems](https://bib-pubdb1.desy.de/record/13085), [Journal of Systems and Software](https://bib-pubdb1.desy.de/record/10142).

DBLP incluye los trabajos publicados en DEBS 2024 e ICPE Companion 2026. Queda pendiente una consulta directa de la cobertura de esas actas en Scopus o Web of Science. [DEBS 2024](https://dblp.org/pid/177/7371.html), [ICPE Companion 2026](https://dblp.org/rec/conf/wosp/ChenHMR26.html).

## Preparación de las fichas

Cada ficha contiene la referencia IEEE generada con `biblatex`, el DOI, un resumen propuesto de 100 palabras, un dato concreto con página o sección y una propuesta de nota personal sobre su uso en TA-IND-01.

## Compilación

Compilador utilizado para este documento, Tectonic 0.17.0, basado en XeTeX. El archivo principal es `main.tex`. La bibliografía usa `biblatex`, estilo `ieee` y `backend=bibtex`. Tectonic ejecuta automáticamente las pasadas y el procesamiento de BibTeX.

Se requiere Tectonic y acceso a Internet para descargar los paquetes en la primera compilación. Los paquetes utilizados son `fontenc`, `inputenc`, `babel` con inglés y español, `lmodern`, `geometry`, `csquotes`, `xcolor`, `biblatex`, `biblatex-ieee`, `hyperref` y `fancyhdr`.

Desde `coronel/`, ejecutar en este orden en PowerShell.

```powershell
tectonic main.tex --bundle https://data1.fullyjustified.net/tlextras-2022.0r0.tar
Copy-Item main.pdf FORM-FB-01_coronel.pdf
```

El servidor de paquetes se indica explícitamente porque el servidor de redirección predeterminado falló en este entorno. Los archivos auxiliares de la compilación usada para esta entrega se mantuvieron en una carpeta temporal.

El PDF se verificó visualmente y contiene seis páginas, con las cinco referencias completas y los cinco resúmenes de 100 palabras. El registro de Tectonic conserva un aviso general de referencias indefinidas y solicitud de repetir BibTeX, incluso tras repetir el procesamiento. Se comprobaron la correspondencia de todas las claves con `refs.bib` y la presencia de los datos bibliográficos en el PDF. También aparece el aviso de `biblatex` sobre el backend alternativo BibTeX.

Con una distribución TeX instalada también puede utilizarse el flujo estándar siguiente. Esta alternativa se documenta para reproducibilidad, aunque la compilación realizada aquí utiliza Tectonic.

```sh
pdflatex -halt-on-error main.tex
bibtex main
pdflatex -halt-on-error main.tex
pdflatex -halt-on-error main.tex
```
