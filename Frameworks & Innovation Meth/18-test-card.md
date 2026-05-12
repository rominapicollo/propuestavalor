# 18 — Test Card (Strategyzer)

> Formato estándar de Strategyzer para diseñar un experimento de validación de hipótesis en una sola tarjeta.

---

## Qué es

Una tarjeta creada por **Strategyzer** (Alex Osterwalder + David Bland) que estructura el diseño de un experimento. Es la herramienta operativa para convertir una hipótesis priorizada (RAT) en una acción concreta, con criterio de éxito definido **antes** de ejecutarla.

Junto con la **Learning Card** (siguiente ficha), forma el ciclo experimental de la Etapa 5.

## Para qué sirve

- Diseñar experimentos con disciplina (variables, métricas, criterio).
- Forzar al equipo a comprometerse con criterios de éxito antes de ver el dato.
- Documentar experimentos para no repetirlos.
- Comunicar a stakeholders qué se está validando y cómo.
- Crear un repositorio histórico de aprendizaje organizacional.

## Cuándo usarla

En la **Etapa 5 (Validar)**, después de identificar el RAT. Cada hipótesis priorizada genera al menos una Test Card. Es uno de los tres puntos de control no negociables del proceso.

## Visual del Test Card

```
┌────────────────────────────────────────────────────────────────┐
│  TEST CARD                                                     │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│  HIPÓTESIS                                                     │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Creemos que [SUPUESTO]                                   │  │
│  │ Para [USUARIO]                                           │  │
│  │ Resolverá [RESULTADO ESPERADO]                           │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  EXPERIMENTO                                                   │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Para validarlo / refutarlo, vamos a [ACCIÓN CONCRETA]    │  │
│  │ con [SEGMENTO / N]                                       │  │
│  │ durante [TIEMPO]                                         │  │
│  │ y mediremos [VARIABLE / DATO]                            │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  CRITERIO DE ÉXITO                                             │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Consideraremos VALIDADA la hipótesis si [NÚMERO/UMBRAL]  │  │
│  │ Consideraremos REFUTADA si [NÚMERO/UMBRAL]               │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  DATOS GENERALES                                               │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Tipo de hipótesis:    [Valor / Crecim. / Viab. / Fact.]  │  │
│  │ Costo del experimento: USD ___                           │  │
│  │ Tiempo de ejecución:  ___ días                           │  │
│  │ Confianza si valida:  Baja / Media / Alta                │  │
│  │ Responsable:          [Nombre]                           │  │
│  │ Fecha:                [YYYY-MM-DD]                       │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

## Los componentes explicados

| Bloque | Qué contiene |
|--------|--------------|
| **Hipótesis** | La afirmación que querés validar/refutar (formato de la Plantilla) |
| **Experimento** | Acción concreta + segmento + tiempo + métrica |
| **Criterio de éxito** | Umbral numérico previo a ejecutar |
| **Datos generales** | Tipo, costo, tiempo, confianza, responsable, fecha |

## La regla de "fuerza de la evidencia"

El criterio de éxito debe estar **acorde a la confianza** que querés tener al validar:

| Tipo de evidencia | Fuerza | Cuándo usarla |
|-------------------|--------|---------------|
| Opiniones (encuestas, intent) | Baja | Solo para descartar rápido |
| Comportamiento (clicks, signups) | Media | Para validar interés |
| Compromiso (tiempo, pago, reputación) | Alta | Para validar decisión |
| Dinero real | Muy alta | Para validar viabilidad |

Una hipótesis de pricing **NO se valida con una encuesta** ("¿pagarías USD 9?"). Se valida con un smoke test donde la gente pone su tarjeta.

## Cómo se usa: protocolo paso a paso

1. **Tomá una hipótesis priorizada del RAT.**
2. **Elegí el formato de MVP/experimento** más adecuado (ver Tipología de MVPs).
3. **Definí la acción concreta:** qué vas a hacer, con quién, dónde, durante cuánto.
4. **Definí la métrica principal:** un solo número que define éxito.
5. **Definí el criterio de éxito** ANTES de ejecutar.
   - Validado si: X% / Y absoluto / Z comportamiento.
   - Refutado si: por debajo del umbral.
6. **Estimá costo y tiempo.**
7. **Asignar responsable y fecha.**
8. **Ejecutá el experimento.**
9. **Pasá los resultados a una Learning Card.**

## Ejemplo precompletado: FinFlow

**RAT identificado:** H5 — pricing Pro USD 9/mes con 6% de conversión.

```
┌────────────────────────────────────────────────────────────────────────┐
│  TEST CARD #001                                                        │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│  HIPÓTESIS                                                             │
│  ────────────                                                          │
│  Creemos que el plan Pro a USD 9/mes con cobranza automatizada,       │
│  templates pro y dashboard ARS                                         │
│  Para freelancers latinoamericanos con > USD 2k/mes en clientes        │
│  internacionales                                                       │
│  Resolverá su necesidad de herramienta accesible vs. QuickBooks y      │
│  generará al menos 6% de conversión visitor→signup→Pro                 │
│                                                                        │
│  EXPERIMENTO                                                           │
│  ─────────────                                                         │
│  Para validarlo, vamos a:                                              │
│  1. Construir una landing page con la propuesta de valor de FinFlow    │
│  2. Mostrar 3 planes: Free / Pro USD 9 / Studio USD 19                  │
│  3. CTA "Empezar prueba gratis de 14 días" (con captura de email)     │
│  4. Traer tráfico de 3 canales: Twitter ads + sponsoreo en 2          │
│     comunidades + LinkedIn ads                                        │
│                                                                        │
│  Con freelancers latinoamericanos digitales (segmento target)         │
│  Durante 14 días                                                       │
│  Y mediremos:                                                          │
│  • Visitantes únicos a la landing                                      │
│  • CTR por plan (% que clickean "Empezar")                             │
│  • Conversion rate a "registrar email + tarjeta"                       │
│  • Test A/B paralelo: USD 5 vs USD 9 vs USD 15                         │
│                                                                        │
│  CRITERIO DE ÉXITO                                                     │
│  ──────────────────                                                    │
│  Validado si:                                                          │
│  • ≥ 6% de los visitantes clickean en plan Pro USD 9                   │
│  • ≥ 50% de los que clickean dan email + tarjeta                       │
│  • El CTR de USD 9 es ≥ 70% del CTR de USD 5                           │
│  (= no se cae mucho la conversión al duplicar el precio)              │
│                                                                        │
│  Refutado si:                                                          │
│  • < 3% clickean en plan Pro                                           │
│  • CTR de USD 9 cae a < 50% del CTR de USD 5                           │
│  • Conversion total (visit→tarjeta) < 1%                               │
│                                                                        │
│  Zona ambigua: 3-6% en plan Pro → necesita segundo experimento.        │
│                                                                        │
│  DATOS GENERALES                                                       │
│  ────────────────                                                      │
│  Tipo de hipótesis:    Viabilidad                                      │
│  Costo del experimento: USD 800 (USD 500 ads + USD 300 sponsoreos)    │
│  Tiempo de ejecución:   14 días (3 días construcción + 11 testeo)      │
│  Confianza si valida:   Alta (comportamiento + dinero comprometido)    │
│  Responsable:           Florencia (Growth) + Ana (Producto)            │
│  Fecha de inicio:       2026-05-15                                     │
│  Fecha de cierre:       2026-05-29                                     │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

