---
title: AI Data Extraction para Minería
sidebar_label: AI Data Extraction · Minería
servicio_cross_base: ⚠️ GAP — no existe Cross dedicado en el catálogo actual
vertical: Minería
nivel: N3
version: 0.1 (incipiente · flagged como gap de portfolio)
ultima_actualizacion: 2026-05-11
squad_owner: Squad Vertical Minería · Account Director
bu_lead: Data & AI Evolution
estado_evidencia: Caso propio en industria minera (extracción agéntica de análisis de laboratorio) — N3 incipiente
---

# AI Data Extraction para Minería

**Cross base:** ⚠️ **Gap de portfolio.** En la lista de Cross actual de Data & AI Evolution no existe un Servicio Cross dedicado a "AI Data Extraction". Las capacidades están parcialmente cubiertas dentro de [AI Workflows & Automation](../Servicios%20Cross%20Data/ai-workflows-automation.md) (OCR, LLM/NLP, extracción documental) pero no constituyen un Cross con identidad propia.

**Recomendación al comité de portfolio.** Esta N3 se está documentando como Cross separado siguiendo la decisión del Squad Minería, sobre la base de que el PDF de adaptación lo identificó como offerta diferenciada. Hay dos caminos legítimos: (a) elevar la conversación a la BU para ascender AI Data Extraction como Cross propio (Nivel 2) con el caso minero como evidencia, o (b) tratar esta N3 como aterrizaje minero del Cross AI Workflows con foco específico en el bloque de extracción. Esta card es válida en ambos caminos; el delta es solo la cabecera. Hasta que la BU resuelva, la card se mantiene apuntando al gap.

**Vertical:** Minería | **Versión:** 0.1 | **Última actualización:** 2026-05-11

---

## 1. Caso de uso con nombre propio y dolor de negocio

### Caso principal: **Extracción Inteligente de Datos desde Documentación Operacional y Contractual Minera**

**Dolor de negocio.** Una operación minera produce y consume volúmenes enormes de documentación no estructurada: contratos de proveedores y subcontratistas (la gran minería opera con 1.000–3.000 contratos activos), licitaciones, certificados de análisis de laboratorio, reportes de terreno, bitácoras de turno, planes de tronadura, reportes de geólogo, permisos sectoriales, informes de inspección de equipos críticos. **La información clave está atrapada en formatos no consultables**: PDFs escaneados, planillas heterogéneas con macros, formularios en papel digitalizados, bitácoras manuscritas. Las consecuencias son: (a) decisiones que dependen de un humano leyendo documentos a tiempo y se retrasan o se toman con información parcial; (b) riesgos contractuales ocultos en cláusulas que nadie revisa hasta que aparece la disputa; (c) datos operativos valiosos (resultados de laboratorio, lecturas de terreno) que se reingresan a mano con errores antes de poder alimentar un sistema de decisión.

### Casos de uso adicionales bajo el mismo N3

