---
title: Data & MLOps para Minería
sidebar_label: Data & MLOps · Minería
servicio_cross_base: Data & MLOps
vertical: Minería
nivel: N3
version: 0.1 (incipiente)
ultima_actualizacion: 2026-05-11
squad_owner: Squad Vertical Minería · Account Director
bu_lead: Data & AI Evolution
estado_evidencia: Caso extrapolable desde Aerolíneas (LATAM) y Retail (Walmart) + caso propio en industria minera (extracción agéntica de análisis de laboratorio) — N3 incipiente
---

# Data & MLOps para Minería

**Cross base:** [Data & MLOps](../Servicios%20Cross%20Data/data-ml-ops.md) | **Vertical:** Minería | **Versión:** 0.1 | **Última actualización:** 2026-05-11

> Esta card no repite el Cross base. Documenta el *delta* específico para cuentas de la vertical minera. Para el alcance genérico, ver la card del Cross.

---

## 1. Caso de uso con nombre propio y dolor de negocio

### Caso principal: **Vista 360° Mina-Planta y Monitoreo Predictivo de Activos Críticos**

**Dolor de negocio.** En una operación minera integrada (mina, chancado, molienda, flotación, filtrado, despacho) los datos viven en silos verticales: el FMS (Fleet Management System) de mina no conversa con el DCS/SCADA de planta; el CMMS de mantenimiento no conversa con el historian de proceso; el sistema de laboratorio no conversa con planificación. La consecuencia financiera es directa: cuando un molino SAG sale de operación no programada, la pérdida de throughput por hora se mide en miles de toneladas y, según la ley y precio del commodity, en cientos de miles a millones de dólares por día. El dolor no es "no tenemos dashboards" — es que **el plan de producción se cumple por debajo de lo posible y nadie puede atribuir con precisión cuánto de la brecha proviene de mina, cuánto de planta y cuánto de la interfase entre ambas**. La conversación con el cliente arranca acá: cuánta tonelada deja de moverse por mes por falta de visibilidad operacional unificada.

### Casos de uso adicionales bajo el mismo N3

