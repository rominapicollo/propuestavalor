# 12 — Wardley Maps

> Mapas estratégicos de Simon Wardley para visualizar componentes de una propuesta según su madurez evolutiva y decidir dónde innovar.

---

## Qué es

Una técnica de mapeo estratégico creada por **Simon Wardley** que combina dos ejes:

- **Eje vertical (Y):** cadena de valor (de las necesidades del usuario hacia abajo, a los componentes que las habilitan).
- **Eje horizontal (X):** evolución (de génesis a commodity).

A diferencia de un diagrama de arquitectura, un Wardley Map es **direccional**: muestra hacia dónde se mueven los componentes con el tiempo y permite decidir dónde innovar vs. dónde usar algo estándar.

## Para qué sirve

- Decidir qué componentes construir desde cero vs. cuáles consumir como commodity.
- Detectar dónde está la verdadera oportunidad de diferenciación.
- Anticipar movimientos del mercado (todo tiende a evolucionar hacia commodity).
- Comunicar estrategia técnica a stakeholders no técnicos.
- Evitar invertir en innovar componentes que ya son commodities.

## Cuándo usarlo

En la **Etapa 4 (Diseñar la propuesta)**, **opcionalmente**, cuando tu propuesta tiene varios componentes tecnológicos y tenés que decidir dónde invertir esfuerzo de I+D. Si tu solución es monolítica y simple, podés saltearlo.

## Visual del mapa

```
        VISIBLE
            ▲
            │                                                                
   USUARIO  │  [Usuario]                                                     
            │      │                                                         
            │      │ necesita                                                
            │      ▼                                                         
        NECESI- │ [Necesidad] ──────────────────                                              
        DADES   │                                                            
            │      │ habilitada por                                          
            │      ▼                                                         
        CAPACI- │  [Capacidad] ───────────────                                                 
        DADES   │                                                            
            │      │ habilitada por                                          
            │      ▼                                                         
        COMPONEN│ [Componente]  ─────────────                                                 
        TES     │      │                                                     
            │      │ habilitado por                                          
            │      ▼                                                         
        INFRA-  │  [Infraestructura] ──────                                                   
        ESTRUC. │                                                            
            ▼                                                                
        INVISIBLE                                                            
                ─────────────────────────────────────────────────────────►   
                                                                             
                GÉNESIS    CUSTOM    PRODUCTO     COMMODITY                
                (nuevo,    (a medida)(comprable,  (utility,                
                única vez)            replicable) ubicuo)                  
                                                                             
                EVOLUCIÓN ─────────────►                                     
```

## Las 4 etapas de evolución

| Etapa | Descripción | Ejemplo (computación) |
|-------|-------------|----------------------|
| **Génesis** | Algo nuevo, único, mal entendido. Alta incertidumbre. | Computación cuántica (hoy) |
| **Custom-Built** | Construido a medida, costoso, sin estándares | Mainframes en los 60 |
| **Producto** | Productizado, comprable de varios proveedores | Servidores físicos en los 2000 |
| **Commodity** | Utility, indistinguible entre proveedores, pagás por uso | Cloud (AWS, GCP, Azure) |

**Insight central:** todo se mueve de izquierda a derecha con el tiempo. La pregunta estratégica es: ¿en qué punto de la evolución está cada componente de mi propuesta?

## Reglas estratégicas según etapa

| Etapa del componente | Estrategia recomendada |
|----------------------|------------------------|
| **Génesis** | Experimentar, hacer I+D, aceptar fallas |
| **Custom-Built** | Construir si te diferencia; tercerizar si no |
| **Producto** | Comprar (no construir); el diferencial está en otro lado |
| **Commodity** | Consumir como utility (AWS, etc.); construir es despilfarro |

**Error clásico:** construir desde cero algo que ya es commodity (ej: tu propio sistema de pagos cuando podés usar Stripe).

## Cómo se usa: protocolo paso a paso

1. **Definí al usuario** y su necesidad principal (la cima del mapa).
2. **Listá los componentes** necesarios para satisfacer esa necesidad. Pensá en **capacidades**, no en features.
3. **Ordená verticalmente** según visibilidad: cuanto más cerca del usuario, más arriba.
4. **Conectá los componentes** mostrando dependencias.
5. **Posicioná horizontalmente** cada componente en su etapa evolutiva actual.
6. **Aplicá las reglas estratégicas:**
   - Componentes en génesis → invertir si son diferenciales.
   - Componentes en commodity → consumir, no construir.
7. **Anticipá movimientos:** ¿qué componentes se moverán hacia la derecha en 1-2 años?
8. **Tomá decisiones de make-vs-buy** explícitas.

## Ejemplo precompletado: FinFlow

**Necesidad del usuario:** "Gestionar mi facturación y cobranza profesional sin perder dinero ni tiempo."

