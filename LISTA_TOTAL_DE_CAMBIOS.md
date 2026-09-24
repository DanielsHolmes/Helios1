# Resumen Exhaustivo de Cambios Realizados en las Landings de Helios1 Capital

Este documento detalla **todos los cambios realizados**, las métricas financieras actualizadas conforme al archivo `Helios1 Loan Product Matrix (1).xlsx`, los nuevos campos integrados en los formularios de captura y las ubicaciones exactas (archivos y secciones) donde se aplicaron las modificaciones.

---

## 1. Resumen Global de Cambios

1. **Actualización Completa de Métricas y Tasas (Product Matrix):**
   - Se reemplazaron todas las cifras y tasas desactualizadas con los valores oficiales de la Matriz de Productos para los 5 programas de financiamiento.
2. **Estandarización de Formularios de Captura de Leads:**
   - Se agregaron los campos `Estimated FICO`, `Purchase Price` y `Expected Value` en **todas** las landing pages, **excepto en Multifamily**, donde únicamente se incorporó `Estimated FICO` (a solicitud expresa).
3. **Mención "No Bank Statements Needed":**
   - Incorporado de forma prominente en el Trust Bar, Program Snapshot y FAQ de **Fix & Flip**, **Ground Up Construction** y **Stabilized Bridge**.
4. **Opciones de Tasación (Appraisal / No Appraisal):**
   - Agregada información clara sobre la alternativa **"No Appraisal Option / AMC Appraisal"** tanto en **Ground Up Construction** como en **Fix & Flip**.
5. **Reemplazo de Términos Poco Atractivos:**
   - En **Bridge Financing**, se eliminó el término `"Non-Recourse"` y se reemplazó por un concepto institucional más persuasivo y diferenciador: **"Asset-Based Underwriting"** (junto con la tasa competitiva fija desde `9.49%+ Fixed`).
   - Se actualizó el carrusel de programas cruzados en las 5 landings para reflejar este cambio.
6. **Eliminación de Tiers No Prioritarios:**
   - **Fix & Flip:** Se retiró la sección de *Heavy Rehab & Value-Add*.
   - **Bridge Financing:** Se retiró la sección de *Commercial Bridge Financing*.
7. **División de Programas Complejos:**
   - **DSCR:** Se dividió en una sección principal de **Single Property DSCR** y una sección independiente y dedicada exclusivamente a **Portfolio DSCR** (Portafolios de hasta 20 propiedades).
   - **Multifamily:** Se estructuró formalmente en dos tiers: **Multifamily Perm (5+ Unit Properties)** y **Multifamily Bridge (5+ Unit Properties)**.
8. **Sincronización Total con la Documentación:**
   - Se actualizó el archivo maestro `Landings/Helios Ads landings.md` en sus 5 secciones para que el contenido en Markdown sea idéntico al código HTML en producción.

---

## 2. Detalle de Campos Nuevos en los Formularios

| Landing Page | Archivo | Campos Agregados |
| :--- | :--- | :--- |
| **Ground-Up Construction** | `Landings/ground-up-construction.html` | `Estimated FICO`, `Purchase Price`, `Expected Value` |
| **Fix & Flip** | `Landings/fix-and-flip.html` | `Estimated FICO`, `Purchase Price`, `Expected Value` |
| **DSCR Rental Properties** | `Landings/dscr-rental-properties.html` | `Estimated FICO`, `Purchase Price`, `Expected Value` |
| **Residential Bridge** | `Landings/bridge-financing.html` | `Estimated FICO`, `Purchase Price`, `Expected Value` |
| **Multifamily** | `Landings/multifamily.html` | `Estimated FICO` *(exclusivamente)* |

*Nota:* Cada nuevo campo cuenta con su etiqueta correspondiente, placeholders contextuales formateados (`e.g., 720`, `e.g., $450,000`, `e.g., $650,000`) y atributos `name` e `id` semánticos para la integración con el backend o CRM.

---

## 3. Detalle de Cambios por Landing Page

### A. Ground Up Construction (`Landings/ground-up-construction.html`)

