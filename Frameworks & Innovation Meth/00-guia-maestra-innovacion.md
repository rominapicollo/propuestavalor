# Guía Maestra de Innovación Tecnológica

> Una práctica integrada de innovación que combina Design Thinking, Lean Startup y Continuous Discovery, pensada para equipos que construyen productos y servicios tecnológicos.

---

## Filosofía base

Tres principios rigen todo el proceso:

1. **Trazabilidad de extremo a extremo** — Cada decisión debe poder rastrearse desde un objetivo de negocio hasta un problema real del usuario.
2. **Validación antes que construcción** — Testear hipótesis con el experimento más barato posible antes de invertir en construir.
3. **Aprendizaje sobre certeza** — Las preguntas correctas valen más que las respuestas brillantes.

---

## Las 5 etapas

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  1. EMPATIZAR  →  2. DEFINIR  →  3. IDEAR  →  4. DISEÑAR  →  5. VALIDAR
│                                                                 │
│       ↑                                                    │    │
│       └────────────── Aprender y re-iterar ────────────────┘    │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

### Etapa 1 — Empatizar

**Objetivo:** entender profundamente al usuario antes de pensar en soluciones.

| Framework | Función | Ficha |
|-----------|---------|-------|
| The Mom Test | Protocolo para entrevistas que no te mientan | `01-mom-test.md` |
| Empathy Map | Síntesis emocional del usuario | `02-empathy-map.md` |
| Customer Journey Map | Recorrido actual del usuario y sus dolores | `03-customer-journey-map.md` |
| Jobs To Be Done | Propósito profundo: el "para qué" | `04-jobs-to-be-done.md` |

**Output esperado:** entendimiento validado del usuario, sus jobs y los puntos altos de dolor.

---

### Etapa 2 — Definir la oportunidad

**Objetivo:** enmarcar qué problema vale la pena resolver.

| Framework | Función | Ficha |
|-----------|---------|-------|
| Opportunity Canvas | ¿Hay oportunidad real? | `05-opportunity-canvas.md` |
| Opportunity Solution Tree | Trazabilidad outcome → oportunidad → solución | `06-opportunity-solution-tree.md` |

**Output esperado:** árbol con oportunidades priorizadas, listo para sumar ramas de solución.

---

### Etapa 3 — Idear

**Objetivo:** generar soluciones candidatas y filtrarlas.

| Framework | Función | Ficha |
|-----------|---------|-------|
| How Might We | Reformular problemas en preguntas generativas | `07-how-might-we.md` |
| Crazy 8s | Divergencia rápida sin filtros | `08-crazy-8s.md` |
| Matriz DVF | Filtro Deseabilidad / Viabilidad / Factibilidad | `09-matriz-dvf.md` |

**Output esperado:** 2-3 soluciones candidatas conectadas a oportunidades concretas.

---

### Etapa 4 — Diseñar la propuesta

**Objetivo:** bajar las soluciones a una propuesta concreta y testeable.

| Framework | Función | Ficha |
|-----------|---------|-------|
| Value Proposition Canvas | Encajar pains/gains con la solución | `10-value-proposition-canvas.md` |
| Lean Canvas | Modelo de negocio en una página | `11-lean-canvas.md` |
| Wardley Maps | Posicionamiento estratégico (opcional) | `12-wardley-maps.md` |
| North Star Metric | Métrica única de éxito | `13-north-star.md` |
| Story Mapping | Backlog priorizado con corte de MVP | `14-story-mapping.md` |
| Pre-mortem | Identificar riesgos antes de invertir | `15-pre-mortem.md` |

**Output esperado:** propuesta completa con métrica de éxito, alcance del MVP y riesgos identificados.

---

### Etapa 5 — Validar

**Objetivo:** validar hipótesis con experimentos baratos (Build-Measure-Learn).

| Framework | Función | Ficha |
|-----------|---------|-------|
| Plantilla de Hipótesis | Formular hipótesis testeables | `16-plantilla-hipotesis.md` |
| RAT | Priorizar el supuesto más riesgoso | `17-rat.md` |
| Test Card | Diseñar el experimento | `18-test-card.md` |
| Learning Card | Capturar el aprendizaje | `19-learning-card.md` |
| Tipología de MVPs | Elegir el MVP más barato según el aprendizaje buscado | `20-tipologia-mvps.md` |
| AARRR | Métricas del funnel cuando ya hay tracción | `21-aarrr.md` |

**Output esperado:** evidencia para decidir: **perseverar, pivotar o descartar**.

---

## Flujo de trabajo integrado

