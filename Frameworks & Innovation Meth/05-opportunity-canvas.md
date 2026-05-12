# 05 — Opportunity Canvas

> Lienzo de Jeff Patton para enmarcar una oportunidad de producto en una sola página, antes de definir solución.

---

## Qué es

Un canvas creado por **Jeff Patton** que mapea en un solo lienzo los elementos esenciales de una oportunidad: usuarios, problemas, alternativas actuales, ideas de solución, restricciones de negocio y métricas. Sirve como el primer "frame" estratégico de una idea.

## Para qué sirve

- Validar si una oportunidad vale la pena perseguirla.
- Forzar al equipo a explicitar supuestos antes de construir.
- Conectar el lado del usuario con el lado del negocio.
- Compartir contexto rápido con stakeholders.

## Cuándo usarlo

En la **Etapa 2 (Definir la oportunidad)**, después de empatizar con el usuario y antes de bajar a Lean Canvas o Value Proposition Canvas.

## Visual del canvas

```
┌────────────────────────────────────────────────────────────────────────────────┐
│                                                                                │
│                       OPPORTUNITY CANVAS                                       │
│                                                                                │
├──────────────────────┬───────────────────────────┬─────────────────────────────┤
│ 1. PROBLEMAS         │ 2. SOLUCIONES IDEAS       │ 3. USUARIOS Y CLIENTES      │
│                      │                           │                             │
│ Qué dolores reales   │ Qué se podría construir   │ Quién tiene el problema     │
│ detectaste           │ para resolver los         │ y quién lo paga             │
│                      │ problemas                 │                             │
│                      │                           │                             │
├──────────────────────┴───────────────────────────┼─────────────────────────────┤
│ 4. SOLUCIONES ACTUALES                           │ 5. PROBLEMA DE NEGOCIO      │
│                                                  │                             │
│ Qué hacen hoy los usuarios para resolver         │ Qué le pasa al negocio si   │
│ esto (competidores, hacks, workarounds)          │ no resolvemos esto          │
│                                                  │                             │
├──────────────────────────────────────────────────┼─────────────────────────────┤
│ 6. LIMITACIONES DE LA SOLUCIÓN                   │ 7. PRESUPUESTO              │
│                                                  │                             │
│ Qué supuestos asumimos, qué riesgos hay,         │ Cuánto está dispuesto a    │
│ qué podría salir mal                             │ invertir el negocio         │
│                                                  │                             │
├──────────────────────────────────────────────────┴─────────────────────────────┤
│ 8. ADOPCIÓN                                                                    │
│                                                                                │
│ Cómo van a descubrir, probar y adoptar la solución los usuarios                │
│                                                                                │
├────────────────────────────────────────────────────────────────────────────────┤
│ 9. MÉTRICAS                                                                    │
│                                                                                │
│ Cómo vamos a medir éxito (usuarios y negocio)                                  │
│                                                                                │
└────────────────────────────────────────────────────────────────────────────────┘
```

## Los 9 bloques explicados

| # | Bloque | Pregunta clave |
|---|--------|----------------|
| 1 | **Problemas** | ¿Qué dolores reales del usuario detectamos? |
| 2 | **Soluciones / Ideas** | ¿Qué podríamos construir para resolverlos? |
| 3 | **Usuarios y clientes** | ¿Quién tiene el problema y quién paga? (no siempre es el mismo) |
| 4 | **Soluciones actuales** | ¿Qué hacen hoy para resolverlo? Competidores + workarounds |
| 5 | **Problema de negocio** | ¿Qué le pasa al negocio si no resolvemos esto? |
| 6 | **Limitaciones de la solución** | ¿Qué supuestos asumimos? ¿Qué riesgos hay? |
| 7 | **Presupuesto** | ¿Cuánto está dispuesto a invertir el negocio? |
| 8 | **Adopción** | ¿Cómo van a descubrir y probar la solución? |
| 9 | **Métricas** | ¿Cómo medimos el éxito del usuario y del negocio? |

## Cómo se usa: protocolo paso a paso

1. **Reuní el material previo:** Empathy Map, Journey Map, JTBD, notas del Mom Test.
2. **Convocá un taller de 90-120 minutos** con producto, diseño, ingeniería y al menos una voz de negocio.
3. **Llená en este orden** (no de izquierda a derecha):
   - Primero: 3 (usuarios) → 1 (problemas) → 4 (soluciones actuales)
   - Luego: 5 (problema de negocio) → 9 (métricas)
   - Después: 2 (ideas) → 6 (limitaciones)
   - Por último: 7 (presupuesto) → 8 (adopción)
4. **Marcá explícitamente las hipótesis** (lo que asumís sin evidencia).
5. **Decidí si la oportunidad es perseguible** o si necesitás más investigación.

