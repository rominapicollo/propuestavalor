---
title: Recommendation Model as Product para Minería
sidebar_label: Recommendation Model · Minería
servicio_cross_base: Recommendation Model as Product
vertical: Minería
nivel: N3
version: 0.1 (incipiente)
ultima_actualizacion: 2026-05-11
squad_owner: Squad Vertical Minería · Account Director
bu_lead: Data & AI Evolution
estado_evidencia: Sin caso propio en industria minera. Casos extrapolables fuertes desde Koandina (Logística) y Cencosud (Retail) — N3 incipiente con extrapolación que requiere validación de traducción explícita
---

# Recommendation Model as Product para Minería

**Cross base:** [Recommendation Model as Product](../Servicios%20Cross%20Data/recommendation-model-as-product.md) | **Vertical:** Minería | **Versión:** 0.1 | **Última actualización:** 2026-05-11

> ⚠️ Esta N3 se apoya en casos extrapolables desde verticales no mineras. La conversación con el cliente exige hacer explícita la extrapolación (qué patrón se sostiene, qué cambia) — caja directa del bloque 9.

---

## 1. Caso de uso con nombre propio y dolor de negocio

### Caso principal: **Sistema de Recomendación de Planes de Mantenimiento y Rutas de Acarreo**

**Dolor de negocio.** En una operación minera de gran escala, dos universos de decisiones operacionales se toman miles de veces al mes contra heurísticas estables pero subóptimas: (1) **planes de mantenimiento** de la flota de equipos críticos —camiones de extracción, palas, perforadoras, equipos auxiliares— se diseñan típicamente desde calendarios OEM-driven y experiencia del Reliability Engineer; las intervenciones suelen ser conservadoras o reactivas, dejando MTBF y costo de mantenimiento por tonelada por debajo del potencial; (2) **rutas de acarreo dentro de la mina** se asignan por el dispatcher en función de visibilidad inmediata, sin un sistema que recomende combinaciones óptimas pala-camión-stockpile considerando estado del terreno, condiciones climáticas, ciclo histórico y restricciones operativas. El dolor financiero: cada punto porcentual de mejora en disponibilidad de flota o en toneladas movidas por hora se traduce en millones de dólares anuales para una operación de >50.000 t/día. El dolor cultural es más profundo: hay decisiones que la organización ya identificó como subóptimas pero que sigue tomando "como siempre" porque no hay sistema que ofrezca alternativa accionable en tiempo y forma.

### Casos de uso adicionales bajo el mismo N3