- **Extracción de contratos de proveedores y subcontratistas** — cláusulas críticas (penalidades, SLAs, indexación de precios, garantías, gatillos de renegociación), exposición agregada por proveedor, riesgos cruzados entre contratos. Crítico para abastecimiento y legal.
- **Digitalización y estructuración de bitácoras de campo, reportes de turno y formularios de inspección** — caso del PDF base del squad.
- **Extracción de reportes geológicos y drillhole logs** — descripciones litológicas, geotécnicas, leyes por intervalo, recuperación, RQD. Hoy se ingresan a mano a los sistemas de modelamiento (Leapfrog, Vulcan, Datamine). (*Idea adicional SME — Fuente: AusIMM "The Mining Engineering Handbook" para taxonomía estándar de drillhole logs, [ausimm.com](https://www.ausimm.com)*)
- **Extracción de certificados de análisis de laboratorio externos** — caso propio Acid (análisis de agua, suelo, foliar con GCP/Gemini). Extensible a certificados de leyes minerales en ensayes externos.
- **Extracción de planes de tronadura y reportes post-tronadura** — datos de cargas, secuencias, resultados de fragmentación, vibraciones registradas — para retroalimentar modelos de optimización de tronadura. (*Idea adicional SME*)
- **Extracción de informes de inspección de equipos críticos** — informes de NDT (Non-Destructive Testing) sobre molinos, estanques de relaves, estructuras de planta — fuente clave para reliability y para reportes regulatorios bajo GISTM. (*Idea adicional SME*)
- **Extracción de planes de cierre y planes de manejo de residuos masivos** — documentación regulatoria extensa que se actualiza periódicamente y debe trazarse contra evidencia operacional. (*Idea adicional SME*)

---

## 2. Para qué cuentas de la vertical aplica y para cuáles no

**Aplica fuerte.**
- Operaciones de gran minería con corpus documental significativo (>500 contratos activos, >10.000 documentos operacionales/año).
- Cuentas con sistemas legacy donde la digitalización del input es vista como cuello de botella reconocido.
- Operaciones que ya están migrando su modelo de datos a una plataforma moderna y necesitan ingestar el histórico documental.
- Cuentas con áreas de Abastecimiento, Legal o Compliance con dolor explícito por gestión contractual.

**No aplica (o aplica más débil).**
- Operaciones donde la documentación ya está bien estructurada en sistemas (caso poco frecuente en minería) — la oportunidad se reduce.
- Cuentas que apenas pueden financiar discovery; este tipo de extracción rinde por volumen y requiere algo de escala para ROI claro.

---

## 3. Qué cambia respecto al Cross base de referencia (AI Workflows & Automation)

| Dimensión | AI Workflows como Cross base | Delta de AI Data Extraction en minería |
|---|---|---|
| **Foco del entregable** | Workflow end-to-end con extracción + decisión + acción | Extracción + estructuración + entrega a sistema downstream (no se hace cargo de la decisión ni acción) |
| **Tipo de input dominante** | Documentos estandarizables | Documentos altamente heterogéneos: planillas con macros antiguas, escaneos de baja calidad, formularios pre-digitales, manuscritos |
| **Output dominante** | Decisión ejecutada, acción tomada | Dataset estructurado, alimentación a sistema de registro (LIMS, SAP, ERP, plataforma geológica) con trazabilidad fin-a-fin |
| **Modelos típicos** | Agentes orquestados | Pipelines OCR + LLM + NLP especializados + validadores domain-specific |
| **Equipo agregado** | Workflow Architect | **Domain Expert minero por tipo de documento** (geólogo para logs, metalurgista para laboratorio, legal minero para contratos). Sin este rol, la extracción se llena de errores que no se detectan |
| **Entregables agregados** | — | Diccionario de datos por tipo documental, mapeo de equivalencias entre nomenclaturas históricas y modernas (las leyes se reportaron como %Cu, ppm Cu, kg Cu/t en distintos períodos), pipeline de QA con muestreo humano |
| **No incluye** | — | Decisión sobre el dato extraído, ingreso a sistemas safety-critical (PLCs), reemplazo de revisión legal humana en contratos críticos |

---

## 5. Resultados esperables verticalizados

**KPI de negocio.**
- Reducción del tiempo de procesamiento documental: **70–90%** vs. baseline manual (consistente con caso propio Acid en laboratorio minero y caso LATAM contratos).
- Reducción del costo unitario de procesamiento por documento: rango habitual USD 0.001–0.01 por documento procesado, según complejidad (referencia: caso Walmart Gemini USD 0.00119 por boleta validada).
- Reducción de errores de ingreso: típicamente del 5–15% manual al <1% automatizado con QA muestral.

**KPI operacional.**
- Cobertura documental: % del corpus migrado a estructura consultable (meta 60%+ del histórico crítico en 12 meses).
- Tiempo de detección de riesgo contractual o anomalía documental: de meses a horas.
- Adherencia de áreas usuarias al sistema de consulta del corpus estructurado.

---

## 6. Operativa típica en esta industria

- **Duración del engagement.** Discovery 3–4 semanas con muestreo del corpus; piloto sobre un tipo documental crítico 2–3 meses; extensión a otros tipos 4–8 meses.
- **Modalidad de contratación.** Híbrida: proyecto cerrado para construcción + pago por documento procesado o por volumen mensual para operación. La parte por volumen es atractiva en minería porque alinea costo con uso real.
- **Sponsor target.** Dependiendo del tipo documental: Gerencia de Abastecimiento (contratos), Gerencia de Geología o Recursos Mineros (logs y reportes), Gerencia de Operaciones (bitácoras y turno), Gerencia de Medio Ambiente (certificados de laboratorio), Legal (contratos críticos).
- **Ciclo de venta.** 2–5 meses — más corto que predictive maintenance, similar a workflows, especialmente cuando el cliente trae ya identificado el tipo documental que duele más.
- **Dedicación esperada del cliente.** Domain Expert por tipo documental 20–30% durante construcción, 5% en operación; QA muestral acordado entre 1% y 5% del volumen para sostener confiabilidad.
- **Logística específica.** Visita a faena necesaria solo si el corpus a digitalizar incluye documentación física en sitio (bitácoras, archivos de geólogo). En caso contrario, trabajo remoto con extracción de muestras representativas.

---

## 7. Posicionamiento competitivo en la vertical

**Vendors activos.**
- **OCR / IDP generalistas** — ABBYY, Kofax (Tungsten), Microsoft Document Intelligence, AWS Textract, Google Document AI. Fortalezas: producto maduro para documentos estándar (facturas, formularios estructurados). Debilidades: pierden precisión con documentos mineros heterogéneos sin un dominio especializado encima.
- **Plataformas IDP con LLM** — Hyperscience, Indico, Rossum. Fortalezas: mejor manejo de variabilidad. Debilidades: no traen taxonomía minera; requieren igual a un integrador con conocimiento del dominio.
- **Plataformas geológicas con módulos de carga** — Seequent Leapfrog Edge / Central, Datamine Discover, Maptek. Fortalezas: integración nativa con el flujo geológico. Debilidades: solo cubren su silo documental.
- **Consultoras de digitalización minera** — locales en Chile y Perú; típicamente pago por hora con software open-source ensamblado a medida.

**Diferenciales de Acid.**
- Caso propio reciente en la vertical (extracción agéntica de laboratorio con GCP/Gemini) — evidencia directa.
- Capacidad de combinar IDP con LLM modernos (no solo OCR clásico) y con orquestación agéntica — pocos competidores hacen los tres bien.
- Modelo de costo por documento procesado disponible — alinea con el patrón financiero minero de OpEx vs. CapEx.

**Objeciones típicas.**
- *"Ya probamos OCR antes y no funcionó."* → La generación previa de OCR es muy distinta de los modelos actuales (LLM multimodales con grounding). La diferencia es de orden de magnitud, no incremental. Demostramos con muestra del corpus del cliente en discovery.
- *"Los documentos críticos requieren revisión humana siempre."* → De acuerdo. El servicio no reemplaza la revisión donde es exigida (legal, regulatoria); la acelera prefiltrando, resumiendo y marcando puntos de atención. La revisión humana se enfoca donde aporta valor, no en leer 200 páginas de boilerplate.
- *"Tenemos clases de documentos muy específicas (drillhole logs, reportes geológicos)."* → Por eso el servicio incorpora Domain Expert minero por tipo documental. Sin ese rol no se entrega calidad; con ese rol, los tipos especializados son donde más valor se libera.

---

## 8. Stack típico de las cuentas de la vertical

**Sistemas destino de datos extraídos.** SAP MM/SD (contratos y abastecimiento), LIMS (LabWare, STARLIMS) para laboratorio, plataformas geológicas (Leapfrog, Vulcan, Datamine, Surpac), Maximo / SAP PM (mantenimiento), Enablon / Cority (EHS).

**Repositorios documentales actuales.** SharePoint, OpenText, Documentum, Box, network shares Windows (extremadamente común), archivos físicos en faena (común para bitácorias y permisos).

**Cloud y servicios IA.** AWS (Textract, Bedrock), GCP (Document AI, Vertex AI con Gemini — caso propio Acid en minería), Azure (Document Intelligence, OpenAI Service).

**Restricciones.** Contratos típicamente bajo NDA estricta; certificados de laboratorio pueden tener restricciones de propietario del análisis; conectividad limitada en faenas remotas obliga frecuentemente a procesamiento en cloud con sync desde sitio.

---

## 9. Evidencias y casos en la vertical

**Caso propio en industria minera (directo y reciente).**
- *Extracción agéntica de análisis de laboratorio (agua, suelo y foliar) con GCP y Gemini* — análisis de estudios en formatos heterogéneos generando datos estructurados y recomendaciones accionables desde fuentes no digitalizadas. Es el caso ancla de esta N3.

**Casos extrapolables fuertes.**
- *LATAM — Gestión de contratos con OCR e IA Generativa, 90% de reducción en tiempo de búsqueda y revisión*: traslación directa al caso de contratos en minería.
- *Clínica Privada — OCR con 78% de precisión en documentos médicos manuscritos*: relevante para bitácoras y formularios manuscritos mineros (precisión piso 78% para corpus duros).
- *Walmart — Validación automática de imágenes con Gemini, USD 0.00119 por boleta*: prueba de costo unitario y operación a escala.

**Referencias públicas.**
- AusIMM Mining Engineering Handbook — referencia de taxonomía documental minera estándar.
- GISTM y guías ICMM para gestión documental de relaves y compliance — disparadores de inversión en extracción documental confiable. *[icmm.com](https://www.icmm.com)* · *[globaltailingsreview.org](https://globaltailingsreview.org)*.
- Reportería ANM (Colombia), SERNAGEOMIN (Chile), MINEM (Perú) — esquemas regulatorios destino para datos extraídos.

**Estado de evidencia.** N3 **incipiente con caso propio anclado en la vertical**. Calificable a calibrada tras dos N4 ejecutadas sobre tipos documentales distintos al ancla.

---

## Anexo: Gap de portfolio y backlog

**Acción para el comité de portfolio.** Evaluar ascenso de "AI Data Extraction" a Cross dedicado con dueño BU, dado que: (a) existe caso propio en minería + caso extrapolable mayor en LATAM, (b) la conversación de cliente es distinta a la de AI Workflows orquestado, (c) el patrón financiero (pago por documento) es diferente al de workflow orquestado. Si el comité confirma el ascenso, esta N3 actualiza su cabecera; si se mantiene como sub-bloque de AI Workflows, esta card se refactoriza como sección dentro de la N3 de AI Workflows.

**Backlog.** Construir catálogo de tipos documentales mineros con muestras anonimizadas para acelerar discovery. Definir precios por documento por tipo. Identificar partners de OCR especializado en logs geológicos si conviene OEM.
