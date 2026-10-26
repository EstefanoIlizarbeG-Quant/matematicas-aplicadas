# Matemáticas aplicadas

Colección de apuntes en LaTeX con desarrollos matemáticos, demostraciones, ejemplos numéricos y figuras vectoriales. Reúne avances en álgebra lineal, probabilidad, optimización, econometría y métodos numéricos, con aplicaciones en aprendizaje automático y portafolios.

## Apuntes disponibles

Los nueve documentos son archivos autónomos: cada `.tex` contiene su preámbulo, desarrollo, figuras y referencias.

| Área | Apunte | Contenido principal |
| --- | --- | --- |
| Álgebra lineal | [Álgebra lineal, probabilidad y optimización](notas/algebra_lineal/Algebra_Lineal_Probabilidad_Optimizacion.tex) | Espacios vectoriales, momentos, normal multivariada, cálculo matricial y optimización. |
| Álgebra lineal | [PCA, teorema espectral, SVD y portafolios](notas/algebra_lineal/PCA_Teorema_Espectral_SVD_ML_Portafolios.tex) | Descomposiciones matriciales, reducción de dimensión, regresión y riesgo de portafolios. |
| Probabilidad | [Varianza y covarianza matricial: MCO, IV y SVR](notas/probabilidad/Varianza_Covarianza_Matricial_MCO_IV_SVR.tex) | Momentos escalares y vectoriales, propagación de covarianzas y estimadores. |
| Econometría | [Desarrollo del modelo logit](notas/econometria/Logit_Desarrollo_Completo.tex) | Probabilidad logística, verosimilitud, gradiente, Hessiana, estimación e inferencia. |
| Econometría | [Datos de panel: pooled, FE y RE](notas/econometria/Datos_de_Panel_Pooled_FE_RE.tex) | Transformaciones de panel, efectos fijos y aleatorios, inferencia y extensiones. |
| Econometría | [Discontinuidad, Tobit y Heckman](notas/econometria/RD_Tobit_Heckman_Completo.tex) | Identificación en un umbral, censura, truncamiento y selección muestral. |
| Econometría | [Mincer, modelo principal y Heckman: desarrollo matemático](notas/econometria/Tesis_Mincer_Principal_Heckman_Matematica.tex) | Especificaciones salariales, interacciones, controles temporales y corrección por selección. |
| Métodos numéricos | [Integrales, CDF, Gauss, Padé y minimax](notas/metodos_numericos/Integrales_CDF_Gauss_Pade_Minimax.tex) | Cuadratura, aproximaciones polinómicas y racionales, estabilidad y error. |
| Métodos numéricos | [Normal estándar y algoritmos de cálculo](notas/metodos_numericos/Phi_Normal_Gauss_Algoritmos_200.tex) | Evaluación de la distribución normal, aproximaciones y laboratorios numéricos. |

Los apuntes conservan desarrollos relacionados y algunas secciones compartidas: por ejemplo, el documento de álgebra amplía contenidos del apunte de PCA. Se mantienen como materiales independientes para facilitar su consulta.

## Compilación

Abrir el repositorio completo en VS Code y utilizar la receta **latexmk (pdfLaTeX)** de LaTeX Workshop. Los requisitos y las instrucciones están en [COMPILACION.md](COMPILACION.md).

Ejemplo desde la raíz del repositorio:

```bash
latexmk -cd -pdf -interaction=nonstopmode -halt-on-error -file-line-error -outdir=build notas/econometria/Logit_Desarrollo_Completo.tex
```

Los resultados se generan en una carpeta `build/` junto al documento correspondiente.

## Figuras y código

Las figuras están definidas dentro de los `.tex` mediante TikZ y PGFPlots, incluidos gráficos en dos y tres dimensiones. Los ejemplos de Python y MATLAB que aparecen en los apuntes permanecen en sus respectivos listados de código.

Este repositorio conserva el código fuente. Los PDF compilados, las imágenes generadas y los archivos auxiliares se excluyen mediante `.gitignore`.

## Organización

| Carpeta | Uso |
| --- | --- |
| `notas/algebra_lineal/` | Álgebra, optimización, PCA y SVD. |
| `notas/probabilidad/` | Momentos y covarianzas de escalares, vectores y matrices. |
| `notas/econometria/` | Logit, panel, discontinuidad, Tobit, Mincer y Heckman. |
| `notas/metodos_numericos/` | Integración y aproximación de funciones de distribución. |
| `codigo/` | Espacio disponible para futuros programas independientes. |
| `bibliografia/` | Espacio disponible para futuras bibliografías compartidas. |
| `plantillas/` | Plantilla mínima para comprobar el entorno. |

## Estado del material

Apuntes de estudio en desarrollo. La organización y la comprobación técnica de compilación facilitan su reproducción; las demostraciones y los ejemplos pueden seguir ampliándose y revisándose.
