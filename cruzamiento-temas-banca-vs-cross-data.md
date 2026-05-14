---
title: Cruzamiento de Ejes Estratégicos Banca Chile × Servicios Cross Data & AI
estado: borrador inicial para discusión con squad Banca + BU Data & AI Evolution
ultima_actualizacion: 2026-05-14
owner: Account Director Squad Banca
contexto_input: Frame estratégico del squad Banca Chile (Open Finance, Core legacy, Neobancos, IA & personalización, Regulación CMF, Stack propietario)
---

# Cruzamiento · 6 ejes estratégicos Banca × 11 Servicios Cross Data & AI

Cruce de los 6 ejes estratégicos del frame del squad Banca (Chile) contra los 11 Servicios Cross actuales de la BU Data & AI Evolution. **Objetivo:** identificar dónde la oferta Data & AI tiene fit directo, fit habilitador y dónde el tema vive principalmente en otra BU (engineering, product, cyber).

---

## Resumen visual: matriz de fit

| Cross Data \ Eje Banca | Open Finance | Core legacy | Neobancos | IA & Pers. | Reg. CMF | Stack prop. |
|---|---|---|---|---|---|---|
| **Data & MLOps** | ▲ habilitador | — | ▲ habilitador | ●●● fit directo | ●● fit fuerte | ●● fit fuerte |
| **Recommendation Model as Product** | — | — | ●●● fit directo | ●●● fit directo | — | ▲ habilitador |
| **AI Workflows & Automation** | ▲ habilitador | — | ●● fit fuerte | ●●● fit directo | ●●● fit directo | — |
| **AI Agents & RAGs empresariales** | — | — | ●● fit fuerte | ●●● fit directo | ●● fit fuerte | — |
| **Data as Product** | ●●● fit directo | ●● fit fuerte | ▲ habilitador | ●● fit fuerte | ●●● fit directo | ●● fit fuerte |
| **Data Integration Services** | ●●● fit directo | ●●● fit directo | ▲ habilitador | ▲ habilitador | ●● fit fuerte | ●●● fit directo |
| **Data Analytics & Monitoring** | ●● fit fuerte | ▲ habilitador | ▲ habilitador | ●● fit fuerte | ●●● fit directo | ▲ habilitador |
| **Data Reporting** | ▲ habilitador | — | — | — | ●●● fit directo | — |
| **Data Exploration & Insights** | — | — | ●● fit fuerte | ●● fit fuerte | ▲ habilitador | — |
| **Forecast & Demand Planning** | — | — | ●● fit fuerte | ●● fit fuerte | — | — |
| **Business Process Optimization** | — | ▲ habilitador | ●● fit fuerte | ▲ habilitador | ●● fit fuerte | — |

**Leyenda.** ●●● fit directo (N3 prioritario, conversación natural) · ●● fit fuerte (caso de uso claro, sponsor identificable) · ▲ habilitador (no es lead pero es prerequisito de otros casos) · — sin fit relevante.

---

## 1. Eje: Open Finance (Ley Fintech)

**Contexto.** APIs y datos compartidos bajo CMF. Demanda estructural de arquitectura API-first. BCI y BdCh en posición ideal (referencia del frame).

**Lectura desde Data & AI.** Open Finance es estructuralmente un problema de **datos como producto + integración API-first**. La conversación con el banco arranca por cómo expone sus datos al ecosistema (TPPs, agregadores, autoridades CMF) y cómo consume datos de otros emisores. Acid llega con dos Cross core y varios habilitadores.

**Cross con fit directo.**
- **Data as Product** — el activo central de Open Finance es un catálogo de productos de datos con contratos, ownership y SLA. Sin esto, los APIs son frágiles y la conversación con CMF es difícil. Casos: catálogo de productos de cuentas/transacciones/inversiones; gobernanza Dataplex/Collibra; trazabilidad de consumo TPP.
- **Data Integration Services** — la mecánica de exponer y consumir vía API requiere pipelines confiables, integración entre core legacy + capa moderna + APIs externos. Casos: orquestación de extracción desde core hacia capa de productos de datos; integración con sandboxes regulatorios CMF.

