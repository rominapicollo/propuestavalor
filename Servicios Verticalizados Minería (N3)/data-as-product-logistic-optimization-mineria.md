---
title: Data as Logistic Optimization Product para Minería
sidebar_label: Data as Logistic Optimization · Minería
servicio_cross_base: Data as Product (con extensión a Logistic Optimization)
vertical: Minería
nivel: N3
version: 0.1 (incipiente)
ultima_actualizacion: 2026-05-11
squad_owner: Squad Vertical Minería · Account Director
bu_lead: Data & AI Evolution
estado_evidencia: Sin caso propio en industria minera para optimización logística minera específica. Casos extrapolables fuertes desde Koandina (Logística B2B), Walmart (operación), LATAM (despacho tiempo real) — N3 incipiente
---

# Data as Logistic Optimization Product para Minería

**Cross base:** [Data as Product](../Servicios%20Cross%20Data/data-as-product.md) | **Vertical:** Minería | **Versión:** 0.1 | **Última actualización:** 2026-05-11

> **Nota de mapeo.** El nombre "Data as Logistic Optimization Product" usado en el PDF del squad apunta a una aplicación específica del Cross *Data as Product* — la cadena logística minera —, no a un Cross separado. Esta N3 documenta cómo el Cross *Data as Product* se materializa en un producto de datos que sostiene la optimización logística característica de una operación minera: el flujo concentrado/cátodos/mineral entre mina, planta, stockpile, ferrocarril, puerto, naviera.

---

## 1. Caso de uso con nombre propio y dolor de negocio

### Caso principal: **Producto de Datos para Optimización de Logística Mina-Puerto y Acarreo Interno**

**Dolor de negocio.** La cadena logística minera es uno de los procesos más caros y más fragmentados de la operación. Un concentrado de cobre o un cátodo nace en mina, pasa por planta, luego stockpile, luego transporte (camión, ferrocarril, mineroducto), llega al puerto, espera en patio, embarca en buque, viaja a refinería destino. **Cada eslabón tiene un sistema de información distinto, con un dueño distinto, con calidad de dato distinta**: el FMS dispatch tiene los datos de acarreo interno; SAP MM/SD tiene los datos comerciales; el operador de ferrocarril (FCAB en Chile, Volcan-Cerro de Pasco operations en Perú) tiene los datos de cargas y tránsito; el agente naviero tiene los datos de demurrage. El cliente quiere optimizar la cadena pero no puede porque **no existe un producto de datos confiable que muestre la cadena completa con la latencia que la optimización requiere**. La consecuencia financiera: costo logístico por tonelada por encima del optimo, demurrage en puerto, ciclos de acarreo subóptimos dentro de la mina, decisiones de despacho que se toman tarde o con datos incompletos. El delta de valor entre baseline y operación optimizada en una cuenta mediana es típicamente USD 5–15M/año.

### Casos de uso adicionales bajo el mismo N3

