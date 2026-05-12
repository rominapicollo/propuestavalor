# 21 — AARRR (Pirate Metrics)

> Framework de métricas de funnel de Dave McClure: Acquisition, Activation, Retention, Referral, Revenue.

---

## Qué es

Un framework creado por **Dave McClure** (500 Startups) que descompone el customer journey en cinco etapas operativas, cada una con sus propias métricas. Se llama "Pirate Metrics" porque las iniciales suenan a "AARRR!" como el grito de un pirata.

A diferencia de la North Star Metric (que es **una sola** métrica de valor), AARRR es un **funnel completo** que te permite ver dónde se pierden usuarios en cada etapa.

## Para qué sirve

- Identificar cuál es la etapa débil del funnel y enfocar mejoras ahí.
- Medir el negocio de manera operativa, no solo estratégica.
- Asignar responsabilidades por etapa (Growth/Marketing → Acquisition; Producto → Activation/Retention; etc.).
- Detectar leaks antes de invertir en más adquisición.
- Comunicar tracción a inversores y stakeholders.

## Cuándo usarlo

En la **Etapa 5 (Validar)** y siguiente, cuando ya tenés tracción y usuarios reales pasando por tu producto. Antes de tener tracción es prematuro y te puede llevar a optimizar prematuramente.

## Las 5 etapas

```
                    ADQUISICIÓN
                    ▼
┌──────────────────────────────────────┐
│    A  Acquisition                    │   ← Visitantes
│       (cómo llegan)                  │
└──────────────────────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────┐
│    A  Activation                     │   ← Primer "aha moment"
│       (primera experiencia exitosa)  │
└──────────────────────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────┐
│    R  Retention                      │   ← Vuelven y siguen usando
│       (los que vuelven y siguen)     │
└──────────────────────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────┐
│    R  Referral                       │   ← Recomiendan a otros
│       (recomiendan / invitan)        │
└──────────────────────────────────────┘
                    │
                    ▼
┌──────────────────────────────────────┐
│    R  Revenue                        │   ← Pagan
│       (generan ingresos)             │
└──────────────────────────────────────┘
                    │
                    ▼
                    DINERO
```

**Nota:** algunas variantes ponen Revenue antes de Referral. La idea es que después de pagar, el usuario contento se vuelve referenciador.

## Cada etapa en detalle

### A — Acquisition (Adquisición)

**Pregunta:** ¿cómo descubren tu producto?

**Métricas clave:**
- Visitantes únicos / mes.
- Tráfico por canal (orgánico, paid, referral, direct).
- CAC (Costo de Adquisición de Cliente) por canal.
- CPC (Costo por Click).
- Conversion rate visitor → signup.

**Responsables típicos:** Marketing, Growth, SEO/SEM.

**Señal de problema:** mucho tráfico pero pocos signups → problema de match canal/mensaje, o de promesa engañosa.

### A — Activation (Activación)

**Pregunta:** ¿el usuario tiene su primera experiencia exitosa?

**Métricas clave:**
- Activation Rate (% de signups que completan la acción clave).
- Time to First Value (cuánto tarda en alcanzar el "aha moment").
- % de usuarios que completan el onboarding.

**Responsables típicos:** Producto, UX, Onboarding.

**Señal de problema:** mucha gente se registra pero pocos llegan al "aha". Generalmente es un problema de onboarding o de fricción en el flujo crítico.

**Concepto clave:** definí qué acción es el "aha moment" para tu producto.
- Para Slack: enviar 2.000 mensajes en un equipo.
- Para Facebook: tener 7 amigos en 10 días.
- Para FinFlow: emitir Y cobrar la primera factura.

### R — Retention (Retención)

**Pregunta:** ¿los usuarios siguen volviendo y usándolo?

**Métricas clave:**
- DAU/MAU (Daily Active Users / Monthly Active Users).
- Stickiness = DAU/MAU (cuanto más cerca de 1, más "diaria" la app).
- Cohort retention curves (Day 1, Day 7, Day 30, etc.).
- Churn rate mensual.

**Responsables típicos:** Producto.

**Señal de problema:** retención que cae rápido a 0 en cohortes = producto sin Product-Market Fit.

**Benchmark de Sean Ellis:** si el 40% de tus usuarios dice que estaría "muy decepcionado" si tu producto desapareciera, tenés PMF.

### R — Referral (Referidos)

**Pregunta:** ¿los usuarios traen a otros?

**Métricas clave:**
- Factor viral (K-factor) = invitaciones por usuario × tasa de conversión de invitación.
- % de signups que vienen de referidos.
- NPS (Net Promoter Score).

**Responsables típicos:** Producto + Growth (programa de referidos).

**Señal de problema:** K < 0.3 indica que el growth no es viral. Si necesitás scale, requerirá más inversión en paid.

