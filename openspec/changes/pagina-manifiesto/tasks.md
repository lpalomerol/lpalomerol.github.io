## 1. Tracking GA4 en index.html existente

- [x] 1.1 Añadir data attributes (`data-ga-label`) a los 3 `<details>` en `#trayectoria` con labels descriptivos
- [x] 1.2 Añadir data attributes a CTAs principales (hero agendar, hero ver soluciones, nav solicitar, contacto email)
- [x] 1.3 Añadir data attributes a enlaces de navbar
- [x] 1.4 Implementar script inline GA4 que procese `data-ga-label` y envíe eventos (expand_publication, cta_click, nav_click, download_manifesto)
- [x] 1.5 Verificar que los eventos no interfieren con la navegación nativa (anchor links, mailto)

## 2. Página manifiesto

- [x] 2.1 Crear `manifiesto/index.html` con navbar y footer coherentes con `index.html`
- [x] 2.2 Implementar hero con título "Manifiesto · Luis Palomero, PhD"
- [x] 2.3 Implementar sección de anti-pilares (5 tarjetas con estilo destacado)
- [x] 2.4 Implementar sección de 5 pilares con tarjetas (color por pilar: azul, esmeralda, ámbar, violeta, slate)
- [x] 2.5 Añadir enlace de descarga a `/assets/docs/manifesto.pdf` con `download` attribute y data-ga-label
- [x] 2.6 Añadir CTA a contacto (enlace a mailto o `/#contacto`)
- [x] 2.7 Añadir script inline GA4 a la página manifiesto

## 3. Integración y navegación

- [x] 3.1 Añadir enlace "Manifiesto" a la navbar de `index.html`
- [x] 3.2 Añadir enlace "Manifiesto" al footer de `index.html`
- [x] 3.3 Verificar navegación fluida entre `index.html` y `manifiesto/index.html`

## 4. Configuración GA4 (manual en GA4 console)

- [ ] 4.1 Marcar `cta_click` como conversión en GA4 admin panel
- [ ] 4.2 Marcar `download_manifesto` como conversión en GA4 admin panel
- [ ] 4.3 Marcar `expand_publication` como conversión (opcional, engagement)
- [ ] 4.4 Configurar funnel de exploración: `/` → `/manifiesto` → `cta_click`

## 5. Verificación (manual)

- [ ] 5.1 Probar que navbar y footer enlazan correctamente a `/manifiesto`
- [ ] 5.2 Probar que descarga de PDF funciona
- [ ] 5.3 Probar que CTA a contacto funciona
- [ ] 5.4 Verificar eventos GA4 en consola del navegador (network tab, filter por `gtag` o `collect`)
- [ ] 5.5 Verificar responsive (mobile/tablet) en ambas páginas