```
┌────────────────────────────────────────────────────────────────┐
│ ETAPA 1: EMPATIZAR                                             │
│                                                                │
│   Mom Test ──→ Empathy Map ──→ Journey Map ──→ JTBD            │
│                                                                │
│   Output: insights del usuario                                 │
└────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────┐
│ ETAPA 2: DEFINIR                                               │
│                                                                │
│   Opportunity Canvas ──→ Opportunity Solution Tree             │
│                                                                │
│   Output: oportunidades priorizadas                            │
└────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────┐
│ ETAPA 3: IDEAR                                                 │
│                                                                │
│   How Might We ──→ Crazy 8s ──→ Matriz DVF                     │
│                                                                │
│   Output: 2-3 soluciones candidatas                            │
└────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────┐
│ ETAPA 4: DISEÑAR                                               │
│                                                                │
│   VPC ──→ Lean Canvas ──→ Wardley ──→ North Star               │
│        ──→ Story Mapping ──→ Pre-mortem                        │
│                                                                │
│   Output: propuesta completa + MVP definido                    │
└────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────┐
│ ETAPA 5: VALIDAR                                               │
│                                                                │
│   Hipótesis ──→ RAT ──→ Test Card ──→ MVP ──→ Learning Card    │
│                                              ──→ AARRR         │
│                                                                │
│   Output: evidencia + decisión                                 │
└────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                  PERSEVERAR / PIVOTAR / DESCARTAR
                              │
                              └──→ (volver a Etapa 1, 2, 3 o 4)
```

---

## El hilo invisible que conecta todo: el Opportunity Solution Tree

La trazabilidad se mantiene gracias al **Opportunity Solution Tree** (Teresa Torres). Lo armás en la Etapa 2 y lo seguís alimentando durante todo el proceso:

```
                    [Outcome de negocio]
                            │
              ┌─────────────┼─────────────┐
              │             │             │
        [Oportunidad]  [Oportunidad]  [Oportunidad]
              │             │             │
        ┌─────┴─────┐       │             │
        │           │       │             │
    [Solución]  [Solución]  ...           ...
        │           │
   [Experimento][Experimento]
```

**Regla de oro:** si una idea no se puede trazar hacia arriba hasta una oportunidad real del usuario, esa idea no debería existir.

---

## Reglas de adaptación según el riesgo dominante

No usás todos los frameworks en cada proyecto. Identificás el riesgo principal y profundizás ahí:

| Riesgo dominante | Pregunta clave | Foco |
|------------------|----------------|------|
| **Problema** | ¿Esto le importa a alguien? | Pesado en Etapas 1-2 |
| **Solución** | ¿Nuestra propuesta lo resuelve? | Pesado en Etapas 3-4 + VPC |
| **Modelo** | ¿Hay negocio? | Lean Canvas + experimentos de monetización |
| **Técnico** | ¿Se puede construir? | Wardley Map + spike técnico temprano |

---

## Los tres puntos de control no negociables

1. **Mom Test (Etapa 1)** — Sin entrevistas reales bien hechas, todo lo demás se contamina con suposiciones.
2. **Value Proposition Canvas (Etapa 4)** — Sin fit usuario-solución demostrable línea por línea, no hay propuesta de valor real.
3. **Test/Learning Cards (Etapa 5)** — Sin disciplina experimental, hay opinión disfrazada de dato.

---

## Caso de ejemplo unificado: FinFlow

A lo largo de las fichas individuales se desarrolla **FinFlow**, una app de gestión financiera y facturación pensada para freelancers latinoamericanos.

**Contexto:**
- Freelancers en LATAM tienen ingresos en múltiples monedas, clientes que pagan tarde, complejidad fiscal por país y herramientas globales (QuickBooks, FreshBooks) que no se adaptan a la región.
- Outcome de negocio: capturar el 5% del mercado de freelancers digitales de LATAM en 18 meses.

Usar un solo caso a través de todas las fichas permite ver cómo cada artefacto se conecta y alimenta al siguiente.

---

## Cómo trabajar esta guía

1. Leé esta guía maestra completa una vez.
2. Identificá la etapa donde estás hoy y el riesgo dominante.
3. Abrí las fichas de los frameworks que aplican a tu etapa.
4. Aplicá los frameworks **en orden**, dejando que el output de uno alimente al siguiente.
5. Documentá cada artefacto en un mismo espacio (Notion, Miro, Figjam, carpeta compartida) para que el equipo vea la trazabilidad completa.
6. Revisá el árbol de oportunidades cada 2 semanas. Cambia. Tiene que cambiar.

---

## Bibliografía y referencias clave

- *The Mom Test* — Rob Fitzpatrick
- *Continuous Discovery Habits* — Teresa Torres
- *Lean Startup* — Eric Ries
- *Running Lean* — Ash Maurya
- *Value Proposition Design* — Strategyzer / Alex Osterwalder
- *Inspired* / *Empowered* — Marty Cagan
- *User Story Mapping* — Jeff Patton
- *Wardley Maps* — Simon Wardley

---

*Última actualización: documento vivo, revisar trimestralmente.*