- **Pipelines productivos para monitoreo predictivo de activos críticos** — correas overland, molinos SAG/bolas, chancadores primarios, palas eléctricas, camiones de extracción. Inputs: vibración, temperatura, corriente, presión hidráulica, telemetría OEM. KPI: MTBF, downtime no programado, costo de mantenimiento por tonelada movida.
- **Telemetría energética y de consumo de agua productivizada** — consumo kWh/tonelada por área, m³/tonelada de agua fresca vs. recirculada. Hoy es input de reportes ESG mensuales con latencia de semanas; se productiviza como modelo de consumo con alertas operacionales. (*Idea adicional SME — Fuente: ICMM Water Stewardship Framework, [icmm.com/en-gb/environmental-stewardship/water](https://www.icmm.com/en-gb/environmental-stewardship/water-stewardship)*)
- **Short-Interval Control productivizado** — pipelines que llevan datos de mina y planta a tableros de turno con resolución horaria, no diaria, para que el dispatcher y el jefe de turno cierren brechas plan-real dentro del turno. (*Idea adicional SME — Fuente: McKinsey, "The next-generation mining operating model", [mckinsey.com/industries/metals-and-mining/our-insights](https://www.mckinsey.com/industries/metals-and-mining/our-insights)*)
- **Pipelines de calidad de mineral mina-planta** — leyes ROM declaradas vs. leyes reales en alimentación a planta, con cierre de balance por turno. (*Idea adicional SME*)

---

## 2. Para qué cuentas de la vertical aplica y para cuáles no

**Aplica fuerte.**
- Operaciones de gran minería del cobre, oro y litio en Chile, Perú y Norte de Argentina, con producción anual relevante para el grupo y plan de producción exigente (P80 o superior dentro de su portafolio).
- Operaciones integradas mina-planta con planta concentradora propia (no toll milling puro).
- Cuentas en estado de madurez Growth o Mature dentro del squad: ya tienen iniciativas digitales previas y un CDO o Gerencia de Transformación Digital instalada.
- Operaciones con activos críticos en clase 1A/1B de criticidad (SAG, bolas, chancadores primarios, correas overland) donde un evento de downtime supera US$100K/día de impacto.

**No aplica (o aplica más débil).**
- Faenas de mediana y pequeña minería sin DCS/historian instalado: el insumo de datos no existe y este N3 sin esa base se vuelve un proyecto de instrumentación, no de Data & MLOps.
- Operaciones puramente de exploración o en cierre, sin plan de producción activo.
- Faenas con OT/IT segmentado por contratos de servicios con OEM (Caterpillar, Komatsu, ABB, Metso) que bloquean acceso a la telemetría — viable solo si la cuenta tiene apetito para renegociar contratos de datos con el OEM.

---

## 3. Qué cambia respecto al Cross base

| Dimensión | Cross base | Delta minería |
|---|---|---|
| **Fuentes de datos** | Bases transaccionales, eventos digitales | OT (historians PI, Aspen IP21), SCADA, FMS (Modular DISPATCH, Wenco, Caterpillar MineStar Fleet), CMMS (SAP PM, Maximo), LIMS de laboratorio, telemetría OEM (Cat Vital, Komtrax) |
| **Latencia objetivo** | Batch diario o near real time | Tiempo real estricto (segundos) para activos críticos; horario para Short-Interval Control |
| **Seguridad** | Estándar cloud | Segregación IT/OT con DMZ industrial, cumplimiento IEC 62443, controles de no afectar disponibilidad de planta |
| **Edge computing** | Opcional | Habitual — conectividad satelital o fibra limitada en faenas remotas obliga a procesamiento en mina |
| **Modelos típicos** | Forecasting, scoring, recomendadores | Detección de anomalías en señales vibroacústicas, modelos de degradación, RUL (Remaining Useful Life) |
| **Equipo agregado** | — | Reliability Engineer (cliente), Domain Expert minero (Acid), Geometalurgista cuando se involucra leyes |
| **Entregables agregados** | — | Mapeo IT/OT, plan de transición OPC-UA, gateway de datos OT→cloud, runbook de degradación grácil ante pérdida de conectividad |
| **No incluye** | — | Instrumentación nueva, integración con sistemas safety-critical (PLCs de paradas de emergencia), ciberseguridad OT en profundidad |

---

## 5. Resultados esperables verticalizados

**KPI de negocio.**
- Reducción de downtime no programado en activos críticos: **15–30%** sobre baseline en 12 meses (benchmark: BHP Operating System, Rio Tinto Mine of the Future, casos públicos GMG Group). *Fuente: Global Mining Guidelines Group, [gmggroup.org](https://gmggroup.org/guidelines)*.
- Aumento de OEE de planta concentradora: **2–5 puntos porcentuales** absolutos (benchmark típico industria gran minería del cobre: OEE 70–82% según operación).
- Reducción de costo de mantenimiento por tonelada movida: **5–12%**, principalmente vía conversión de correctivo a planificado.

**KPI operacional.**
- Cierre de brecha plan-real de producción por turno con resolución horaria.
- Tiempo medio de detección (MTTD) de degradación en activo crítico: de días/semanas a horas.
- Cobertura de activos críticos bajo monitoreo predictivo: meta 80%+ de clase 1A/1B en 12 meses.

**Caveat de honestidad.** Para que estos números se sostengan, el cliente necesita: (a) historian instalado y operativo, (b) instrumentación mínima en los activos críticos, (c) un Reliability Engineer del lado del cliente que cierre el ciclo entre alerta y intervención. Sin (c), el modelo predice y nadie actúa: la N3 sigue siendo vendible pero el valor no se realiza.

---

## 6. Operativa típica en esta industria

- **Duración del engagement.** Discovery 4–6 semanas; piloto sobre un activo crítico 3–4 meses; escalamiento a fleet de activos 6–12 meses adicionales. Total fase 1–2: 9–14 meses.
- **Modalidad de contratación.** Proyecto cerrado por fase + retainer mensual de DataOps/MLOps post go-live. Muy común el split CapEx (proyecto) + OpEx (operación) para encajar en la planificación financiera minera.
- **Sponsor target.** CDO, Gerencia de Transformación Digital, Gerencia de Mantenimiento (Reliability) o Gerencia de Operaciones. En Chile y Perú aparece frecuentemente la VP de Operaciones como sponsor cuando el caso es de planta concentradora.
- **Ciclo de venta.** 4–9 meses desde primer contacto a kickoff. La gran minería tiene comités de inversión trimestrales y procesos de gestión del cambio en sitio que no se aceleran con discount.
- **Dedicación esperada del cliente.** Reliability Engineer 30–50% durante piloto; Domain Expert de proceso 20%; Plataforma/IT 15–20% para integraciones; sponsor ejecutivo 2h/semana en steerco mensual.
- **Logística específica.** Visitas a faena obligatorias en discovery (no se entiende el problema desde Santiago/Lima); inducción HSE para Acidians que visitan sitio (mínimo medio día por faena); coordinación con la ventana de mantención mayor del cliente para releases productivos críticos.

---

## 7. Posicionamiento competitivo en la vertical

**Vendors activos en la vertical.**
- **OEM tech stacks** — Caterpillar Cat MineStar Health, Komatsu Modular Mining DataMine, Hitachi Wenco — bundled con flota. Fortalezas: integración nativa con telemetría OEM. Debilidades: silos por marca de flota, lock-in de datos, no resuelven planta.
- **Consultoras globales tier 1** — McKinsey QuantumBlack, Accenture Industry X, Deloitte Digital. Fortalezas: gravitas ejecutiva, frameworks. Debilidades: precio (3–5x), dependencia de subcontratistas para delivery técnico.
- **Especialistas mineros tecnológicos** — Hexagon Mining (Mining HxGN), Seeq (analytics OT), Cognite (DataOps industrial), AspenTech (Mtell predictive). Fortalezas: producto vertical. Debilidades: licenciamiento alto y modelo product-led que requiere igual a un integrador.
- **System integrators OT regionales** — Arcadis, Bechtel, JRI, Sigdo Koppers. Fortalezas: cercanía a la faena. Debilidades: predominio mecánico/eléctrico, no Data & MLOps maduro.

**Diferenciales de Acid en minería.**
- Cloud-native con experiencia probada en pipelines en producción que sostienen SLA en operación 24x7 (caso LATAM despacho NRT, caso Walmart plataforma operacional).
- Lenguaje de producto y MLOps de origen — no es retrofit desde consultoría tradicional ni desde mecanizado OT.
- Capacidad de combinar IT (cloud, data eng, ML) con orquestación de la interfase IT/OT mediante partnerships con integradores locales, sin pretender ser SI eléctrico.

**Objeciones típicas y respuestas.**
- *"Ya tenemos contrato con Cat MineStar / Wenco para flota."* → No competimos con el FMS, lo integramos. El delta es la vista unificada mina-planta y los modelos que el FMS no provee. Caso comparable: LATAM repositorio centralizado con datos de proveedores externos.
- *"Nosotros tenemos un equipo interno de data science minero."* → Bien, el N3 acelera *productivizar* lo que ya hacen. Lo común no es ausencia de modelos sino modelos que viven en notebooks y no en producción.
- *"Esto requiere acceso a OT que IT no nos va a dar."* → Conversación de gobernanza temprana, con arquitectura DMZ que no compromete safety. Si la cuenta no resuelve el gating IT/OT, este N3 no arranca y conviene saberlo en discovery.

---

## 8. Stack típico de las cuentas de la vertical

**Capas OT.** Historians: OSIsoft PI System (dominante), Aspen IP21, GE Proficy. SCADA/DCS: ABB Ability, Emerson DeltaV, Honeywell Experion, Siemens PCS7. PLCs: Allen-Bradley, Siemens S7. Protocolos: OPC-UA (objetivo), Modbus, DNP3.

**FMS / dispatch.** Modular DISPATCH (Hitachi), Wenco (Hitachi), Caterpillar MineStar Fleet, Hexagon HxGN MineOperate.

**CMMS y ERP.** SAP S/4HANA (mayoritario en gran minería), IBM Maximo, Infor EAM.

**LIMS.** LabWare LIMS, STARLIMS, Sample Manager.

**Cloud preferida.** AWS (predominante en Codelco, Antofagasta Minerals, BHP), Azure (creciente en Newmont, Anglo American), GCP (puntual). Patrón híbrido es la norma: workloads de modelo en cloud, edge en faena.

**Restricciones regulatorias y de sitio.**
- Chile: SERNAGEOMIN para seguridad minera; Ley 21.000 SEC para energía; estándares de operación de relaves bajo GISTM y Ley 21.420.
- Perú: OSINERGMIN para seguridad; estándares MINEM.
- Conectividad: enlaces satelitales o fibra de capacidad limitada en faenas remotas obligan a edge.
- Ciberseguridad OT: cumplimiento IEC 62443 cuando aplica, segregación estricta IT/OT, cero impacto a disponibilidad de planta.

---

## 9. Evidencias y casos en la vertical

**Caso propio en industria minera (extrapolable parcial).**
- *Extracción agéntica de análisis de laboratorio (agua, suelo y foliar) con GCP y Gemini* — referenciado en la card del Cross AI Workflows. Demuestra capacidad de operar con datos de laboratorio y formatos heterogéneos en una operación minera, aunque el alcance específico no es predictivo de activos. Sirve como prueba de acceso al sitio y cumplimiento HSE de un Acidian en faena minera.

**Casos extrapolables desde otras verticales.**
- *LATAM — Repositorio centralizado de datos de despacho en tiempo real* (Aerolíneas): la lógica de unificar datos operacionales con disponibilidad NRT para tomar decisiones de turno es el patrón directamente transferible a "Vista 360° mina-planta". Lo que cambia es la fuente (OT historians vs. sistemas de vuelo), no el patrón.
- *Walmart — Plataforma de datos operacional* (Retail): DataOps con ownership estricto, estándares y ~95% de reducción en errores de carga. Patrón aplicable a la disciplina de Data & MLOps en una operación 24x7.

**Casos públicos de referencia en la industria.**
- BHP Operating System / Operations Services — caso público de transformación operacional basada en datos. *Fuente: [bhp.com/news/case-studies](https://www.bhp.com/news/case-studies)*.
- Codelco Distrito Norte transformación digital — caso público regional. *Fuente: [codelco.com/transformacion-digital](https://www.codelco.com)*.
- Rio Tinto Mine of the Future / autonomous mining — referencia global. *Fuente: [riotinto.com/about/innovation](https://www.riotinto.com/en/about/innovation)*.

**Estado de evidencia.** N3 **incipiente** según el criterio del framework (sección 4.1). El caso propio en la vertical existe pero no es del mismo alcance; los casos extrapolables son sólidos en el patrón pero requieren validación de traducción con el cliente. La primera N4 sobre esta N3 será la que califique para promoverla a N3 calibrada.

---

## Anexo: Owner del documento y backlog de calibración

- **Owner del documento.** Account Director del Squad Minería.
- **BU lead del Cross.** Data & AI Evolution.
- **Próxima revisión.** Tras la primera N4 ejecutada sobre esta N3, o a los 90 días — lo que ocurra primero.
- **Backlog de calibración.**
  - Validar con BU mapeo final de "Data & AI Ops" (PDF) ↔ Cross "Data & MLOps" o si justifica un Cross combinado nuevo.
  - Completar bloque 9 con benchmarks específicos de gran minería del cobre Chile cuando ejecutemos primera N4.
  - Levantar referencias de partnerships locales con SI OT (JRI, Sigdo Koppers, BBosch) para arquitectura IT/OT.
