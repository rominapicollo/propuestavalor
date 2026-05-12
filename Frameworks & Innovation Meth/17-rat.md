# 17 — RAT (Riskiest Assumption Test)

> Priorización de hipótesis: identificar y testear primero el supuesto que, si está mal, hace caer todo lo demás.

---

## Qué es

Una técnica popularizada por **Rik Higham** y el equipo de **GV (Google Ventures)** como evolución del concepto de MVP. La idea: en lugar de construir un "producto mínimo viable" (que aún implica construir un producto), identificás el **supuesto más riesgoso** del modelo y diseñás el experimento más barato y rápido para validarlo o refutarlo.

**Frase clave de Rik Higham:**
> *"No necesitás un MVP. Necesitás un RAT. Validá el supuesto más riesgoso antes de construir nada."*

## Para qué sirve

- Evitar gastar tiempo y dinero en supuestos secundarios cuando hay uno crítico sin validar.
- Acelerar el aprendizaje: el experimento más informativo se ejecuta primero.
- Reducir el costo de fallar (fallás antes y más barato).
- Centrar la conversación del equipo en "¿qué nos haría dudar más?".

## Cuándo usarlo

En la **Etapa 5 (Validar)**, inmediatamente después de redactar las hipótesis con la Plantilla. El RAT es la priorización: el output del RAT alimenta la primera Test Card.

## La fórmula del RAT

Cada hipótesis se evalúa en dos dimensiones:

| Dimensión | Qué medís | Escala |
|-----------|-----------|--------|
| **Impacto si está mal** | ¿Cuánto se rompe si la hipótesis es falsa? | 1 (poco) — 5 (todo se cae) |
| **Evidencia actual** | ¿Cuánto sabemos hoy? | 1 (nada) — 5 (validado) |

**Score de riesgo = Impacto × (6 − Evidencia)**

Cuanto **mayor** el score, **más riesgosa** la hipótesis. Esa es la que se testea primero.

## Visual de la matriz RAT

```
                        IMPACTO si está mal
                  ───────────────────────────►
                  Bajo                    Alto

                   1     2     3     4     5
                ┌─────┬─────┬─────┬─────┬─────┐
            5  │  1  │  2  │  3  │  4  │  5  │  ◄── Mucha evidencia
   E       (alta)──────────────────────────────  (riesgo bajo)
   V        4  │  2  │  4  │  6  │  8  │ 10 │
   I           ├─────┼─────┼─────┼─────┼─────┤
   D        3  │  3  │  6  │  9  │ 12 │ 15 │
   E           ├─────┼─────┼─────┼─────┼─────┤
   N        2  │  4  │  8  │ 12 │ 16 │ 20 │
   C           ├─────┼─────┼─────┼─────┼─────┤
   I        1  │  5  │ 10 │ 15 │ 20 │ 25 │  ◄── Sin evidencia
   A      (baja)└─────┴─────┴─────┴─────┴─────┘  (riesgo alto)
                                          ▲
                                          │
                            Esquina top-right del RIESGO MÁXIMO
                            (impacto alto + sin evidencia)
                            → ESTO ES TU RAT
```

## Cómo se usa: protocolo paso a paso

1. **Reuní las hipótesis** formuladas con la Plantilla.
2. **Convocá al equipo** (mínimo 3 personas: producto, diseño, ingeniería).
3. **Para cada hipótesis, puntuá:**
   - Impacto si está mal (1-5).
   - Evidencia actual (1-5).
4. **Calculá el score** = Impacto × (6 − Evidencia).
5. **Ordená de mayor a menor score.**
6. **Elegí la top 1** como **el RAT** (la asunción más riesgosa).
7. **Diseñá la Test Card más barata y rápida posible** para validar/refutar esa hipótesis.
8. **Re-evalúa el ranking** después de cada experimento. El nuevo RAT puede ser distinto.

## Ejemplo precompletado: FinFlow

**Hipótesis del producto** (del ejemplo de la Plantilla):

| ID | Hipótesis | Impacto | Evidencia | Score | Ranking |
|----|-----------|---------|-----------|-------|---------|
| H5 | Pricing Pro USD 9/mes con 6% conversión | 5 (todo el modelo financiero depende) | 1 (sin evidencia) | **25** | 🔴 #1 |
| H2 | Cobranza automatizada sube cobros de 55→75% | 5 (diferencial central) | 2 (1 entrevista mencionó) | **20** | 🔴 #2 |
| H3 | Canal comunidades CAC < USD 12 | 4 (afecta growth pero hay alternativas) | 2 (referencias indirectas) | **16** | 🟡 #3 |
| H1 | Balance ARS visible aumenta retención | 4 | 3 (entrevistas lo sugieren) | **12** | 🟡 #4 |
| H8 | WhatsApp Business API funciona | 3 (hay alternativa: email) | 2 | **12** | 🟡 #4 |
| H7 | Integración API AFIP factible | 5 (sin esto no hay producto) | 4 (otros lo hicieron) | **10** | 🟢 #6 |
| H4 | Programa referidos K > 0.3 | 3 | 2 | **12** | 🟡 #4 |
| H6 | Plan Studio 1% adopción | 2 | 1 | **10** | 🟢 #6 |