1. **Formulario del Hero (`#hero-form`):**
   - Agregados los campos `Estimated FICO` (selector de 620 a 760+ con valor por defecto 680-719), `Purchase Price / Land Cost` e `Expected Value (ARV)`.
2. **Trust Bar (`.trust-bar`):**
   - Actualizado con 4 propuestas de valor clave:
     - *Rates starting at 8.75%+ (Interest-Only)*
     - *Up to 90% LTC (100% Construction Costs)*
     - *No Bank Statements Needed*
     - *No Appraisal Option Available*
3. **Program Snapshot (`#programs`):**
   - **Sustitución de Maximum LTV por Tasas:** Se reemplazó la tarjeta de LTV por **Rate** (`Starting at 8.75%+ Interest-Only, No Prepayment Penalty`).
   - **Opciones de Appraisal:** Se agregó la tarjeta **Appraisal Options** (`No appraisal option available / AMC appraisal required for standard terms`).
   - **Documentación:** Se agregó la tarjeta **Documentation** (`No Bank Statements Needed`).
   - **Apalancamiento:** Up to 90% LTC (Permitted: 75% Initial LTC | Unpermitted: 60% Initial LTC | Lot Acquisition: up to 75%).
   - **Construcción:** Up to 100% of construction budget.
   - **Velocidad:** Pre-aprobación en 24 horas y desembolso de draws en 24–48 horas.
4. **Sección FAQ (`#faq`):**
   - Actualizada la respuesta sobre constructores primerizos (califican asociándose con un General Contractor con experiencia).
   - Agregada pregunta y respuesta sobre opciones de tasación (No-Appraisal vs AMC Appraisal).
   - Agregada pregunta y respuesta confirmando que no se requieren extractos bancarios.
5. **Carrusel de Programas (`#portfolio-carousel`):**
   - Tarjeta 4 (Bridge): Reemplazado `"Non-Recourse Avail."` por `"Fixed from 9.49%"`.

---

### B. Fix & Flip Financing (`Landings/fix-and-flip.html`)

1. **Formulario del Hero (`#hero-form`):**
   - Agregados los campos `Estimated FICO`, `Purchase Price` y `Expected Value (ARV)`.
2. **Trust Bar (`.trust-bar`):**
   - Actualizado a:
     - *Rates starting at 8.75%+*
     - *Up to 90% LTC (100% on Exception)*
     - *100% Rehab Funding*
     - *No Bank Statements Needed*
     - *No Appraisal Option Available*
3. **Eliminación de Tiers Secundarios:**
   - Se removió por completo la sección/tier de **Heavy Rehab & Value-Add**, dejando la landing enfocada 100% en Fix & Flip residencial ágil.
4. **Program Snapshot (`#programs`):**
   - Grid unificado de 12 tarjetas técnicas con datos de la matriz:
     - **Tasa:** Starting at `8.75%+` (anteriormente figuraba 9.99%+).
     - **Monto de Préstamo:** $100K a $5MM por propiedad.
     - **Apalancamiento:** Up to 90% LTC (100% en casos excepcionales) / 100% de fondos de rehabilitación / Máximo 70%–75% LTARV.
     - **Tasación:** Opciones de No Appraisal y AMC Appraisal.
     - **Documentación:** No Bank Statements Needed.
     - **Tiempos:** Cierres de 7 a 14 días hábiles; reembolsos de draws en 24–48 horas.
     - **Score mínimo:** FICO 620+.
5. **Sección FAQ (`#faq`):**
   - Se retiró la pregunta sobre Heavy Rehab.
   - Se añadieron preguntas específicas sobre las opciones de tasación (No-Appraisal) y la calificación sin extractos bancarios.
6. **Carrusel de Programas:**
   - Tarjeta 4 (Bridge): Reemplazado `"Non-Recourse Avail."` por `"Fixed from 9.49%"`.

---

### C. DSCR Rental Properties (`Landings/dscr-rental-properties.html`)

