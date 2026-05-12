# 10 — Value Proposition Canvas (VPC)

> Canvas de Strategyzer (Osterwalder) para diseñar y validar la propuesta de valor encajando solución y necesidades del usuario.

---

## Qué es

Un lienzo creado por **Alex Osterwalder** y el equipo de Strategyzer que descompone una propuesta de valor en dos lados: el **perfil del cliente** (lo que necesita) y el **mapa de valor** (lo que ofrecés). La propuesta es exitosa cuando ambos lados "encajan" (fit) línea por línea.

## Para qué sirve

- Diseñar propuestas de valor que conectan con dolores y deseos reales.
- Verificar visualmente si tu solución cubre los pains y gains del usuario.
- Detectar features que sobran (no atacan ningún pain/gain) o pains sin atacar.
- Alinear equipo y stakeholders sobre qué es lo que la propuesta promete.

## Cuándo usarlo

En la **Etapa 4 (Diseñar la propuesta)**, después de filtrar ideas con DVF y antes (o en paralelo) del Lean Canvas. Es uno de los tres puntos de control no negociables.

## Visual del canvas

```
┌───────────────────────────────────────────────────────────────────────────┐
│                                                                           │
│                     VALUE PROPOSITION CANVAS                              │
│                                                                           │
├──────────────────────────────────┬────────────────────────────────────────┤
│      MAPA DE VALOR               │      PERFIL DEL CLIENTE                │
│      (lo que ofrecés)            │      (lo que necesita)                 │
│                                  │                                        │
│   ┌─────────────────┐            │            ┌─────────────────┐         │
│   │                 │            │            │                 │         │
│   │  ALIVIADORES    │            │            │   PAINS         │         │
│   │  DE DOLOR       │ ◄──────────┼─FIT────────► (dolores,       │         │
│   │  (pain          │            │            │   frustraciones)│         │
│   │   relievers)    │            │            │                 │         │
│   │                 │            │            │                 │         │
│   ├─────────────────┤            │            ├─────────────────┤         │
│   │                 │            │            │                 │         │
│   │  PRODUCTOS Y    │            │            │   JOBS          │         │
│   │  SERVICIOS      │            │            │   (tareas, jobs)│         │
│   │                 │            │            │                 │         │
│   │                 │            │            │                 │         │
│   ├─────────────────┤            │            ├─────────────────┤         │
│   │                 │            │            │                 │         │
│   │  CREADORES DE   │            │            │   GAINS         │         │
│   │  GANANCIAS      │ ◄──────────┼─FIT────────► (beneficios,    │         │
│   │  (gain          │            │            │   resultados    │         │
│   │   creators)     │            │            │   esperados)    │         │
│   │                 │            │            │                 │         │
│   └─────────────────┘            │            └─────────────────┘         │
│                                  │                                        │
└──────────────────────────────────┴────────────────────────────────────────┘

         FORMA: CUADRADO                       FORMA: CÍRCULO
   (estructurado, lo que vos hacés)      (orgánico, no lo controlás)
```

## Los 6 bloques explicados

### Lado del Cliente (lo que vos NO controlás)

| Bloque | Qué capturar |
|--------|--------------|
| **Jobs** | Tareas funcionales, emocionales y sociales que el cliente intenta lograr |
| **Pains** | Resultados malos, obstáculos, riesgos, frustraciones |
| **Gains** | Resultados deseados, beneficios concretos, sueños, métricas de éxito |

### Lado del Valor (lo que vos SÍ controlás)

| Bloque | Qué capturar |
|--------|--------------|
| **Productos y servicios** | Qué ofrecés concretamente (lista de productos / features / servicios) |
| **Pain Relievers** | Cómo cada elemento alivia uno o más pains |
| **Gain Creators** | Cómo cada elemento crea uno o más gains |

## El "fit" (encaje) — la regla clave

El canvas funciona solo cuando hay **fit línea por línea**:

- Cada Pain del cliente debe tener al menos un Pain Reliever que lo ataque.
- Cada Gain del cliente debe tener al menos un Gain Creator que lo cree.
- Los Pain Relievers / Gain Creators que no atacan ningún Pain / Gain real son **features de sobra**.

**Tres tipos de fit (en orden de madurez):**

1. **Problem-Solution Fit** — La propuesta resuelve un problema validado en papel.
2. **Product-Market Fit** — Hay evidencia de uso real y disposición a pagar.
3. **Business Model Fit** — Hay un modelo escalable y rentable alrededor.

