## Why

El manifiesto existe actualmente solo como markdown interno. Para compartirlo con colaboradores, revisores y en contextos académicos necesito una versión profesional en PDF. LaTeX es el formato natural para esto: reproducible, profesional, y alineado con los propios pilares del manifiesto (estándares altos, simplicidad).

## What Changes

- Creación de `assets/docs/manifesto.tex` con el contenido completo del manifiesto en LaTeX
- Compilación a `assets/docs/manifesto.pdf` mediante `pdflatex`
- Sin portada independiente, con cabecera en primera página
- Un solo archivo `.tex` (sin división en includes)
- Enlace de descarga del PDF desde la raíz del proyecto (referenciable desde `manifesto.md`)

## Capabilities

### New Capabilities
- `manifesto-pdf`: documento PDF profesional del manifiesto, generado desde LaTeX

### Modified Capabilities
<!-- None -->

## Impact

- Se añade `assets/docs/manifesto.tex` y `assets/docs/manifesto.pdf`
- Sin impacto en código existente, dependencias o sistemas