1. **Formulario del Hero (`#hero-form`):**
   - Agregados los campos `Estimated FICO`, `Purchase Price` y `Expected Value`.
2. **Navegación Superior (`.nav-links`):**
   - Se dividieron los enlaces de acceso rápido en **Single DSCR** (`#programs`) y **Portfolios** (`#portfolios`).
3. **Program Snapshot Principal - Single Property DSCR (`#programs`):**
   - 12 tarjetas exclusivas para propiedades individuales (1–4 unidades, condos, townhomes, PUDs y STRs):
     - **Tasa:** Starting at `5.75%`.
     - **Monto:** $75,000 – $2,500,000.
     - **LTV Máximo:** Hasta 80% (85% por excepción en Purchase; 80% Rate/Term; 75%–80% Cash-Out).
     - **DSCR Mínimo:** 0.75x (coberturas menores evaluadas caso a caso).
     - **Plazos:** 30 años fijo y ARM híbridos (5, 7, 10 años); Amortización completa o Interest-Only parcial.
     - **FICO:** Mínimo 660.
     - **Seasoning:** Sin tiempo mínimo de permanencia requerido (Zero Seasoning).
     - **Cierre:** 2 a 3 semanas; sin W-2s, nóminas ni declaraciones de impuestos personales.
4. **Nueva Sección Independiente - Portfolio DSCR (`#portfolios`):**
   - Creada directamente debajo del contenido principal de DSCR, con encabezado propio (*"Portfolios Up to 20 Properties"*), subtítulo explicativo y grid de 12 tarjetas:
     - **Tipo de Préstamo:** Blanket Cross-Collateralized Loan (un solo cierre para todo el portafolio).
     - **Tamaño del Portafolio:** Hasta 20 propiedades y montos de $100,000 a $3,000,000.
     - **Tasa:** Starting at `5.75%`.
     - **LTV:** Hasta 80% Purchase & Rate/Term; 75% Cash-Out.
     - **DSCR Mínimo:** 1.00x para el paquete de propiedades.
     - **Ocupación Mínima:** 90% por conteo de unidades.
     - **Precio de Liberación (Release Price):** 1.2x del monto asignado por propiedad para ventas individuales.
     - **Plazos y Cierre:** 30 años fijo/ARM y tiempos de cierre de 4 a 6 semanas.
5. **Carrusel de Programas:**
   - Tarjeta 4 (Bridge): Reemplazado `"Non-Recourse Avail."` por `"Fixed from 9.49%"`.

---

### D. Residential Bridge Financing (`Landings/bridge-financing.html`)

1. **Formulario del Hero (`#hero-form`):**
   - Agregados los campos `Estimated FICO`, `Purchase Price` y `Expected Value`.
2. **Trust Bar (`.trust-bar`):**
   - Se eliminó `"Flexible non-recourse options"` y se actualizó a:
     - *Rates starting at 9.49%+ (Fixed)*
     - *Up to 85% LTC / 70% LTV*
     - *No Bank Statements Needed*
     - *Close in as Fast as 10 Days*
     - *Asset-Based Underwriting*
3. **Eliminación de Commercial Bridge Financing:**
   - Se retiró la sección y referencias a *Commercial Bridge Financing (Retail, Office, Industrial)* de esta landing para mantenerla enfocada en *Residential Stabilized Bridge*.
4. **Program Snapshot - Stabilized Bridge (`#programs`):**
   - 12 tarjetas actualizadas con las cifras de la matriz:
     - **Tasa:** Starting at `9.49%+ Fixed`.
     - **Monto:** $100,000 a $3,500,000.
     - **Plazo:** 12 a 24 meses con opciones de extensión.
     - **Apalancamiento:** Hasta 85% LTC / 70% LTV.
     - **Estructura de Riesgo (Reemplazo de Non-Recourse):** **Asset-Based Underwriting** (suscripción enfocada en el colateral y la viabilidad del activo).
     - **Documentación:** No Bank Statements Needed.
     - **Cobertura:** 1.10x DSCR mínimo si la propiedad está en condición C3.
     - **Tiempo de Cierre:** Tan rápido como 10 días hábiles.
     - **Experiencia:** Flexible, sin cantidad mínima obligatoria de cierres previos.
     - **Score mínimo:** FICO 680+.
