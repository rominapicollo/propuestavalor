# 15 — Pre-mortem

> Ejercicio de Gary Klein: imaginar que el proyecto ya fracasó y reconstruir por qué, ANTES de empezar a construir.

---

## Qué es

Una técnica creada por **Gary Klein** (psicólogo cognitivo) que invierte la lógica del análisis de riesgos tradicional. En lugar de preguntar "¿qué podría salir mal?", el pre-mortem te pide imaginar que el proyecto **ya fracasó** y escribir la historia retrospectiva de por qué.

El cambio de tiempo verbal —de futuro condicional a pasado consumado— libera al equipo del optimismo defensivo y hace aparecer riesgos que la prospección normal oculta.

## Para qué sirve

- Sacar a la luz riesgos que el equipo intuye pero no se anima a verbalizar.
- Identificar puntos ciegos antes de invertir tiempo y dinero.
- Generar planes de mitigación preventivos.
- Calibrar el optimismo del equipo (todos los equipos sobreestiman su capacidad).
- Detectar consenso falso ("todos estamos de acuerdo pero nadie está convencido").

## Cuándo usarlo

Al final de la **Etapa 4 (Diseñar la propuesta)**, después de tener Lean Canvas + Value Proposition Canvas + Story Mapping. Es el último filtro antes de empezar a construir.

También se puede usar en cualquier hito grande: lanzamiento, fundraising, expansión a nuevo mercado, contrato grande.

## La diferencia entre pre-mortem y post-mortem

| Post-mortem | Pre-mortem |
|-------------|------------|
| Después del fracaso | **Antes** del fracaso |
| Aprender para el próximo proyecto | Prevenir el fracaso actual |
| Mira al pasado real | Mira a un pasado imaginado |
| Genera defensividad | Genera apertura (es ficción) |

## Cómo se usa: protocolo paso a paso

1. **Reuní al equipo completo** (producto, diseño, ingeniería, negocio). Idealmente 5-10 personas.
2. **Plantear el escenario:**
   > "Imaginen que estamos en [fecha futura, típicamente 6-12 meses]. El proyecto **fracasó rotundamente.** No solo no logramos los objetivos: fue un fracaso reconocido. Lo cancelamos / no consigamos siguiente ronda / el equipo se disolvió.
   > Su misión: escribir, en silencio, durante 10 minutos, por qué fracasamos."
3. **Trabajo individual (10 min).** Cada persona escribe en post-its tantas razones como pueda. Sin filtros, sin discutir.
4. **Compartir en ronda.** Cada persona lee sus razones. **No se cuestionan ni se descartan.**
5. **Agrupar por categoría** (técnico, mercado, equipo, dinero, regulación, timing, etc.).
6. **Priorizar las 3-5 razones más probables** y/o más impactantes (puede ser por votación dot-voting).
7. **Para cada razón priorizada, definir:**
   - Indicadores tempranos de que está pasando.
   - Acción preventiva concreta.
   - Responsable y fecha.
8. **Documentar el resultado** y revisitar en cada hito relevante del proyecto.

## El formato del prompt que dispara mejores respuestas

El prompt importa. Hay diferencias entre:

| Prompt | Calidad de respuestas |
|--------|----------------------|
| "¿Qué podría salir mal?" | Lista genérica, baja profundidad |
| "¿Qué riesgos tenemos?" | Listas defensivas, poca creatividad |
| "Imaginen que fracasamos. ¿Por qué?" | **Más riesgos identificados, más concretos** |
| "Llevamos 6 meses y todo se cayó. Escribí el obituario del proyecto." | Aún más profundo, narrativo |

El estudio original de Klein muestra que la formulación como **"imaginen un futuro consumado"** aumenta la cantidad y calidad de riesgos detectados en un 30%.

## Ejemplo precompletado: FinFlow

**Contexto:** equipo de FinFlow al final de Etapa 4. Tienen Lean Canvas V2, Value Proposition Canvas con fit razonable, y un Story Map con MVP definido para los próximos 4 meses.

**Prompt usado:**
> "Imaginen que estamos en abril de 2027. FinFlow fracasó. Cerramos la empresa, devolvimos lo que pudimos a los inversores, y el equipo se disolvió. Escriban en 10 minutos por qué."

**Razones recolectadas (todas las del equipo, sin filtrar):**

