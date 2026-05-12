# 03 — Customer Journey Map

> Visualización del recorrido completo del usuario para detectar puntos de dolor y oportunidades de innovación.

---

## Qué es

Un mapa que representa la experiencia completa de un usuario al intentar lograr un objetivo, desde antes de interactuar con tu producto hasta después. Cada paso incluye lo que el usuario hace, piensa, siente y los puntos de contacto que toca.

## Para qué sirve

- Visualizar la experiencia end-to-end del usuario, no solo el momento del producto.
- Identificar los **picos de dolor** y **momentos de la verdad**.
- Detectar gaps entre la experiencia esperada y la real.
- Encontrar oportunidades concretas de innovación en cada etapa.
- Alinear equipos cross-funcionales sobre cómo es la experiencia real.

## Cuándo usarlo

En la **Etapa 1 (Empatizar)**, después del Empathy Map. También se puede revisitar en la Etapa 4 para ubicar dónde encaja la solución propuesta.

## Visual del Journey Map

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                       CUSTOMER JOURNEY MAP                                   │
├───────────┬───────────┬───────────┬───────────┬───────────┬─────────────────┤
│  FASE 1   │  FASE 2   │  FASE 3   │  FASE 4   │  FASE 5   │   FASE 6        │
│ Conciencia│ Búsqueda  │ Decisión  │   Uso     │  Soporte  │  Retención      │
├───────────┼───────────┼───────────┼───────────┼───────────┼─────────────────┤
│ ACCIONES  │           │           │           │           │                 │
│ qué hace  │           │           │           │           │                 │
├───────────┼───────────┼───────────┼───────────┼───────────┼─────────────────┤
│ TOUCHPOINT│           │           │           │           │                 │
│ canales   │           │           │           │           │                 │
├───────────┼───────────┼───────────┼───────────┼───────────┼─────────────────┤
│ PENSAMIENT│           │           │           │           │                 │
│ qué piensa│           │           │           │           │                 │
├───────────┼───────────┼───────────┼───────────┼───────────┼─────────────────┤
│ EMOCIÓN   │   😐      │    😟     │   😩      │   😡      │      😐         │
│ curva     │           │           │           │           │                 │
├───────────┼───────────┼───────────┼───────────┼───────────┼─────────────────┤
│ DOLORES   │           │           │           │           │                 │
├───────────┼───────────┼───────────┼───────────┼───────────┼─────────────────┤
│ OPORTUNID.│           │           │           │           │                 │
└───────────┴───────────┴───────────┴───────────┴───────────┴─────────────────┘
```

## Las filas explicadas

| Fila | Qué capturar |
|------|--------------|
| **Acciones** | Lo que el usuario hace físicamente o digitalmente |
| **Touchpoints** | Canales y puntos de contacto que usa |
| **Pensamientos** | Lo que se dice a sí mismo en ese momento |
| **Emoción** | Curva emocional (escala -2 a +2 o emojis) |
| **Dolores** | Frustraciones específicas de esa fase |
| **Oportunidades** | Posibilidades de mejora o innovación |

## Cómo se usa: protocolo paso a paso

1. **Elegí un persona específico** (el del Empathy Map).
2. **Definí el objetivo del journey** (no la app: el objetivo de vida del usuario).
3. **Definí el alcance temporal:** ¿desde cuándo y hasta cuándo? Incluí pre y post.
4. **Listá las fases** (típicamente 4-7).
5. **Llená cada celda** con datos reales (entrevistas, no asunciones).
6. **Dibujá la curva emocional** uniendo los emojis/scores entre fases.
7. **Identificá los valles** (puntos más bajos) — esos son tus oportunidades.
8. **Anotá oportunidades concretas** en la última fila.

## Ejemplo precompletado: FinFlow

**Persona:** Camila, diseñadora UX freelance.
**Objetivo del journey:** facturar y cobrar un proyecto de USD 2.500 a un cliente de EE.UU.

```
┌──────────────┬──────────────┬──────────────┬──────────────┬──────────────┬──────────────┐
│ 1. ACUERDO   │ 2. EJECUCIÓN │ 3. FACTURACIÓN│ 4. COBRO     │ 5. CONVERSIÓN│ 6. CIERRE    │
│ con cliente  │ del trabajo  │              │              │ a ARS        │ fiscal       │
├──────────────┼──────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ ACCIONES                                                                                │
│              │              │              │              │              │              │
│ Negocia      │ Trabaja en   │ Arma factura │ Espera 30-45 │ Recibe USD,  │ Carga datos  │
│ monto y      │ el proyecto  │ en planilla, │ días, envía  │ paga         │ en planilla, │
│ moneda por   │              │ envía PDF    │ recordatorios│ comisiones,  │ pasa al      │
│ email/Slack  │              │ por email    │ por WhatsApp │ convierte    │ contador     │
│              │              │              │              │              │              │
├──────────────┼──────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ TOUCHPOINTS                                                                             │
│              │              │              │              │              │              │
│ Email,       │ Figma, Slack │ Excel, Gmail │ WhatsApp,    │ Wise/Payoneer│ Drive, mail  │
│ Calendly,    │              │              │ Email        │ + banco      │ al contador  │
│ Slack        │              │              │              │              │              │
│              │              │              │              │              │              │
├──────────────┼──────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ PENSAMIENTOS                                                                            │
│              │              │              │              │              │              │
│ "Cobro USD,  │ "Tengo que   │ "Esta factura│ "¿Cuándo me  │ "¿Cuánto me  │ "¿Está bien  │
│ pero al      │ acordarme de │ ¿la armo en  │ paga? No me  │ entró real?  │ esto para    │
│ tipo oficial │ facturar el  │ inglés? ¿con │ atrevo a     │ Perdí algo en│ AFIP? Mejor  │
│ pierdo"      │ último día"  │ qué número?" │ insistir"    │ Wise"        │ que vea Juan"│
│              │              │              │              │              │              │
├──────────────┼──────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ EMOCIÓN                                                                                 │
│              │              │              │              │              │              │
│      😊      │      😐      │      😟      │     😩       │      😟      │      😨      │
│     (+1)     │     (0)      │     (-1)     │    (-2)      │    (-1)      │     (-2)     │
│              │              │              │              │              │              │
├──────────────┼──────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ DOLORES                                                                                 │
│              │              │              │              │              │              │
│ Incertidumbre│ Posterga la  │ No tiene     │ Vergüenza al │ Pérdida real │ Miedo a      │
│ sobre cuánto │ admin hasta  │ template,    │ reclamar.    │ no visible.  │ errores      │
│ va a quedar  │ último       │ riesgo de    │ Ansiedad por │ Múltiples    │ fiscales.    │
│ en ARS       │ momento      │ errores      │ flujo de caja│ comisiones   │ Depende de   │
│              │              │              │              │ ocultas      │ tercero      │
│              │              │              │              │              │              │
├──────────────┼──────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ OPORTUNIDADES                                                                           │
│              │              │              │              │              │              │
│ Calculadora  │ Recordatorio │ Template de  │ Recordatorios│ Dashboard    │ Exportación  │
│ pre-cierre   │ automático de│ factura      │ automáticos +│ con monto    │ directa a    │
│ de TC y      │ facturación  │ pro con      │ scripts de   │ ARS real     │ formato      │
│ neto en ARS  │ al cliente   │ datos        │ cobranza no  │ post comisión│ AFIP /       │
│              │              │ fiscales LATAM│ invasivos    │              │ contador     │
└──────────────┴──────────────┴──────────────┴──────────────┴──────────────┴──────────────┘
```

**Análisis de los valles emocionales:**

- **Fase 4 (Cobro):** valle profundo. La vergüenza de reclamar combinada con incertidumbre de flujo de caja = oportunidad alta.
- **Fase 6 (Cierre fiscal):** otro valle. Dependencia de un tercero (contador) y miedo a multas.

**Conclusión accionable:** las dos oportunidades de mayor impacto están en **automatizar la cobranza con respeto profesional** (Fase 4) y en **eliminar la fricción fiscal** (Fase 6). El MVP debería priorizar al menos una de las dos.

## Tips para no caer en errores comunes

- **No empieces por el touchpoint con tu producto.** Empezá antes y terminá después.
- **Una fila por usuario, no un journey "promedio"** de varios.
- **Datos reales, no imaginados.** Si una celda no la pudiste validar en entrevistas, marcala como hipótesis.
- **Buscá las "delight opportunities"** (los picos también importan, no solo los valles).
- **Pegalo en la pared** del equipo. Tiene que ser visible permanentemente.

## Variantes útiles

- **Service Blueprint:** versión expandida que agrega la línea de procesos internos del backstage (útil cuando innovás un servicio, no solo un producto digital).
- **Future State Journey:** mapeás cómo querés que sea la experiencia después de tu solución. Útil para alinear visión.

## Conexión con otros frameworks

- **Se alimenta de:** Mom Test, Empathy Map, observaciones.
- **Alimenta a:**
  - **Opportunity Canvas** (los valles son las oportunidades a evaluar)
  - **Opportunity Solution Tree** (oportunidades concretas por fase)
  - **Story Mapping** (las fases del journey se convierten en columnas del story map)
  - **JTBD** (los pensamientos en cada fase revelan jobs específicos)

## Lectura recomendada

- *This Is Service Design Doing* — Marc Stickdorn et al.
- *Mapping Experiences* — James Kalbach.