**Cross habilitadores.**
- **Data & MLOps** — para servir modelos productivos vía API (scoring, antifraude) con SLA exigido por consumo TPP.
- **AI Workflows & Automation** — automatización de procesos de onboarding TPP, gestión de consentimientos, revocaciones.
- **Data Analytics & Monitoring** — observability de APIs Open Finance, alertas de uso anómalo, KPIs de consumo.

**Hipótesis de N3 prioritaria.**
> *"Plataforma de Productos de Datos para Open Finance"* — caso fuerte con BCI y BdCh, sponsor CDO + Gerencia Open Finance, dolor regulatorio + competitivo (no estar listo ante CMF y ante TPPs).

---

## 2. Eje: Core bancario legacy

**Contexto.** Cores de los 90 (Bantotal, Cobis, Altamira, IBM TCS BaNCS variants). Modernización lenta y costosa. Estrategia: strangler pattern + microservicios.

**Lectura desde Data & AI.** Este eje vive **principalmente fuera de Data & AI**. Es un tema de modernización de aplicaciones, microservicios, devops, cloud foundation — la BU lead natural es Engineering / App Modernization. La superficie para Data & AI es periférica pero importante.

**Cross con fit directo.** Ninguno en lead. La conversación Data & AI no se gana acá.

**Cross con fit fuerte (rol periférico).**
- **Data Integration Services** — durante el strangler, mantener un puente de datos entre core legacy y los microservicios nuevos es crítico. Sin ese puente, los microservicios se construyen sin datos consistentes. Caso: pipelines CDC desde el core hacia data lake mientras se sustituyen funcionalidades.
- **Data as Product** — productos de datos transitorios que abstraen el core para que el resto del banco no dependa de su modelo de datos legacy.

**Cross habilitadores.**
- **Business Process Optimization** — entender cuáles procesos quedan obsoletos con la modernización y cuáles requieren rediseño antes de sustituir.
- **Data Analytics & Monitoring** — observability durante la transición.

**Hipótesis de N3.** Acid no debería liderar este eje desde Data & AI. La oportunidad es **acompañar** un programa de modernización liderado por engineering/product con productos de datos transitorios.

---

## 3. Eje: Presión de neobancos

**Contexto.** Tenpo, MACH, Mercado Pago, Nubank crecen fuerte. Estrategia banco tradicional: product engineering + UX ágil para reducir gap de experiencia.

**Lectura desde Data & AI.** Aunque el lead es product/UX, los neobancos compiten en gran medida con **personalización en tiempo real, hipersegmentación, asistentes conversacionales y antifraude veloz** — todas capacidades de Data & AI. Acid puede entrar acá como diferenciador de la propuesta del squad de Banca.

**Cross con fit directo.**
- **Recommendation Model as Product** — el delta de experiencia de un Tenpo o Nubank vs. un banco tradicional incluye recomendación de productos personalizados, ofertas contextualizadas, next-best-action. Acid tiene caso comparable fuerte (Koandina + Cencosud) trasladable a recomendación financiera (productos bancarios, segmentos de campaña).
- **AI Workflows & Automation** — workflows de onboarding ágil (cuenta abierta en <5min como en neobancos), automatización de KYC, asistentes que reducen carga de call center.

**Cross con fit fuerte.**
- **AI Agents & RAGs empresariales** — asistente conversacional para clientes (estilo Nubank Bia), o para empleados de sucursal/contact center (RAG sobre productos y procedimientos). Caso comparable directo: LATAM agentes conversacionales con +90% precisión, Cencosud agentes WhatsApp.
- **Data Exploration & Insights** — análisis de comportamiento de cliente para identificar gaps de experiencia frente a neobancos.
- **Forecast & Demand Planning** — forecast de churn, de adquisición, de cross-sell.
- **Business Process Optimization** — rediseño de procesos de onboarding, atención y autoservicio que hoy demoran días vs. minutos.

**Hipótesis de N3 prioritaria.**
> *"Motor de Personalización y Next-Best-Action para el Cliente Bancario"* — Sponsor: Gerencia de Productos Retail + CDO. Dolor competitivo claro (churn hacia neobancos), KPI: conversión, ARPU, NPS.

---

## 4. Eje: IA y personalización (modelos de riesgo, fraude, asistentes conversacionales)

**Contexto.** Modelos de riesgo, fraude, asistentes conversacionales. Habilitación: staffing AI/ML + Salesforce + Databricks.

