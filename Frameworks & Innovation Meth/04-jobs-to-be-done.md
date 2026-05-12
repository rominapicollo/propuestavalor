# 04 — Jobs To Be Done (JTBD)

> Framework para entender qué "trabajo" intenta lograr el usuario al contratar un producto o servicio, más allá de las funcionalidades.

---

## Qué es

Un marco de pensamiento popularizado por **Clayton Christensen** que sostiene que los usuarios "contratan" productos para hacer un *job* (una tarea, una transformación) en su vida. Si entendés el job, entendés qué resuelve realmente tu producto y contra qué compite (que no siempre es lo obvio).

**Frase fundacional:** *"La gente no quiere un taladro de 6mm, quiere un agujero de 6mm en la pared… en realidad quiere una repisa colgada… en realidad quiere una casa más linda… en realidad quiere sentirse orgulloso de su hogar."*

## Para qué sirve

- Salir del foco en features para enfocarte en propósito.
- Entender contra quién competís realmente (a veces no es tu competidor directo).
- Detectar oportunidades de innovación que no son evidentes desde el producto.
- Definir el "trabajo principal" que tu propuesta de valor debe resolver.

## Cuándo usarlo

En la **Etapa 1 (Empatizar)**, después de entrevistas y Empathy Map. Es el último filtro antes de pasar a definir oportunidades.

## Las tres dimensiones de un Job

Todo job tiene tres dimensiones que conviven simultáneamente:

| Dimensión | Qué es | Ejemplo (FinFlow) |
|-----------|--------|-------------------|
| **Funcional** | La tarea concreta a resolver | Facturar a un cliente del exterior |
| **Emocional** | Cómo quiere sentirse | Sentirse profesional, no amateur |
| **Social** | Cómo quiere ser percibido | Que sus clientes lo vean como "una empresa seria" |

Una buena propuesta de valor cubre las tres, no solo la funcional.

## Plantilla del Job Statement

```
Cuando [situación / contexto],
quiero [motivación / acción],
para [resultado esperado / outcome].
```

**Ejemplo simple:**
*"Cuando termino un proyecto con un cliente del exterior, quiero facturar de manera profesional y rápida, para que me paguen a tiempo y yo me sienta como un negocio en serio."*

## Las "fuerzas" que afectan la contratación (Switch Forces)

Modelo de Bob Moesta y Chris Spiek para entender por qué alguien "contrata" o "despide" un producto:

```
        ┌─────────────────────────────────────────┐
        │                                         │
        │    EMPUJAN HACIA EL CAMBIO (Push)       │
        │    Dolor con la situación actual        │
        │                                         │
        └──────────────────┬──────────────────────┘
                           │
                           ▼
        ┌─────────────────────────────────────────┐
        │       SITUACIÓN ACTUAL ────→ SITUACIÓN  │
        │                              DESEADA    │
        └──────────────────┬──────────────────────┘
                           ▲
                           │
        ┌──────────────────┴──────────────────────┐
        │                                         │
        │    ATRACCIÓN DE LO NUEVO (Pull)         │
        │    Promesa de la nueva solución         │
        │                                         │
        └─────────────────────────────────────────┘

        ─────────── FUERZAS QUE FRENAN ───────────

        ┌─────────────────────────────────────────┐
        │   HÁBITO (Habit)                        │
        │   Inercia del comportamiento actual     │
        └─────────────────────────────────────────┘
        ┌─────────────────────────────────────────┐
        │   ANSIEDAD (Anxiety)                    │
        │   Miedos respecto a lo nuevo            │
        └─────────────────────────────────────────┘
```

Para que haya "contratación" (switch), las fuerzas que empujan al cambio deben superar a las que frenan.

## Cómo se usa: protocolo paso a paso

1. **Definí al usuario** y revisá su Empathy Map.
2. **Identificá un evento concreto** donde "contrató" una solución (la última vez que enfrentó el problema).
3. **Reconstruí la historia:**
   - ¿Cuándo empezó a pensar en cambiar?
   - ¿Qué probó antes?
   - ¿Qué lo convenció finalmente?
4. **Formulá el job statement** con la plantilla `Cuando… quiero… para…`.
5. **Identificá las tres dimensiones** (funcional, emocional, social).
6. **Mapeá las cuatro fuerzas** (push, pull, hábito, ansiedad).
7. **Listá los "competidores reales"** (todo lo que el usuario contrataría para el mismo job).