```
        VISIBLE
            ▲                                                                       
            │ [Camila — freelancer]                                                  
            │     │                                                                  
            │     ▼                                                                  
            │ [Facturación profesional multi-moneda]                                 
            │     │                                                                  
            │     ▼                                                                  
            │ [App de gestión financiera] ◄── DIFERENCIACIÓN                       
            │     │  │  │                                                            
            │ ┌───┘  │  └────┐                                                       
            │ ▼      ▼       ▼                                                       
            │ [Cobr] [Conver-[Compliance fiscal]                                     
            │  auto] sión TC] LATAM                                                  
            │  │      │       │                                                      
            │  │      │       ▼                                                      
            │  │      │   [APIs gubernamentales (AFIP/SAT)] ◄── PRODUCTO            
            │  │      ▼                                                              
            │  │  [Datos de TC real-time] ◄── PRODUCTO                              
            │  ▼                                                                     
            │ [Pasarela de pagos] ◄── PRODUCTO / COMMODITY                          
            │  │                                                                     
            │  ▼                                                                     
            │ [Mensajería WhatsApp Business API] ◄── PRODUCTO                       
            │                                                                        
            │                                                                        
            │ [Infraestructura cloud] ◄── COMMODITY                                  
            │ [Auth / DB / Storage] ◄── COMMODITY                                    
            ▼                                                                        
        INVISIBLE                                                                    
              ──────────────────────────────────────────────────────────►            
              GÉNESIS     CUSTOM       PRODUCTO        COMMODITY                  
```

**Lectura estratégica:**

| Componente | Etapa | Decisión |
|------------|-------|----------|
| App de gestión financiera (UX/UI propia) | Custom | **Construir.** Es el diferencial. |
| Cobranza automatizada | Génesis-Custom | **Construir.** Pocas alternativas en LATAM. |
| Conversión TC real-time | Producto | **Comprar/Integrar.** APIs como Open Exchange Rates. |
| Compliance fiscal LATAM | Custom | **Construir.** Es ventaja regional. |
| APIs gubernamentales | Producto | **Integrar.** AFIP, SAT, SII tienen APIs públicas. |
| Pasarela de pagos | Commodity | **Integrar.** Stripe, MercadoPago. No construir. |
| Mensajería WhatsApp | Producto | **Integrar.** Twilio o WhatsApp Business directo. |
| Infraestructura cloud | Commodity | **Consumir.** AWS / GCP. |
| Auth / DB / Storage | Commodity | **Consumir.** Auth0, Supabase, etc. |

**Insight estratégico clave:**
- El equipo debería **invertir 70% del esfuerzo de desarrollo** en lo Custom (UX de la app + cobranza automatizada + compliance LATAM).
- El **30% restante** en integraciones, no en construcción.
- Construir su propia pasarela de pagos sería un **error estratégico**: comoditizado, regulado, capital-intensivo.

**Movimientos anticipados:**
- "Compliance fiscal LATAM" se moverá hacia "Producto" en 3-5 años. Si FinFlow no acumula ventaja de marca/usuarios antes, perderá la oportunidad.
- "Conversión TC real-time" ya está moviéndose hacia commodity (más APIs gratuitas).

## Patrones comunes (Climatic Patterns)

Simon Wardley identifica patrones predecibles en cómo evolucionan los componentes:

1. **Everything evolves.** Nada queda en génesis para siempre.
2. **Commoditization enables higher-order innovation.** Cuando algo se vuelve commodity (ej: electricidad), se habilitan nuevas innovaciones encima (ej: electrodomésticos).
3. **Inertia is the enemy.** Los incumbentes resisten el movimiento de sus componentes hacia commodity → los startups ganan.
4. **Co-evolution of practice.** A medida que algo evoluciona, evolucionan también las prácticas alrededor.

## Cuándo NO usar Wardley Maps

- Productos muy simples con pocos componentes.
- Cuando no tenés visibilidad ni del usuario ni de la cadena de valor (etapas tempranas: primero hacé Mom Test).
- Si el equipo está estresado con plazos de delivery; este es un ejercicio estratégico, no operativo.
- Si no estás dispuesto a tomar decisiones difíciles de "no construir esto".

## Tips para aplicarlo bien

- **Llamá las cosas por su nombre.** "Datos del usuario" no es un componente. "API REST de perfiles de usuario con autenticación JWT" sí.
- **Una necesidad por mapa.** Si tu producto cubre varias necesidades, hacé un mapa por cada una.
- **Hacelo con el equipo técnico Y de negocio juntos.** Si lo hace solo ingeniería, sesgo de "lo nuestro es génesis"; si lo hace solo negocio, sesgo de "es todo commodity".
- **Discutí los movimientos futuros.** El mapa hoy es menos importante que las flechas hacia dónde se mueven los componentes.
- **No te obsesiones con la precisión.** Es una herramienta de discusión estratégica, no un diagrama formal.

## Conexión con otros frameworks

- **Se alimenta de:** Lean Canvas (componentes del modelo), arquitectura técnica preliminar.
- **Alimenta a:**
  - **Decisiones de make-vs-buy**
  - **Roadmap técnico**
  - **Estrategia competitiva** (sabés contra quién competís en cada componente)
  - **Pre-mortem** (los riesgos en componentes commodity son distintos a los de génesis)

## Lectura recomendada

- *Wardley Maps* — Simon Wardley (libro publicado en serie en Medium, gratuito, busca "Wardley Maps Medium").
- Sitio: learnwardleymapping.com.
