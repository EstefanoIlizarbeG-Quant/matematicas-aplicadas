# Matemáticas aplicadas

Repositorio de notas de estudio en LaTeX, demostraciones, ejercicios y código reproducible, con aplicaciones en estadística, econometría y aprendizaje automático.

## Estado

Entorno inicial preparado. Los documentos matemáticos se incorporarán y organizarán por tema a medida que se revisen.

## Organización

| Carpeta | Contenido |
| --- | --- |
| `notas/` | Archivos `.tex` y sus capítulos, organizados por tema y documento. |
| `codigo/` | Programas de Python, MATLAB u otros lenguajes que generan ejemplos y figuras. |
| `bibliografia/` | Bibliografías `.bib` compartidas, cuando sean necesarias. |
| `plantillas/` | Plantilla mínima para comprobar la compilación. |

Consulta [COMPILACION.md](COMPILACION.md) para trabajar con VS Code y MiKTeX.

## Incorporación de material

1. Crear una carpeta por documento dentro del tema correspondiente en `notas/`.
2. Conservar los archivos `.tex`, `.bib`, estilos y código necesarios para reproducirlo.
3. Documentar el archivo principal, el motor de compilación y las dependencias de cada documento.
4. Conservar las fuentes de las figuras: TikZ/PGFPlots dentro de LaTeX o los programas que las generan.

La configuración de Git excluye resultados compilados, imágenes generadas y archivos temporales. El catálogo y las instrucciones particulares se completarán después de revisar los documentos.