## Cómo se usa: protocolo paso a paso

1. **Llená primero el lado del cliente** (a la derecha). Usá la información del Empathy Map, JTBD, Journey Map y entrevistas.
   - Listá **3-7 jobs** principales (con sus dimensiones funcional/emocional/social).
   - Listá **5-10 pains** (priorizá por intensidad y frecuencia).
   - Listá **5-10 gains** (priorizá por relevancia).
2. **Después llená el lado del valor** (a la izquierda).
   - Listá productos y servicios concretos.
   - Para cada producto/feature, escribí qué pain alivia y qué gain crea.
3. **Validá el fit** con una matriz línea por línea.
4. **Identificá huecos:**
   - Pains sin pain reliever = oportunidades sin atacar.
   - Pain relievers sin pain = features de sobra.
5. **Marcá hipótesis vs. evidencia** en cada elemento.
6. **Iterá** después de cada ciclo de validación.

## Ejemplo precompletado: FinFlow

**Segmento:** Freelancer LATAM con clientes internacionales, ingreso USD 2-10k/mes.

```
┌──────────────────────────────────────┬────────────────────────────────────────┐
│ MAPA DE VALOR (FinFlow)              │ PERFIL DEL CLIENTE (Camila freelancer) │
├──────────────────────────────────────┼────────────────────────────────────────┤
│ PAIN RELIEVERS                       │ PAINS                                  │
│                                      │                                        │
│ 1. Conversor TC en tiempo real con   │ 1. Pierde dinero en TC sin saber       │
│    cálculo del monto neto en ARS     │    cuánto (4% promedio mensual)        │
│                                      │                                        │
│ 2. Recordatorios automáticos de      │ 2. Olvida facturar a tiempo            │
│    cobranza enviados desde identidad │                                        │
│    profesional (no del freelancer)   │ 3. Vergüenza de reclamar pagos         │
│                                      │    atrasados                           │
│ 3. Templates de factura con campos   │                                        │
│    fiscales por país (LATAM)         │ 4. Miedo a problemas con AFIP / fisco  │
│                                      │                                        │
│ 4. Exportación directa a formato     │ 5. Tiempo perdido en admin             │
│    AFIP y otros entes fiscales       │    no facturable                       │
│                                      │                                        │
│ 5. Importación desde Excel +         │ 6. Múltiples herramientas inconexas    │
│    onboarding asistido               │    (planilla + PDFs + mails)           │
│                                      │                                        │
├──────────────────────────────────────┼────────────────────────────────────────┤
│ PRODUCTOS Y SERVICIOS                │ JOBS                                   │
│                                      │                                        │
│ • App web + móvil de gestión         │ Funcionales:                           │
│   financiera                         │ • Facturar a clientes en múltiples    │
│ • Generador de facturas multimoneda  │   monedas                              │
│ • Dashboard de ingresos en ARS       │ • Hacer seguimiento de cobros          │
│ • Sistema de cobranza automatizada   │ • Convertir USD a ARS                  │
│ • Integración con Stripe / Mercado-  │ • Cumplir con normativa fiscal         │
│   Pago / Wise                        │                                        │
│ • Exportador para contador           │ Emocionales:                           │
│ • Reportes fiscales por país         │ • Sentirse profesional                 │
│                                      │ • Tener tranquilidad                   │
│                                      │                                        │
│                                      │ Sociales:                              │
│                                      │ • Ser percibido como "empresa seria"   │
│                                      │ • Pertenecer a una comunidad de        │
│                                      │   freelancers exitosos                 │
│                                      │                                        │
├──────────────────────────────────────┼────────────────────────────────────────┤
│ GAIN CREATORS                        │ GAINS                                  │
│                                      │                                        │
│ a. Dashboard con balance neto ARS    │ A. Saber exactamente cuánto ganó al    │
│    real, en tiempo real              │    mes en ARS netos                    │
│                                      │                                        │
│ b. Facturas con diseño profesional   │ B. Cobrar a tiempo sin perseguir       │
│    + logo personalizable             │    clientes                            │
│                                      │                                        │
│ c. Cobranza automatizada que sigue   │ C. Tranquilidad fiscal                 │
│    al cliente sin involucrar al      │                                        │
│    freelancer                        │ D. Sentirse "como empresa", no como    │
│                                      │    amateur                             │
│ d. Alertas de mejor TC y ventana de  │                                        │
│    conversión sugerida               │ E. Tiempo libre para diseñar (no para  │
│                                      │    admin)                              │
│ e. Comunidad de freelancers usuarios │                                        │
│    + benchmarks anónimos             │ F. Ganar más por mejor visibilidad     │
│                                      │    del cambio                          │
│                                      │                                        │
└──────────────────────────────────────┴────────────────────────────────────────┘
```

