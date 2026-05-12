# 20 — Tipología de MVPs

> Catálogo de formatos de MVP para elegir el más barato según el aprendizaje que necesitás.

---

## Qué es

Un catálogo de tipos de "Minimum Viable Product" (y "Pretotypes" según Alberto Savoia), cada uno diseñado para validar un tipo distinto de hipótesis. La idea: **el formato del MVP debe elegirse según qué querés aprender**, no según qué querés construir.

No todos los MVPs son productos; muchos son experimentos manuales o simulaciones.

## Para qué sirve

- Elegir el experimento más barato que dé la evidencia necesaria.
- Evitar construir productos completos cuando un experimento simple alcanza.
- Validar distintos tipos de hipótesis (interés, viabilidad, usabilidad, modelo).
- Tener un repertorio: la mayoría de equipos solo conocen 1-2 tipos.

## Cuándo usarla

En la **Etapa 5 (Validar)**, después de identificar el RAT y al diseñar cada Test Card. La elección del tipo de MVP es parte del diseño del experimento.

## Catálogo de tipos de MVP

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│ TIPO            │ COSTO    │ TIEMPO  │ APRENDIZAJE PRINCIPAL                    │
├─────────────────┼──────────┼─────────┼──────────────────────────────────────────┤
│ Landing Page    │ Bajo     │ 1-5 d   │ ¿Hay interés? ¿Vale la pena explorar?    │
│ Smoke Test      │ Bajo     │ 5-10 d  │ Disposición a pagar / suscribirse        │
│ Concierge       │ Medio    │ 1-4 sem │ ¿La propuesta de valor resuelve el job?  │
│ Wizard of Oz    │ Medio    │ 1-3 sem │ ¿Funciona el flujo end-to-end?           │
│ Mago de Papel   │ Bajo     │ 1-3 d   │ Usabilidad de un flujo / pantalla        │
│ Prototype Interact.│ Medio │ 1-2 sem │ Usabilidad de un flujo digital           │
│ MVP funcional   │ Alto     │ 2-4 m   │ Comportamiento real en producto v1       │
│ Crowdfunding    │ Medio    │ 1-2 m   │ Disposición a pagar real (dinero ahora)  │
│ Pre-sales       │ Bajo     │ 1-3 sem │ Compromiso real de pago en B2B           │
└─────────────────┴──────────┴─────────┴──────────────────────────────────────────┘
```

## Los tipos explicados en detalle

### 1. Landing Page

**Qué es:** una página web única con propuesta de valor + CTA (captura de email o "Quiero acceso").

**Qué valida:** interés general, claridad del mensaje.

**Visual:**
```
┌────────────────────────────────────┐
│                                    │
│  [Headline: tu propuesta de valor] │
│                                    │
│  [Sub: lo que resuelve y para quién]│
│                                    │
│  [Hero image o screenshot]         │
│                                    │
│  [Beneficios en 3 columnas]        │
│                                    │
│  [Email] [Quiero acceso anticipado]│
│                                    │
└────────────────────────────────────┘
```

**Cuándo usarla:** etapa muy temprana, antes de invertir tiempo de producto. Mide si el headline solo ya genera curiosidad.

**Limitaciones:** "Sí, me interesa" no es lo mismo que "sí, voy a pagar".

### 2. Smoke Test

**Qué es:** landing page que finge que el producto existe y permite "comprar" o "registrarse" → al hacer click, muestra "estamos en lista de espera".

**Qué valida:** **disposición real a comprometerse** (más fuerte que landing simple).

**Ejemplo clásico:** Dropbox. Drew Houston hizo un video de 3 min mostrando el producto que no existía. La lista de espera saltó de 5k a 75k personas. Validado.

**Cuándo usarla:** validar pricing, propuesta de valor concreta, intención de compra.

**Tips:**
- Si pedís tarjeta de crédito (sin cobrar), el dato es mucho más fuerte que solo email.
- Si el visitante hace pre-pago (aunque sea reembolsable), es la validación más fuerte.

### 3. Concierge MVP

**Qué es:** ofrecés el servicio **manualmente, persona a persona**, sin construir software. El cliente recibe el valor real; el equipo aprende qué hace falta automatizar.

**Cuándo usarla:** servicios complejos donde no sabés bien cuál es el flujo crítico.

**Ejemplo clásico:** Food on the Table. Antes de construir la app, el fundador iba personalmente a las casas a planear menús semanales y hacía la lista de compras manualmente.

**Diferencia con Wizard of Oz:** en Concierge el usuario **sabe** que es un humano atendiéndolo; en Wizard of Oz cree que es un sistema automatizado.

### 4. Wizard of Oz

**Qué es:** el usuario interactúa con una interfaz que parece automatizada, pero detrás hay personas haciendo el trabajo manual.

**Cuándo usarla:** cuando el algoritmo / lógica que querés validar es complejo y construirlo es caro, pero la interfaz es simple.

**Ejemplo:** Zappos en sus inicios. Nick Swinmurn no tenía stock; cuando alguien compraba zapatos, él iba al shopping, los compraba y los enviaba personalmente. Validó la hipótesis "la gente compra zapatos online" antes de invertir en logística.

**Tips:**
- Funciona bien para validar matching, recomendación, traducción, soporte AI.
- Tenés que poder responder rápido (los usuarios no esperan).
- No escala más allá del experimento, ese es el punto.

### 5. Mago de Papel (Paper Prototype)

**Qué es:** sketches en papel o whiteboard de las pantallas, mostrados al usuario en orden. El usuario "toca" donde cree que tocaría y vos mostrás la próxima hoja.

**Qué valida:** lógica de flujo, claridad de UX, mental models del usuario.

**Cuándo usarla:** muy temprano en diseño, antes de tocar Figma. Es ultra-barato y genera feedback rico.

**Tips:**
- Usá marcadores gruesos: fuerza simplicidad.
- 5-10 pantallas máximo.
- Después podés escalar a prototipos en Figma/Marvel para validar más.

### 6. Prototype Interactivo (Figma, Marvel, Invision)

**Qué es:** prototipo digital clickeable, sin código real, que simula el producto.

**Qué valida:** usabilidad detallada, mental models en flujo digital.

**Cuándo usarla:** después del mago de papel, antes de construir código.

**Métrica típica:** tasa de éxito en completar tareas + tiempo + cantidad de errores.

### 7. MVP funcional (Minimum Viable Product clásico)

**Qué es:** versión mínima del producto, **real y funcional**, lanzada a usuarios reales.

**Qué valida:** comportamiento real, no declarado. Adopción, retención, NPS.

**Cuándo usarla:** después de varios experimentos previos. **No debería ser tu primer MVP.**

**Atención:** la mayoría de equipos saltan directo acá. Es lo más caro y lo más arriesgado.

### 8. Crowdfunding

**Qué es:** campaña en Kickstarter / Indiegogo / similar donde la gente paga por anticipado por algo que aún no existe.

**Qué valida:** disposición real a pagar + tamaño del mercado.

**Cuándo usarla:** productos físicos o con narrativa clara y emocional. Menos efectivo para SaaS B2B.

**Ejemplo:** Pebble Smartwatch — USD 10 millones en pre-ventas antes de fabricar.

### 9. Pre-sales (B2B)

**Qué es:** vender el producto antes de construirlo, con contratos firmados y pago anticipado (o LOI).

**Qué valida:** disposición a pagar real en B2B.

**Cuándo usarla:** productos B2B donde el ciclo de venta ya implica conversaciones largas.

**Tip:** ofrecer descuento por "early adopter" + lock de precio a cambio de feedback temprano.

## Cómo elegir el tipo de MVP correcto

Use esta tabla decisión:

| ¿Qué querés aprender? | MVP recomendado |
|----------------------|-----------------|
| ¿Hay interés inicial? | Landing Page |
| ¿La gente se inscribe / da email? | Landing Page con captura |
| ¿La gente paga? | Smoke Test (con tarjeta) o Pre-sales |
| ¿La propuesta de valor resuelve el job? | Concierge |
| ¿Funciona el flujo end-to-end con tecnología compleja? | Wizard of Oz |
| ¿Las pantallas son claras? | Mago de Papel → Prototype |
| ¿Cuánto retiene la propuesta a largo plazo? | MVP funcional |
| ¿El mercado es lo suficientemente grande? | Crowdfunding o Smoke Test escalado |
| ¿B2B compraría esto? | Pre-sales / Letter of Intent |

## Cómo se usa: protocolo paso a paso

1. **Tomá la hipótesis priorizada del RAT.**
2. **Identificá el tipo de aprendizaje** que necesitás (interés / comportamiento / pago / usabilidad / retención).
3. **Elegí el MVP más barato** que entregue ese aprendizaje.
4. **Diseñá la Test Card** con ese formato.
5. **Construí lo mínimo indispensable.** Cero features extra.
6. **Ejecutá y medí.**
7. **Documentá con Learning Card.**
8. **Decidí:** ¿el aprendizaje justifica avanzar al siguiente MVP (más grande), o se necesita otro experimento del mismo nivel?

## Ejemplo precompletado: FinFlow

**Hipótesis a validar (orden por RAT):**

| Hipótesis | Tipo de aprendizaje | MVP elegido | Costo estimado |
|-----------|---------------------|-------------|----------------|
| H5: Pricing Pro USD 9 | Disposición a pagar | **Smoke Test** con landing + tarjeta requerida + A/B | USD 800 |
| H2: Cobranza automatizada sube cobros | Funciona el flujo | **Concierge** durante 4 semanas: el equipo envía recordatorios manualmente a 20 freelancers piloto | USD 0 (tiempo equipo) |
| H1: Balance ARS visible aumenta retención | Comportamiento | **Wizard of Oz**: enviar balance ARS por WhatsApp manualmente cada lunes a 30 usuarios durante 6 semanas | USD 200 |
| H3: Canal comunidades CAC < USD 12 | Adquisición real | **Sponsoreo piloto**: 3 comunidades durante 4 semanas con landing dedicada | USD 1.500 |
| H7: API AFIP factible | Aprendizaje técnico | **Spike técnico**: 2 devs senior, 1 sprint, 100 facturas de prueba | USD 0 (tiempo equipo) |

**Flujo recomendado:**

```
Semana 1-2:    Smoke Test (H5)           ──► Learning Card #001
                  │
                  ▼
            ¿pricing validado?
                  │
       ┌──────────┴──────────┐
       ▼ Sí                  ▼ No (pivot)
                          
