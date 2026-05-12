# 08 — Crazy 8s

> Sprint de ideación individual: 8 ideas en 8 minutos, una idea por minuto. Cantidad por encima de calidad.

---

## Qué es

Una técnica del **Google Design Sprint** (Jake Knapp) que fuerza al equipo a generar 8 ideas distintas en 8 minutos, sobre una sola hoja A4 plegada en 8 partes. La presión del tiempo desactiva el filtro interno (el "esto no va a funcionar") y libera ideas que normalmente no aparecerían.

## Para qué sirve

- Generar volumen de ideas rápidamente.
- Forzar al equipo a no quedarse con la primera idea.
- Garantizar diversidad de ideas (cada persona genera 8 distintas).
- Evitar el sesgo de quien habla más fuerte en brainstormings tradicionales.

## Cuándo usarlo

En la **Etapa 3 (Idear)**, después de tener uno o más HMW seleccionados y antes de la matriz DVF de priorización.

## Visual del formato

```
┌──────────────────────────────────────────┐
│   1            │            2            │
│                │                         │
│                │                         │
│                │                         │
├────────────────┼─────────────────────────┤
│   3            │            4            │
│                │                         │
│                │                         │
│                │                         │
├────────────────┼─────────────────────────┤
│   5            │            6            │
│                │                         │
│                │                         │
│                │                         │
├────────────────┼─────────────────────────┤
│   7            │            8            │
│                │                         │
│                │                         │
│                │                         │
└──────────────────────────────────────────┘

   Una hoja A4 plegada en 8.
   Una idea por casillero, 1 minuto cada uno.
```

## Cómo se usa: protocolo paso a paso

1. **Prepará materiales:** hoja A4 por persona, marcadores de punta gruesa (no lapiceras finas: fuerzan trazos rápidos), cronómetro visible.
2. **Recordá el HMW** seleccionado. Tiene que estar visible durante todos los 8 minutos.
3. **Doblá la hoja en 8** (mitad, mitad, mitad).
4. **Anunciá las reglas:**
   - 1 idea por casillero.
   - 1 minuto por casillero.
   - Cantidad sobre calidad.
   - Sketch + frase corta, no texto.
   - **Está prohibido detenerse aunque parezca mala la idea.**
5. **Arrancá el cronómetro.** Cada minuto cantás el cambio de casillero.
6. **Al terminar** (8 min exactos), cada persona elige sus **2 mejores ideas** y las refina por 5-10 minutos en hojas aparte (a esto se le llama a veces "Solution Sketch" o "Crazy 4s").
7. **Compartí** en silencio (los sketches pegados en una pared) antes de discutir.
8. **Vota con puntos** (heat map): cada persona pone 3-5 puntos en las ideas que más le interesan.
9. **Pasá las top 3-5 ideas** al filtro DVF.

## Reglas para que funcione

- **Trabajo individual primero.** Nada de discutir durante los 8 minutos.
- **El cronómetro manda.** Si alguien no llenó las 8, está bien; pero no se extiende el tiempo.
- **No hay ideas "malas" durante el ejercicio.** El filtro viene después.
- **Sketch antes que texto.** Un dibujo simple comunica más que 5 viñetas.
- **Sin computadoras.** El papel y la mano fuerzan velocidad.

## Ejemplo precompletado: FinFlow

**HMW:** *¿Cómo podríamos hacer que el seguimiento de cobros se sienta como una gestión profesional y no como un reclamo personal?*

**Crazy 8s de una persona del equipo (transcripto):**

