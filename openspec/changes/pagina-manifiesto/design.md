## Context

Sitio estático HTML (Tailwind via CDN). Sin build step. Una sola página (`index.html`) con secciones ancladas. GA4 Google tag presente. Manifiesto existe como `.tex`, `.pdf` y `.md` pero no enlazado. Tres `<details>` expandibles en la sección `#trayectoria` sin tracking actual.

Restricciones: sin framework, sin bundler, sin JS modules. Tracking inline con `gtag`.

## Goals / Non-Goals

**Goals:**
- Página `/manifiesto` navegable, coherente con diseño existente
- Resumen web de anti-pilares (hook) + 5 pilares (tarjetas/iconos)
- Enlace de descarga a PDF completo
- CTA a contacto
- Navbar y footer con enlace "Manifiesto"
- Eventos GA4: `expand_publication`, `cta_click`, `nav_click`, `download_manifesto`

**Non-Goals:**
- No cambiar el diseño/estilo del sitio existente
- No añadir build step ni framework
- No migrar a múltiples páginas (solo esta)
- No modificar contenido del manifiesto original

## Decisions

**Decisión 1: Página plana (`manifiesto.html`) vs subdirectorio `manifiesto/index.html`**
- Elegido: `manifiesto/index.html` → URL `/manifiesto` más limpia, escalable si hay más contenido
- Alternativa: `manifiesto.html` → más simple pero URL menos limpia

**Decisión 2: Contenido resumido vs transcripción completa**
- Elegido: resumen web con anti-pilares (hook) + 5 pilares como tarjetas. El PDF es la versión completa.
- Razón: una transcripción completa sería demasiado densa. El resumen engancha, el PDF profundiza.

**Decisión 3: Tracking events inline vs data attributes**
- Elegido: data attributes (`data-ga-label`) en elementos trackeables + script que los procesa
- Razón: separa la intención de tracking del HTML, el script es declarativo y reutilizable

**Decisión 4: Toggle event vs click event para expandibles**
- Elegido: evento `toggle` en `<details>` en lugar de click en `<summary>`
- Razón: `toggle` discrimina open/close; click no sabe el estado.

## Risks / Trade-offs

- **[Rendimiento]** Script inline puede bloquear paint → mitigado: script al final del `<body>` con `defer` implícito
- **[Precisión GA4]** Eventos toggle pueden duplicarse si el usuario abre/cierra rápido → usar `setTimeout` para debounce simple
- **[SEO]** Página nueva sin build → no hay problema, es HTML plano indexable
- **[Mantenimiento]** Si se añaden más `<details>` en el futuro, el script los captura automáticamente si siguen el patrón

## Arquitectura

```
index.html (existente)
├── navbar → nuevo enlace "Manifiesto"
├── #trayectoria → <details> con data-ga-label (sin cambio visual)
├── CTAs → data-ga-label añadido
├── footer → nuevo enlace "Manifiesto"
└── script inline GA4 expandido

manifiesto/index.html (nuevo)
├── navbar (copy + enlace "Manifiesto" activo)
├── hero: "Manifiesto · Luis Palomero, PhD"
├── anti-pilares (cards, hook inicial)
├── 5 pilares (tarjetas con ícono/color)
├── CTA: descargar PDF + solicitar evaluación
├── footer
└── script inline GA4

Eventos GA4:
┌──────────────────────────────────────────┐
│ expand_publication  → toggle en <details>│
│   label: nombre del paper                │
│   action: open | close                   │
│                                          │
│ cta_click           → click en CTA       │
│   label: hero_agendar, hero_ver,         │
│          nav_solicitar, contacto_email,  │
│          manifesto_cta, manifesto_pdf    │
│                                          │
│ nav_click           → click en nav link  │
│   label: soluciones, enfoque,            │
│          trayectoria, contacto,          │
│          manifiesto                      │
│                                          │
│ download_manifesto  → click en PDF link  │
└──────────────────────────────────────────┘

Conversiones en GA4:
- cta_click
- download_manifesto
- expand_publication (secundario, engagement)
```