- **Producto de datos para optimización de transporte de concentrado/insumos faena-puerto** (caso PDF) — visibilidad fin-a-fin de la cadena, datos productivos para que planificación logística asigne despachos óptimos.
- **Producto de datos para rutas de camiones de acarreo intra-mina** (caso PDF) — datos productivos en tiempo real para minimizar tiempos muertos pala-camión-stockpile, sin reemplazar al FMS sino alimentándolo con datos confiables.
- **Producto de datos para gestión de stockpiles** — visibilidad en tiempo real de inventarios, calidades por stockpile, rotación, edad del mineral apilado — base para decisiones de blending y de despacho. (*Idea adicional SME — Fuente: AusIMM literatura sobre stockpile management, [ausimm.com](https://www.ausimm.com)*)
- **Producto de datos para supply chain de insumos críticos** — bolas de molienda, neumáticos OTR, reactivos de flotación, combustible, ANFO — visibilidad de consumo, stock, lead time, riesgo de quiebre. Crítico para que abastecimiento no sea el cuello de botella. (*Idea adicional SME — Fuente: Cochilco "Costos de producción minera del cobre", reportes públicos, [cochilco.cl](https://www.cochilco.cl)*)
- **Producto de datos para emisiones logísticas (Scope 3 transporte)** — base trazable para reportería Scope 3 de transporte de concentrado y de movimiento intra-faena. Cada vez más exigido por inversionistas y por estándares ICMM/TCFD. (*Idea adicional SME — Fuente: ICMM Climate Investment Framework, [icmm.com/climate-investment-framework](https://www.icmm.com/en-gb/our-principles/climate-change)*)
- **Producto de datos para flujo de comercialización** — desde producción a embarque a refinación a liquidación final con cliente. Permite a comercial proyectar revenue con incertidumbre acotada. (*Idea adicional SME*)

---

## 2. Para qué cuentas de la vertical aplica y para cuáles no

**Aplica fuerte.**
- Operaciones con cadena logística compleja: producción que sale por puerto (concentrado de cobre, cátodos, fierro) con múltiples eslabones de transporte.
- Cuentas con flota de acarreo de >30 camiones de extracción mayores donde el FMS no integra con sistemas de stockpile y comercialización.
- Operaciones con stockpiles activos y blending recurrente.
- Cuentas con CDO o Gerencia de Transformación Digital establecida que valora "data products" como concepto.

**No aplica (o aplica más débil).**
- Operaciones puramente domésticas sin componente puerto/comercialización internacional.
- Cuentas sin DataOps básico instalado — productivizar un producto de datos sobre stack inmaduro no rinde.
- Faenas underground con dinámica logística diferente (transporte interno por jaula/shaft, no por camión).

---

## 3. Qué cambia respecto al Cross base

| Dimensión | Cross base | Delta minería |
|---|---|---|
| **Tipo de producto de datos** | Productos transversales con ownership por dominio | Producto de datos cross-eslabón de la cadena logística — el dominio es "logística minera", el dueño es típicamente Supply Chain o Operaciones |
| **Fuentes integradas** | Bases transaccionales y operacionales del cliente | FMS dispatch, SAP MM/SD, sistemas de stockpile, sistemas de operador ferroviario (terceros), sistemas portuarios, agentes navieros, sistemas de pesaje en mina y puerto |
| **Latencia objetivo** | Variable | Tiempo real estricto para acarreo intra-mina; near real time (minutos) para stockpile y puerto; batch diario para comercialización |
| **Calidad y trazabilidad** | Estándares de dominio | Trazabilidad fin-a-fin desde tronadura a entrega — crítico para reconciliación metalúrgica y compliance comercial |
| **Equipo agregado** | — | Operations Research Engineer, Logistics Planner del cliente, Domain Expert minero, Comercial / Trading Lead del cliente para visibilidad commercial |
| **Entregables agregados** | — | Modelo de datos de cadena logística minera, integración con sistemas de terceros (operador ferroviario, naviera, agente portuario), módulo de reconciliación metalúrgica |
| **No incluye** | — | Operación de la logística física, contratos con operadores logísticos, negociación commercial — sí los datos para tomar mejor todas esas decisiones |

---

## 5. Resultados esperables verticalizados

**KPI de negocio.**
- Reducción de costo logístico por tonelada de concentrado puesto en puerto: **3–8%** (referencia Cochilco "Anuario de estadísticas del cobre" para costos logísticos típicos en gran minería del cobre Chile). *Fuente: [cochilco.cl/Listado%20Temtico/Anuario.aspx](https://www.cochilco.cl)*.
- Reducción de demurrage en puerto: 15–40% sobre baseline donde existe el dolor (varía mucho por operación).
- Reducción de tiempo de ciclo de acarreo intra-mina: 3–8% con un producto de datos confiable detrás del FMS — equivalente a 2–6% adicional de toneladas movidas/turno.
- Aumento de adherencia al plan de despacho: meta 95%+ en 12 meses.

**KPI operacional.**
- % de eslabones de la cadena con data disponible NRT (objetivo: 80%+ en 12 meses).
- Tiempo medio de detección de desviación logística (mineral retrasado en stockpile, camión detenido, demora portuaria).
- Reconciliación metalúrgica mina-planta-puerto con error <0.5% (referencia industria).

---

## 6. Operativa típica en esta industria

- **Duración del engagement.** Discovery 4–6 semanas; primer producto de datos (un eslabón crítico) 4 meses; cadena fin-a-fin 9–14 meses.
- **Modalidad de contratación.** Proyecto cerrado por eslabón + retainer mensual de DataOps. Habitual modalidad CapEx (proyecto) + OpEx (operación) para encajar planificación financiera minera.
- **Sponsor target.** Gerencia de Supply Chain / Logística, Gerencia de Operaciones, CDO o Gerencia de Transformación Digital como patrocinador transversal. Eventualmente Gerencia Comercial cuando el producto de datos llega a comercialización.
- **Ciclo de venta.** 5–9 meses.
- **Dedicación esperada del cliente.** Logistics Planner 30%, OR Engineer 25%, Plataforma/IT 15%, comercial 5–10%.
- **Logística específica.** Visitas a faena y a puerto necesarias en discovery. Coordinación con terceros (operador ferroviario, naviera) para acceso a sus datos suele ser el camino crítico — anticipar gating contractual.

---

## 7. Posicionamiento competitivo en la vertical

**Vendors activos.**
- **TMS / Supply Chain platforms generalistas** — SAP TM, Oracle TMS, Blue Yonder. Fortalezas: enterprise grade. Debilidades: requieren mucha customización para minería; no integran nativamente con FMS minero.
- **Plataformas verticales mineras** — Hexagon HxGN MineEnterprise, Wenco Insight, Caterpillar MineStar Edge. Fortalezas: integración nativa con flota. Debilidades: cobertura de cadena limitada a la mina; no llegan al puerto.
- **Especialistas en logística minera** — Sentient Logistics, Optitrack para tracking, JDA (Blue Yonder) para planning. Fortalezas: producto vertical. Debilidades: cobertura por eslabón fragmentada.
- **Consultoras de transformación** — McKinsey, Accenture, EY con prácticas mineras. Fortalezas: change management. Debilidades: precio premium, dependencia continua.

**Diferenciales de Acid.**
- Foco en *producto de datos* (no en plataforma operacional ni en consultoría) — el delta es entregar datos confiables fin-a-fin con ownership y SLA, que después alimentan cualquier sistema downstream que el cliente quiera (su TMS, su FMS, su BI).
- Casos comparables fuertes: LATAM repositorio de despacho NRT, Walmart plataforma operacional con DataOps maduro — patrones de "producto de datos en operación 24x7" probados.
- Capacidad de integrar con sistemas de terceros (operador logístico, naviera) — necesidad central en cadena minera.

**Objeciones típicas.**
- *"Tenemos SAP TM y BI corporativo."* → Bien. SAP TM gestiona el transporte; nosotros entregamos el dato que SAP TM y el resto del stack consume. No reemplazamos SAP TM.
- *"Cada eslabón tiene su sistema, esto va a ser eterno."* → De acuerdo. Por eso el modelo es por eslabón con onda creciente: arrancamos por el de mayor dolor (típicamente acarreo intra-mina o stockpile/puerto) y extendemos. Los eslabones tempranos pagan los siguientes.
- *"No vamos a lograr que el operador ferroviario nos abra sus datos."* → Es el principal riesgo. Lo resolvemos en discovery con un mapeo formal de los contratos de datos con terceros. Si no hay forma, ajustamos el alcance al perímetro donde sí hay datos.

---

## 8. Stack típico de las cuentas de la vertical

**Fuentes integradas habituales.** FMS (Modular DISPATCH, Wenco, MineStar Fleet, Hexagon HxGN), SAP MM/SD/TM, sistemas de pesaje (Mettler-Toledo, Avery Weigh-Tronix), sistemas de stockpile (a veces nativos OEM, a veces planillas), sistemas de operador ferroviario (FCAB Antofagasta, FEPASA, etc.), sistemas portuarios (Navis N4, Octopi), sistemas de agente naviero, AIS (datos de buques).

**Cloud preferida.** AWS, Azure, GCP con patrón híbrido.

**Estándares.** ICMM Climate Investment Framework para reportería Scope 3; INCOTERMS para contratos; ISO 28000 para supply chain security; protocolos LME para cathodes y concentrate market.

**Restricciones.** Contratos de datos con terceros (operador logístico) suelen ser el camino crítico. Confidencialidad commercial alta para datos de embarques. Conectividad desde puerto puede ser similar a faena (limitada).

---

## 9. Evidencias y casos en la vertical

**Sin caso propio en industria minera para logística minera específica.** Honestidad explícita.

**Casos extrapolables (fuertes).**
- *LATAM — Repositorio centralizado de datos de despacho en tiempo real con Dataplex en GCP, gobernanza completa, disponibilidad NRT*: patrón directamente trasladable a producto de datos de cadena logística minera. Lo que se sostiene: arquitectura, ownership, gobernanza, latencia. Lo que cambia: las fuentes (sistemas de vuelo → sistemas mineros y portuarios).
- *Koandina — Infraestructura de datos escalable para modelos B2B con API 99.9% disponibilidad y modelo mixto heurístico+ML*: patrón "producto de datos + recomendador" que es exactamente lo que la cadena logística minera demanda.
- *Walmart — Plataforma de datos operacional con DataOps maduro, ~95% reducción en errores de carga, productividad operacional duplicada*: prueba de que se sostiene operación 24x7 con calidad.

**Referencias públicas de industria.**
- Cochilco "Anuario de Estadísticas del Cobre" — referencia de costos logísticos y producción Chile. *[cochilco.cl](https://www.cochilco.cl)*.
- BHP / Rio Tinto / Newmont casos publicados de optimización de cadena (autonomous haulage + smart port). *[bhp.com](https://www.bhp.com)*, *[riotinto.com](https://www.riotinto.com)*.
- ICMM Climate Investment Framework — guía para reportería Scope 3 de transporte minero. *[icmm.com](https://www.icmm.com)*.
- World Bank "Climate-Smart Mining Initiative" — referencia de Scope 3 e implicancias en cadena. *[worldbank.org/climate-smart-mining](https://www.worldbank.org/en/topic/extractiveindustries/brief/climate-smart-mining-facility)*.

**Estado de evidencia.** N3 **incipiente** con extrapolación robusta del patrón de producto de datos. Promoción a calibrada tras primera N4 ejecutada sobre al menos un eslabón de la cadena minera real.

---

## Anexo: Owner y backlog

- **Owner.** Account Director Squad Minería.
- **Backlog.**
  - Mapear las cadenas logísticas características de las cuentas del squad para identificar primer eslabón de aterrizaje (intra-mina vs. stockpile vs. puerto).
  - Levantar contratos de datos con terceros logísticos de las cuentas del squad para anticipar gating.
  - Construir partnership de delivery con un especialista portuario para casos de uso puerto-embarque.
  - Definir el modelo de datos canónico de cadena logística minera como activo del squad.