5. **Sección FAQ (`#faq`):**
   - Se sustituyó la consulta de non-recourse por una explicación de **Asset-Based Underwriting**.
   - Se añadieron respuestas sobre cierre rápido en 10 días y calificación sin extractos bancarios.
6. **Carrusel de Programas:**
   - Tarjeta 4 (Bridge): Reemplazado `"Non-Recourse Avail."` por `"Fixed from 9.49%"`.

---

### E. Multifamily Real Estate Financing (`Landings/multifamily.html`)

1. **Formulario del Hero (`#hero-form`):**
   - Se agregó **únicamente** el campo `Estimated FICO` (dropdown de 620 a 760+ con valor sugerido 680–719). No se añadieron *Purchase Price* ni *Expected Value*, respetando la instrucción precisa del usuario.
2. **Trust Bar (`.trust-bar`):**
   - Actualizado a:
     - *Rates starting at 6.49%+*
     - *5+ Units up to 30 Units*
     - *Up to 75% LTV / 80% LTC*
     - *Multifamily Perm & Bridge Solutions*
3. **Program Snapshot Dividido en Dos Tiers (`#programs`):**
   - **Tier 1: Multifamily Perm (5+ Unit Properties):**
     - Propiedades elegibles: 5+ Unidades hasta 30 unidades (Multifamily y Mixto comercial).
     - Monto del préstamo: $350,000 a $6,000,000.
     - Tasa de interés: Desde `6.49%+`.
     - Plazos: 30 años fijo o ARM híbrido (5, 7, 10 años).
     - Amortización: Tabla de amortización a 30 años.
     - LTV máximo: Hasta 75% para Purchase y Rate/Term; hasta 70% para Cash-Out.
     - DSCR mínimo: 1.10x.
     - FICO mínimo: 680.
     - Tiempo de cierre: 4 a 6 semanas.
   - **Tier 2: Multifamily Bridge (5+ Unit Properties):**
     - Propiedades elegibles: 5+ Unidades hasta 30 unidades (Adquisición, Value-Add, Reposicionamiento y Estabilización).
     - Monto del préstamo: $1,000,000 a $10,000,000.
     - Tasa de interés: `SOFR + 450 bps` o alternativas de tasa fija.
     - Plazo: 12 a 24 meses (con opciones de extensión).
     - Apalancamiento: Hasta 75% Initial LTC | Hasta 80% Blended LTC | Hasta 70% LTARV.
     - Métricas de suscripción: **9.0% Minimum Debt Yield** y **1.20x Takeout DSCR**.
     - Comisión de originación: 1.5% a 2.5%.
     - Tiempo de cierre: 3 a 4 semanas.
     - FICO mínimo: 680.
4. **Sección FAQ (`#faq`):**
   - Actualizada para clarificar la diferencia entre Multifamily Perm y Multifamily Bridge, límites de apalancamiento, y requisitos de Debt Yield (9%) y DSCR (1.10x).
5. **Carrusel de Programas:**
   - Tarjeta 4 (Bridge): Reemplazado `"Non-Recourse Avail."` por `"Fixed from 9.49%"`.

---

### F. Documento Maestro (`Landings/Helios Ads landings.md`)

