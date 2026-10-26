# Compilación

## Documentos de la colección

Los nueve apuntes de `notas/` son documentos autónomos y utilizan **pdfLaTeX**. Las figuras TikZ/PGFPlots, tablas, referencias y listados de código están incluidos en cada archivo. No requieren imágenes, capítulos ni bibliografías externas.

## VS Code + MiKTeX

Requisitos: VS Code, MiKTeX y la extensión LaTeX Workshop (`James-Yu.latex-workshop`). El comando `latexmk` debe estar disponible; en MiKTeX puede requerir una instalación de Perl.

1. Abrir la carpeta completa `matematicas-aplicadas` en VS Code.
2. Abrir cualquiera de los apuntes de `notas/`, o `plantillas/nota.tex` para una comprobación breve del entorno.
3. Ejecutar **LaTeX Workshop: Build with recipe** y elegir **latexmk (pdfLaTeX)**.
4. Abrir la vista previa con **LaTeX Workshop: View LaTeX PDF file**.

La salida se guarda en la carpeta `build/` situada junto al archivo principal. La configuración también ofrece XeLaTeX y LuaLaTeX para futuros materiales; los nueve apuntes actuales se compilan con pdfLaTeX.

## Terminal

Desde la raíz del repositorio:

```bash
latexmk -cd -pdf -interaction=nonstopmode -halt-on-error -file-line-error -outdir=build notas/econometria/Logit_Desarrollo_Completo.tex
```

Para otro apunte, sustituir la ruta por la de su archivo `.tex`. El argumento `-cd` hace que las rutas relativas se resuelvan desde la carpeta del documento. `latexmk` repite las pasadas necesarias para actualizar índices, citas y referencias.

## Paquetes

Los preámbulos declaran los paquetes necesarios. Incluyen Latin Modern, AMS, `mathtools`, `bm`, `geometry`, `microtype`, `booktabs`, `enumitem`, `xcolor`, TikZ, PGFPlots, `tikz-3dplot`, `tcolorbox`, `caption`, `fancyhdr`, `hyperref`, `listings` y `needspace`. Algunos apuntes también utilizan `etoolbox`.

En MiKTeX, permitir la instalación de paquetes que falten. Para activar todas las convenciones en español, instalar también `babel-spanish`. Los nueve apuntes comprueban si `spanish.ldf` está disponible antes de cargar ese idioma.

## Figuras

Los gráficos TikZ y PGFPlots se compilan con el documento. Los listados de Python y MATLAB se muestran como texto y no se ejecutan durante la compilación. No se necesita activar `shell-escape`.

Las indicaciones de rutas personales que aparecen en algunos apuntes corresponden a su preparación original. Para esta organización se utiliza la carpeta del repositorio y la salida `build/` de cada tema.

## Comprobación técnica

La comprobación de compilación revisa que LaTeX procese el documento y genere un PDF legible por las herramientas de lectura. La ejecución de los listados de programación y la revisión de todas las demostraciones son comprobaciones distintas.
