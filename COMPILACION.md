# Compilación

## VS Code + MiKTeX

Requisitos: VS Code, MiKTeX y la extensión LaTeX Workshop (`James-Yu.latex-workshop`). El comando `latexmk` debe estar disponible; en MiKTeX puede requerir una instalación de Perl.

1. Abrir la carpeta completa `matematicas-aplicadas` en VS Code.
2. Abrir `plantillas/nota.tex` para comprobar el entorno.
3. Ejecutar **LaTeX Workshop: Build with recipe** y elegir **latexmk (pdfLaTeX)**.
4. Abrir la vista previa con **LaTeX Workshop: View LaTeX PDF file**.

La salida se guarda en la carpeta `build/` situada junto al archivo principal. Para documentos que usen `fontspec` u otras dependencias específicas, están disponibles también las recetas XeLaTeX y LuaLaTeX. El motor correcto de cada apunte se indicará tras revisar su preámbulo.

## Terminal

Desde la raíz del repositorio:

```bash
latexmk -cd -pdf -interaction=nonstopmode -halt-on-error -file-line-error -outdir=build plantillas/nota.tex
```

Para compilar un documento recibido, sustituir `plantillas/nota.tex` por la ruta de su archivo principal. El argumento `-cd` hace que las rutas relativas se resuelvan desde la carpeta del documento.

## Figuras

Los gráficos TikZ y PGFPlots se compilan con el documento. Cuando una figura dependa de Python o MATLAB, se conservará su programa y se documentará cómo ejecutarlo antes de compilar. Las dependencias concretas se añadirán al recibir esos programas.

## Comprobación inicial

La plantilla permite verificar el motor y los paquetes básicos. Esta comprobación no valida todavía los apuntes que se incorporen después.
