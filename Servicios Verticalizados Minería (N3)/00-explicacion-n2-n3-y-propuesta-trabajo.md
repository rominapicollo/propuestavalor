---
title: Qué es N2, qué es N3 y cómo proponemos construir los N3 de Minería
audiencia: Dueños de la vertical de Minería (Account Director, Squad Lead, Sponsor)
ultima_actualizacion: 2026-05-18
owner: Squad Vertical Minería
---

# Qué es N2, qué es N3 y cómo proponemos construir los N3 de Minería

> Documento corto para alinear con los dueños de la vertical antes de arrancar.

---

## 1. La pirámide en una imagen mental

Acid organiza su propuesta de valor en cuatro niveles que van de lo genérico a lo específico:

| Nivel | Qué es | Quién es dueño | Ejemplo en minería |
|---|---|---|---|
| **N1 — Capacidades** | Las disciplinas técnicas (data engineering, ML, cloud, IA generativa, UX, etc.) | BU correspondiente | "Sabemos hacer pipelines de datos productivos" |
| **N2 — Servicios Cross** | Un servicio empaquetado que se vende a cualquier industria | BU dueña | "AI Workflows & Automation" |
| **N3 — Propuesta por Industria** | El mismo N2 traducido a una vertical específica con su lenguaje, su dolor y sus números | Squad Vertical (AD) | "Automatización de reportería SERNAGEOMIN y permisos en faenas remotas" |
| **N4 — Hipótesis por Cuenta** | La propuesta concreta para *una* cuenta específica con KPI medible y plazo | AD + Client Success de la cuenta | "Si lo implementamos en Cuenta X, en 9 meses reducimos 60% el tiempo de reportería ambiental" |

**La regla mental:** N2 le habla a cualquier cliente. N3 le habla a un cliente de minería. N4 le habla *a ese* cliente de minería.

---

## 2. Qué es un N2 (Servicio Cross)

Un **N2** es un servicio empaquetado que vive en una BU y se puede vender a cualquiera de las 5 industrias del ICP de Acid (Retail, Aerolíneas, Banca, Salud, Minería). Está construido sobre capacidades técnicas (N1) que ya existen y se vendió al menos una vez.

**Cómo se reconoce un N2:**
- Tiene una "card" formal con 10 bloques (qué es, para quién, qué incluye, resultados, equipo, etc.)
- Tiene un dueño claro: una BU.
- Está disponible para que los squads verticales lo usen.

**Ejemplo en minería.** La BU Data & AI Evolution tiene hoy 11 N2 publicados (los Cross). Por ejemplo:
- *Data & MLOps* — un N2 que dice "ponemos modelos de ML en producción con ciclos de despliegue, monitoreo y reentrenamiento".
- *AI Workflows & Automation* — un N2 que dice "automatizamos procesos con IA generativa que lee documentos y ejecuta acciones".
- *Recommendation Model as Product* — un N2 que dice "construimos motores de recomendación productivos con API".

**Lo importante:** el N2 no le habla específicamente a minería. Le habla a cualquier cliente. Es **el insumo**. No el output.

---

## 3. Qué es un N3 (Propuesta por Industria)

Un **N3** toma un N2 y lo *aterriza* a una industria específica. No repite el N2 — lo **traduce**: con qué nombre se llama el caso de uso en la industria, qué dolor de negocio resuelve en el lenguaje del cliente, qué KPI mueve, qué stack particular tiene esa industria, contra quién competimos en esa industria, qué casos hemos hecho ahí.

**Cómo se reconoce un N3:**
- Tiene un nombre propio que un C-Level de la industria reconoce (no "Data & MLOps" sino "Vista 360° Mina-Planta y Monitoreo Predictivo de Activos Críticos").
- Habla del dolor de negocio en plata: "cuando un molino SAG sale de operación no programada, se pierden miles de toneladas por hora".
- Tiene una card de 9 bloques distinta a la del N2: caso de uso, qué cuentas aplican, qué cambia respecto al N2 base, KPI verticalizados, operativa típica, competidores en la industria, stack típico, casos de la industria.

