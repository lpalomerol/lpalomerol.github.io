## MODIFIED Requirements

### Requirement: Reordenar secciones
El manifesto SHALL mover la sección de anti-pilares al inicio del documento, antes de la declaración de intenciones, para actuar como filtro rápido para el lector.

#### Scenario: Anti-pilares visible al inicio
- **WHEN** se abre el manifesto.md
- **THEN** la primera sección tras el título es "Anti-pilares" o "Lo que no soy"

### Requirement: Validación experimental como principio
El manifesto SHALL incluir una sección que establezca que el modelado in silico genera hipótesis, no conclusiones, y que la validación experimental es necesaria para confirmar hallazgos bioinformáticos.

#### Scenario: Sección de validación experimental presente
- **WHEN** se lee el manifesto
- **THEN** contiene una sección que aborda validación experimental como principio

### Requirement: Contrato bidireccional
El manifesto SHALL incluir una sección que describa qué recibe el colaborador/cliente y qué espera el autor de él.

#### Scenario: Sección colaborativa presente
- **WHEN** se lee el manifesto
- **THEN** contiene una sección con "qué recibes" y "qué espero de ti"

### Requirement: Límite de competencia
El manifesto SHALL incluir una declaración explícita sobre dónde termina la competencia del autor (datos, pipelines, modelos) y dónde empieza la del biólogo/clínico (biología tumoral, relevancia clínica).

#### Scenario: Límite de competencia presente
- **WHEN** se lee el manifesto
- **THEN** contiene una declaración explícita de límite de competencia

### Requirement: Traducción de testing para no-ingenieros
El manifesto SHALL reescribir la sección de filosofía de testing en términos que un biólogo o PI pueda entender — no cobertura de código, sino confianza en resultados.

#### Scenario: Testing en lenguaje de cliente
- **WHEN** se lee la sección de testing
- **THEN** evita jerga técnica de ingeniería de software y usa términos como "verificaciones automáticas" y "consistencia de resultados"

### Requirement: Transparencia en uso de IA
El manifesto SHALL incluir una nota sobre cómo el colaborador puede saber qué partes del trabajo han sido asistidas por IA.

#### Scenario: Nota de transparencia IA
- **WHEN** se lee la sección de IA
- **THEN** incluye cómo se comunica al colaborador el uso de IA