```
┌──────────────────────────────────┬──────────────────────────────────┐
│ 1. Bot de WhatsApp                │ 2. "Modo gerente"                │
│                                   │                                  │
│ Asistente de cobranza que envía   │ Toggle que cambia el remitente   │
│ recordatorios desde un número     │ del email del freelancer al      │
│ profesional, no del freelancer    │ "Departamento de Cobranzas       │
│                                   │ FinFlow"                         │
│ [sketch: bubbles WhatsApp]        │ [sketch: switch on/off]          │
├──────────────────────────────────┼──────────────────────────────────┤
│ 3. Factura con link de pago       │ 4. Calendario público de         │
│    integrado                      │    facturación                   │
│                                   │                                  │
│ Toda factura emitida incluye      │ El freelancer comparte un        │
│ link 1-click (Stripe/MercadoPago) │ Google Calendar público con      │
│                                   │ todos sus compromisos de cobro   │
│ [sketch: factura con botón]       │ [sketch: agenda]                 │
├──────────────────────────────────┼──────────────────────────────────┤
│ 5. Reportes de "puntualidad"      │ 6. Pago suscripción              │
│    al cliente                     │                                  │
│                                   │ El cliente firma una vez para    │
│ Email trimestral al cliente con   │ autorizar débitos automáticos al │
│ su récord como pagador            │ recibir cada factura             │
│ ("pagás en 14 días promedio")     │                                  │
│ [sketch: badge "good payer"]      │ [sketch: tarjeta con tick]       │
├──────────────────────────────────┼──────────────────────────────────┤
│ 7. Cobranza colaborativa entre    │ 8. Streaks de cobranza           │
│    freelancers                    │                                  │
│                                   │ Gamificación: si lográs cobrar   │
│ Comunidad donde varios freelancer │ todas tus facturas en 30 días    │
│ compartían listas de "buenos      │ x meses seguidos, unlock features│
│ pagadores"                        │                                  │
│ [sketch: marketplace de scoring]  │ [sketch: streak de fuego]        │
└──────────────────────────────────┴──────────────────────────────────┘
```

**Top 2 seleccionadas por esa persona (Solution Sketch refinado):**

1. **Bot de WhatsApp** (combinado con #2 Modo gerente): el freelancer activa al "asistente de cobranzas" y desde ahí los recordatorios se envían desde una identidad profesional (FinFlow Cobranzas), no desde el número personal.

2. **Factura con link de pago integrado** (combinado con #6): toda factura emitida tiene un link de pago, y opcionalmente el cliente puede autorizar débitos automáticos para futuros cobros.

**Después de votar en equipo (heat map):**

- Idea 1+2 (bot + modo gerente): 11 puntos.
- Idea 3+6 (factura con link + débito auto): 9 puntos.
- Idea 5 (reportes de puntualidad): 7 puntos.
- Resto: < 4 puntos.

**Las 3 ideas con más calor pasan a la matriz DVF.**

## Variantes útiles

| Variante | Diferencia | Cuándo usarla |
|----------|------------|----------------|
| **Crazy 4s** | 4 ideas en 4 minutos | Si tenés poco tiempo o equipos cansados |
| **Crazy 16s** | 8 ideas en 8 min + 8 en otros 8 min | Para problemas muy abiertos |
| **Crazy 8 cruzado** | Cada persona pasa la hoja en cada minuto, otra agrega ideas | Brainwriting 6-3-5 fusionado |
| **Crazy 8 con prompts** | Cada casillero tiene un prompt distinto ("¿y si fuera B2B?", "¿y si no hubiera internet?") | Para forzar diversidad de ángulos |

## Tips para que las ideas sean buenas

- **Cambiá la pregunta cada 2-3 casilleros mentalmente:** "¿y si lo hacemos al revés?", "¿y si la app no existiera?", "¿y si fuera para niños?".
- **Permití las ideas locas.** Las 2 últimas suelen ser las más raras y a veces las más valiosas.
- **No edites mientras dibujás.** Si dudás, dibujá igual y pasá al siguiente.
- **Trabajá de pie** si podés. Mejora la energía y la rapidez.
- **Si una persona se traba** repetidamente, dale el HMW invertido ("¿cómo podríamos empeorarlo?") para 1 ronda. Suele desbloquear.

## Errores comunes

- **Discutir durante el ejercicio.** Es trabajo individual y silencioso.
- **Extender el tiempo "para que se complete".** El límite es parte del valor.
- **Compartir verbalmente las ideas antes de pegarlas.** Sesgo de quién habló primero.
- **Saltar el filtrado y enamorarse de una idea por persona.** Tiene que haber filtro DVF posterior.

## Conexión con otros frameworks

- **Se alimenta de:** How Might We (el HMW es el prompt).
- **Alimenta a:**
  - **Matriz DVF** (las ideas filtradas se evalúan)
  - **Solution Sketches** (refinamiento detallado de las top 2)
  - **Storyboard** (la idea ganadora se convierte en secuencia de pantallas)
  - **Opportunity Solution Tree** (las soluciones seleccionadas se cuelgan como ramas)

## Lectura recomendada

Jake Knapp — *Sprint: How to Solve Big Problems and Test New Ideas in Just Five Days* (2016).
Google Design Sprint Kit: designsprintkit.withgoogle.com.