## Tips para diseñar buenas Test Cards

- **Una hipótesis, un experimento, una métrica principal.** Si tu experimento mide cinco cosas, probablemente esté testeando cinco hipótesis (y no validás bien ninguna).
- **El criterio de éxito se escribe en lápiz, pero firmado en sangre.** No lo moves después de ver los datos.
- **Definí también la zona ambigua.** Casi nunca el dato es blanco o negro. Anticipá qué hacés si cae en gris.
- **Estimá costo y tiempo realistas.** Los experimentos sin restricción se extienden indefinidamente.
- **Usá la métrica más cercana al comportamiento real.** "Intent" (encuestas) es más débil que "behavior" (clicks); "behavior" es más débil que "commitment" (pago).
- **Documentá los experimentos descartados también.** Si decidiste no hacer algo, escribilo. Ese aprendizaje también vale.

## Errores comunes

| Error | Cómo evitarlo |
|-------|---------------|
| Criterio de éxito vago | Forzá número y umbral antes de ejecutar |
| Test demasiado caro para la pregunta | Si la hipótesis es básica, el experimento debe serlo también |
| No definir criterio de refutación | El equipo termina interpretando cualquier dato como confirmación |
| Múltiples experimentos en paralelo sin diseño | Las variables se contaminan |
| Falta de fecha de cierre | Los experimentos se vuelven proyectos eternos |

## Variantes de Test Cards según objetivo

| Tipo de experimento | Cuándo usarlo |
|---------------------|---------------|
| **Smoke Test** | Validar interés (landing + CTA) |
| **A/B Test** | Comparar dos variantes |
| **Wizard of Oz** | Simular feature compleja con trabajo manual |
| **Concierge** | Servicio manual personalizado para aprender |
| **Customer Interview** | Validar problema cualitativamente |
| **Prototype Test** | Validar usabilidad de una solución |
| **Pre-sales / Crowdfunding** | Validar disposición a pagar real |

Cada uno tiene su propia plantilla, pero todos siguen la estructura básica de la Test Card.

## Conexión con otros frameworks

- **Se alimenta de:** Plantilla de Hipótesis, RAT, Tipología de MVPs.
- **Alimenta a:**
  - **Learning Card** (el resultado del experimento se documenta)
  - **Opportunity Solution Tree** (los experimentos se cuelgan como hojas)
  - **Backlog de discovery** (próximas Test Cards en cola)

## Lectura recomendada

- *Testing Business Ideas* — David J. Bland & Alex Osterwalder (catálogo de 44 experimentos con Test Cards).
- Strategyzer — Test Cards y Learning Cards descargables.
- *The Right It* — Alberto Savoia (concepto de "Pretotype").