Se sincronizaron íntegramente las 5 secciones de especificación en Markdown:
1. **Sección 1 (Ground-Up Construction):** Nuevos campos en el formulario, tasa desde 8.75%+, eliminación de Maximum LTV en el snapshot, opciones de tasación (AMC vs No Appraisal), mención de no bank statements y FAQs actualizadas.
2. **Sección 2 (Fix & Flip):** Nuevos campos en el formulario, tasa desde 8.75%+, eliminación total de la sección *Heavy Rehab*, opciones de tasación, mención de no bank statements y FAQs actualizadas.
3. **Sección 3 (DSCR Rental Properties):** Nuevos campos en el formulario, separación visual y textual entre *Single Property DSCR* y *Portfolio DSCR (Up to 20 Properties)* con todas las métricas de la matriz.
4. **Sección 4 (Bridge Financing):** Renombrado del encabezado a *Residential Bridge Financing*, nuevos campos en el formulario, eliminación de *Commercial Bridge*, actualización a *Stabilized Bridge* (tasa fija desde 9.49%+, cierre en 10 días), sustitución de Non-Recourse por Asset-Based Underwriting y FAQs actualizadas.
5. **Sección 5 (Multifamily):** Incorporación de *Estimated FICO* únicamente en el formulario, división de Program Snapshot en *Tier 1: Multifamily Perm* y *Tier 2: Multifamily Bridge* con todas sus métricas financieras y FAQs actualizadas.

---

### G. Página Principal (`index.html`)

Se generaron e integraron 7 nuevas imágenes fotorrealistas de alta definición (aspect ratio 3:2) en dos secciones estratégicas de la home:

1. **Sección "How It Works" (`#how` - *Bring Us the Deal. We’ll Start With the Opportunity.*):**
   - **Paso 01 (`assets/step1-submit-deal.jpg`):** Planos arquitectónicos, folleto institucional de fondo de inversión y tablet con rendimiento de portafolio frente a ventanal con rascacielos.
   - **Paso 02 (`assets/step2-experienced-lender.jpg`):** Dos profesionales de inversión en asesoría en sala de juntas moderna con vistas a la ciudad.
   - **Paso 03 (`assets/step3-structure-financing.jpg`):** Term sheet de deuda inmobiliaria, modelo de estructuración de capital, pluma ejecutiva y maqueta arquitectónica.
   - **Paso 04 (`assets/step4-move-toward-closing.jpg`):** Llaves de propiedad sobre documentos de cierre firmados y carpeta de depósito en garantía (*Escrow*), con apretón de manos al fondo.
   - Se añadió animación suave de zoom en hover (`scale(1.04)`) a las tarjetas.

2. **Sección "Insights" (`#insights` - *Better Financing Decisions Start With Better Questions*):**
   - **Artículo 1 (`assets/insight-dscr-comparison.jpg`):** Inversionista en traje analizando hojas de cálculo y gráficos de comparación de préstamos DSCR frente a ventana con residencias de lujo.
   - **Artículo 2 (`assets/insight-ground-up-finance.jpg`):** Arquitecta/desarrolladora con casco y planos en obra de construcción residencial de lujo en estructura inicial bajo la luz matutina.
   - **Artículo 3 (`assets/insight-construction-draws.jpg`):** Inspectora de obra en chaleco con tablet digital auditando hitos y calendario de desembolsos (*Draw Milestone Schedules*) en interior de vivienda en construcción.

3. **Sección "About / Credibility" (`#about` - *Real Estate Lending Informed by Capital Markets Experience*):**
   - **Imagen Principal (`assets/capital-markets-lending.jpg`):** Comité de inversión y socios ejecutivos en una sala de juntas ejecutiva de esquina con ventanales hacia el distrito financiero, analizando en pantalla interactiva la analítica de cartera de deuda inmobiliaria (*Real Estate Credit Fund: Debt Financing Portfolio Analytics*), con modelos de crédito estructurado en portátiles y term sheets impresos. Sustituye la imagen genérica anterior de sala de estar.

---

## 4. Estado de Verificación y Compilación

- **Validación Sintáctica HTML:** Todos los archivos HTML (`.html`) fueron analizados mediante analizadores de estructura (`HTMLParser`) confirmando cero etiquetas sin cerrar, jerarquías semánticas correctas y coherencia en identificadores de formulario.
- **Estilos CSS:** Se mantuvieron intactos los esquemas de color, tipografía y diseño responsivo del diseño original, utilizando las clases utilitarias (`.field`, `.trust-bar`, `.snapshot-card`, `.program-tier`, `.badge`) ya existentes.
- **Git Status:** Todos los cambios se encuentran contenidos y limpios dentro del repositorio.
