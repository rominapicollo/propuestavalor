# 09 — Matriz DVF (Deseabilidad, Viabilidad, Factibilidad)

> Filtro de tres lentes de IDEO para evaluar y priorizar ideas de manera balanceada.

---

## Qué es

Un marco de evaluación creado por **IDEO** y David Kelley que sostiene que toda innovación exitosa debe ser **deseable** para el usuario, **viable** para el negocio y **factible** técnicamente. Si falla en alguna de las tres, fracasa.

```
                    ┌─────────────────┐
                    │  DESEABILIDAD   │
                    │ (¿lo quieren?)  │
                    └─────────┬───────┘
                              │
              ┌───────────────┼───────────────┐
              │           INNOVACIÓN          │
              │           EXITOSA             │
              │           (las 3 cumplidas)   │
              └───────────────┬───────────────┘
                              │
              ┌───────────────┴───────────────┐
              │                               │
      ┌───────▼────────┐             ┌────────▼────────┐
      │  VIABILIDAD    │             │  FACTIBILIDAD   │
      │ (¿hay negocio?)│             │ (¿se puede      │
      │                │             │  construir?)    │
      └────────────────┘             └─────────────────┘
```

## Para qué sirve

- Filtrar ideas balanceando tres dimensiones que suelen estar en tensión.
- Generar conversación cross-funcional (negocio + diseño + ingeniería) sobre cada idea.
- Detectar qué tipo de validación necesita cada idea (cada lente requiere experimentos distintos).
- Priorizar el roadmap más allá del entusiasmo de un equipo individual.

## Cuándo usarlo

En la **Etapa 3 (Idear)**, después de Crazy 8s para filtrar el set de ideas generadas. También al final de la Etapa 4 como check de la propuesta integral.

## Las tres lentes explicadas

### 1. Deseabilidad (¿lo quieren?)

Foco en el usuario. Pregunta clave: ¿la idea resuelve un dolor real?

**Indicadores positivos:**
- Hay evidencia (entrevistas, datos) del problema.
- Los usuarios usan workarounds para resolverlo.
- La idea cubre dimensiones funcionales, emocionales y sociales del job.

**Indicadores negativos:**
- "Sería lindo tener" pero nadie lo pide activamente.
- Solo resuelve un problema funcional, sin gancho emocional.
- El usuario no cambia hábito por esto.

### 2. Viabilidad (¿hay negocio?)

Foco en el modelo de negocio. Pregunta clave: ¿esto puede generar valor económico sostenible?

**Indicadores positivos:**
- Hay disposición a pagar (validada o evidente).
- El costo de servir es menor al precio.
- El mercado tiene tamaño suficiente para el objetivo.
- Hay canales de distribución alcanzables.

**Indicadores negativos:**
- El CAC sería mayor al LTV.
- El nicho es muy chico para el objetivo.
- Requiere subsidios permanentes.
- Restricciones regulatorias bloquean el modelo.

### 3. Factibilidad (¿se puede construir?)

Foco en lo técnico y operativo. Pregunta clave: ¿podemos construir y operar esto con los recursos disponibles?

**Indicadores positivos:**
- La tecnología existe o es accesible.
- El equipo tiene (o puede adquirir) las skills.
- El time-to-market es razonable.
- Las dependencias externas son manejables.

**Indicadores negativos:**
- Requiere I+D de varios años.
- Depende de tecnologías que aún no existen comercialmente.
- Requiere skills muy escasas o caras.
- Tiene dependencias regulatorias largas (APIs gubernamentales, certificaciones).

## Visual de la matriz (versión scoring)

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  IDEA                       │ DESEAB. │ VIABIL. │ FACTIB. │ TOTAL   │
│                             │ (1-5)   │ (1-5)   │ (1-5)   │         │
│  ─────────────────────────────────────────────────────────────────  │
│  Bot de WhatsApp cobranza   │    5    │    4    │    3    │   12    │
│  Factura con link de pago   │    4    │    5    │    5    │   14    │
│  Dashboard balance ARS neto │    5    │    4    │    4    │   13    │
│  Convertidor TC con alertas │    3    │    3    │    4    │   10    │
│  Streaks de gamificación    │    2    │    2    │    4    │    8    │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

## Visual de la matriz (versión cualitativa por idea)

