## Context

El manifiesto existe como `manifesto.md` en la raíz del proyecto. Para compartirlo en contextos académicos (colaboradores, revisores, adjunto a papers) necesito una versión PDF profesional generada desde LaTeX.

## Goals / Non-Goals

**Goals:**
- Archivo `manifesto.tex` que compile correctamente con pdflatex
- PDF resultante profesional, con tipografía serif y maquetación limpia
- Sin portada independiente, pero con cabecera en primera página
- Un solo archivo .tex (sin includes)
- PDF colocado en `assets/docs/manifesto.pdf`

**Non-Goals:**
- No se modifica la web pública (se hará en un cambio aparte)
- No se incluye tooling de compilación automática (CI/CD para LaTeX)
- No se versiona el PDF en git (solo el .tex)

## Decisions

- **Clase document**: `article` — la más simple, suficiente para el contenido
- **Papel**: Letter — formato estándar para documentos académicos
- **Alineación**: ragged right (\RaggedRight de ragged2e) — mejora legibilidad en textos cortos
- **Tipografía**: `mathpazo` (Palatino) para cuerpo — serif, buena legibilidad en papel
- **Títulos**: `sectsty` con `\normalfont\bfseries` — negro, sin serif
- **No portada**: cabecera centrada al inicio (\begin{center}), título grande en azul, autor y fecha, luego \hrule y contenido directo. Sin \maketitle ni \titlepage
- **Cita principal**: \colorbox{blue!10} con texto en azul oscuro para la declaración inicial "Construyo pipelines..."
- **Listas**: guión largo (\textendash) como bullet, con enumitem para espaciado compacto
- **Anti-pilares**: misma tipografía que el resto (sin italics), solo cambia el contenido
- **Fecha**: v1.0 · junio 2026
- **Compilación**: `pdflatex manifesto.tex` — sin bibtex, sin makeindex, sin dependencias extra

### Packages (6)
```latex
\usepackage[letterpaper, margin=2.5cm, bottom=3cm]{geometry}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage[spanish]{babel}
\usepackage{mathpazo}
\usepackage{sectsty}
\allsectionsfont{\normalfont\bfseries}
\usepackage{microtype}
\usepackage{ragged2e}
\usepackage{enumitem}
```

## Risks / Trade-offs

- **Caracteres UTF-8**: pdflatex no maneja UTF-8 bien con según qué fuentes → usado inputenc + fontenc T1. Alternativa: xelatex. Decisión: empezar con pdflatex; si da problemas con acentos, migrar.
- **LaTeX no instalado**: quien quiera compilar necesita TeX Live. Mitigación: el PDF compilado se sube al repo.
