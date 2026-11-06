# FORM-FB-01 - Fichas bibliográficas (carpeta `reinoso`)

Aplicaciones Distribuidas (ISR-701), UTEQ, séptimo nivel, paralelo A.
Autor de esta carpeta: Reinoso Vélez Eduardo David.

## Compilación

- Compilador: `pdflatex` (probado con MiKTeX 25.12 en Windows; también compila con TeX Live en Linux)
- Archivo principal: `main.tex`
- Procesador de bibliografía: `biber` (el documento usa `biblatex` con `backend=biber`)
- Dependencias (paquetes LaTeX): `babel` (spanish), `biblatex` (estilo `ieee`), `csquotes`, `hyperref`, `geometry`, `enumitem`. MiKTeX instala los que falten al compilar por primera vez.

Desde esta carpeta (`reinoso/`), en la terminal:

```
pdflatex main
biber main
pdflatex main
pdflatex main
```

Resultado: `main.pdf`. El PDF compilado entregado está en `FORM-FB-01_reinoso.pdf`.

Si se compila con TeXstudio: en Opciones > Configurar TeXstudio > Compilar, la herramienta de bibliografía por defecto debe ser Biber.

## Contenido

- `main.tex`: carátula, declaración de uso de IA y 5 fichas bibliográficas
- `refs.bib`: referencias verificadas una a una contra su DOI o ISBN
- `FORM-FB-01_reinoso.pdf`: PDF compilado