**Ejemplo en minería.** Sobre el N2 *Data & MLOps* construimos el N3:
> **"Vista 360° Mina-Planta y Monitoreo Predictivo de Activos Críticos"**

Lo que cambia del N2 al N3:
- *El nombre.* El cliente minero no compra "Data & MLOps" — compra una vista mina-planta unificada que le evita downtime no programado.
- *Las fuentes.* El N2 habla de bases de datos transaccionales; el N3 habla de PI System, FMS Modular DISPATCH, Maximo, LIMS.
- *Los KPI.* El N2 habla de "modelos en producción"; el N3 habla de "reducción de downtime 15–30%", "aumento OEE 2–5 puntos".
- *Los competidores.* El N2 ignora competencia; el N3 dice "no competimos con Cat MineStar, lo integramos".
- *El equipo.* El N3 incorpora roles que el N2 no menciona: Reliability Engineer del cliente, Domain Expert minero, Geometalurgista cuando se involucra leyes.

**Lo importante:** un N3 sin nombre propio + sin números de la industria + sin diferenciales contra competidores de la industria *no es un N3, es catálogo*.

---

## 4. Por qué importa construir los N3 ahora

Hasta ahora, la conversación de Acid con un cliente minero arrancaba con un Cross genérico ("podemos hacerle ML productivo") y se viralizaba propuesta por propuesta. Eso funcionó para vender, pero **no acumula**: cada propuesta es desde cero, no hay un activo del squad, y el cliente percibe que Acid no entiende minería.

Construir N3 cambia eso. Por cada N3 que el squad publica:
- Las conversaciones arrancan con el cliente reconociéndose ("eso es lo que me pasa").
- Las N4 (propuestas por cuenta) se arman 3-4 veces más rápido sobre el mismo N3.
- El squad acumula un activo que sobrevive a las personas.
- Marketing puede producir contenido que habla en minería, no en general.

En el marco del rollout ABE, este es el primer momento estructural en que el squad vertical tiene **dueño claro de los N3**. Antes no había quién los construyera.

---

## 5. La propuesta de trabajo

### Lo que ya hicimos

Tenemos un primer paso ya en el repo, en el branch `mineria`:
- **Marco de los 5 N3 sobre los Cross del PDF inicial** (Adaptación Minería - Data, mayo 2026):
  1. *Vista 360° Mina-Planta y Monitoreo Predictivo* sobre Data & MLOps
  2. *Automatización de Reportería Regulatoria y Extracción Documental* sobre AI Workflows & Automation
  3. *Recomendación de Mantenimiento y Rutas de Acarreo* sobre Recommendation Model
  4. *Producto de Datos para Optimización Logística Mina-Puerto* sobre Data as Product
- **Archivo de ideación** con 7 propuestas adicionales de N3 sobre Cross no listados en el PDF (GISTM/tailings, ESG, forecast insumos, RAG operacional, geometalurgia, IT/OT, BPO HSE).

Estos N3 están en estado **incipiente**: la primera versión escrita por el squad. Falta calibrarlos con la BU y con clientes reales.

### Cómo proponemos seguir — en tres olas (3 a 6 meses)

**Ola 1 — Una vertical, una N3, manual y completa (próximos 60 días).**
- Elegimos una cuenta donde el squad ya tenga tracción y un Cross con caso claro.
- AD + BU lead trabajan en sesiones de 2-3 horas, 1-2 veces por semana, sobre la card de 9 bloques del N3 elegido.
- Output: N3 lista para usar en cuentas Tier A y B, y el aprendizaje sobre cómo construir un N3.

**Ola 2 — Dos N3 más, también manual (días 60–120).**
- Aprovechamos el patrón aprendido en Ola 1 para producir 2 N3 más sobre Cross distintos.
- El squad de minería ya conoce qué pregunta del template cuesta más, dónde poner energía, qué descartar.
- Esta ola calibra el template: lo que funcionó se mantiene, lo que falla se descarta.

**Ola 3 — Las N3 restantes con asistencia tecnológica (días 120 en adelante).**
- Una vez calibrado el template y con 3 N3 ejemplares, recién aquí entra un skill que genera un draft de N3 a partir del Cross + inputs estructurados.
- El squad y la BU lo revisan en sesiones más cortas. La automatización **acelera** lo que la organización ya sabe hacer.

