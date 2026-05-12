# 16 — Plantilla de Hipótesis

> Estructura formal de Lean Startup para convertir supuestos en hipótesis testeables.

---

## Qué es

Una plantilla derivada del método científico aplicada al desarrollo de productos. Cada supuesto del negocio se reescribe como una hipótesis con:

- **Una afirmación falsable** (que podría ser falsa).
- **Una predicción medible** (qué pasará si es verdadera).
- **Un criterio de validación claro** (qué número o señal lo confirma o refuta).

Si no podés formularlo así, no es una hipótesis: es una opinión.

## Para qué sirve

- Convertir supuestos vagos en afirmaciones precisas.
- Forzar al equipo a comprometerse con un criterio de validación **antes** de tener el dato.
- Evitar el "hindsight bias" (interpretar el resultado como confirmación post-hoc).
- Generar disciplina experimental.
- Documentar aprendizajes para no repetir experimentos.

## Cuándo usarla

En la **Etapa 5 (Validar)**, después de tener Lean Canvas + Value Proposition Canvas. Cada bloque marcado como `[H]` (hipótesis) en esos canvas se redacta usando esta plantilla.

## La plantilla principal

```
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│   Creemos que [SUPUESTO]                                       │
│                                                                │
│   Para [USUARIO / SEGMENTO]                                    │
│                                                                │
│   Resolverá / generará [RESULTADO ESPERADO]                    │
│                                                                │
│   Lo sabremos cuando [CRITERIO DE VALIDACIÓN MEDIBLE]          │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

**Ejemplo simple:**

> Creemos que **mostrar el balance neto en ARS en tiempo real en el dashboard**
> Para **freelancers que cobran en USD desde Argentina**
> Resolverá **la incertidumbre sobre cuánto ganaron realmente en ARS**
> Lo sabremos cuando **el 70% de los usuarios que vean el dashboard regresen al menos 3 veces en la primera semana** y **el NPS de la feature sea > +30**.

## Las 4 tipologías de hipótesis (Lean Startup)

Eric Ries propone clasificar cada hipótesis en una de cuatro tipologías:

| Tipo | Pregunta que responde | Ejemplo |
|------|----------------------|---------|
| **Valor** | ¿Los usuarios encuentran valor en esto? | "Los freelancers usan el dashboard 3+ veces/semana" |
| **Crecimiento** | ¿Cómo se descubre/comparte el producto? | "El 20% de los usuarios invitan a otro freelancer en su primer mes" |
| **Viabilidad** | ¿Hay un negocio rentable detrás? | "Los freelancers están dispuestos a pagar USD 9/mes" |
| **Factibilidad** | ¿Podemos construirlo / operarlo? | "Podemos procesar 10k facturas/día sin que la latencia supere 2s" |

Una hipótesis bien formulada se enfoca en **una sola tipología** a la vez. Si tu hipótesis combina varias, separala.

## Cómo se usa: protocolo paso a paso

1. **Listá todos los supuestos del Lean Canvas + VPC** marcados como `[H]`.
2. **Para cada supuesto, redactá una hipótesis** usando la plantilla.
3. **Clasificá cada hipótesis** según tipología (valor / crecimiento / viabilidad / factibilidad).
4. **Asegurate de que cada hipótesis sea:**
   - **Falsable:** podría ser falsa.
   - **Específica:** un sujeto, un resultado, un número.
   - **Temporal:** "en la primera semana", "en 30 días", "en cohort mes 1".
   - **Medible:** con un dato cuantitativo, no con percepción.
5. **Priorizá las hipótesis** con RAT (siguiente ficha).
6. **Para cada hipótesis priorizada, diseñá una Test Card.**
7. **Documentá las hipótesis** en un repositorio único. Marcá su estado: pendiente / en validación / validada / refutada.

## Hipótesis bien formuladas vs. mal formuladas

| ❌ Mal formulada | ✅ Bien formulada |
|------------------|-------------------|
| "Los freelancers van a amar nuestra app" | "El 70% de los freelancers que prueban FinFlow en su primer mes regresan al menos 3 veces en los siguientes 7 días" |
| "Necesitamos integración con WhatsApp" | "Si agregamos recordatorios por WhatsApp, la tasa de cobranza dentro de los 30 días subirá del 60% al 75% en cohortes de usuarios activos" |
| "El pricing está bien" | "Al menos el 40% de los visitantes que ven el plan Pro USD 9/mes harán click en 'Suscribirme', medido en una landing dedicada en una campaña de 7 días" |
| "La conversión de free a pago va a ser buena" | "El 8% de los usuarios free se convertirán a Pro dentro de los primeros 60 días, sin promociones especiales" |

## Ejemplo precompletado: FinFlow

**Contexto:** equipo de FinFlow está iniciando Etapa 5. Tiene Lean Canvas V2 con varios `[H]`. Las desglosa en hipótesis testeables.

### Hipótesis de Valor

**H1 — Valor del balance ARS en tiempo real**
> Creemos que **mostrar el balance neto en ARS al instante después de cargar una factura en USD**
> Para **freelancers argentinos con ingresos > USD 2k/mes**
> Resolverá **la incertidumbre sobre cuánto ganaron realmente**
> Lo sabremos cuando **el 70% de los usuarios visiten el dashboard ≥ 3 veces/semana en sus primeros 14 días Y el NPS de la feature sea > +30**.

**H2 — Valor de cobranza automatizada**
> Creemos que **enviar recordatorios automáticos de cobranza desde una identidad profesional (no del freelancer)**
> Para **freelancers que tienen pagos atrasados frecuentes**
> Resolverá **el dolor emocional de reclamar pagos**
> Lo sabremos cuando **el porcentaje de facturas cobradas dentro de los 30 días suba del 55% (baseline) al 75% en la cohorte que activa la feature**.

### Hipótesis de Crecimiento

**H3 — Canal comunidades**
> Creemos que **sponsoreos en 5 grupos de WhatsApp/Discord de freelancers**
> Para **freelancers latinoamericanos activos en comunidades digitales**
> Generará **un CAC promedio < USD 12 y al menos 200 signups/mes**
> Lo sabremos cuando **luego de 8 semanas de actividad, el costo blended por signup sea ≤ USD 12 y el volumen ≥ 200 signups/mes**.

**H4 — Referidos**
> Creemos que **un programa "1 mes gratis por cada amigo que active"**
> Para **usuarios Pro activos**
> Generará **un factor viral K > 0.3**
> Lo sabremos cuando **en los primeros 90 días del programa, los usuarios activos generen en promedio 0.3 nuevos signups activados**.

### Hipótesis de Viabilidad

**H5 — Disposición a pagar Pro**
> Creemos que **el plan Pro a USD 9/mes**
> Para **freelancers latinoamericanos con > USD 2k/mes**
> Resolverá **la necesidad de pricing accesible vs. herramientas globales (USD 30+/mes)**
> Lo sabremos cuando **al menos el 6% de los usuarios free conviertan a Pro dentro de los 60 días sin promociones especiales**.

**H6 — Plan Studio**
> Creemos que **el plan Studio a USD 19/mes con multi-usuario**
> Para **estudios pequeños de 2-5 freelancers que trabajan juntos**
> Generará **un ARPU ponderado mayor**
> Lo sabremos cuando **al menos el 1% de los usuarios totales estén en plan Studio en el mes 6**.

### Hipótesis de Factibilidad

**H7 — Integración API AFIP**
> Creemos que **podemos construir la integración con la API de facturación electrónica de AFIP**
> Para **el equipo técnico (2 devs senior)**
> Resolverá **la emisión automatizada de facturas tipo C/E**
> Lo sabremos cuando **logremos emitir 100 facturas de prueba con < 1% de error en un sprint de 3 semanas**.

**H8 — WhatsApp Business API**
> Creemos que **la integración con WhatsApp Business API**
> Para **el sistema de cobranza automatizada**
> Resolverá **el envío de recordatorios sin que el freelancer firme cada uno**
> Lo sabremos cuando **logremos aprobación del template de mensajes y volumen 1000 mensajes/día con costo < USD 0.10/mensaje en piloto**.

### Hoja de control de hipótesis

```
┌──────┬──────────────────────────┬─────────────┬───────────┬───────────────┐
│ ID   │ Hipótesis                │ Tipo        │ Prioridad │ Estado        │
├──────┼──────────────────────────┼─────────────┼───────────┼───────────────┤
│ H1   │ Balance ARS              │ Valor       │ Alta      │ En validación │
│ H2   │ Cobranza automatizada    │ Valor       │ Alta      │ Pendiente     │
│ H3   │ Canal comunidades        │ Crecimiento │ Alta      │ En validación │
│ H4   │ Referidos                │ Crecimiento │ Media     │ Pendiente     │
│ H5   │ Pricing Pro USD 9        │ Viabilidad  │ Crítica   │ En validación │
│ H6   │ Plan Studio              │ Viabilidad  │ Baja      │ Pendiente     │
│ H7   │ API AFIP                 │ Factibilidad│ Alta      │ Validada      │
│ H8   │ WhatsApp Business API    │ Factibilidad│ Alta      │ Refutada      │
└──────┴──────────────────────────┴─────────────┴───────────┴───────────────┘
```

**H8 refutada:** WhatsApp Business API tiene aprobación demorada y costos altos. **Pivotar** a recordatorios por email + SMS para MVP, dejar WhatsApp para V2.

## Tips para formular buenas hipótesis

- **Si no podés decir "podría estar equivocado", no es hipótesis.**
- **Cuantificá siempre el criterio.** "Mucha gente" no es criterio; "el 70% en 14 días" sí.
- **Hacé el criterio difícil de mover post-hoc.** Si no lo escribiste antes del experimento, no vale.
- **Una hipótesis por experimento.** Si querés validar tres cosas, hacé tres experimentos.
- **Hipótesis nulas también son válidas.** "Esperamos NO ver diferencia entre A y B" es información.

## Errores comunes

| Error | Por qué falla |
|-------|---------------|
| Hipótesis ambigua | No se puede validar/refutar |
| Múltiples variables | No sabés cuál impacta |
| Criterio elegido post-hoc | Sesgo de confirmación |
| Resultados directos como hipótesis | "Tendremos 1000 usuarios" no es hipótesis, es objetivo |
| Confirmar en lugar de testear | Diseñar el experimento para que dé sí |

## Conexión con otros frameworks

- **Se alimenta de:** Lean Canvas (cada `[H]`), Value Proposition Canvas (cada fit es hipótesis), Pre-mortem (riesgos top), Opportunity Solution Tree (cada solución implica hipótesis).
- **Alimenta a:**
  - **RAT** (priorización de hipótesis)
  - **Test Card** (cada hipótesis genera una Test Card)
  - **Learning Card** (el resultado se documenta)
  - **Tipología de MVPs** (el tipo de hipótesis determina el formato MVP)

## Lectura recomendada

- *The Lean Startup* — Eric Ries (cap. sobre validated learning).
- *Testing Business Ideas* — David J. Bland & Alex Osterwalder (catálogo de experimentos).
- Strategyzer — Test Cards y Hypothesis Templates (descargables).