**Lectura desde Data & AI.** **El eje natural y prioritario para la BU Data & AI Evolution en Banca.** Aquí lidera la BU, no acompaña. La concentración de fits directos es la más alta de los 6 ejes.

**Cross con fit directo.**
- **Data & MLOps** — el corazón: productivizar modelos de riesgo crediticio, fraude, scoring, propensión, todo lo que hoy vive en notebooks o en motores legacy. Caso comparable: Koandina API 99.9% disponibilidad regional.
- **Recommendation Model as Product** — recomendación de productos financieros, hipersegmentación de campañas (caso comparable Cencosud directo).
- **AI Workflows & Automation** — workflows de IA generativa para back office (gestión de reclamos, análisis de contratos hipotecarios, KYC documental). Caso comparable LATAM: 90% reducción en tiempo de gestión de contratos.
- **AI Agents & RAGs empresariales** — asistentes conversacionales para clientes (CX) y para empleados (productividad). Caso comparable LATAM: ecosistema de agentes con +60% adherencia en usuarios expertos.

**Cross con fit fuerte.**
- **Data Exploration & Insights** — descubrimiento de patrones de fraude, segmentación avanzada de cartera, análisis de profitability por cliente.
- **Data Analytics & Monitoring** — monitoreo de modelos en producción (drift, bias, performance) — cada vez más exigido por reguladores.
- **Forecast & Demand Planning** — forecast de riesgo agregado, forecast de demanda de crédito, forecast de pre-pagos hipotecarios.
- **Data as Product** — base de feature store que alimenta todos los modelos con disciplina.

**Cross habilitadores.**
- **Data Integration Services** — sin pipelines confiables hacia Databricks/Salesforce, ningún modelo es productivo.
- **Business Process Optimization** — rediseño del proceso post-modelo (el modelo predice, alguien tiene que actuar).

**Hipótesis de N3 prioritarias.** Este eje justifica probablemente **3 o 4 N3 distintos**:
> *"Plataforma de Modelos de Riesgo y Fraude Productivos"* (Data & MLOps)
> *"Asistente Conversacional Bancario CX y Empleado"* (AI Agents + AI Workflows)
> *"Motor de Personalización y Campañas"* (Recommendation Model)
> *"Feature Store y Productos de Datos para IA"* (Data as Product)

---

## 5. Eje: Regulación CMF (NCG 454, Ley 19.628, continuidad operacional)

**Contexto.** NCG 454 (gestión de continuidad operacional y seguridad de la información), Ley 19.628 (protección de datos personales), continuidad operacional. Habilitación: QA, cybersecurity, compliance técnico.

**Lectura desde Data & AI.** Eje **estructural y vinculante** — todo banco debe cumplir, todo modelo y producto de datos vive bajo este marco. Acid llega con varios Cross con fit directo: trazabilidad, monitoreo, automatización de reportería, gobernanza.

**Cross con fit directo.**
- **Data as Product** — el marco de NCG 454 y Ley 19.628 exige ownership, contratos, trazabilidad y controles de acceso por dominio — exactamente lo que produce este Cross. Casos: catálogo de datos con clasificación de sensibilidad PII, ownership por dominio, lineage end-to-end. Caso comparable directo: Koandina Data Lake seguro con 40+ roles y políticas en Lake Formation.
- **AI Workflows & Automation** — automatización de reportería periódica a CMF (NCG 454 reporting, declaraciones operacionales, incidentes de continuidad), gestión de derechos ARCO bajo Ley 19.628 (acceso, rectificación, cancelación, oposición). Caso comparable: LATAM contratos.
- **Data Reporting** — dashboard regulatorio y reportería ad-hoc para CMF y para directorio.
- **Data Analytics & Monitoring** — monitoreo de continuidad operacional, observability de pipelines críticos, alertas tempranas de incidentes.

**Cross con fit fuerte.**
- **Data & MLOps** — governance de modelos para auditoría regulatoria (CMF está acercándose a modelos en producción como objeto de regulación bajo enfoque de "AI act" o equivalente). Lineage, versionado, registro de decisiones.
- **AI Agents & RAGs empresariales** — RAG sobre marco regulatorio para áreas de compliance.
- **Data Integration Services** — pipelines para reportería regulatoria masiva (volúmenes para CMF son altos y plazos exigentes).
- **Business Process Optimization** — rediseño de procesos de continuidad operacional y gestión de incidentes.