### Visualización en matriz

```
                        IMPACTO
                  ───────────────────────────►
                   1     2     3     4     5
                ┌─────┬─────┬─────┬─────┬─────┐
            5  │     │     │     │     │     │
                ├─────┼─────┼─────┼─────┼─────┤
   E        4  │     │     │     │     │ H7  │
                ├─────┼─────┼─────┼─────┼─────┤
   V        3  │     │     │     │ H1  │     │
                ├─────┼─────┼─────┼─────┼─────┤
   I        2  │     │ H6  │ H4  │ H3  │ H2  │
                ├─────┼─────┼─────┼─────┼─────┤
   D        1  │     │     │ H8  │     │ H5🔴│
                └─────┴─────┴─────┴─────┴─────┘
                                          
                                       RAT = H5
```

### El RAT identificado

**Hipótesis crítica = H5: pricing Pro USD 9/mes con 6% conversión.**

**Por qué es el RAT:**
- **Impacto:** 5. Toda la proyección financiera del Lean Canvas asume estos números. Si la disposición a pagar es 50% menor o la conversión es la mitad, el modelo no llega al break-even.
- **Evidencia:** 1. Nadie validó esto. Es una asunción tomada de "lo que cobran competidores en mercados maduros".

**Lo riesgoso de no testearlo primero:** construir un MVP completo durante 4 meses y descubrir en el mes 5 que la gente paga USD 3-4, no USD 9. Habrías tirado 4 meses de equipo a la basura.

### El experimento más barato para testear H5

**Smoke Test con landing page de precios:**
- 5-7 días de armado.
- Landing con propuesta de valor + plan Pro USD 9/mes (también A/B con USD 5/mes y USD 15/mes).
- Tráfico pago a comunidades (~ USD 500 budget).
- Métrica: % de visitantes que clickean "Empezar prueba" en cada plan.
- Criterio: si CTR del plan USD 9 > 8% y > el de USD 5 / no se diferencia mucho, validamos.

**Después del Smoke Test:**
- Si valida → H5 baja a evidencia 4 → score 10 → ya no es el RAT. Se pasa a H2.
- Si refuta → pivotar precio en Lean Canvas y rehacer ranking. El nuevo RAT puede ser un pricing más bajo + economía de escala.

## La sutil diferencia entre RAT y MVP

| RAT | MVP |
|-----|-----|
| Testea **un supuesto** específico | Testea **la propuesta completa** |
| Puede no involucrar construir nada | Implica construir algo (mínimo) |
| Foco: **aprender** | Foco: **lanzar versión usable** |
| Tiempo: días | Tiempo: semanas a meses |
| Costo: USD 100 — USD 1.000 | Costo: USD 10.000 — USD 100.000 |

**Buena práctica:** ejecutá varios RATs antes de empezar a construir cualquier MVP. Cuando termines de validar los 3-5 supuestos más riesgosos, el MVP queda mucho mejor diseñado.

## Tips para hacerlo bien

- **No te enamores de la hipótesis.** El equipo tiende a votar bajo riesgo en lo que ya construyó mentalmente. El facilitador debe contraargumentar.
- **Diferenciá "no sabemos" de "creemos que sí".** Pensar "obviamente esto es así" suele ser síntoma de baja evidencia, no de alta.
- **Re-ranking después de cada experimento.** Una hipótesis validada pierde su score; otra que no parecía urgente puede subir.
- **Documentá la evidencia.** Si decís que algo tiene evidencia 4, mostrá el dato. Si no, es 2.
- **El RAT puede ser una hipótesis externa.** A veces es regulatoria, técnica externa o de mercado, no solo de producto.

## Errores comunes

| Error | Por qué falla |
|-------|---------------|
| Saltearse el ranking y testear lo más fácil | Sesgo a confirmar; ignorás el riesgo real |
| Subestimar la evidencia ("tenemos 3 entrevistas, ya está") | 3 entrevistas no es validación; es señal |
| No re-rankear post-experimento | Repetís el mismo orden aunque cambió el escenario |
| Testear hipótesis débilmente formuladas | Falla la plantilla, falla el RAT |

## Conexión con otros frameworks

- **Se alimenta de:** Plantilla de Hipótesis, Lean Canvas, Pre-mortem (los riesgos top son hipótesis críticas).
- **Alimenta a:**
  - **Test Card** (la hipótesis priorizada se diseña como experimento)
  - **Tipología de MVPs** (el formato MVP se elige según qué se quiere aprender)
  - **Roadmap de discovery** (ordena qué experimentos correr en qué secuencia)

## Lectura recomendada

- Rik Higham — *The Riskiest Assumption Test (RAT)* (Medium, 2016). Artículo fundacional.
- *Testing Business Ideas* — David J. Bland & Alex Osterwalder.
- GV — Design Sprint Methodology (relacionado).
