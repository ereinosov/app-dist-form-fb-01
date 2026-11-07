# FORM-FB-01 · Fichas bibliográficas

Fundamentos de sistemas distribuidos. Las fichas preparan el análisis de Apache Cassandra en comparación con MongoDB para TA-IND-01.

## Archivos

| Archivo | Contenido |
|---|---|
| `main.tex` | Documento principal con las cinco fichas y la declaración de uso de IA |
| `referencias.bib` | Cinco registros bibliográficos con sus DOI |
| `main.pdf` | PDF obtenido al compilar `main.tex` |
| `README.md` | Instrucciones de compilación |

## Compilación en Overleaf

1. Crea un proyecto vacío y coloca `main.tex` y `referencias.bib` en la raíz.
2. Selecciona `main.tex` como documento principal y `pdfLaTeX` como compilador en la configuración del proyecto.
3. Pulsa **Recompilar**. Overleaf ejecuta Biber automáticamente a partir de la configuración de `biblatex`.
4. Comprueba que aparecen las cinco referencias completas y descarga el PDF. Si quedan citas sin resolver, recompila desde cero.

## Compilación local

Se requiere una distribución TeX con pdfLaTeX, Biber y los paquetes `babel` con español, `lmodern`, `geometry`, `microtype`, `csquotes`, `biblatex`, `biblatex-ieee` y `hyperref`. Desde la carpeta del proyecto, ejecuta estos comandos en orden.

```sh
pdflatex -halt-on-error main.tex
biber main
pdflatex -halt-on-error main.tex
pdflatex -halt-on-error main.tex
```

Cada referencia de ficha se genera con `\fullcite` y el estilo IEEE a partir de `referencias.bib`. El DOI enlazado debajo de cada referencia permite abrir la publicación.

