## ADDED Requirements

### Requirement: Página manifiesto accesible desde navegación
El sitio DEBE tener una página `/manifiesto` accesible desde la navbar principal y el footer de todas las páginas.

#### Scenario: Enlace en navbar
- **WHEN** un usuario visita cualquier página del sitio
- **THEN** la navbar DEBE contener un enlace "Manifiesto" que apunte a `/manifiesto`

#### Scenario: Enlace en footer
- **WHEN** un usuario visita cualquier página del sitio
- **THEN** el footer DEBE contener un enlace "Manifiesto" que apunte a `/manifiesto`

#### Scenario: Navegación desde index
- **WHEN** un usuario hace clic en "Manifiesto" desde `index.html`
- **THEN** el navegador DEBE navegar a `/manifiesto`

### Requirement: Contenido de la página manifiesto
La página `/manifiesto` DEBE contener un resumen web del manifiesto con anti-pilares, pilares y enlaces a recursos adicionales.

#### Scenario: Hero con título
- **WHEN** un usuario accede a `/manifiesto`
- **THEN** DEBE ver un encabezado con "Manifiesto" y el subtítulo "Luis Palomero, PhD"

#### Scenario: Anti-pilares visibles
- **WHEN** un usuario hace scroll en `/manifiesto`
- **THEN** DEBE ver los 5 anti-pilares del manifiesto presentados como tarjetas o lista destacada

#### Scenario: 5 pilares visibles
- **WHEN** un usuario hace scroll en `/manifiesto`
- **THEN** DEBE ver los 5 pilares (Reproducibilidad, Altos estándares, Simplicidad, Narrativa, IA como soporte) presentados como tarjetas individuales

#### Scenario: Enlace a PDF completo
- **WHEN** un usuario visita `/manifiesto`
- **THEN** DEBE ver un enlace o botón para descargar/abrir el PDF completo del manifiesto en `/assets/docs/manifesto.pdf`

#### Scenario: CTA a contacto
- **WHEN** un usuario visita `/manifiesto`
- **THEN** DEBE ver un CTA para solicitar evaluación o contactar, que enlace a `/#contacto` o al mail directo

### Requirement: Coherencia visual con el sitio existente
La página `/manifiesto` DEBE mantener el mismo estilo visual (Tailwind, paleta, tipografía) que `index.html`.

#### Scenario: Mismo header y footer
- **WHEN** un usuario navega a `/manifiesto`
- **THEN** DEBE ver el mismo navbar sticky y footer que en el sitio principal

#### Scenario: Misma paleta de colores
- **WHEN** un usuario visualiza `/manifiesto`
- **THEN** los colores, tipografía y espaciado DEBEN coincidir con los del sitio principal