## Ejemplo precompletado: FinFlow

**Usuario:** Camila, diseñadora UX freelance.

**Job Statement principal:**
*"Cuando termino un proyecto con un cliente internacional, quiero gestionar la facturación, cobranza y conversión a ARS de forma confiable y profesional, para sentirme dueña de mi negocio sin perder plata ni tiempo y sin avergonzarme al reclamar."*

**Las tres dimensiones:**

| Dimensión | Job específico |
|-----------|----------------|
| **Funcional** | Generar facturas válidas, hacer seguimiento, recibir el pago, convertir a ARS, registrar para AFIP |
| **Emocional** | Sentirse profesional, en control, tranquila respecto a temas fiscales |
| **Social** | Que sus clientes la vean como "una empresa seria", que sus pares vean que tiene su negocio ordenado |

**Switch forces aplicadas:**

```
PUSH (lo que la empuja al cambio):
- Perdió USD 180 en un mes en comisiones que no entendió
- Cliente se quejó de factura "rara" hecha en Excel
- Pareja le dijo "tenés que organizarte"

PULL (lo que la atrae de la nueva solución):
- Promesa de saber su balance en ARS real al instante
- Templates de factura profesional
- Cobranza automática sin que ella tenga que reclamar

HÁBITO (lo que la frena):
- Excel ya lo tiene armado, "funciona"
- Conoce los pasos, aunque sean tediosos
- Cambiar implica migrar datos

ANSIEDAD (lo que la asusta):
- ¿Y si pierdo facturas viejas?
- ¿Y si el sistema falla y me complica con AFIP?
- ¿Cuánto cuesta? ¿Vale la pena para mi volumen?
```

**Competidores reales (todo lo que cubre el mismo job):**

- QuickBooks / FreshBooks (apps globales)
- Wave, Holded (apps de contabilidad)
- Una planilla de Excel + carpeta de PDFs (status quo)
- Contratar a un contador full service
- No facturar nada y "verlo después" (el competidor más peligroso: la inacción)

**Implicaciones para el diseño:**

1. **Reducir hábito:** ofrecer migración asistida desde Excel.
2. **Bajar ansiedad:** prueba gratuita 30 días, exportación libre, sin lock-in.
3. **Reforzar pull funcional:** la primera pantalla debe mostrar el balance neto en ARS.
4. **Reforzar pull emocional/social:** facturas con diseño profesional, exportables como PDF de marca.

## Tipos de jobs (importante distinguir)

| Tipo | Descripción | Ejemplo |
|------|-------------|---------|
| **Main job** | El objetivo central del usuario | Gestionar su negocio freelance |
| **Related jobs** | Tareas adyacentes que el usuario también querría resolver | Hacer su declaración de ganancias |
| **Emotional jobs** | Sentimientos que el usuario busca | Sentirse en control |
| **Consumption chain jobs** | Tareas para usar el producto en sí | Aprender a usarlo, importar datos |

Innovar muchas veces es resolver **related jobs** o **consumption chain jobs** que los competidores ignoran.

## Tips para aplicarlo bien

- **No confundas job con tarea.** "Llenar formulario de factura" es tarea. "Cobrar de manera profesional" es job.
- **Buscá la abstracción correcta.** Demasiado abstracto ("ser feliz") no sirve; demasiado concreto ("apretar el botón enviar") tampoco.
- **Si el job no tiene dimensión emocional, profundizá más.** Siempre hay una.
- **Validá el job con entrevistas Switch Interview** (preguntar específicamente por la última vez que "contrató" la solución actual).
- **El job es estable; las soluciones cambian.** Por eso es un buen ancla estratégica.

## Conexión con otros frameworks

- **Se alimenta de:** Mom Test (especialmente preguntas sobre pasado), Empathy Map.
- **Alimenta a:**
  - **Opportunity Canvas** (el job define la oportunidad central)
  - **Value Proposition Canvas** (el job va directo al cuadrante de "Jobs" del Customer Profile)
  - **Lean Canvas** (el "Problema" se reformula como "este job mal resuelto")
  - **Story Mapping** (el job es la columna principal en el eje del journey)

## Lectura recomendada

- *Competing Against Luck* — Clayton Christensen
- *The Jobs To Be Done Playbook* — Jim Kalbach
- *When Coffee and Kale Compete* — Alan Klement
