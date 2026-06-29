## Context

Documento interno de principios profesionales. No requiere cambios arquitectónicos, nuevas dependencias, ni modificaciones a la web pública. Es un archivo markdown estático que vive en el repo como referencia.

## Goals / Non-Goals

**Goals:**
- Un archivo `manifesto.md` legible, bien estructurado, con los 5 pilares
- Ubicado en la raíz del proyecto web (visible para quien tenga acceso al repo, no enlazado desde la web)
- Escrito en español, coherente con el idioma del proyecto

**Non-Goals:**
- No se renderiza ni enlaza en la página web
- No requiere CSS, JS, ni integración con el frontend
- No es un documento público ni de marketing

## Decisions

- **Formato**: Markdown plano. Sin build steps ni tooling.
- **Ubicación**: Raíz del proyecto (`/manifesto.md`). Es el lugar natural para un documento de identidad del proyecto.
- **Idioma**: Español. Es el idioma del proyecto y del autor.
- **Tono**: Declarativo, personal, filosófico. No técnico-operativo.

## Risks / Trade-offs

- **Riesgo de desactualización** → Es un documento de principios, no de procedimientos. Los principios cambian lento. Si cambian, se actualiza el manifesto.
- **Visibilidad en el repo** → Cualquiera con acceso al repo lo ve. Es aceptable — es una declaración de intenciones, no información sensible.
