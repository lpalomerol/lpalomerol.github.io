## Context

El manifiesto (`manifesto.md`) y su versión PDF (`manifesto.tex` → `manifesto.pdf`) han sido revisados por dos expertos externos. Ambos coinciden en que falta perspectiva del colaborador/cliente. Se necesita una revisión de contenido y correcciones técnicas menores.

## Goals / Non-Goals

**Goals:**
- Revisar `manifesto.md` con los cambios de contenido acordados
- Sincronizar `manifesto.tex` con los mismos cambios
- Aplicar correcciones técnicas al .tex (compatibilidad B/N, overfull hbox, portabilidad)
- Mover anti-pilares al principio del documento
- Añadir sección de entregables ("lo que recibirás")
- Añadir sección de validación experimental
- Añadir límite de competencia explícito
- Traducir testing a lenguaje de cliente/biólogo
- Recompilar PDF

**Non-Goals:**
- No se modifica la web pública
- No se crean versiones separadas para cada audiencia

## Decisions

- **Estructura del manifiesto (nuevo orden)**:
  1. Anti-pilares (filtro rápido)
  2. Declaración de intenciones
  3. Principio rector: simplicidad radical
  4. Pilares (1-5)
  5. Filosofía de testing (versión traducida)
  6. Validación experimental (nuevo)
  7. Contrato colaborativo (nuevo: qué recibes y qué espero)
  8. IA como herramienta (se mantiene pero con nota de transparencia)

- **Correcciones técnicas .tex**:
  - `\colorbox{blue!10}` → regla vertical (`\mdframed` o similar) para compatibilidad B/N
  - Overfull hbox: añadir `\hyphenation` manual o `\sloppy` local
  - `\enquote` → mantener csquotes pero añadir nota de dependencia

## Risks / Trade-offs

- **Regla vertical vs colorbox**: la regla funciona en B/N y color, pero ocupa más espacio horizontal. Se reduce el ancho de texto en ~0.5cm.
- **Anti-pilares al principio**: puede ahuyentar a algún cliente que justo necesita un transformer. Es el objetivo — es filtro, no pérdida.
