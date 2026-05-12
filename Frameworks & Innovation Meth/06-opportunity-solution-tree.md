# 06 — Opportunity Solution Tree

> Árbol visual de Teresa Torres que conecta un outcome de negocio con oportunidades del usuario, soluciones y experimentos.

---

## Qué es

Una técnica de **Continuous Discovery** creada por **Teresa Torres** que visualiza la trazabilidad entre un objetivo de negocio (outcome) y los experimentos que se ejecutan, pasando por las oportunidades del usuario y las soluciones candidatas. Es el "mapa mental" del proceso de descubrimiento.

## Para qué sirve

- Mantener la trazabilidad entre estrategia de negocio y experimentación.
- Evitar enamorarse de una sola solución (forzando alternativas).
- Hacer visible el proceso de descubrimiento al equipo y stakeholders.
- Priorizar dónde invertir tiempo de discovery.
- Detectar cuándo una solución no se traza hacia ninguna oportunidad real (= matarla).

## Cuándo usarlo

En la **Etapa 2 (Definir oportunidad)** se arma la versión inicial. Después se actualiza continuamente durante todo el proceso. Es el artefacto vivo más importante de toda la metodología.

## Visual del árbol

```
                        ┌─────────────────────┐
                        │   OUTCOME (Negocio) │
                        │   Métrica objetivo  │
                        └──────────┬──────────┘
                                   │
            ┌──────────────────────┼──────────────────────┐
            │                      │                      │
   ┌────────▼────────┐    ┌────────▼────────┐    ┌────────▼────────┐
   │  OPORTUNIDAD 1  │    │  OPORTUNIDAD 2  │    │  OPORTUNIDAD 3  │
   │ (problema/job   │    │                 │    │                 │
   │  del usuario)   │    │                 │    │                 │
   └────────┬────────┘    └────────┬────────┘    └────────┬────────┘
            │                      │                      │
       ┌────┴────┐             ┌───┴───┐              ┌───┴───┐
       │         │             │       │              │       │
  ┌────▼──┐ ┌────▼──┐      ┌───▼──┐ ┌──▼───┐      ┌──▼───┐ ┌─▼────┐
  │SOLUC. │ │SOLUC. │      │SOLUC.│ │SOLUC.│      │SOLUC.│ │SOLUC.│
  │  A    │ │  B    │      │  C   │ │  D   │      │  E   │ │  F   │
  └───┬───┘ └───┬───┘      └──┬───┘ └──┬───┘      └──┬───┘ └──┬───┘
      │         │             │        │             │        │
   ┌──▼──┐   ┌──▼──┐        ┌──▼──┐ ┌──▼──┐       ┌──▼──┐ ┌──▼──┐
   │EXP. │   │EXP. │        │EXP. │ │EXP. │       │EXP. │ │EXP. │
   │  1  │   │  2  │        │  3  │ │  4  │       │  5  │ │  6  │
   └─────┘   └─────┘        └─────┘ └─────┘       └─────┘ └─────┘
```

## Los 4 niveles del árbol

| Nivel | Qué contiene | Pregunta clave |
|-------|--------------|----------------|
| **Outcome** | Un objetivo de negocio medible | ¿Qué métrica de negocio queremos mover? |
| **Oportunidades** | Problemas, dolores o jobs del usuario validados | ¿Qué problemas del usuario, si los resolvemos, impactan en el outcome? |
| **Soluciones** | Ideas concretas para resolver cada oportunidad | ¿Cómo podríamos resolver esta oportunidad? |
| **Experimentos** | Tests para validar cada solución | ¿Cómo testeamos rápido y barato si esta solución funciona? |

## Reglas para construirlo bien

1. **Un solo outcome por árbol.** Si tenés varios, hacé un árbol por cada uno.
2. **Las oportunidades son del usuario, no de la empresa.** "Lanzar al mercado X" no es oportunidad; "el usuario pierde dinero por TC" sí lo es.
3. **Mínimo 2-3 oportunidades por outcome.** Si solo se te ocurre una, no exploraste suficiente.
4. **Mínimo 2-3 soluciones por oportunidad.** Te fuerza a no enamorarte de la primera idea.
5. **Cada solución requiere al menos 1 experimento.** Si no la podés testear, no es una solución todavía.

## Cómo se usa: protocolo paso a paso

1. **Definí el outcome** con métrica y horizonte temporal claros.
2. **Volcá oportunidades** desde Mom Test, Empathy Map, Journey Map, JTBD. Una oportunidad = una hoja del nivel 2.
3. **Priorizá oportunidades** con criterios explícitos (impacto en outcome, evidencia, tamaño del problema).
4. **Para las top 2-3 oportunidades, generá 2-3 soluciones cada una** usando How Might We + Crazy 8s.
5. **Para cada solución, listá experimentos posibles** (referenciá Test Card + Tipología de MVPs).
6. **Elegí la solución y el experimento más prometedores** y ejecutá.
7. **Actualizá el árbol semanalmente** según aprendizajes. Eliminá ramas muertas, sumá nuevas.

## Ejemplo precompletado: FinFlow