Semana 3-6:    Concierge (H2)            ──► Learning Card #002
                + Wizard of Oz (H1)      ──► Learning Card #003
                + Spike técnico (H7)     ──► Learning Card #004
                  │
                  ▼
            ¿todo coherente?
                  │
                  ▼
Semana 7-18:  MVP funcional              ──► Lanzamiento + medición
              (con lo validado)
```

**El razonamiento de elegir Concierge para H2 (cobranza):**

- **No** elegimos construir directamente el sistema automatizado: hubiera tomado 6-8 semanas.
- **No** elegimos un smoke test: queríamos validar que la cobranza realmente sube los cobros, no solo el interés.
- **Sí** elegimos Concierge: el equipo asigna 1 persona a enviar recordatorios manualmente desde una identidad "FinFlow Cobranzas" a 20 freelancers piloto durante 4 semanas. Se mide el porcentaje de facturas cobradas dentro de 30 días vs. baseline.
- **Costo real:** 0 dinero, ~8 horas/semana de una persona.
- **Aprendizaje esperado:** si el flujo manual mejora los cobros del 55% al 75%, validamos que vale la pena automatizar. Si no, sabemos que el problema no era el recordatorio, era otra cosa.

## Tips para no equivocarte de tipo de MVP

- **No elijas el tipo que ya sabés construir.** Elegí el más barato para el aprendizaje que necesitás.
- **No construyas software cuando podés simular manualmente.** Concierge y Wizard of Oz son subutilizados.
- **El Smoke Test es para hipótesis de viabilidad/interés, no de usabilidad.** No mide si la app es usable.
- **MVP funcional viene después de varios experimentos previos.** Si saltás directo, es porque querés "lanzar", no validar.
- **Combiná múltiples MVPs.** Una sola hipótesis bien validada puede requerir 2-3 experimentos distintos.

## Errores comunes

| Error | Por qué falla |
|-------|---------------|
| MVP = primera versión del producto | Te lleva a construir antes de validar |
| Saltarse Concierge / Wizard of Oz | Construís features que el usuario no necesita |
| Landing sin captura de compromiso | Datos demasiado débiles para decidir |
| Pre-sales sin LOI firmado | "Sí, lo compraría" no es venta |
| Smoke Test con copy del producto sin sentido | Aprenderás algo distinto a lo que querés |

## Conexión con otros frameworks

- **Se alimenta de:** RAT, Plantilla de Hipótesis.
- **Alimenta a:**
  - **Test Card** (especifica el formato del experimento)
  - **Story Mapping** (lo que NO está en el MVP queda en V2+)
  - **Learning Card** (resultado del experimento)

## Lectura recomendada

- *Testing Business Ideas* — David J. Bland & Alex Osterwalder (catálogo de 44 experimentos).
- *The Right It* — Alberto Savoia (concepto de Pretotype).
- *The Lean Startup* — Eric Ries (cap. sobre tipos de MVP).
- Steve Blank — *The Four Steps to the Epiphany* (Customer Development).