### Por qué manual primero (la trampa a evitar)

La tentación es saltar al skill automático "porque ya entendemos". La complejidad real de un N3 solo aparece cuando se ejercita:
- ¿Qué pregunta del template no se entiende?
- ¿Qué bloque cuesta llenar?
- ¿Dónde el squad y la BU tienen lecturas distintas del mismo dolor?

Esa complejidad es lo que el ejercicio manual hace visible y resoluble. Si se automatiza antes, queda enterrada en el output del skill y reaparece más tarde, cuando ya hay tres o cuatro N3 producidas con el mismo error de origen.

### Qué necesitamos de los dueños de la vertical

1. **Decisión de qué N3 arrancar primero** (Ola 1). Recomendación del squad: elegir el cruce donde tengamos cuenta foco, Cross con caso reciente y BU lead disponible. Candidatos: el N3 de *AI Workflows & Automation* (tenemos caso propio reciente con GCP/Gemini en una operación minera) o el N3 de *Vista 360° Mina-Planta* (mayor upside financiero pero más fricción técnica IT/OT).
2. **Asignación de dedicación.** El AD del squad +25% durante 8 semanas; la BU lead de Data & AI Evolution +10%; un Reliability Engineer o Domain Expert del cliente +20% si se aterriza con cuenta foco desde la Ola 1.
3. **Compromiso de patrocinio ante el cliente.** Si la Ola 1 se ancla en una cuenta real, el sponsor ejecutivo de la vertical asiste a la primera reunión de validación con el cliente.
4. **Mandato de prioridad.** Definir explícitamente que estos N3 son objetivo Q3 del squad y no compiten con la pila táctica del trimestre.

---

## 6. Lo que NO estamos proponiendo (para evitar malentendidos)

- **No estamos inventando capacidades nuevas.** Trabajamos sobre Cross que ya existen.
- **No estamos reescribiendo los Cross.** El N3 vive aparte del N2 base.
- **No estamos prometiendo casos cerrados.** Estos N3 son armas comerciales del squad; las ventas (N4) se cierran cuenta por cuenta.
- **No estamos pidiendo presupuesto adicional.** El esfuerzo entra dentro de la dedicación del squad y de la BU.
- **No estamos atando a un cliente único.** Los N3 son activos del squad; sirven para BHP, Codelco, Antofagasta, Minera Escondida, MEL, Anglo American Sur, Collahuasi, Quebrada Blanca y para cualquier cuenta nueva.

---

## 7. Próximos pasos concretos

1. **Reunión de 60 min con los dueños de la vertical** para validar este enfoque y decidir cuál N3 arrancar en Ola 1.
2. **Confirmar BU lead** disponible (BU Data & AI Evolution).
3. **Kickoff de Ola 1** con calendario de sesiones de 8 semanas.
4. **Primer review interno** del N3 producido al final de la semana 4.
5. **Validación con cliente foco** del N3 al final de la semana 8.

---

## Apéndice: glosario rápido

- **Cross / N2.** Servicio empaquetado que una BU ofrece a cualquier industria. Hoy hay 11 Cross de la BU Data & AI Evolution.
- **N3.** Aterrizaje del N2 a una industria específica. Es el delta para minería.
- **N4.** Propuesta concreta para una cuenta específica, vive en la sección 08 del Plan de Cuenta.
- **AD.** Account Director — dueño económico y relacional de la cuenta y del squad vertical.
- **BU.** Business Unit — dueña de las capacidades y los Cross.
- **Card.** Documento navegable que estructura un N2 o un N3 con sus bloques estandarizados.
- **Squad vertical.** Equipo del AD que cubre una industria entera (en este caso, minería).
- **Tier A/B/C/D.** Clasificación de cuentas por potencial. Los N3 personalizados se construyen para Tier A y B.

---

**¿Preguntas?** Esta es la primera versión del documento. Las dudas de los dueños son input directo para mejorarlo antes de subir el proceso a operación.
