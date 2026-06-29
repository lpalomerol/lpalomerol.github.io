## MODIFIED Requirements

### Requirement: Sincronizar contenido con manifesto.md
El archivo .tex SHALL reflejar todos los cambios de contenido aplicados a manifesto.md (reordenación, nuevas secciones, traducciones).

#### Scenario: Contenido sincronizado
- **WHEN** se comparan manifesto.md y manifesto.tex
- **THEN** ambos contienen las mismas secciones con el mismo contenido

### Requirement: Reemplazar colorbox por regla vertical
El PDF SHALL usar una regla vertical (no un colorbox) para la cita destacada, garantizando legibilidad tanto en color como en impresión B/N.

#### Scenario: Regla vertical presente
- **WHEN** se inspecciona el PDF
- **THEN** la cita destacada usa una regla vertical en lugar de fondo azul

### Requirement: Resolver overfull hbox
El .tex SHALL corregir los overfull hbox en líneas 52 y 137 (desbordamiento ~0.2pt) mediante hyphenation manual o \sloppy local.

#### Scenario: Sin overfull hbox
- **WHEN** se compila `pdflatex manifesto.tex`
- **THEN** el log no contiene advertencias de overfull hbox

### Requirement: Compatibilidad \enquote
El .tex SHALL mantener el uso de csquotes pero añadirá un fallback o nota de dependencia para compilación portable.

#### Scenario: Compilación portable
- **WHEN** se compila en un sistema sin babel-spanish
- **THEN** el documento no falla por \enquote indefinido
