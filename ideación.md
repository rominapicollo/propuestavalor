---
title: Ideación de N3 verticalizados para Minería sobre Cross no contemplados en el PDF inicial
estado: borrador para discusión squad + BU
ultima_actualizacion: 2026-05-11
owner: Account Director Squad Minería
---

# Ideación · N3 adicionales para Minería sobre Cross no listados en el PDF

> El PDF "Offerings Actuales — Adaptación Minería" (mayo 2026) marcó 5 Cross con aplicabilidad a la vertical (Data & AI Ops, AI Workflows & Automation, AI Data Extraction, AI Recommendation System, Data as Logistic Optimization Product). Este documento explora, desde la mirada SME, **N3 adicionales sobre Cross del catálogo que el PDF no consideró**.
>
> Estas ideas no están al nivel de evidencia de una N3 calibrada. Son insumo para que el squad y la BU evalúen cuáles ascender al ejercicio formal de construcción de N3.

---

## 1. AI Agents & RAGs empresariales · Asistente Operacional Minero

**Cross base.** [AI Agents & RAGs empresariales](Servicios%20Cross%20Data/ai-agents-bi-analytics-data-operations.md)

**Hipótesis de N3.** Una operación minera tiene cientos de procedimientos operativos estandarizados (POEs), instructivos de seguridad, manuales de equipos OEM, planes de cierre, contratos sindicales, normativa sectorial y regulatoria. Hoy ese conocimiento vive en SharePoints fragmentados y en la cabeza de gente con turnos 7x7. **Un asistente RAG que un operador, supervisor o jefe de turno puede consultar en faena** —"qué dice el POE para arranque de molino tras parada mayor", "cómo se reporta una observación SERNAGEOMIN bajo el procedimiento X"— libera el conocimiento crítico de los pocos custodios humanos y reduce dependencia de personal específico.

**Casos potenciales.**
- RAG de procedimientos operacionales y planes de respuesta a emergencia.
- RAG de manuales OEM con búsqueda contextual (diagnóstico, troubleshooting en taller).
- Asistente HSE — consulta de matriz IPER, controles críticos, normativa.
- Asistente regulatorio — consulta sobre obligaciones SERNAGEOMIN/MINEM/SMA por tipo de evento o proceso.
- Agente que monitorea desviaciones de pipelines de datos operacionales mineros y alerta cuando hay incidencia (extensión natural del Cross).

**Por qué encaja.** Caso comparable LATAM (Ecosistema de agentes IA Gen con +60% de adherencia) demuestra que el patrón "agente que destraba conocimiento crítico" se sostiene en operaciones complejas. La traducción a minería cambia el corpus pero conserva el patrón.

