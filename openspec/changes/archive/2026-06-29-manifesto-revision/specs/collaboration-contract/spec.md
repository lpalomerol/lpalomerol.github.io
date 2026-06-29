## ADDED Requirements

### Requirement: Sección de entregables
El manifesto SHALL incluir una sección que liste los entregables concretos que recibe el colaborador: pipeline reproducible, reporte PDF, tests automatizados, datos versionados, figuras publicables.

#### Scenario: Lista de entregables presente
- **WHEN** se lee el manifesto
- **THEN** contiene una sección "Lo que siempre recibirás" con una lista de entregables

### Requirement: Condiciones de colaboración
El manifesto SHALL incluir las condiciones básicas de colaboración: rondas de revisión incluidas, política de cambios de alcance, formato de entrega.

#### Scenario: Condiciones presentes
- **WHEN** se lee la sección de colaboración
- **THEN** incluye rondas de revisión y política de cambios de alcance
