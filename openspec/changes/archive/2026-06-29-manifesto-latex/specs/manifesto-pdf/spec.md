## ADDED Requirements

### Requirement: Archivo .tex compilable
El proyecto SHALL contener un archivo `assets/docs/manifesto.tex` que compile correctamente con `pdflatex` sin errores.

#### Scenario: Compilación exitosa
- **WHEN** se ejecuta `pdflatex manifesto.tex`
- **THEN** el comando termina con código de salida 0 y genera `manifesto.pdf`

### Requirement: Contenido completo del manifiesto
El PDF resultante SHALL contener el texto completo del manifiesto: declaración de intenciones, principio rector, 5 pilares, filosofía de testing y anti-pilares.

#### Scenario: Todo el contenido presente
- **WHEN** se extrae el texto del PDF
- **THEN** contiene las secciones del manifiesto (declaración, simplicidad radical, 5 pilares, testing, anti-pilares)

### Requirement: Diseño profesional sin portada
El PDF SHALL tener una cabecera en primera página (título, autor, versión, fecha) sin página de portada independiente. El contenido empieza en la misma página.

#### Scenario: Cabecera presente
- **WHEN** se visualiza la primera página del PDF
- **THEN** muestra título, autor y fecha antes del contenido sin page break

### Requirement: Un solo archivo fuente
El manifiesto LaTeX SHALL ser un único archivo `.tex`, sin división en múltiples archivos incluidos.

#### Scenario: Archivo único
- **WHEN** se inspecciona el directorio `assets/docs/`
- **THEN** solo existe un archivo `.tex` para el manifiesto (sin archivos `.sty` o `.tex` adicionales)

### Requirement: PDF descargable
El proyecto SHALL contener `assets/docs/manifesto.pdf` compilado y listo para descargar.

#### Scenario: PDF existe
- **WHEN** se lista el directorio `assets/docs/`
- **THEN** existe `manifesto.pdf`