**Fuentes.**
- ICMM "Health and Safety Performance Indicators", referencia de matrices críticas. *[icmm.com/en-gb/health-and-safety](https://www.icmm.com/en-gb/health-and-safety)*
- IIMCH "Manual de procedimientos operacionales mineros" como referencia conceptual. *[iimch.cl](https://www.iimch.cl)*

---

## 2. Data Analytics & Monitoring · Monitoreo de Depósitos de Relaves (GISTM)

**Cross base.** [Data Analytics & Monitoring](Servicios%20Cross%20Data/data-analytics-monitoring.md)

**Hipótesis de N3.** Probablemente la N3 con **mayor justificación regulatoria y reputacional** de toda la vertical post-2019 (post-rotura de Brumadinho, Vale Brasil). El estándar global GISTM (Global Industry Standard on Tailings Management) obliga a operadores a monitoreo continuo de depósitos de relaves con instrumentación, alertas y trazabilidad de evidencia. **La N3 productiviza ese monitoreo**: integración de datos de piezómetros, inclinómetros, GPS, InSAR, radar interferométrico, drones LiDAR, sensores ambientales aguas abajo. Salida: dashboards de salud del depósito en tiempo real, alertas tempranas de comportamiento anómalo, evidencia trazable para Ingeniero de Registro y para reportería GISTM.

**Casos potenciales.**
- Monitoreo continuo de depósitos activos con sensores físicos + satelitales (InSAR).
- Monitoreo de muros de contención de embalses (relaves o agua) — vibración, deformación, freática.
- Monitoreo de stocks de mineral apilado para señales de inestabilidad.
- Monitoreo de calidad de agua aguas abajo de la operación (consumo y descarga).
- Monitoreo de emisiones a la atmósfera (material particulado, gases) con integración a estaciones de calidad de aire.

**Por qué encaja.** Es un caso con altísimo sponsor ejecutivo: pos-Brumadinho, los CEOs de mining majors firman declaraciones de cumplimiento GISTM bajo responsabilidad personal. Hay presupuesto disponible (inversión global en tailings safety estimada >USD 10B en planificación 2026–2030). Para Acid el delta es: combinar Data Analytics & Monitoring del Cross + Domain Expert geotécnico minero (partner) + integración con servicios satelitales (InSAR vendors: Tre Altamira, Sarmap).

**Fuentes.**
- Global Tailings Review — GISTM standard. *[globaltailingsreview.org/the-global-industry-standard](https://globaltailingsreview.org/the-global-industry-standard/)*
- ICMM Tailings Management. *[icmm.com/en-gb/environmental-stewardship/tailings-management](https://www.icmm.com/en-gb/environmental-stewardship/tailings-management)*
- Comisión Chilena Cobre Cochilco — reportes de seguridad de depósitos. *[cochilco.cl](https://www.cochilco.cl)*
- Tre Altamira (vendor InSAR estándar industria minera) — referencia de servicios satelitales. *[treuropea.com](https://site.tre-altamira.com)*

---

## 3. Forecast & Demand Planning · Forecast de Consumo de Insumos Críticos

**Cross base.** [Forecast & Demand Planning](Servicios%20Cross%20Data/forecast-demand-planning.md)

**Hipótesis de N3.** El consumo de **insumos críticos de operación minera** —bolas de molienda, neumáticos OTR, reactivos de flotación (xantatos, espumantes, modificadores de pH), combustible diesel, ANFO/explosivos, lubricantes, repuestos OEM— representa típicamente 35–45% del costo de operación. Estos consumos hoy se proyectan con metodologías heurísticas y experiencia, frecuentemente con error de 10–20% que se traduce en sobre-stock (costo de capital) o sub-stock (paralización). Un forecast moderno con drivers operacionales (plan de producción, ley alimentación, dureza del mineral, condiciones del equipo) reduce el error y libera capital de trabajo.

**Casos potenciales.**
- Forecast de consumo de bolas de molienda y revestimientos.
- Forecast de consumo de reactivos de flotación según ley y mineralogía alimentación.
- Forecast de consumo de combustible para flota de extracción.
- Forecast de neumáticos OTR con drivers de horas-equipo y condiciones de pista.
- Forecast de demanda de repuestos críticos OEM (especialmente lead times largos: 6–12 meses).

**Por qué encaja.** Caso de uso bien definido, sponsor claro (Supply Chain / Abastecimiento), datos disponibles en SAP + historian + CMMS, dolor cuantificable en USD. ROI rápido y conversación menos política que la de optimización de operación o planta.

**Fuentes.**
- Cochilco "Costos de producción minera del cobre" — referencia de mix de costos por insumo. *[cochilco.cl](https://www.cochilco.cl)*
- Ausenco / Hatch publicaciones sobre forecasting de bolas y reactivos. Literatura técnica AusIMM y SAG Conferences.

---

## 4. Data Exploration & Insights · Optimización Geometalúrgica y Ley de Corte

**Cross base.** [Data Exploration & Insights](Servicios%20Cross%20Data/data-exploration-insights.md)

**Hipótesis de N3.** La capa de **geometalurgia** —relacionar la información del modelo de bloques (litología, alteración, leyes, dureza, índice de molienda) con el comportamiento en planta (recuperación, throughput, consumo de reactivos)— es estructuralmente subexplotada en muchas operaciones. Existen los datos del lado geológico (campañas de muestreo, ensayos metalúrgicos) y los datos del lado de planta (resultados de procesamiento) pero rara vez se cruzan de forma sistemática a escala de modelo de bloques. **La N3 conecta ambos universos** para que decisiones de planificación corto y mediano plazo (secuenciamiento, ley de corte, blending) tengan mejor base predictiva.

**Casos potenciales.**
- Modelo geometalúrgico predictivo de recuperación por bloque.
- Optimización dinámica de ley de corte ante variaciones de precio del commodity.
- Análisis de drivers de variabilidad de recuperación que el geólogo o el metalurgista no había aislado.
- Cross-análisis drillhole logs ↔ resultados de planta para refinar modelos geológicos.
- Análisis exploratorio para identificar zonas del yacimiento con mayor sensibilidad a precio.

**Por qué encaja.** Es uno de los casos de mayor impacto financiero potencial (cada punto de recuperación adicional en gran minería del cobre vale decenas de millones/año). Pero también uno de los más exigentes en evidencia y conversación con áreas técnicas tradicionales (geología, planificación, metalurgia). Pasar a N3 calibrada requiere alianza fuerte con geometalurgista del cliente o un partner especializado.

**Fuentes.**
- AusIMM "Mineral Resource and Ore Reserve Estimation" — referencia técnica. *[ausimm.com](https://www.ausimm.com)*
- SAG Conference proceedings — referencia técnica para casos de uso de geometalurgia. *[sagconference.com](https://www.sagconference.com)*
- McKinsey "Capturing the value of geometallurgy" — paper público de referencia. *[mckinsey.com/industries/metals-and-mining/our-insights](https://www.mckinsey.com/industries/metals-and-mining/our-insights)*

---

## 5. Data Integration Services · Integración IT/OT Mina-Planta

**Cross base.** [Data Integration Services](Servicios%20Cross%20Data/data-integration-services.md)

**Hipótesis de N3.** Es el **prerequisito habilitador** para varias otras N3 (Data & MLOps minería, Recommendation Model minería, Data as Logistic Optimization). En muchas cuentas mineras la integración IT/OT no está resuelta y se vende como N3 propia: pipeline de datos desde historians (PI System), DCS, FMS, CMMS, LIMS hacia un data lake corporativo, con seguridad OT y latencia adecuada.

**Casos potenciales.**
- Integración historian PI System → data lake cloud, con telemetría histórica y NRT.
- Integración FMS dispatch → repositorio de operación.
- Integración SAP + Maximo + LIMS → modelo de datos operacional integrado.
- Integración telemetría OEM (Cat Vital, Komtrax, etc.) → modelo unificado de flota.
- Integración planta DCS → modelo operacional consolidado.

**Por qué encaja.** Si bien parte se solapa con el N3 de Data & MLOps minería, hay cuentas donde el alcance es solo "habilitar integración", sin productivizar modelos todavía. Esos casos abren puerta de menor riesgo y construyen el habilitador para la conversación posterior.

**Nota de pricing.** Es la N3 con mayor sensibilidad a partnerships con integradores OT locales (JRI, Sigdo Koppers, BBosch). Conviene tener el partnership formalizado antes de venderla.

**Fuentes.**
- OSIsoft / AVEVA PI System documentation. *[osisoft.com](https://www.osisoft.com)* / *[aveva.com](https://www.aveva.com)*
- IEC 62443 — estándar de ciberseguridad OT industrial. *[iec.ch](https://webstore.iec.ch/en/publication/7029)*
- GMG Group "Open Mining Format" para interoperabilidad minera. *[gmggroup.org](https://gmggroup.org/guidelines/)*

---

## 6. Data Reporting · Reportería ESG y Sustentabilidad

**Cross base.** [Data Reporting](Servicios%20Cross%20Data/data-reporting.md)

**Hipótesis de N3.** Hay solapamiento con el N3 de AI Workflows (automatización de reportes regulatorios) pero el ángulo aquí es distinto: **construcción del producto de reportería ESG/sustentabilidad** como dashboard interactivo + reportes generados (no solo automatización de envío al regulador). Para los stakeholders modernos de minería (inversores institucionales, ICMM signatories, índices de sustentabilidad) el reporte ya no es PDF anual: es plataforma de transparencia continua con KPIs visibles.

**Casos potenciales.**
- Plataforma de reportería climática TCFD continua con Scope 1, 2 y 3.
- Plataforma de reportería de agua (consumo, recirculación, descargas) alineada con CDP Water y ICMM.
- Plataforma de reportería de biodiversidad y cierre alineada con TNFD (Taskforce on Nature-related Financial Disclosures).
- Plataforma de reportería social (comunidades, derechos humanos) alineada con ICMM/IRMA.
- Dashboard ESG ejecutivo para Board y CEO.

**Por qué encaja.** Mandatos crecientes desde inversores institucionales (CalPERS, NBIM, BlackRock), de IFC Performance Standards, y de ICMM signatory commitments. Conversación de tablero/CFO/Sustentabilidad, no de operación. Sponsor de alto nivel.

**Fuentes.**
- ICMM Mining Principles & Performance Expectations. *[icmm.com/en-gb/our-principles](https://www.icmm.com/en-gb/our-principles)*
- TCFD recommendations (Task Force on Climate-related Financial Disclosures). *[fsb-tcfd.org](https://www.fsb-tcfd.org/)*
- TNFD framework. *[tnfd.global](https://tnfd.global)*
- CDP Water Disclosure. *[cdp.net/en/water](https://www.cdp.net/en/water)*
- IRMA — Initiative for Responsible Mining Assurance. *[responsiblemining.net](https://responsiblemining.net)*

---

## 7. Business Process Optimization · Optimización de Procesos HSE y Cambio de Turno

**Cross base.** [Business Process Optimization](Servicios%20Cross%20Data/business-process-optimization.md)

**Hipótesis de N3.** Hay procesos de soporte minero que no son operación física pero que cuestan plata y degradan la productividad por ineficiencia: **cambio de turno** (hand-over, briefing, asignación de tareas), **gestión de incidentes HSE** (registro, investigación, cierre, lecciones aprendidas), **gestión de paradas mayores** (planificación, ejecución, retorno a producción), **gestión de visitas** (proveedores, contratistas, visitas oficiales con permisos sectoriales). Estos procesos se ejecutan con planillas, papel y sistemas legacy. La N3 los rediseña, automatiza el flujo y mide el resultado.

**Casos potenciales.**
- Optimización del proceso de cambio de turno (typicamente 60–90 min × 3 turnos × 365 días).
- Optimización del proceso de gestión de incidentes HSE (registro → investigación → acciones correctivas → cierre).
- Optimización del proceso de planificación y ejecución de paradas mayores (typically 7–30 días × 1–4 veces/año).
- Optimización del proceso de gestión de visitas y contratistas con permisos.

**Por qué encaja.** Es el complemento "no-IA" del N3 de AI Workflows. Cuando el cliente quiere primero ordenar el proceso antes de automatizarlo, esta N3 entrega valor sin requerir madurez digital previa. Útil como entry point en cuentas en estado Customer o Early Growth.

**Fuentes.**
- ICMM Health and Safety Performance Indicators. *[icmm.com/en-gb/health-and-safety](https://www.icmm.com/en-gb/health-and-safety)*
- BHP Operating System — case study público de optimización de procesos operacionales mineros. *[bhp.com](https://www.bhp.com)*
- McKinsey "Lean mining" papers — *[mckinsey.com/industries/metals-and-mining/our-insights](https://www.mckinsey.com/industries/metals-and-mining/our-insights)*

---

## Recomendación al squad y a la BU

**Priorización sugerida para construcción formal de N3 (próximos 2 trimestres):**

1. **Monitoreo de Depósitos de Relaves (GISTM)** — el de mayor sponsor ejecutivo + presupuesto + diferencial regulatorio. Si se gana un piloto, abre conversación corporativa con cualquier major.
2. **Reportería ESG y Sustentabilidad** — sponsor CFO/Board, ciclo corto, ROI claro.
3. **Forecast de Consumo de Insumos Críticos** — conversación menos política, dolor cuantificable, ROI rápido.

**Para evaluación posterior:**

4. **Asistente Operacional Minero (RAG)** — depende del estado de adopción de IA generativa en la cuenta.
5. **Optimización Geometalúrgica** — alto valor pero alta exigencia técnica y political clearance; mejor abordarla tras consolidar relación.
6. **Integración IT/OT** — viable como entry-point en cuentas Customer; conviene formalizar partnership OT antes.
7. **BPO HSE y Cambio de Turno** — útil como alternativa "no-IA" para cuentas que aún no aceptan capa IA.

**Acción inmediata para el squad.**
- Llevar este documento al próximo comité de planning trimestral del squad y al review con la BU Data & AI Evolution.
- Priorizar 1–2 de las ideas para construir N3 formal antes de cierre Q3 2026.
- Cada N3 nueva sigue el proceso del Framework de Construcción (sección 4): trigger, insumos, artefacto, criterio mínimo de evidencia.