```
ÁREA: ADOPCIÓN / MERCADO
─────────────────────────
1. Los freelancers prefirieron seguir con su Excel a pesar de los demos.
2. El segmento target es demasiado nicho para escalar a 3.000 users pagos.
3. Subestimamos cuánto cuesta cambiar el hábito de uso de Excel.
4. El canal "comunidades" no escaló: dependimos de 3 influencers que pidieron equity.
5. Wave o QuickBooks lanzaron una versión LATAM en español y nos arrasaron.

ÁREA: TÉCNICO / COMPLIANCE
──────────────────────────
6. AFIP cambió su API de facturación en plena construcción y tuvimos que rehacer.
7. Las regulaciones de cada país (4 mercados objetivo) explotaron el scope.
8. WhatsApp Business API rechazó nuestra cuenta y la cobranza automatizada nunca funcionó.
9. La integración con Stripe LATAM requirió más cumplimiento del esperado.

ÁREA: EQUIPO / EJECUCIÓN
────────────────────────
10. Perdimos al PM principal a mes 5 y nunca lo reemplazamos bien.
11. El equipo era muy técnico y subestimamos el peso del go-to-market.
12. Nos enamoramos del feature "dashboard balance ARS" y descuidamos cobranza.
13. Nunca hicimos suficientes entrevistas continuas (solo al principio).

ÁREA: NEGOCIO / DINERO
──────────────────────
14. El CAC fue 3x lo proyectado por canales pagos vs comunidades.
15. La disposición a pagar no era USD 9 sino USD 3-4.
16. El churn fue 8-10% mensual, no 5%.
17. No conseguimos próxima ronda porque las métricas de retención fueron flojas.

ÁREA: TIMING / EXTERNAS
───────────────────────
18. Una devaluación grande en uno de los mercados destruyó el comportamiento del usuario.
19. Lanzamos en estación de impuestos cuando los usuarios estaban saturados.
20. Argentina implementó una nueva regulación cambiaria que invalidó nuestro modelo de TC.
```

**Top 5 priorizadas por probabilidad × impacto:**

| # | Razón | Indicadores tempranos | Acción preventiva | Responsable |
|---|-------|----------------------|-------------------|-------------|
| 1 | Disposición a pagar es USD 3-4 no USD 9 (riesgo 15) | Smoke test con landing muestra CTR < 1% en plan Pro | **Validar pricing con 2 smoke tests A/B antes de construir** | PM |
| 2 | Churn alto (riesgo 16) | Cohorte mes 2 retiene < 70% | **Implementar activation tracking desde día 1; alertar si Day-7 retention cae** | Data + PM |
| 3 | Canal comunidades no escala (riesgo 4) | Mes 3 = 80% del traffic depende de 2 fuentes | **Diversificar canales desde mes 2; tener 4 fuentes en mes 6** | Growth |
| 4 | Cambio en API AFIP (riesgo 6) | Anuncios AFIP de cambios en facturación electrónica | **Arquitectura desacoplada: módulo de integración fiscal separado y versionado** | CTO |
| 5 | Subestimación de cambio de hábito vs Excel (riesgo 3) | Time to first invoice > 7 días en cohortes | **Migrador automático desde Excel + onboarding asistido** | Producto |

**Documentación de pre-mortem:**
- Se archiva en Notion bajo `/Producto/Riesgos/Pre-mortem FinFlow Q2 2026`.
- Se revisita en cada review trimestral.
- Se chequea con datos al mes 3, 6 y 12.

## Tips para que el pre-mortem funcione

- **Hacelo antes de empezar a construir.** Si ya invertiste 3 meses, hay sesgo del costo hundido.
- **Permití anonimato.** En equipos jerárquicos, la gente no critica al jefe. Si necesitás, usá un Google Form.
- **No descartes nada en la fase de recolección.** Lo descartás en la priorización, no antes.
- **Tomá las razones más raras en serio.** A veces son las más reveladoras (un junior detecta lo que un senior normaliza).
- **Convertí las top 5 en acciones, no en lista de "estar atentos".** Si no hay responsable y fecha, no se hace.
- **Repetilo cada 6 meses.** Los riesgos cambian con el contexto.

## Variantes útiles

| Variante | Cuándo usarla |
|----------|---------------|
| **Pre-mortem en parejas** | Equipos chicos: 2 personas se desafían mutuamente |
| **Pre-mortem por área** | Proyectos grandes: cada área hace su propio pre-mortem |
| **Murder boarding** | Versión más confrontacional: cada idea se "asesina" antes de aceptarla |
| **Black hat thinking** (De Bono) | Solo se piensa críticamente durante un período fijo |
| **Inversion** (Charlie Munger) | Pensar al revés: ¿qué haría seguro nuestro fracaso? Evitar eso. |

## Errores comunes

- **Hacerlo como formalidad.** Si los líderes no toman en serio los resultados, el equipo deja de poner energía la próxima vez.
- **Detallar demasiado.** El pre-mortem no es un análisis exhaustivo de riesgos: es disparo creativo.
- **Mezclarlo con análisis FODA.** Son ejercicios distintos; mezclados pierden valor.
- **Convertirlo en sesión de quejas.** El moderador debe sostener el frame ficticio ("imaginen…") y no dejar que se vuelva crítica al management actual.

## Conexión con otros frameworks

- **Se alimenta de:** Lean Canvas (hipótesis riesgosas), Value Proposition Canvas (puntos de no-fit), Story Mapping (alcance comprometido).
- **Alimenta a:**
  - **Plantilla de Hipótesis** (cada riesgo top se convierte en hipótesis a vigilar)
  - **RAT** (el riesgo más alto se vuelve el primer experimento)
  - **Plan de mitigación / risk register**
  - **Roadmap** (las acciones preventivas son trabajo real)

## Lectura recomendada

- *Sources of Power* — Gary Klein.
- HBR (2007) — *Performing a Project Premortem* (artículo corto y aplicable).
- *Thinking, Fast and Slow* — Daniel Kahneman (referencia al concepto).