**Concepto clave:**
- K > 1 = crecimiento viral exponencial (raro).
- K = 0.3 — 0.7 = referidos contribuyen, pero no son el motor único.
- K < 0.2 = el motor del growth es otro (paid, content, sales).

### R — Revenue (Ingresos)

**Pregunta:** ¿el producto genera ingresos sostenibles?

**Métricas clave:**
- MRR (Monthly Recurring Revenue).
- ARPU (Average Revenue Per User).
- LTV (Lifetime Value).
- Ratio LTV/CAC (objetivo: > 3x).
- Payback period (cuántos meses tarda en recuperarse el CAC).

**Responsables típicos:** Negocio, Pricing, Sales (B2B).

**Señal de problema:** LTV/CAC < 1 = perdés dinero por cada cliente. LTV/CAC entre 1 y 3 = sobrevivís pero no podés escalar.

## Cómo se usa: protocolo paso a paso

1. **Definí el funnel específico** de tu producto (cómo se ve cada etapa para vos).
2. **Definí la métrica principal de cada etapa.** Empezá con una sola por etapa.
3. **Definí la "acción clave" de Activation** (tu "aha moment").
4. **Implementá el tracking** (analytics: Mixpanel, Amplitude, GA, etc.).
5. **Establecé baselines** después de 1-2 meses de tracking.
6. **Identificá la etapa más débil** (el "leak" más grande).
7. **Concentrá esfuerzos en mejorar esa etapa** (no en mejorar todas a la vez).
8. **Revisitá mensualmente** y ajustá el foco.

## Ejemplo precompletado: FinFlow

**Funnel completo definido:**

```
┌──────────────────────────────────────────────────────────────────┐
│ ACQUISITION                                                      │
│ Definición: visitante único llega a finflow.app                  │
│ Métrica principal: visitantes únicos / mes                       │
│ Canales: comunidades (40%), SEO (30%), paid (20%), referidos (10%)│
├──────────────────────────────────────────────────────────────────┤
│                          ↓                                       │
├──────────────────────────────────────────────────────────────────┤
│ ACTIVATION                                                       │
│ Definición: usuario emite Y cobra su primera factura             │
│ Métrica principal: % signups que activan en 14 días              │
│ Submétricas:                                                     │
│   - % completan onboarding                                       │
│   - % cargan al menos 1 cliente                                  │
│   - % emiten al menos 1 factura                                  │
│   - % marcan al menos 1 factura como cobrada                     │
├──────────────────────────────────────────────────────────────────┤
│                          ↓                                       │
├──────────────────────────────────────────────────────────────────┤
│ RETENTION                                                        │
│ Definición: usuario activo en mes N+1 después de activar          │
│ Métrica principal: retention en cohortes (Day 7, 30, 60, 90)    │
│ Stickiness: DAU/MAU                                              │
│ Churn objetivo: < 5%/mes                                         │
├──────────────────────────────────────────────────────────────────┤
│                          ↓                                       │
├──────────────────────────────────────────────────────────────────┤
│ REVENUE                                                          │
│ Definición: usuario paga al menos 1 mes de plan Pro              │
│ Métrica principal: MRR                                           │
│ Submétricas: ARPU, LTV, % conversión free → Pro                  │
├──────────────────────────────────────────────────────────────────┤
│                          ↓                                       │
├──────────────────────────────────────────────────────────────────┤
│ REFERRAL                                                         │
│ Definición: usuario invita y trae a otro freelancer              │
│ Métrica principal: K-factor                                      │
│ NPS objetivo: > +30                                              │
└──────────────────────────────────────────────────────────────────┘
```

**Dashboard mensual de FinFlow (ejemplo del mes 6):**

