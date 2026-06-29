## ADDED Requirements

### Requirement: Documento manifesto.md en raíz del proyecto
El proyecto SHALL contener un archivo `manifesto.md` en la raíz que declare los principios fundamentales como ML engineer para oncología.

#### Scenario: Archivo existe
- **WHEN** se revisa la raíz del proyecto
- **THEN** existe un archivo `manifesto.md`

#### Scenario: Formato markdown válido
- **WHEN** se procesa el archivo como markdown
- **THEN** no hay errores de sintaxis markdown

### Requirement: Principio rector de simplicidad radical
El manifesto SHALL declarar la simplicidad como principio rector: métodos comprensibles para clínicos e investigadores, cero magia, código que se explica en 5 minutos.

#### Scenario: Sección de simplicidad presente
- **WHEN** se lee el manifesto
- **THEN** contiene una sección que establece la simplicidad como principio rector

### Requirement: Cinco pilares documentados
El manifesto SHALL documentar los siguientes pilares:
1. Reproducibilidad y robustez en producción
2. Altos estándares de programación
3. Simplicidad en métodos (sin magia)
4. Narrativa coherente (cada pipeline cuenta una historia)
5. IA como herramienta de soporte, no sustituto

#### Scenario: Todos los pilares presentes
- **WHEN** se lee el manifesto
- **THEN** los cinco pilares están documentados como secciones o subsecciones

### Requirement: Filosofía de testing
El manifesto SHALL incluir una filosofía de testing de tipo principialista (no métrica): testing como confianza, como documentación de comportamiento, como red que permite refactorizar hacia la simplicidad.

#### Scenario: Filosofía de testing presente
- **WHEN** se lee el manifesto
- **THEN** contiene una sección dedicada a la filosofía de testing

### Requirement: Documento no visible en web pública
El manifesto SHALL ser un documento interno. No debe enlazarse desde la navegación, el hero, el footer ni ninguna sección visible de la web pública.

#### Scenario: Sin enlaces en HTML
- **WHEN** se inspecciona el index.html
- **THEN** no hay enlaces a manifesto.md

#### Scenario: Sin referencia en navegación
- **WHEN** se revisan los elementos nav del sitio
- **THEN** no hay referencias a manifesto.md
