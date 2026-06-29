## Why

La landing page actual no tiene una sección que comunique los principios y valores de trabajo. El manifiesto existe como PDF/LaTeX pero no está enlazado desde el sitio. Una página separada con un resumen visual permite a clientes potenciales entender la filosofía de trabajo y genera una señal medible en GA4 (pageview única, funnel hacia contacto).

## What Changes

- Nueva página `/manifiesto` con resumen web-native del manifiesto
- Contenido: anti-pilares (hook), 5 pilares (tarjetas), enlace a PDF completo, CTA a contacto
- Navbar actualizada con enlace "Manifiesto"
- Footer actualizado con enlace
- Eventos GA4 custom para medir interacción:
  - `expand_publication` (toggles en trayectoria)
  - `cta_click` (botones principales)
  - `nav_click` (navegación)
  - `download_manifesto` (descarga PDF)
- Goals/Conversiones configurados en GA4

## Capabilities

### New Capabilities
- `pagina-manifiesto`: Página independiente con resumen del manifiesto, anti-pilares y pilares, enlace a PDF y CTA a contacto
- `ga4-event-tracking`: Eventos custom GA4 para medir interacciones clave (expandables, CTAs, navegación, descargas)

### Modified Capabilities
- Ninguna (no hay specs existentes que modificar)

## Impact

- `index.html`: navbar y footer (nuevo enlace)
- `manifesto.tex` / `manifesto.pdf`: ya existen, se referencian
- Nuevo archivo: `manifiesto.html` (o `manifiesto/index.html`)
- Script inline de tracking GA4 en ambas páginas
- Configuración manual en GA4 console para marcar conversiones
