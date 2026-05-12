# 19 — Learning Card (Strategyzer)

> Tarjeta gemela de la Test Card para capturar el aprendizaje de un experimento y tomar la decisión: perseverar, pivotar o descartar.

---

## Qué es

Una tarjeta de **Strategyzer** que complementa a la Test Card. Mientras la Test Card diseña el experimento **antes** de ejecutarlo, la Learning Card captura el resultado y la decisión **después**.

Es el cierre del ciclo Build → Measure → **Learn**.

## Para qué sirve

- Convertir datos brutos en aprendizajes accionables.
- Forzar al equipo a tomar una decisión explícita (perseverar / pivotar / descartar).
- Crear memoria organizacional: lo que se aprendió queda documentado y accesible.
- Justificar decisiones a stakeholders con evidencia, no con opiniones.
- Detectar patrones a través de múltiples experimentos.

## Cuándo usarla

En la **Etapa 5 (Validar)**, inmediatamente después de cada experimento ejecutado con una Test Card.

## Visual del Learning Card

```
┌────────────────────────────────────────────────────────────────┐
│  LEARNING CARD                                                 │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│  HIPÓTESIS ORIGINAL                                            │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ [Referencia a Test Card # ___]                           │  │
│  │ Creíamos que [SUPUESTO]                                  │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  OBSERVACIÓN                                                   │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Lo que pasó realmente (datos crudos)                     │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  APRENDIZAJE / INSIGHT                                         │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Lo que ahora entendemos / sabemos                        │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  DECISIÓN                                                      │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ ◯ PERSEVERAR — la hipótesis se valida; seguimos          │  │
│  │ ◯ PIVOTAR — ajustar la propuesta basados en lo aprendido │  │
│  │ ◯ DESCARTAR — la hipótesis se refuta; matamos esta rama  │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  PRÓXIMOS PASOS                                                │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ • Acción concreta 1                                      │  │
│  │ • Acción concreta 2                                      │  │
│  │ • Próximo experimento sugerido                           │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
│  DATOS GENERALES                                               │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ Confianza del aprendizaje: Baja / Media / Alta           │  │
│  │ Costo total real:          USD ___                       │  │
│  │ Tiempo real:               ___ días                      │  │
│  │ Responsable:               [Nombre]                      │  │
│  │ Fecha:                     [YYYY-MM-DD]                  │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

## Las 3 decisiones posibles

### 1. PERSEVERAR
La hipótesis se validó. Seguimos por este camino.

- Las métricas alcanzaron el criterio de éxito.
- Hay evidencia suficiente para invertir más.
- Próximo paso: escalar, construir el siguiente nivel.

### 2. PIVOTAR
La hipótesis no se validó como esperábamos, pero hay señales suficientes para ajustar.

- Tipos de pivote (Eric Ries identifica 10):
  - **Zoom-in pivot:** una feature se convierte en producto.
  - **Zoom-out pivot:** lo que era el producto se convierte en una feature.
  - **Customer segment pivot:** mismo producto, otro usuario.
  - **Customer need pivot:** mismo usuario, otra necesidad.
  - **Platform pivot:** de app a plataforma o viceversa.
  - **Business architecture pivot:** B2C ↔ B2B.
  - **Value capture pivot:** cambio de modelo de monetización.
  - **Engine of growth pivot:** cambio de motor (viral, paid, sticky).
  - **Channel pivot:** mismo producto, otro canal.
  - **Technology pivot:** misma promesa, otra tecnología.

### 3. DESCARTAR
La hipótesis se refutó. No hay base para continuar por este camino.

- Las métricas cayeron muy por debajo del criterio.
- Documentar la "rama muerta" en el Opportunity Solution Tree.
- Liberar recursos para otras hipótesis.

## Cómo se usa: protocolo paso a paso

1. **Recopilá los datos** del experimento ejecutado.
2. **Convocá una sesión de 30-60 min** con el equipo del experimento.
3. **Reviá la hipótesis original y el criterio de éxito** definidos en la Test Card.
4. **Volcá los datos crudos** en "Observación", sin interpretación.
5. **Interpretá colectivamente** qué significa, en "Aprendizaje".
6. **Tomá la decisión explícita** entre perseverar / pivotar / descartar. **No la dejes implícita.**
7. **Definí próximos pasos concretos** con responsable y fecha.
8. **Asigná confianza al aprendizaje** según fuerza de la evidencia.
9. **Archivá la Learning Card** en un repositorio accesible para el equipo.
10. **Actualizá el Opportunity Solution Tree** según la decisión.

## Ejemplo precompletado: FinFlow

**Contexto:** Test Card #001 (smoke test de pricing) ejecutada. Datos recolectados después de 14 días.

```
┌────────────────────────────────────────────────────────────────────────┐
│  LEARNING CARD #001                                                    │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│  HIPÓTESIS ORIGINAL                                                    │
│  ──────────────────                                                    │
│  [Test Card #001]                                                      │
│  Creíamos que el plan Pro a USD 9/mes tendría ≥ 6% de conversión       │
│  visitor→signup en el segmento de freelancers LATAM con > USD 2k/mes.  │
│                                                                        │
│  OBSERVACIÓN (datos crudos)                                            │
│  ────────────────────────────                                          │
│  Tráfico generado:           2.847 visitantes únicos (14 días)         │
│  Por canal:                                                            │
│    • Twitter ads:            1.120 visitantes                          │
│    • LinkedIn ads:             892 visitantes                          │
│    • Sponsoreo comunidades:    835 visitantes                          │
│                                                                        │
│  CTR por plan (% visitantes que clickean "Empezar"):                   │
│    • Plan Free:              22.4%                                     │
│    • Plan Pro USD 5/mes:     11.8%                                     │
│    • Plan Pro USD 9/mes:      4.1%                                     │
│    • Plan Studio USD 19/mes:  1.3%                                     │
│                                                                        │
│  Conversion completa (visit → email + tarjeta):                        │
│    • Free:                   16.7%                                     │
│    • Pro USD 5:               7.2%                                     │
│    • Pro USD 9:               2.1%                                     │
│    • Studio USD 19:           0.4%                                     │
│                                                                        │
│  Calidad de los emails capturados (rebote, dominio):                  │
│    • 89% emails con dominio profesional                                │
│    • 11% gmails/personales                                             │
│                                                                        │
│  APRENDIZAJE / INSIGHT                                                 │
│  ──────────────────────                                                │
│  • El plan Pro a USD 9 no alcanza el umbral (4.1% < 6%).               │
│  • Pero a USD 5 supera holgadamente (11.8%). La elasticidad de precio  │
│    es muy fuerte en este segmento: bajar 44% el precio sube el CTR     │
│    casi 3x.                                                            │
│  • La gente clickea pero no completa con tarjeta: solo 2.1% completa   │
│    en USD 9 vs CTR de 4.1%. Hay fricción adicional en el commitment.   │
│  • El plan Studio USD 19 no tiene demanda en este segmento (1.3% CTR).│
│    Probablemente el segmento real para Studio sea otro.                │
│  • Hay un cluster claro de "viability" en USD 5-7.                     │
│                                                                        │
│  DECISIÓN                                                              │
│  ──────────                                                            │
│  ◯ PERSEVERAR                                                          │
│  ●▶ PIVOTAR (cambio de precio + cambio de segmento para Studio)       │
│  ◯ DESCARTAR                                                           │
│                                                                        │
│  Pivote específico:                                                    │
│  1. Bajar plan Pro a USD 6/mes (entre USD 5 que funciona y USD 9       │
│     que no, con margen de prueba).                                     │
│  2. Replantear plan Studio: testear en segmento "agencias y estudios   │
│     pequeños" en vez de freelancers solo.                              │
│  3. Reformular Lean Canvas con nuevo pricing y rehacer proyección.     │
│                                                                        │
│  PRÓXIMOS PASOS                                                        │
│  ──────────────                                                        │
│  • [Esta semana] Actualizar Lean Canvas V3 con pricing USD 6/mes.      │
│    Recalcular break-even (estimación: ~5.000 users Pro).               │
│  • [Próximas 2 semanas] Test Card #002: nuevo smoke test               │
│    USD 6 vs USD 7 con tarjeta requerida desde el inicio.               │
│  • [Próximas 4 semanas] Test Card #003: pivote de Studio: smoke test   │
│    a segmento "agencias 2-5 personas".                                 │
│  • Re-evaluar el RAT con la nueva información.                         │
│                                                                        │
│  DATOS GENERALES                                                       │
│  ────────────────                                                      │
│  Confianza del aprendizaje:   Alta (n suficiente + comportamiento +    │
│                               algo de dinero comprometido)             │
│  Costo total real:            USD 920 (USD 800 estimado + USD 120     │
│                               extra de tráfico)                        │
│  Tiempo real:                 16 días (2 días más de lo estimado)      │
│  Responsable:                 Florencia (Growth)                       │
│  Fecha:                       2026-05-30                                │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

## Tips para escribir buenas Learning Cards

- **Diferenciá observación de interpretación.** Los datos van en "Observación", lo que significan va en "Aprendizaje".
- **No suavices la decisión.** Si la hipótesis se cayó, escribí "descartar". Si pivotás, especificá cómo. No dejes ambigüedad.
- **Una Learning Card por experimento.** No mezcles.
- **Hacelas visibles al equipo entero.** El conocimiento es organizacional, no del responsable individual.
- **Releelas trimestralmente.** A veces un patrón emerge solo cuando ves 5 Learning Cards juntas.
- **Marcá las "ramas muertas" en el Opportunity Solution Tree** con referencia a la Learning Card.

## Patrones útiles cuando juntás varias Learning Cards

A medida que tu repositorio crece, podés detectar:

| Patrón | Qué significa | Acción |
|--------|---------------|--------|
| Múltiples experimentos validan el mismo segmento | Foco confirmado | Doblar apuesta en ese segmento |
| Múltiples experimentos refutan el mismo canal | Canal estructuralmente débil | Eliminar de la estrategia |
| Pivot recurrente en pricing | Modelo de monetización no validado | Pre-mortem sobre viabilidad |
| Validaciones débiles ("media confianza" varias veces) | Experimentos poco rigurosos | Subir el nivel de evidencia exigido |
| Decisiones "perseverar" sin pasar criterio | Sesgo de confirmación | Revisar criterios y proceso |

## Errores comunes

| Error | Por qué falla |
|-------|---------------|
| Reinterpretar el criterio post-hoc | Sesgo de confirmación; invalida el aprendizaje |
| No documentar experimentos fallidos | Se repiten los mismos errores |
| "Aprendizaje" vago ("la gente parece interesada") | No sirve para tomar decisiones |
| Decisión implícita ("seguimos viendo") | Energía dispersa, sin foco |
| Archivar Learning Cards y nunca releerlas | Memoria organizacional se pierde |

## Conexión con otros frameworks

- **Se alimenta de:** Test Card (con sus resultados).
- **Alimenta a:**
  - **Opportunity Solution Tree** (actualización del árbol según aprendizajes)
  - **Lean Canvas** (cada Learning Card puede generar una nueva versión)
  - **Value Proposition Canvas** (refinamiento de pains/gains/relievers)
  - **Próximas Test Cards** (nuevas hipótesis a validar)
  - **Roadmap** (reorientación según evidencia)

## Lectura recomendada

- *Testing Business Ideas* — David J. Bland & Alex Osterwalder.
- Strategyzer — Test Cards y Learning Cards descargables.
- *The Lean Startup* — Eric Ries (cap. sobre pivote y los 10 tipos).
