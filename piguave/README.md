# FORM-FB-01: Fichas bibliográficas

**Estudiante:** Nixon Piguave  
**Asignatura:** Aplicaciones Distribuidas (ISR-701)  
**Nivel y paralelo:** Séptimo nivel, paralelo A  
**Tema:** Fundamentos de sistemas distribuidos y arquitecturas distribuidas

## Archivos

- `main.tex`: archivo principal del documento.
- `refs.bib`: referencias bibliográficas.
- `FORM-FB-01-Piguave.pdf`: documento compilado.
- `README.md`: instrucciones de compilación.

## Requisitos

- Una distribución de LaTeX, como TeX Live o MiKTeX.
- Biber para procesar las referencias.
- Los paquetes `fontenc`, `inputenc`, `babel` (español), `csquotes`, `biblatex` (estilo IEEE), `hyperref`, `geometry` y `xcolor`.

## Compilación

**Compilador:** pdfLaTeX  
**Procesador de bibliografía:** Biber  
**Archivo principal:** `main.tex`

Desde esta carpeta, ejecuta los comandos en este orden:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
