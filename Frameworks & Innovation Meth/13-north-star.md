# 13 — North Star Metric (NSM) / Framework

> La métrica única que captura el valor que tu producto entrega al usuario y, al moverse, mueve al negocio.

---

## Qué es

Un framework popularizado por **Amplitude** y **Sean Ellis** (creador del concepto de Product-Market Fit) que sostiene que toda compañía debe tener **una única métrica principal** que represente el valor entregado al usuario. Si esa métrica sube, el negocio crece como consecuencia.

**Frase clave:** *"La North Star Metric es el output del valor que tu producto entrega; el revenue es el output de ese valor capturado."*

## Para qué sirve

- Alinear a toda la organización detrás de un norte único.
- Evitar optimizar métricas que no representan valor real (vanity metrics).
- Conectar acciones del equipo con impacto real.
- Tomar decisiones de roadmap rápidas: ¿esto mueve la NSM o no?
- Comunicar tracción de manera clara a inversores y equipo.

## Cuándo usarlo

En la **Etapa 4 (Diseñar la propuesta)** se define la NSM. En la **Etapa 5 (Validar)** se mide. Se revisita anualmente porque a medida que el producto madura, la NSM puede evolucionar.

## Las 3 características de una buena NSM

1. **Representa valor para el usuario.** No es revenue, no es signups. Es un proxy de cuándo el usuario obtiene valor.
2. **Es predictiva del negocio.** Si sube la NSM, el revenue sube como consecuencia (con cierto lag).
3. **Es accionable.** El equipo puede mover esta métrica con su trabajo diario.

## Estructura del framework

```
                ┌──────────────────────────────────┐
                │      NORTH STAR METRIC           │
                │  (la métrica única de valor)     │
                └────────────────┬─────────────────┘
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
   ┌────▼────┐              ┌────▼────┐              ┌────▼────┐
   │ INPUT 1 │              │ INPUT 2 │              │ INPUT 3 │
   │(breadth)│              │ (depth) │              │(frequen-│
   │ Cuántos │              │  Qué    │              │  cy)    │
   │ usuarios│              │  tan    │              │ Cada    │
   │         │              │  intenso│              │ cuánto  │
   └─────────┘              └─────────┘              └─────────┘
        │                        │                        │
        ▼                        ▼                        ▼
   ¿Qué acción del          ¿Qué acción del          ¿Qué acción del
   equipo lo mueve?         equipo lo mueve?         equipo lo mueve?
```

**Las 3 dimensiones típicas de inputs:**

- **Breadth (amplitud):** ¿cuántos usuarios distintos lo hacen?
- **Depth (profundidad):** ¿qué tan intensamente lo hacen?
- **Frequency (frecuencia):** ¿con qué frecuencia lo hacen?
- **Efficiency (eficiencia):** ¿qué tan rápido / fácil lo hacen? (a veces se suma como cuarta dimensión)

## Ejemplos de NSM reales

| Empresa | NSM | Por qué funciona |
|---------|-----|------------------|
| **Airbnb** | Noches reservadas | Captura valor entregado (huéspedes + anfitriones) |
| **Spotify** | Tiempo de escucha | Más escucha = más valor recibido |
| **Slack** | Mensajes enviados por equipo activo | Si los equipos chatean mucho, están enganchados |
| **WhatsApp** | Mensajes enviados | Valor central del producto |
| **Facebook** | Daily Active Users (DAU) | Engagement repetido |
| **Amazon** | Productos comprados por cliente / mes | Frecuencia + amplitud de compras |

**Ojo:** "usuarios registrados" o "MRR" NO son buenas NSM. La primera no mide valor entregado, la segunda mide valor capturado (consecuencia).

## Contramétricas (Counter Metrics)

Toda NSM puede ser hackeada o crecer a costa de otra cosa importante. Las **contramétricas** son las que vigilás para que la NSM no te haga daño:

| Si tu NSM es… | Contramétrica clave |
|---------------|---------------------|
| Tiempo en la app | Net Promoter Score (que el tiempo no sea por frustración) |
| Mensajes enviados | Spam reportado / churn |
| Pedidos completados | Tasa de devolución / cancelación |
| Sesiones por usuario | Burnout / unsubscribe rate |

## Cómo se usa: protocolo paso a paso

1. **Definí el momento "aha"** de tu producto: ¿cuándo el usuario obtiene valor real?
2. **Convertilo en una métrica medible** que combine usuario + acción + frecuencia.
   - Plantilla: `[Sujeto] que [acción de valor] [con qué frecuencia]`.
3. **Validá las 3 características:** ¿representa valor? ¿es predictiva? ¿es accionable?
4. **Descomponela en 3-4 inputs** (breadth, depth, frequency, efficiency).
5. **Para cada input, listá las acciones del equipo** que lo mueven.
6. **Definí contramétricas.**
7. **Mostrala en un dashboard visible para todo el equipo.** Si no la ve nadie, no funciona.

## Ejemplo precompletado: FinFlow

**Momento "aha" del usuario:** la primera vez que ve su balance neto en ARS al instante después de cobrar una factura en USD, sin tener que calcular nada manualmente.

**NSM candidata:**

> **Facturas emitidas Y cobradas por usuario activo / mes**

(Ojo a la conjunción "emitidas Y cobradas": ambas tienen que pasar para contar como evento.)

**Por qué funciona:**

