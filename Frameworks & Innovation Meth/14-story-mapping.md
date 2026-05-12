# 14 — Story Mapping

> Técnica de Jeff Patton para visualizar el journey del usuario y descomponer features en historias priorizables, con corte explícito de MVP.

---

## Qué es

Una técnica creada por **Jeff Patton** que organiza el backlog de producto en dos dimensiones: horizontalmente sigue el journey del usuario (de izquierda a derecha) y verticalmente prioriza las historias dentro de cada paso (lo esencial arriba, lo deseable abajo). Cortes horizontales = releases / MVPs.

A diferencia de un backlog plano de Jira, un Story Map muestra **la narrativa completa** del producto.

## Para qué sirve

- Visualizar el producto end-to-end desde la perspectiva del usuario.
- Decidir alcance del MVP de manera explícita y discutible.
- Detectar gaps en el flujo de usuario antes de construir.
- Comunicar al equipo el "por qué" detrás de cada historia.
- Reemplazar la pregunta "¿en qué orden hacemos los tickets?" por "¿qué experiencia mínima entregamos primero?".

## Cuándo usarlo

Al final de la **Etapa 4 (Diseñar la propuesta)**, después de tener Value Proposition Canvas con fit razonable y antes de planificar sprints.

## Visual del story map

```
┌──────────────────────────────────────────────────────────────────────────────┐
│ EJE HORIZONTAL: backbone (las grandes acciones del usuario, en orden)        │
│                                                                              │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐        │
│  │ ACTIVIDAD│  │ ACTIVIDAD│  │ ACTIVIDAD│  │ ACTIVIDAD│  │ ACTIVIDAD│        │
│  │    1     │  │    2     │  │    3     │  │    4     │  │    5     │        │
│  └─────┬────┘  └─────┬────┘  └─────┬────┘  └─────┬────┘  └─────┬────┘        │
│        │             │             │             │             │             │
│  ┌─────▼────┐  ┌─────▼────┐  ┌─────▼────┐  ┌─────▼────┐  ┌─────▼────┐        │
│  │ Tarea 1.1│  │ Tarea 2.1│  │ Tarea 3.1│  │ Tarea 4.1│  │ Tarea 5.1│        │
│  │ Tarea 1.2│  │ Tarea 2.2│  │ Tarea 3.2│  │ Tarea 4.2│  │ Tarea 5.2│        │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  └──────────┘        │
│                                                                              │
├──── MVP / RELEASE 1: lo mínimo para que el journey funcione end-to-end ──────┤
│                                                                              │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐        │
│  │ User     │  │ User     │  │ User     │  │ User     │  │ User     │        │
│  │ story 1A │  │ story 2A │  │ story 3A │  │ story 4A │  │ story 5A │        │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  └──────────┘        │
│                                                                              │
├──── RELEASE 2: agregar profundidad y delight ────────────────────────────────┤
│                                                                              │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐        │
│  │ Story 1B │  │ Story 2B │  │ Story 3B │  │ Story 4B │  │ Story 5B │        │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  └──────────┘        │
│                                                                              │
├──── RELEASE 3+: features avanzadas, casos edge ──────────────────────────────┤
│                                                                              │
│  ┌──────────┐                ┌──────────┐                ┌──────────┐        │
│  │ Story 1C │                │ Story 3C │                │ Story 5C │        │
│  └──────────┘                └──────────┘                └──────────┘        │
└──────────────────────────────────────────────────────────────────────────────┘

  EJE VERTICAL: prioridad (lo esencial arriba, lo deseable abajo)
```

## Los componentes del story map

| Elemento | Qué es |
|----------|--------|
| **Backbone (espina)** | Las grandes actividades del usuario en orden cronológico |
| **Tareas / pasos** | Lo que el usuario hace dentro de cada actividad |
| **Historias / user stories** | Las features concretas que habilitan cada paso |
| **Líneas de corte (releases)** | Horizontales: separan MVP, V2, V3, etc. |

## Cómo se usa: protocolo paso a paso