**Hipótesis de N3 prioritaria.**
> *"Gobierno de Datos y Cumplimiento NCG 454 + Ley 19.628"* — Sponsor: CDO + Compliance + CISO. Dolor regulatorio claro y vinculante. ROI: evitar sanciones + acelerar respuesta ante requerimientos CMF.

---

## 6. Eje: Stack propietario (Salesforce, Databricks, Azure BCI, AWS BdCh)

**Contexto.** Stack heterogéneo por banco. BCI ancla en Azure + Databricks + Salesforce. BdCh en AWS + Databricks + Salesforce. Certificación = ventaja competitiva.

**Lectura desde Data & AI.** Eje **de habilitación de delivery**, no de N3 propio. Determina cuáles competencias técnicas necesitamos certificar y cuáles partnerships traer. Pero **se monetiza indirectamente**: cada Cross se aterriza con stack del cliente, y la capacidad de hacerlo bien es diferencial.

**Cross con fit directo.**
- **Data Integration Services** — integración multi-cloud (Azure ↔ AWS ↔ GCP) y con Salesforce. Es el Cross que más se beneficia de certificación en los stacks propietarios.

**Cross con fit fuerte.**
- **Data & MLOps** — modelos en Databricks (común a BCI y BdCh) y servidos vía Azure o AWS. Capacidad Databricks es delta competitivo claro.
- **Data as Product** — productos de datos sobre Databricks lakehouse, con integración a Salesforce como sistema de consumo (CRM).

**Cross habilitadores.**
- **Recommendation Model** y **AI Agents** se montan sobre Databricks + el cloud preferido del banco.

**Acción transversal.**
- Confirmar certificaciones del squad: Databricks (Lakehouse Specialty), Salesforce (Data Cloud, Sales Cloud), Azure (Data Engineer, Solutions Architect), AWS (Data Analytics, ML Specialty).
- Definir partnerships formales con Databricks Chile y Salesforce Chile.
- Cualquier N3 de los otros 5 ejes debe documentar cómo se aterriza sobre Azure (BCI) y AWS (BdCh) — variante por stack.

---

## Recomendación al squad Banca

**Priorización sugerida de construcción de N3 (próximos 2 trimestres):**

**Ola 1 (próximos 90 días) — 2 N3 sobre los ejes de mayor fit y menor fricción.**
1. **N3 sobre IA & Personalización con foco en Asistente Conversacional Bancario** — capitaliza casos comparables LATAM (+90% precisión, +60% adherencia, 90% reducción contratos), sponsor CX claro, dolor competitivo (neobancos), ROI medible. Apunta a un primer N4 en BCI o BdCh.
2. **N3 sobre Open Finance con foco en Productos de Datos** — viento regulatorio + de competencia, sponsor CDO con mandato, diferencial Acid (Data as Product caso Koandina sólido).

**Ola 2 (90–180 días) — 2 N3 sobre los ejes con mayor masa crítica de oportunidad.**
3. **N3 sobre Gobierno de Datos NCG 454 + Ley 19.628** — apoyando el cumplimiento estructural, sponsor vinculante. Combina Data as Product + Data Reporting + AI Workflows.
4. **N3 sobre Modelos de Riesgo y Fraude Productivos** — el caso de uso más grande en volumen para Banca, pero exige feature store maduro y conversación de mayor profundidad técnica. Construcción más lenta pero high-stakes.

**Ola 3 / fuera de scope inmediato.**
- *Core bancario legacy.* No liderar desde Data & AI. Acompañar como complemento.
- *Stack propietario.* Tratar como acción transversal (certificaciones + partnerships), no como N3.

---

## Próximos pasos

1. **Validar el cruzamiento** con el AD del squad Banca, BU lead Data & AI Evolution, y squad de Engineering (para los temas de core legacy y stack propietario).
2. **Identificar primera cuenta foco** entre BCI, BdCh, Itaú, Santander, Scotiabank, Banco Estado y Falabella Financiero para anclar la primera N4.
3. **Producir las dos N3 de Ola 1** siguiendo el proceso del Framework de Construcción (sección 4): card de 9 bloques, casos comparables, criterio mínimo de evidencia.
4. **Confirmar certificaciones críticas** del squad (Databricks, Salesforce, Azure, AWS) y partnerships antes del kickoff de N4.