```
┌─────────────────────────────────────────────────────────────────────┐
│  AARRR DASHBOARD — JUNIO 2026                                       │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│ ACQUISITION                                                         │
│ ─────────────                                                       │
│   Visitantes únicos:        12.400  (+18% vs mes anterior)          │
│   Signups:                   1.450  (= 11.7% conv. visit→signup)    │
│   CAC blended:                USD 9  (objetivo: < USD 12)           │
│   CAC por canal:                                                    │
│     Comunidades:   USD 4   ✅                                       │
│     SEO:           USD 2   ✅                                       │
│     Paid:          USD 28  🔴  (alto, pivotear)                     │
│     Referrals:     USD 0   ✅                                       │
│                                                                     │
│ ACTIVATION                                                          │
│ ───────────                                                         │
│   Signups del mes:           1.450                                  │
│   Activated en 14 días:        490  (= 33.8%)  🔴 LEAK PRINCIPAL    │
│   Funnel detallado:                                                 │
│     Completan onboarding:  72%                                      │
│     Cargan ≥1 cliente:     58%                                      │
│     Emiten ≥1 factura:     41%                                      │
│     Marcan ≥1 cobrada:     34%                                      │
│                                                                     │
│ RETENTION                                                           │
│ ───────────                                                         │
│   D1 retention:   71%   ✅                                          │
│   D7 retention:   48%   ✅                                          │
│   D30 retention:  34%   🟡 (objetivo: 40%)                          │
│   Churn mensual Pro:  4.2%  ✅                                      │
│   Stickiness (DAU/MAU): 0.22                                        │
│                                                                     │
│ REVENUE                                                             │
│ ───────────                                                         │
│   MRR:              USD 14.500  (+22% vs mes anterior)              │
│   Users Pro:        2.150                                           │
│   ARPU:             USD 6.74                                        │
│   LTV estimado:     USD 161 (24 meses promedio)                     │
│   LTV/CAC:          17.9x (excluyendo paid)                         │
│   LTV/CAC blended:  17.9x  ✅                                       │
│   Conversion free → Pro: 7.1% en 60 días                            │
│                                                                     │
│ REFERRAL                                                            │
│ ───────────                                                         │
│   Signups por referido:  142  (= 9.8% del total)                    │
│   K-factor:              0.18                                        │
│   NPS:                   +38   ✅                                    │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

**Análisis y acciones:**

**Leak principal: Activation.** Solo el 33.8% de los signups completa el flujo de "emitir y marcar cobrada una factura". Este es el cuello de botella.

**Decisión del equipo (próximos 90 días):**
1. **Foco prioritario en Activation:** mejorar el funnel desde "completan onboarding" (72%) hasta "marcan cobrada" (34%). Hipótesis: la barrera entre "cargan cliente" y "emiten factura" es la mayor (58% → 41% = -17 puntos).
   - Test #1: tutorial guiado en la emisión de la primera factura.
   - Test #2: factura de ejemplo prellenada con datos ficticios para que el usuario vea cómo queda.
   - Test #3: importación masiva desde Excel para acelerar el setup.
2. **Pausar canal Paid temporalmente.** USD 28 CAC vs USD 9 blended → estamos pagando por usuarios que no activan. Realocar presupuesto a content + comunidades.
3. **Mejorar K-factor.** 0.18 es bajo. Lanzar programa de referidos "1 mes gratis por cada amigo que active".
4. **Mantener pricing:** LTV/CAC de 17.9x es saludable. No tocar.

## Adaptaciones del framework

| Variante | Diferencia |
|----------|------------|
| **HEART (Google)** | Happiness, Engagement, Adoption, Retention, Task success. Más enfocado en UX. |
| **OKR + AARRR** | Cada etapa AARRR se convierte en un Key Result. |
| **RARRA (Lenny Rachitsky)** | Reordena: Retention, Activation, Referral, Revenue, Acquisition. Pone retención primero porque sin ella el resto no importa. |
| **NSM + AARRR** | La North Star Metric es el output; AARRR son los drivers que la mueven. |

**Tendencia actual:** muchos equipos abandonan AARRR puro y se mueven a RARRA, dada la importancia de la retención.

## Tips para que el framework funcione

- **Definí "Activation" con cuidado.** El aha moment debe correlacionar con retención a largo plazo, no ser arbitrario.
- **Trackeá cohortes, no totales.** Total retention engaña por el efecto de nuevos signups.
- **No optimicés todas las etapas a la vez.** Concentrate en la más débil (el "biggest leak first").
- **Mostralo en un dashboard visible** para todo el equipo, mensualmente.
- **Conectalo con la North Star.** AARRR son los drivers; la North Star es el output integral.

## Errores comunes

| Error | Cómo evitarlo |
|-------|---------------|
| Optimizar Acquisition con Activation rota | Resolvé Activation primero, después escala Acquisition |
| Confundir signup con Activation | Signup = registro; Activation = primera experiencia exitosa |
| Medir solo totales, no cohortes | Cohortes muestran si el producto mejora con el tiempo |
| Vanity metrics (DAU absoluto sin contexto) | Acompañalas con métricas relacionales (DAU/MAU, retention) |
| Ignorar Referral hasta tener "muchos usuarios" | Construir las mecánicas de referral desde el día 1 |

## Conexión con otros frameworks

- **Se alimenta de:** North Star Metric (la NSM se descompone en estos drivers), Test/Learning Cards (cada experimento mueve una métrica AARRR).
- **Alimenta a:**
  - **OKRs trimestrales** (cada etapa AARRR puede tener su Objective)
  - **Roadmap** (priorizá features que mueven la métrica más débil)
  - **Pre-mortem** (los riesgos suelen estar en la etapa más débil)
  - **Lean Canvas** (los inputs de "Métricas clave" suelen ser de AARRR)

## Lectura recomendada

- Dave McClure — *Startup Metrics for Pirates* (presentación clásica en SlideShare, 2007).
- *Hacking Growth* — Sean Ellis & Morgan Brown.
- *Lean Analytics* — Alistair Croll & Benjamin Yoskovitz.
- Lenny Rachitsky — posts sobre RARRA y métricas SaaS (lennysnewsletter.com).