**Matriz de fit (extracto, línea por línea):**

| Pain del cliente | Pain Reliever que lo cubre | Fit |
|------------------|----------------------------|-----|
| 1. Pierde dinero en TC | 1. Conversor + alerta TC + 'd' (alertas mejor TC) | ✅ Fuerte |
| 2. Olvida facturar | 2. Recordatorios automáticos | ✅ Fuerte |
| 3. Vergüenza al reclamar | 2. Identidad profesional + cobranza automatizada | ✅ Fuerte |
| 4. Miedo AFIP | 3+4. Templates con campos fiscales + exportador AFIP | ✅ Medio (depende implementación) |
| 5. Tiempo perdido admin | Toda la propuesta | ✅ Medio |
| 6. Múltiples herramientas | Plataforma integral | ✅ Fuerte |

| Gain del cliente | Gain Creator que lo crea | Fit |
|------------------|--------------------------|-----|
| A. Cuánto ganó en ARS | a. Dashboard balance ARS | ✅ Fuerte |
| B. Cobrar a tiempo | c. Cobranza automatizada | ✅ Fuerte |
| C. Tranquilidad fiscal | 3+4. Templates + exportador | ✅ Medio |
| D. Sentirse "empresa" | b. Facturas pro + e. Comunidad | ✅ Medio |
| E. Tiempo libre | Toda la propuesta | ✅ Medio |
| F. Ganar más por TC | d. Alertas mejor TC | ✅ Fuerte |

**Hueco detectado:** ningún elemento ataca específicamente el **gain F** desde una experiencia "delight". Oportunidad de diseño: gamificar el ahorro mensual por TC y mostrar el "extra ganado" como hito.

**Feature de sobra detectada:** "Reportes fiscales por país" no aparece como pain reliever ni gain creator distintivo. Reconsiderar si va en MVP o se posterga.

**Marcas de hipótesis:** los pains 4 y 5 están validados con 6/8 entrevistas. El pain reliever 4 (exportador AFIP) sigue siendo `[hipótesis]` hasta hacer spike técnico de la API.

## Tips para que funcione

- **Una persona = un canvas.** Si tenés segmentos distintos, hacé canvas distintos. Mezclar genera propuestas blandas.
- **Priorizá** dentro de cada bloque (no es lo mismo el pain #1 que el #7).
- **Cuestioná cada elemento del lado del valor:** ¿este feature realmente alivia un pain o crea un gain? Si no, sacalo.
- **El canvas no es un brainstorm.** Es un instrumento de fit. Cada celda debe poder defenderse con evidencia.
- **Mostralo en cada review.** Es el "norte" de la propuesta.
- **Diferenciá pains y gains.** Un gain no es la ausencia de un pain (eso ya está cubierto por el pain reliever). Un gain es algo proactivo que el usuario quiere.

## Errores comunes

| Error | Cómo evitarlo |
|-------|---------------|
| Llenar lado del valor primero | Empezá siempre por el cliente |
| Mezclar segmentos | Un VPC por segmento |
| Confundir features con beneficios | Cada feature debe traducirse a "alivia X / crea Y" |
| Vaciar el canvas y olvidarlo | Revisar después de cada experimento |
| Listar todo igual de importante | Priorizar dentro de cada bloque |

## Conexión con otros frameworks

- **Se alimenta de:** Empathy Map (pains/gains), JTBD (jobs), Customer Journey Map, Opportunity Canvas.
- **Alimenta a:**
  - **Lean Canvas** (problema y propuesta de valor)
  - **Story Mapping** (los pain relievers / gain creators son features priorizables)
  - **Plantilla de Hipótesis** (cada fit es una hipótesis testeable)
  - **MVP** (qué incluir = los pain relievers / gain creators con fit más fuerte)

## Lectura recomendada

- *Value Proposition Design* — Alex Osterwalder, Yves Pigneur, Greg Bernarda, Alan Smith.
- Plantillas oficiales en strategyzer.com.