```
                 ┌─────────────────────────────────────────┐
                 │ OUTCOME                                 │
                 │ Aumentar usuarios activos pagos a 3.000 │
                 │ en 12 meses (con churn < 5%)            │
                 └────────────────┬────────────────────────┘
                                  │
          ┌───────────────────────┼────────────────────────┐
          │                       │                        │
┌─────────▼─────────┐  ┌──────────▼─────────┐  ┌───────────▼──────────┐
│ OPORTUNIDAD 1     │  │ OPORTUNIDAD 2      │  │ OPORTUNIDAD 3        │
│ El usuario pierde │  │ El usuario cobra   │  │ El usuario teme      │
│ dinero en TC sin  │  │ tarde por vergüenza│  │ errores fiscales y   │
│ saber cuánto      │  │ de reclamar        │  │ depende del contador │
│ (7/8 entrevistados│  │ (5/8 entrevistados │  │ (6/8 entrevistados   │
│ confirman)        │  │ confirman)         │  │ confirman)           │
└─────────┬─────────┘  └──────────┬─────────┘  └───────────┬──────────┘
          │                       │                        │
     ┌────┴────┐             ┌────┴────┐              ┌────┴────┐
     │         │             │         │              │         │
┌────▼───┐ ┌───▼────┐    ┌───▼────┐ ┌──▼─────┐    ┌───▼────┐ ┌──▼─────┐
│SOL. A  │ │SOL. B  │    │SOL. C  │ │SOL. D  │    │SOL. E  │ │SOL. F  │
│Dashboard│ │Conver- │    │Recorda-│ │Cobranza│    │Exporta-│ │Asisten-│
│con      │ │tidor TC│    │torios  │ │automa- │    │ción a  │ │te AFIP │
│balance  │ │con     │    │automá- │ │tizada  │    │formato │ │integra-│
│ARS neto │ │alertas │    │ticos no│ │con     │    │AFIP    │ │do      │
│         │ │de TC   │    │invasi- │ │link de │    │directa │ │        │
│         │ │favor.  │    │vos     │ │pago    │    │        │ │        │
└────┬───┘ └────┬───┘    └────┬───┘ └────┬───┘    └────┬───┘ └────┬───┘
     │          │             │          │             │          │
 ┌───▼───┐  ┌───▼───┐     ┌───▼───┐  ┌───▼───┐     ┌───▼───┐  ┌───▼───┐
 │EXP. 1 │  │EXP. 2 │     │EXP. 3 │  │EXP. 4 │     │EXP. 5 │  │EXP. 6 │
 │Smoke  │  │Wizard │     │A/B    │  │Concier│     │Spike  │  │Entre- │
 │test:  │  │of Oz: │     │test   │  │ge:    │     │técnico│  │vistas │
 │landing│  │alertas│     │entre 3│  │opera- │     │de fac-│  │con    │
 │+ pre- │  │TC por │     │textos │  │mos    │     │tibili-│  │conta- │
 │orden  │  │WhatsAp│     │de     │  │cobran-│     │dad de │  │dores  │
 │       │  │       │     │email  │  │za     │     │API    │  │       │
 │       │  │       │     │       │  │manual │     │AFIP   │  │       │
 └───────┘  └───────┘     └───────┘  └───────┘     └───────┘  └───────┘
```

**Lectura del árbol:**

- El outcome se descompone en **3 oportunidades** validadas por entrevistas.
- Cada oportunidad tiene **2 soluciones candidatas** (no nos casamos con una).
- Cada solución tiene **un experimento más barato posible** asignado.
- **Decisión priorizada:** empezamos con Experimento 1 (Smoke Test) y Experimento 4 (Concierge), porque atacan las dos oportunidades de mayor frecuencia (7/8 y 5/8) con métodos de validación más rápidos.

**Ramas muertas (a documentar para no repetir):**
- Solución inicial: "criptomonedas como puente para cobros" → eliminada en sprint 2 por restricción regulatoria del bloque 7 del Opportunity Canvas.

## Tips para no caer en errores comunes

- **Si una solución no se traza a una oportunidad, matala.** Es la regla más importante.
- **No descartes las "ramas muertas".** Documentalas: son aprendizaje organizacional.
- **Releé el árbol en cada planning.** Si nadie lo mira, no funciona.
- **Una oportunidad se valida con datos, no con opiniones.** Marcá "evidencia: X entrevistas / Y dato cuantitativo" en cada hoja.
- **Limitá la profundidad inicial.** No quieras llenar el árbol entero en una sesión. Empezá con outcome + 3 oportunidades. Lo demás emerge.
- **Visualizalo grande.** Miro, Figjam o una pared. Si vive en un Google Doc, muere.

## Diferencias clave con otros artefactos

| Artefacto | Foco | Vida útil |
|-----------|------|-----------|
| **Opportunity Solution Tree** | Trazabilidad y exploración | Vive durante todo el proceso |
| **Lean Canvas** | Snapshot del modelo de negocio | Versionado cada 1-2 meses |
| **Story Map** | Bajada táctica a backlog | Operativo del equipo de delivery |
| **Roadmap** | Planificación temporal | Trimestral |

El árbol es **estratégico**, los otros son **operativos**.

## Conexión con otros frameworks

- **Se alimenta de:** Opportunity Canvas (oportunidades), JTBD (jobs convertidos en oportunidades), Mom Test (evidencia para cada oportunidad).
- **Alimenta a:**
  - **How Might We** (cada oportunidad genera HMW)
  - **Test Card** (cada experimento del árbol se diseña con Test Card)
  - **Tipología de MVPs** (los experimentos eligen formato MVP)
  - **Learning Card** (los aprendizajes vuelven al árbol)

## Lectura recomendada

Teresa Torres — *Continuous Discovery Habits* (2021). Libro fundamental, capítulos 5 y 6 desarrollan el árbol en detalle.
Blog: producttalk.org (Teresa publica plantillas y casos).
