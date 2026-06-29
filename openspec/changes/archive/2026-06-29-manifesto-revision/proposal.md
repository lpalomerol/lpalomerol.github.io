## Why

El manifiesto fue revisado por dos perfiles: un biólogo oncólogo senior y un bioinformático freelance senior. Ambos coinciden en que el documento es sólido pero carece de perspectiva del colaborador/cliente. Es necesario incorporar su feedback para que el manifiesto sea bidireccional, no solo una declaración interna.

## What Changes

- **manifesto.md**: incorporar secciones de validación experimental, contrato colaborativo, límite de competencia, entregables. Mover anti-pilares al principio. Traducir testing a lenguaje de cliente.
- **manifesto.tex**: aplicar los mismos cambios de contenido. Además, correcciones técnicas: reemplazar colorbox por regla vertical para compatibilidad B/N, arreglar overfull hbox, hacer \enquote más portátil.

## Capabilities

### Modified Capabilities
- `personal-manifesto`: El manifiesto existente se revisa para incorporar feedback de dos revisiones externas
- `manifesto-pdf`: El PDF LaTeX se actualiza con los mismos cambios de contenido y correcciones técnicas

### New Capabilities
- `collaboration-contract`: Nueva sección con el contrato bidireccional (qué recibe el colaborador y qué espera el autor)

## Impact

- Modificación de `manifesto.md` (reestructuración y nuevo contenido)
- Modificación de `assets/docs/manifesto.tex` (mismos cambios de contenido + correcciones LaTeX)
- Recompilación a `assets/docs/manifesto.pdf`