1. **Convocá un taller de 2-4 horas** con producto, diseño, ingeniería y al menos una voz de stakeholder.
2. **Recordá la persona y el job principal** del usuario.
3. **Construí el backbone:** las 5-9 actividades principales del journey, izquierda a derecha.
4. **Llená las tareas/pasos** debajo de cada actividad (post-its). No filtres todavía.
5. **Descendé a historias concretas** debajo de cada tarea (variantes, formatos, casos).
6. **Priorizá verticalmente** dentro de cada columna: arriba lo esencial, abajo lo deseable.
7. **Definí el corte del MVP:** una línea horizontal que cruza todas las columnas. Cada celda arriba de la línea es parte del MVP.
   - **Regla:** el MVP debe entregar el journey completo, aunque básico. No es "implementar la columna 1 y 2 completas".
8. **Definí cortes adicionales** para V2, V3, etc.
9. **Cuestioná cada historia** del MVP: ¿se puede sacar y todavía funciona el journey?
10. **Pasalo al backlog de delivery** (Jira, Linear) pero mantené el mapa visible.

## Ejemplo precompletado: FinFlow

**Persona:** Camila, freelancer LATAM con clientes internacionales.
**Job principal:** facturar y cobrar profesionalmente.

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ BACKBONE                                                                                     │
├─────────────┬─────────────┬─────────────┬─────────────┬─────────────┬───────────────────────┤
│ 1. SETUP    │ 2. CLIENTES │ 3. EMITIR   │ 4. SEGUIR   │ 5. COBRAR   │ 6. CERRAR             │
│   INICIAL   │             │   FACTURA   │   COBRO     │             │   FISCAL              │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┼───────────────────────┤
│ Crear cuenta│ Agregar     │ Generar     │ Ver estado  │ Registrar   │ Exportar para         │
│ Conectar    │ cliente     │ factura     │ de cada     │ pago        │ contador              │
│ datos       │             │             │ factura     │ recibido    │                       │
│ fiscales    │             │             │             │             │                       │
├═════════════╪═════════════╪═════════════╪═════════════╪═════════════╪═══════════════════════╡
│  MVP (lo mínimo para que el journey completo funcione end-to-end)                            │
├═════════════╪═════════════╪═════════════╪═════════════╪═════════════╪═══════════════════════╡
│ • Signup    │ • Cargar    │ • Crear     │ • Lista de  │ • Marcar    │ • Exportar a Excel    │
│   con email │   cliente   │   factura   │   facturas  │   factura   │   las facturas del    │
│ • Cargar    │   manual    │   multi-    │   con estado│   como      │   mes                 │
│   datos     │   (nombre,  │   moneda    │   (emitida/ │   "cobrada" │                       │
│   fiscales  │   mail,     │ • PDF       │   cobrada/  │ • Registrar │                       │
│   básicos   │   país,     │   descar-   │   vencida)  │   monto     │                       │
│   (CUIT/    │   moneda)   │   gable     │             │   real      │                       │
│   RFC etc.) │             │ • Enviar    │             │   recibido  │                       │
│             │             │   por email │             │             │                       │
├═════════════╪═════════════╪═════════════╪═════════════╪═════════════╪═══════════════════════┤
│  V2 (profundidad y delight)                                                                  │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┼───────────────────────┤
│ • Onboarding│ • Importar  │ • Template  │ • Recorda-  │ • Link de   │ • Exportar formato    │
│   asistido  │   clientes  │   personali-│   torios    │   pago      │   AFIP                │
│ • Migración │   desde CSV │   zable con │   automáti- │   embebido  │ • Exportar formato    │
│   desde     │ • Vincular  │   logo      │   cos al    │   en factura│   SAT (México)        │
│   Excel     │   contacto  │ • Conversor │   cliente   │ • Conexión  │ • Reporte mensual     │
│             │   recurrente│   TC en     │ • Multi-    │   Stripe /  │   en ARS/MXN/COP      │
│             │             │   tiempo    │   recordat. │   Mercado-  │                       │
│             │             │   real      │   (3, 7,    │   Pago      │                       │
│             │             │             │   15 días)  │             │                       │
├═════════════╪═════════════╪═════════════╪═════════════╪═════════════╪═══════════════════════┤
│  V3+ (avanzado, edge cases)                                                                  │
├─────────────┼─────────────┼─────────────┼─────────────┼─────────────┼───────────────────────┤
│ • Multi-    │ • Cliente   │ • Facturas  │ • Cobranza  │ • Conver-   │ • Integración directa │
│   usuario   │   recurrente│   recurren- │   automati- │   sión auto │   con APIs guberna-   │
│   (Studio)  │   con plan  │   tes       │   zada vía  │   ARS al    │   mentales (AFIP API) │
│ • Permisos  │   de pagos  │ • Multi-    │   WhatsApp  │   cobrar    │ • Asistente fiscal    │
│   por rol   │             │   ítem      │             │ • Notas de  │   IA por país         │
│             │             │   detallado │             │   crédito   │                       │
└─────────────┴─────────────┴─────────────┴─────────────┴─────────────┴───────────────────────┘
```

**Lectura del mapa:**

- **El MVP entrega el journey completo:** Camila se registra, carga un cliente, emite una factura, marca cuándo cobró y exporta a Excel para su contador. **Aunque básico, funciona end-to-end.**
- **V2 agrega delight y profundidad:** templates lindos, recordatorios automáticos, link de pago. Acá empieza el verdadero diferencial.
- **V3 agrega potencia para casos avanzados:** multi-usuario, integraciones gubernamentales, etc.

**Razonamiento del corte de MVP:**

Cada celda del MVP cumple tres criterios:
1. **Es necesaria** para que el journey funcione.
2. **Es suficiente** (versión más simple posible).
3. **Es factible** en 8-10 semanas.

Lo que NO está en el MVP (y por qué):
- Conversor TC en tiempo real → es delight, no esencial para emitir factura.
- Recordatorios automáticos → el usuario puede mandarlos manualmente al principio.
- Integración Stripe → en V1 puede pagarse por transferencia tradicional.

## La regla del "primer paseo end-to-end"

> **Un buen MVP debe permitir al usuario completar el journey completo, aunque mucho sea básico o manual.**
>
> Es mejor un journey completo con cada paso "feo" que un solo paso pulido sin posibilidad de avanzar.

Esto se conoce como "walking skeleton" (esqueleto que camina).

## Tips para que el story map sea útil

- **Visualizalo grande.** Un story map en una pantalla pequeña no sirve. Pared, Miro, Figjam.
- **Usá post-its de colores distintos** para distinguir tipos (UX, backend, integración, etc.).
- **Mantenelo vivo.** No es un entregable de inicio: vive con el producto.
- **Cuestioná cada celda del MVP.** "Si sacamos esto, ¿el journey sigue funcionando?" Si la respuesta es "sí, con dificultad", probablemente lo podés posponer.
- **No detalles excesivamente las V3+.** Lo lejano cambia. Mantenelo a nivel idea.
- **Usalo en planning.** El backlog de Jira sale del story map, no al revés.

## Errores comunes

| Error | Síntoma | Cómo evitarlo |
|-------|---------|---------------|
| MVP = "primer release de cada columna" | Toma muchos meses, no entrega valor incremental | El MVP debe ser un slice horizontal delgado |
| Mezclar backbone con features técnicas | "Setear base de datos" en el backbone | Backbone = lo que hace el usuario |
| Olvidarse del usuario | El mapa parece arquitectura técnica | Cada celda debe poder leerse desde "el usuario..." |
| No actualizar el mapa | Termina siendo decorativo | Revisarlo en cada planning |
| Confundir story map con roadmap temporal | Discutir fechas en lugar de scope | El story map es scope; el roadmap es calendario |

## Conexión con otros frameworks

- **Se alimenta de:** Value Proposition Canvas (las features), Customer Journey Map (el backbone), JTBD (el job que el MVP debe completar).
- **Alimenta a:**
  - **Backlog de delivery** (Jira / Linear)
  - **Roadmap trimestral**
  - **Plantilla de Hipótesis** (cada release es un set de hipótesis a validar)
  - **Test/Learning Cards** (las features del MVP se testean)

## Lectura recomendada

- *User Story Mapping* — Jeff Patton (2014). Libro fundacional.
- Blog: jpattonassociates.com.
- Plantillas en miro.com y figjam.com.