- **Recomendación de planes de mantenimiento** (caso PDF) — recomendaciones basadas en patrones de fallas históricas, sensores y telemetría OEM, optimizando ventanas de mantención para minimizar impacto en producción.
- **Recomendación de rutas de acarreo** (caso PDF) — recomendación dinámica de asignación pala-camión-destino según condiciones del terreno, clima, ciclo histórico.
- **Recomendación de setpoints de planta concentradora** — recomendación de setpoints de molienda (velocidad SAG, agregado de bolas, densidad de pulpa) y flotación (pH, dosis de reactivos, profundidad de espuma) que optimizan recuperación o throughput dados los inputs de calidad de mineral de las próximas horas. Es un sistema operacional que no reemplaza al metalurgista sino que le ofrece la próxima jugada. (*Idea adicional SME — Fuente: GMG Group "Industrial AI in Mining", [gmggroup.org](https://gmggroup.org/guidelines/)*)
- **Recomendación de blending de mineral** — recomendación de mezcla de stockpiles para alimentar a planta con calidad estable que maximice recuperación. Hoy lo hace el planificador con planilla y experiencia. (*Idea adicional SME — Fuente: AusIMM "Spence ore blending case", literatura pública sobre optimización de blending en cobre, [ausimm.com](https://www.ausimm.com)*)
- **Recomendación de configuración de tronadura** — diseño de carga, secuencia, patrón de perforación que minimice fragmentación gruesa para alimentar mejor al chancador. Producto: motor que asigna recomendación al ingeniero de perforación y tronadura. (*Idea adicional SME*)
- **Recomendación de adquisición de insumos críticos** — bolas de molienda, reactivos de flotación, lubricantes, neumáticos OTR — sistema que recomienda momento y volumen de compra dado consumo histórico, lead time y proyección de operación. (*Idea adicional SME*)
- **Recomendación de despliegue de cuadrillas en mantenimiento** — asignación óptima de cuadrillas a trabajos pendientes considerando prioridad, skill, disponibilidad de repuestos. (*Idea adicional SME*)

---

## 2. Para qué cuentas de la vertical aplica y para cuáles no

**Aplica fuerte.**
- Operaciones con flota grande (50+ camiones de extracción mayores, 10+ palas) donde las decisiones de asignación se toman a alta frecuencia y el dispatcher tiene espacio para usar recomendaciones.
- Plantas concentradoras con instrumentación moderna en planta de molienda y flotación.
- Cuentas con Reliability Engineer instalado y CMMS productivo (Maximo o SAP PM con histórico de >2 años).
- Cuentas en estado Growth o Mature, con experiencia previa de productivizar al menos un caso de uso analítico.

**No aplica (o aplica más débil).**
- Operaciones donde el FMS está fuertemente verticalizado por un OEM y la cuenta no tiene apetito para sumar capa de recomendación encima (lock-in OEM).
- Plantas con instrumentación pobre o data quality crítica de los sensores de planta — el modelo aprenderá ruido.
- Cuentas que aún no resolvieron Data & MLOps básico — sin esa base, productivizar un recomendador es un proyecto de plataforma encubierto.
- Operaciones puramente de underground con dinámica muy distinta (ciclos largos, ventilación crítica, lógica operacional diferente) — la N3 requeriría aterrizaje específico para underground.

---

## 3. Qué cambia respecto al Cross base

| Dimensión | Cross base | Delta minería |
|---|---|---|
| **Tipo de recomendación** | Recomendación a usuario final B2C/B2B en plataforma digital | Recomendación a operador especializado (dispatcher, metalurgista, reliability engineer) en sistema operacional |
| **Frecuencia de inferencia** | Recomendación bajo demanda en plataforma | Tiempo real continuo (dispatch) o por turno (planes mantenimiento, setpoints planta) |
| **Tolerancia a error** | Una mala recomendación impacta en una conversión perdida | Una mala recomendación puede costar miles de USD en un ciclo de acarreo errado, o provocar un incidente operacional |
| **Explainability** | Opcional | **Obligatoria** — el operador no acepta una recomendación que no entiende. Modelos black-box bloquean adopción |
| **Modelos típicos** | Colaborativo, contenido, híbrido | Modelos de optimización combinatoria (ruteo, scheduling) + ML predictivo de degradación + modelos de proceso (recuperación, throughput) — frecuentemente híbridos analítico-ML |
| **UI/integración** | API + frontend digital | Integración nativa con dispatch console, CMMS, DCS/operación (no se construye nuevo frontend; se inyecta en el sistema operacional existente) |
| **Equipo agregado** | — | Operations Research Engineer, Geometalurgista o Reliability Engineer del cliente como co-piloto, Domain Expert minero (Acid o partner) |
| **Entregables agregados** | — | Loop de retroalimentación humano-modelo (operador confirma o rechaza recomendación, alimentando reentrenamiento), runbook de degradación grácil ante pérdida de inputs |
| **No incluye** | — | Optimización de safety-critical (paradas, ventilación mina underground, restricciones legales de operación) |

---

## 5. Resultados esperables verticalizados

**KPI de negocio.**
- **Recomendación de mantenimiento:** aumento MTBF 10–25% y reducción de costo mantenimiento por tonelada 5–10% en 12 meses (referencias: BHP Operating System, casos GMG Group "Industrial AI").
- **Recomendación de rutas de acarreo:** mejora de ciclo de acarreo 3–8%, traducido a 2–6% adicional de toneladas movidas/turno. En una operación de 100.000 t/día con margen de USD 20/t es un upside material.
- **Recomendación de setpoints planta:** mejora de recuperación 0.5–2 puntos porcentuales o aumento throughput 2–5%. Para una concentradora de cobre 0.5pp de recuperación con ley promedio 0.7% puede valer USD 15–30M/año.

**KPI operacional.**
- % de recomendaciones aceptadas por el operador (adherencia): meta 60%+ tras estabilización; 80%+ es objetivo de madurez.
- Tiempo medio de decisión del dispatcher / metalurgista: idealmente reducido en 30–50%.
- Frecuencia de override y motivo registrado (input para reentrenamiento).

**Caveat de honestidad.** Los upside grandes (1pp recuperación, 5% throughput) requieren no solo modelo sino disciplina de adopción del operador, calidad de datos de planta y proceso continuo de calibración. Sin esos tres, el modelo recomienda y nadie ejecuta — el valor no se realiza. Vender con honestidad de qué se requiere del cliente para sostener el resultado.

---

## 6. Operativa típica en esta industria

- **Duración del engagement.** Discovery 4–6 semanas; piloto sobre un caso de uso 4–6 meses; escalamiento a operación 24x7 estable +3 meses.
- **Modalidad de contratación.** Proyecto cerrado + retainer MLOps post go-live. Modalidad de pricing por API call o por turno operacional disponible para casos de uso de alta frecuencia.
- **Sponsor target.** Gerencia de Operaciones (rutas, dispatch), Gerencia de Mantenimiento o Reliability (planes mantenimiento), Gerencia de Procesos / Planta (setpoints), CDO / Transformación Digital como patrocinador transversal.
- **Ciclo de venta.** 5–10 meses — la naturaleza de "intervenir el proceso operacional" hace que el ciclo sea más conservador. Recomendamos partir con caso de uso donde la recomendación es accesible al operador sin cambiar workflow mayor.
- **Dedicación esperada del cliente.** Operations Research / Reliability Engineer 30–50% durante piloto; Domain Expert de proceso 25% (clave); operador del sistema operacional 10% (testing de UI/UX).
- **Logística.** Visitas a faena obligatorias en discovery y go-live para entender el contexto del operador real. El operador es quien acepta o rechaza la recomendación: si no se involucra desde el inicio, la N3 falla en adopción.

---

## 7. Posicionamiento competitivo en la vertical

**Vendors activos.**
- **FMS con módulos de optimización** — Modular DISPATCH (Hitachi), Wenco (Hitachi), Caterpillar MineStar Fleet, Hexagon MineOperate (con módulos de OPS y MineEnterprise). Fortalezas: integración nativa con flota. Debilidades: optimización heurística (no ML moderno) en muchos módulos; lock-in a marca de flota.
- **Plataformas APC (Advanced Process Control) para planta** — Honeywell Connected Plant, Emerson Plantweb Insight, ABB Ability Stockyard Management, Metso Outotec Geminex. Fortalezas: productos verticalizados para concentrador. Debilidades: licenciamiento alto, no resuelven el caso de uso fuera de la planta.
- **Especialistas analíticos mineros** — IntelliSense.io (IntelliMine), Petra (Maxta), Veracio (antes Imago), Decoda. Fortalezas: producto vertical. Debilidades: cobertura por caso de uso fragmentada; integraciones limitadas.
- **Consultoras** — McKinsey QuantumBlack, BCG Gamma con prácticas mineras. Fortalezas: capacidad de cambio organizacional. Debilidades: precio premium y modelo de transferencia que deja al cliente con dependencia continua.

**Diferenciales de Acid.**
- Foco en *productivizar* — el caso comparable Koandina (modelo mixto heurístico+ML para recomendar fechas de entrega B2B con 20% de adherencia sostenida) demuestra capacidad de poner recomendadores en producción que tienen *adherencia real* de usuarios operacionales, no solo precisión técnica.
- Capacidad de combinar enfoques heurísticos (que el dominio minero valora porque son explicables) con modelos de ML donde aportan valor — patrón directo desde Koandina.
- Cloud-native + arquitectura escalable (caso Koandina API 99.9% disponibilidad regional AWS) que se sostiene en operación 24x7.

**Objeciones típicas.**
- *"Nuestro FMS ya tiene un módulo de optimización."* → Lo respetamos. El delta es modelos más modernos (ML moderno + telemetría rica) y especialmente integración con datos fuera del FMS (clima, geotécnica, condición de equipo). No reemplazamos el FMS — alimentamos sus parámetros con recomendaciones mejor calibradas.
- *"En planta tenemos APC (Honeywell, Emerson) y no queremos un segundo sistema."* → De acuerdo. El recomendador no compite con APC; opera capa arriba sugiriendo setpoints al APC, no controlando válvulas. La frontera de control queda al APC y al operador.
- *"Los operadores no van a aceptar recomendaciones de un modelo."* → Es el riesgo real. Por eso el modelo se construye con explainability obligatoria, con el operador como co-piloto desde el primer día, con loop de retroalimentación que lo respeta. La adherencia es métrica de proyecto, no aspiración.

---

## 8. Stack típico de las cuentas de la vertical

**Sistemas operacionales destino.** Modular DISPATCH, Wenco, Caterpillar MineStar Fleet, Hexagon — para rutas y dispatch. Maximo, SAP PM — para mantenimiento. Honeywell Connected Plant, Emerson DeltaV, ABB Ability — para planta. PI System como historian base.

**Fuentes de datos.** Telemetría OEM (Caterpillar Vital, Komtrax, Volvo Co-Pilot), historians de planta, CMMS, LIMS, datos meteorológicos (regionales y on-site), DEM/topografía y geotécnica (Leapfrog, Vulcan), modelos de bloques.

**Cloud y plataformas ML.** AWS SageMaker / Bedrock, GCP Vertex AI, Azure ML. Patrón híbrido común con inferencia en edge para baja latencia donde aplica.

**Restricciones.** Latencia sub-segundo para algunos casos (dispatch), interoperabilidad con stack OEM, ciberseguridad OT, conectividad satelital en sitios remotos.

---

## 9. Evidencias y casos en la vertical

**Sin caso propio en industria minera.** Esta es la principal limitación de evidencia para esta N3. Documentar honestamente.

**Casos extrapolables (con traducción explícita).**
- *Koandina — Modelo analítico mixto Heurístico y de ML para recomendar fechas de entrega B2B*: variación absoluta de demanda reducida 5%, **20% de adherencia sostenida en operación**. Patrón extrapolable a recomendación de rutas de acarreo (recomendar la "fecha de entrega óptima" ≈ recomendar el "ciclo de acarreo óptimo"). La adherencia operacional sostenida es la métrica clave que se mantiene.
- *Koandina — Infraestructura de datos escalable para modelos de ML de recomendaciones B2B*: arquitectura AWS regional para modelos mixtos con API 99.9% de disponibilidad. Patrón directamente trasladable a operación 24x7 minera.
- *Cencosud — Modelo de Market Basket + Modelo de cluster por área/tienda*: lógica de combinar productos en asociación es estructuralmente análoga a recomendar combinaciones de stockpiles para blending de mineral.

**Traducción explícita (lo que el AD documenta con el cliente).** Lo que se sostiene del caso Koandina al caso minero es: (a) arquitectura cloud para servir recomendaciones en operación 24x7, (b) modelo híbrido heurístico+ML que es lo que más conviene cuando hay reglas duras de negocio (en minería: restricciones operativas de seguridad y compliance), (c) métrica de adherencia como métrica de proyecto, no solo precisión. Lo que cambia: el dominio del modelo (logística B2B → operación minera) requiere Domain Expert minero; los datos de entrada y la UI son distintos.

**Referencias públicas de industria.**
- BHP Operating System y los casos publicados de optimización de flota — *[bhp.com](https://www.bhp.com)*.
- GMG Group "Industrial AI in Mining" — referencia técnica reciente — *[gmggroup.org](https://gmggroup.org/guidelines/)*.
- McKinsey "Inside a mining company's AI transformation" — caso público de adopción de recomendadores en operación — *[mckinsey.com/industries/metals-and-mining/our-insights](https://www.mckinsey.com/industries/metals-and-mining/our-insights)*.
- IntelliSense.io IntelliMine — vendor especializado que publica casos de uso de recomendadores en concentradoras — *[intellisense.io](https://intellisense.io)*.

**Estado de evidencia.** N3 **incipiente con extrapolación documentada**. El criterio mínimo del framework se cumple por la vía del caso extrapolable (Koandina + Cencosud). La promoción a N3 calibrada requiere primera N4 ejecutada en una cuenta minera real.

---

## Anexo: Owner y backlog

- **Owner.** Account Director Squad Minería.
- **Backlog.**
  - Priorizar primera N4 en una cuenta del squad para construir evidencia propia minera — preferir caso de mantenimiento por menor fricción de adopción inicial.
  - Validar partnerships con especialistas mineros (IntelliSense.io, Petra) para casos donde la cuenta prefiere producto + integrador.
  - Construir muestra de "demo de recomendador minero" sobre datos sintéticos para acelerar discovery.
