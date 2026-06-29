## ADDED Requirements

### Requirement: Tracking de expandibles en trayectoria
El sistema DEBE trackear los eventos `toggle` en los elementos `<details>` de la sección `#trayectoria` mediante GA4.

#### Scenario: Expandir publicación
- **WHEN** un usuario abre un `<details>` en `#trayectoria`
- **THEN** el sistema DEBE enviar `gtag('event', 'expand_publication', { label: '<nombre-publicacion>', action: 'open' })`

#### Scenario: Colapsar publicación
- **WHEN** un usuario cierra un `<details>` en `#trayectoria`
- **THEN** el sistema DEBE enviar `gtag('event', 'expand_publication', { label: '<nombre-publicacion>', action: 'close' })`

#### Scenario: Auto-detección de nuevos details
- **WHEN** se añaden nuevos `<details>` al DOM en `#trayectoria`
- **THEN** el sistema DEBE trackear automáticamente sus eventos `toggle`

### Requirement: Tracking de CTAs
El sistema DEBE trackear los clics en botones CTA principales.

#### Scenario: CTA hero agendar
- **WHEN** un usuario hace clic en "Agendar Sesión de Viabilidad" del hero
- **THEN** el sistema DEBE enviar `gtag('event', 'cta_click', { label: 'hero_agendar' })`

#### Scenario: CTA hero ver soluciones
- **WHEN** un usuario hace clic en "Ver áreas de soporte" del hero
- **THEN** el sistema DEBE enviar `gtag('event', 'cta_click', { label: 'hero_ver_soluciones' })`

#### Scenario: CTA nav solicitar
- **WHEN** un usuario hace clic en "Solicitar Evaluación" de la navbar
- **THEN** el sistema DEBE enviar `gtag('event', 'cta_click', { label: 'nav_solicitar' })`

#### Scenario: CTA contacto email
- **WHEN** un usuario hace clic en el botón "Solicitar Evaluación por Email"
- **THEN** el sistema DEBE enviar `gtag('event', 'cta_click', { label: 'contacto_email' })`

#### Scenario: CTA manifiesto contacto
- **WHEN** un usuario hace clic en el CTA de contacto desde `/manifiesto`
- **THEN** el sistema DEBE enviar `gtag('event', 'cta_click', { label: 'manifesto_cta' })`

### Requirement: Tracking de navegación
El sistema DEBE trackear los clics en enlaces de la navbar.

#### Scenario: Click en nav
- **WHEN** un usuario hace clic en cualquier enlace de la navbar
- **THEN** el sistema DEBE enviar `gtag('event', 'nav_click', { label: '<seccion>' })`

### Requirement: Tracking de descarga del manifiesto
El sistema DEBE trackear los clics en enlaces al PDF del manifiesto.

#### Scenario: Descarga de PDF
- **WHEN** un usuario hace clic en un enlace a `/assets/docs/manifesto.pdf`
- **THEN** el sistema DEBE enviar `gtag('event', 'download_manifesto')`

### Requirement: Script de tracking declarativo y reutilizable
El tracking DEBE implementarse mediante un script inline que lea atributos `data-ga-label` de los elementos trackeables.

#### Scenario: Atributo data-ga-label
- **WHEN** un elemento HTML tiene el atributo `data-ga-label`
- **THEN** el script DEBE registrar un event listener que envíe un evento GA4 con ese valor como label