```
                IDEA: "Bot de WhatsApp para cobranza profesional"
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│  DESEABILIDAD: ★★★★★                                          │
│  Evidencia: 5/8 entrevistadas mencionaron vergüenza al        │
│  reclamar. Resuelve dolor emocional y funcional.               │
│  Riesgo bajo.                                                  │
│                                                                │
│  VIABILIDAD: ★★★★☆                                            │
│  Cobrable como feature premium. Costo bajo de operación.       │
│  Mercado de freelancers LATAM > 5M.                            │
│  Riesgo medio: dependencia de WhatsApp Business API.           │
│                                                                │
│  FACTIBILIDAD: ★★★☆☆                                          │
│  WhatsApp Business API tiene costos por mensaje.               │
│  Requiere número verificado por país. Compliance de privacidad.│
│  Riesgo alto: aprobación de Meta puede demorar 2-3 meses.      │
│                                                                │
│  ─────────────────────────────────────────────────────────     │
│  DECISIÓN: avanzar con experimento, atacando primero el        │
│  riesgo de factibilidad (Spike técnico de WhatsApp API).       │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

## Cómo se usa: protocolo paso a paso

1. **Reuní las ideas filtradas** de Crazy 8s + heat map (típicamente 3-7 ideas).
2. **Convocá un taller cross-funcional** (mínimo: producto, diseño, ingeniería, negocio).
3. **Para cada idea, evaluá** las tres lentes:
   - Modo scoring: puntúa 1-5 cada lente.
   - Modo cualitativo: discutí cada lente y anotá evidencia + riesgos.
4. **Hacé el resumen visual** (matriz comparativa).
5. **Filtrá:**
   - Score total > 12 = avanzar.
   - Una sola lente con score 1-2 = descartar o pivotar.
   - Tres lentes equilibradas con score 3-4 = experimentar.
6. **Para las ideas seleccionadas, definí cuál lente es la más riesgosa** → ese es tu primer experimento (alineado con RAT).

## Ejemplo precompletado: FinFlow

**Contexto:** después de Crazy 8s, el equipo trajo 5 ideas con votos.

**Matriz comparativa:**

```
┌────────────────────────────────────┬───────┬───────┬───────┬───────┬──────────┐
│ IDEA                               │ Des.  │ Viab. │ Fact. │ Total │ Decisión │
├────────────────────────────────────┼───────┼───────┼───────┼───────┼──────────┤
│ Bot de WhatsApp Cobranza           │   5   │   4   │   3   │  12   │ Avanzar  │
│ Factura con link de pago integrado │   4   │   5   │   5   │  14   │ Avanzar  │
│ Dashboard de balance ARS neto      │   5   │   4   │   4   │  13   │ Avanzar  │
│ Reportes de "puntualidad" al       │       │       │       │       │          │
│ cliente                            │   2   │   2   │   5   │   9   │ Descartar│
│ Convertidor TC con alertas         │   3   │   3   │   4   │  10   │ Reserva  │
└────────────────────────────────────┴───────┴───────┴───────┴───────┴──────────┘
```

**Análisis por idea (las que avanzan):**

**Idea 1 — Bot de WhatsApp Cobranza**
- Lente más fuerte: deseabilidad (dolor emocional validado).
- Lente más riesgosa: factibilidad (API de WhatsApp Business compleja y cara).
- **Primer experimento:** Spike técnico de 1 semana para entender costos y latencia de la API. Antes de cualquier prototipo de UX.

**Idea 2 — Factura con link de pago integrado**
- Lente más fuerte: factibilidad (integración con Stripe/MercadoPago es directa).
- Lente más riesgosa: deseabilidad (¿el cliente final usa el link o sigue pagando por transferencia?).
- **Primer experimento:** Smoke test con landing + A/B de prototipos de factura con y sin link.

**Idea 3 — Dashboard de balance ARS neto**
- Lente más fuerte: deseabilidad (dolor cuantificado en entrevistas).
- Lente más riesgosa: viabilidad (¿es feature gratuita que diferencia, o paga?).
- **Primer experimento:** Wizard of Oz: durante 4 semanas enviamos balance manualmente a 20 usuarios por WhatsApp todos los lunes. Medimos engagement y disposición a pagar.

**Idea descartada — Reportes de "puntualidad"**
- Razón: idea creativa pero deseabilidad baja (no soluciona dolor real del freelancer) y viabilidad débil (no genera revenue propio).
- Se documenta como "rama muerta" en el Opportunity Solution Tree.

## Tips para no caer en errores comunes

- **No promedien el score sin contexto.** Una idea con 5-5-1 es peor que una 4-4-4. La que falla en una lente no funciona.
- **Hacé el ejercicio cross-funcional, no individual.** El sesgo de cada disciplina es predecible: diseño infla deseabilidad, ingeniería infla factibilidad, negocio infla viabilidad. Necesitás contrapesos.
- **Marcá la diferencia entre "sabemos" y "asumimos".** Cada celda con score debería tener evidencia o estar marcada como `[hipótesis]`.
- **Revisitá la matriz después de los experimentos.** El score cambia con los datos.

## Variantes y herramientas relacionadas

| Herramienta | Diferencia |
|-------------|------------|
| **DVF** | Triple filtro cualitativo de IDEO |
| **RICE** | Reach, Impact, Confidence, Effort. Más cuantitativo |
| **ICE** | Impact, Confidence, Ease. Versión simplificada de RICE |
| **MoSCoW** | Must, Should, Could, Won't. Priorización binaria de scope |
| **Kano Model** | Clasifica features por satisfacción del usuario |

DVF es ideal en fase de ideación. RICE/ICE son mejores cuando ya tenés un backlog de features que priorizar.

## Conexión con otros frameworks

- **Se alimenta de:** Crazy 8s + heat map.
- **Alimenta a:**
  - **Opportunity Solution Tree** (las ideas que pasan se cuelgan como soluciones)
  - **RAT** (la lente más riesgosa de cada idea es el supuesto a testear primero)
  - **Value Proposition Canvas** (las ideas seleccionadas se llevan al VPC para detallar)
  - **Lean Canvas** (la idea ganadora se modela en Lean Canvas)

## Lectura recomendada

- IDEO Design Thinking Toolkit.
- *Change by Design* — Tim Brown (CEO de IDEO).
- Tim Brown, HBR — *Design Thinking* (2008).