| Característica | Cumple |
|----------------|--------|
| Representa valor para el usuario | ✅ El valor central de FinFlow es facturar + cobrar profesionalmente. |
| Predictiva del negocio | ✅ Cada factura cobrada aumenta engagement → reduce churn → aumenta MRR. |
| Accionable por el equipo | ✅ El equipo puede mejorar features de emisión (templates) y de cobranza (recordatorios). |

**Descomposición en inputs:**

```
                ┌─────────────────────────────────────────┐
                │ NSM: Facturas emitidas y cobradas /     │
                │       usuario activo / mes              │
                └─────────────────┬───────────────────────┘
                                  │
         ┌────────────────────────┼────────────────────────┐
         │                        │                        │
   ┌─────▼─────┐           ┌──────▼─────┐          ┌───────▼─────┐
   │ BREADTH   │           │   DEPTH    │          │  EFFICIENCY │
   │           │           │            │          │             │
   │ % usuarios│           │ Facturas   │          │ Días entre  │
   │ activos   │           │ promedio   │          │ emisión y   │
   │ que       │           │ por        │          │ cobro       │
   │ facturaron│           │ usuario    │          │             │
   │ en el mes │           │ activo/mes │          │             │
   └─────┬─────┘           └──────┬─────┘          └───────┬─────┘
         │                        │                        │
         ▼                        ▼                        ▼
  Acciones:                Acciones:                 Acciones:
  • Onboarding asistido    • Templates más rápidos   • Recordatorios
  • Importación Excel      • Recurrencia auto-       • Link de pago
  • Notificaciones de        sugerida                  embebido
    "todavía no facturaste"• Multi-cliente en una    • Cobranza
                            sola pantalla              automatizada
```

**Contramétricas (lo que vigilamos para que la NSM no nos lastime):**

| Contramétrica | Por qué |
|---------------|---------|
| Churn mensual | Si los usuarios facturan mucho pero se van, hay un problema |
| NPS / CSAT | Que las facturas se emitan no signifique que el usuario esté contento |
| Tickets de soporte por usuario | Volumen de facturas puede esconder fricción |
| % de facturas con errores fiscales | Calidad de la emisión, no solo cantidad |

**Dashboard mensual del equipo:**

```
┌────────────────────────────────────────────────────────────────┐
│ NORTH STAR: Facturas emitidas y cobradas / user activo / mes   │
│                                                                │
│           Q1 2026: 3.2  →  Q2 2026: 4.1  →  Meta Q3: 5.0       │
│                                                                │
│           ↑ +28% trimestre a trimestre                         │
├────────────────────────────────────────────────────────────────┤
│ INPUTS                                                         │
│                                                                │
│ Breadth:    62% usuarios activos facturando (meta: 75%)        │
│ Depth:      5.4 facturas / usuario que factura (meta: 6.5)     │
│ Efficiency: 21 días emisión-cobro (meta: 14 días)              │
├────────────────────────────────────────────────────────────────┤
│ CONTRAMÉTRICAS                                                 │
│                                                                │
│ Churn mensual:        4.2% (límite: 5%) ✅                     │
│ NPS:                  +38 (límite: > 30) ✅                    │
│ Errores fiscales:     0.8% facturas (límite: < 2%) ✅          │
└────────────────────────────────────────────────────────────────┘
```

## Tips para definir una buena NSM

- **No sea ingresos directos.** Si tu NSM es el MRR, vas a tomar decisiones de corto plazo que castigan al usuario.
- **No sea vanity metric.** "Visitas a la web" o "usuarios registrados" no miden valor entregado.
- **Sea fácil de explicar.** Si necesitás 3 párrafos para definirla, no funciona como norte.
- **Tenga una unidad temporal.** "X por mes" / "X por semana" mejor que solo "X".
- **Combiná amplitud + intensidad** cuando puedas: "X por usuario activo / mes" es más rico que solo "X totales".
- **Revisitala anualmente.** Una NSM que funcionó en early stage puede no servir en growth stage.

## Errores comunes

| Error | Síntoma | Solución |
|-------|---------|----------|
| Usar revenue como NSM | Se postergan inversiones en valor de usuario | Revenue es output, no NSM |
| NSM no accionable | El equipo no sabe qué hacer cuando baja | Descomponé en inputs claros |
| Sin contramétricas | NSM crece pero el producto se rompe | Definí 2-3 contramétricas desde el día 1 |
| Cambiar la NSM cada trimestre | El equipo no construye memoria | Una NSM debería durar 12-24 meses mínimo |
| Múltiples NSMs | El equipo se confunde | Una sola NSM por unidad de negocio |

## Conexión con otros frameworks

- **Se alimenta de:** Opportunity Canvas (métricas), Value Proposition Canvas (qué valor entregás), JTBD (cuándo el usuario obtiene valor).
- **Alimenta a:**
  - **AARRR** (los inputs de la NSM suelen mapearse a Activation y Retention)
  - **Roadmap** (cada feature se evalúa por su contribución a la NSM)
  - **OKRs** (la NSM es el Objective principal de la compañía)
  - **Dashboard de equipo** (el norte permanente del producto)

## Lectura recomendada

- *Hacking Growth* — Sean Ellis & Morgan Brown.
- Amplitude — *The North Star Playbook* (gratis en amplitude.com).
- John Cutler — posts sobre North Star (Twitter y Substack).