## Ejemplo precompletado: FinFlow

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                  OPPORTUNITY CANVAS — FinFlow                                   │
├─────────────────────────┬──────────────────────────┬────────────────────────────┤
│ 1. PROBLEMAS            │ 2. SOLUCIONES / IDEAS    │ 3. USUARIOS Y CLIENTES     │
│                         │                          │                            │
│ • Pérdida por TC sin    │ • App de facturación     │ Usuario primario:          │
│   visibilidad           │   multimoneda con        │ Freelancer LATAM con       │
│ • Demora en cobros, sin │   conversión automática  │ clientes internacionales,  │
│   sistema de follow-up  │ • Recordatorios          │ ingreso USD 2-10k/mes      │
│ • Templates de factura  │   automáticos de         │                            │
│   no profesionales      │   cobranza               │ Quien paga: el mismo       │
│ • Estrés fiscal por     │ • Templates de factura   │ usuario (B2C tipo prosumer)│
│   normativas por país   │   pro con campos AFIP    │                            │
│ • Múltiples herramientas│ • Dashboard con balance  │ Segmentos secundarios:     │
│   inconexas             │   neto en ARS real       │ • Estudios pequeños (2-5p) │
│                         │ • Integración con AFIP/  │ • Agencias boutique        │
│                         │   contadores             │                            │
├─────────────────────────┴──────────────────────────┼────────────────────────────┤
│ 4. SOLUCIONES ACTUALES                             │ 5. PROBLEMA DE NEGOCIO     │
│                                                    │                            │
│ • Planillas de Excel + carpeta de PDFs (60% de    │ Si no entramos pronto:     │
│   los freelancers entrevistados)                   │ • Deel y Wise están        │
│ • QuickBooks/FreshBooks (12%, abandonan por       │   expandiendo a LATAM con  │
│   no estar en español ni con AFIP)                 │   funcionalidades adyacent.│
│ • Contadores manuales (20%, pagan USD 50-150/mes) │ • Holded está creciendo    │
│ • No facturan a tiempo / "se acuerdan después"    │   en España y mira la región│
│   (8%, los más jóvenes)                            │ • El mercado se consolida  │
│                                                    │   en 18-24 meses           │
├────────────────────────────────────────────────────┼────────────────────────────┤
│ 6. LIMITACIONES DE LA SOLUCIÓN                     │ 7. PRESUPUESTO             │
│                                                    │                            │
│ Supuestos a validar:                               │ Pre-seed: USD 250k         │
│ • Los freelancers pagarán USD 9-15/mes por esto    │ Equipo: 4 personas         │
│ • La integración con AFIP es construible en        │ (PM, 2 devs, designer)     │
│   tiempo razonable                                 │ Tiempo: 9 meses hasta MVP  │
│ • El TC oficial vs paralelo es resoluble           │   validado                 │
│   legalmente                                       │                            │
│                                                    │ Restricciones:             │
│ Riesgos:                                           │ • No financiamos custodia  │
│ • Regulación AFIP puede cambiar                    │   de fondos en v1          │
│ • Adopción lenta si no hay onboarding muy simple   │ • No soportamos criptos    │
│                                                    │                            │
├────────────────────────────────────────────────────┴────────────────────────────┤
│ 8. ADOPCIÓN                                                                     │
│                                                                                 │
│ • Canal principal: comunidad. Sponsoreos en grupos de WhatsApp/Discord de       │
│   freelancers, referidos con incentivo (1 mes gratis por cada usuario activo)   │
│ • Canal secundario: contenido SEO sobre "cómo facturar al exterior desde X país"│
│ • Onboarding asistido: importación desde Excel + tutorial de 5 min              │
│ • Programa de embajadores con freelancers visibles en Twitter/LinkedIn          │
│                                                                                 │
├─────────────────────────────────────────────────────────────────────────────────┤
│ 9. MÉTRICAS                                                                     │
│                                                                                 │
│ Métricas de usuario:                                                            │
│ • % de freelancers que facturan dentro de la app dentro del primer mes (act.)   │
│ • Tiempo promedio entre fin de proyecto y emisión de factura (objetivo: -50%)   │
│ • % de cobros recibidos dentro de los 30 días                                   │
│                                                                                 │
│ Métricas de negocio:                                                            │
│ • North Star: facturas emitidas y cobradas por usuario activo / mes             │
│ • MRR / ARPU                                                                    │
│ • Churn mensual (objetivo: < 5%)                                                │
│ • CAC vs LTV (objetivo: LTV > 3x CAC en mes 12)                                 │
│                                                                                 │
└─────────────────────────────────────────────────────────────────────────────────┘
```

## Tips para no caer en los errores comunes

- **No empieces por las soluciones.** Si cargás primero "Ideas" te enamorás de una y forzás los demás bloques. Empezá por Usuarios y Problemas.
- **Marcá lo que es hipótesis vs. lo que es evidencia.** Por ejemplo, ponele `[H]` adelante a cada cosa no validada.
- **Cuestioná el bloque de competidores.** El competidor más peligroso suele ser "no hacer nada" o "una planilla".
- **Si no podés llenar el bloque 7 (Presupuesto), no estás listo para construir.** Sin restricciones, no hay decisiones reales.
- **Revisalo mensualmente.** Es un documento vivo, no un entregable.

## Diferencias con Lean Canvas

| Opportunity Canvas | Lean Canvas |
|--------------------|-------------|
| Foco en **una oportunidad específica** | Foco en **modelo de negocio completo** |
| Útil al inicio del problema | Útil al definir la propuesta |
| Más cualitativo | Más cuantitativo/operativo |
| Lo hacés primero | Lo hacés después |

Usá ambos: Opportunity Canvas para enmarcar la oportunidad; Lean Canvas para diseñar el modelo cuando ya tenés solución candidata.

## Conexión con otros frameworks

- **Se alimenta de:** Mom Test, Empathy Map, Customer Journey Map, JTBD.
- **Alimenta a:**
  - **Opportunity Solution Tree** (los problemas validados son las "oportunidades" del árbol)
  - **Lean Canvas** (define problema y segmento)
  - **Value Proposition Canvas** (los problemas son los pains a cubrir)
  - **Plantilla de Hipótesis** (los supuestos del bloque 6 son las primeras hipótesis a testear)

## Lectura recomendada

Jeff Patton — *User Story Mapping* (cap. sobre framing de oportunidad).
Post original en jpattonassociates.com.
