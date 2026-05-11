---
title: Recommendation Model as Product
sidebar_label: Recommendation Model as Product
description: Sistema de recomendación personalizada productizado como API operacional, que aumenta la conversión y mejora la experiencia del usuario en plataformas digitales.
sidebar_position: 3
---

# Recommendation Model as Product
**BU:** Data & AI Evolution | **Servicio Cross:** Recommendation Model as Product | **Versión:** 1.0 | **Última actualización:** 2026-04-28 | **Owner:** Data & AI Evolution Lead

---

## Experiencia de Acidlabs en este servicio

- **Caso Logística: Infraestructura de datos escalable para modelos de ML de recomendaciones en B2B** ([Koandina](/docs/unidades-de-negocio/data-ai-evolution/casos-de-exito/catalogo-de-casos?empresa=Koandina)): arquitectura AWS regional para modelos mixtos de recomendación con API al 99,9% de disponibilidad y adherencia del 20%.
- **Caso Logística: Modelo analítico mixto Heurístico y de ML para recomendar fechas de entrega en B2B** ([Koandina](/docs/unidades-de-negocio/data-ai-evolution/casos-de-exito/catalogo-de-casos?empresa=Koandina)): modelo de recomendación de fechas que redujo la variación absoluta de demanda en 5% y alcanzó 20% de adherencia sostenida.
- **Caso Retail: Hipersegmentación de clientes mediante modelos híbridos de ML y Heurísticos para campañas de marketing** ([Cencosud](/docs/unidades-de-negocio/data-ai-evolution/casos-de-exito/catalogo-de-casos?empresa=Cencosud)): mecanismo de recomendación por segmento para optimizar conversión en canales digitales, con reglas de negocio parametrizables.
- **Caso Retail: Modelo de Market Basket + Modelo de cluster por área/tienda** ([Cencosud](/docs/unidades-de-negocio/data-ai-evolution/casos-de-exito/catalogo-de-casos?empresa=Cencosud)): modelo de asociación de productos para recomendaciones en ecommerce y tienda física, escalado a múltiples tiendas.

---

## Qué es este servicio

Construimos motores de recomendación personalizada que viven en producción: expuestos como API consumible, integrados al stack del cliente y con un ciclo de vida definido para monitorearlos, reentrenarlos y evolucionarlos. El entregable no es un notebook ni un prototipo — es un sistema operacional que mejora la experiencia del usuario final y aumenta la conversión en plataformas digitales.

---

## Qué problema resuelve

- Catálogos extensos con baja tasa de descubrimiento: los usuarios no encuentran lo relevante y el negocio pierde conversión.
- Experiencias homogéneas que no se adaptan al perfil de cada usuario, a pesar de tener datos de comportamiento disponibles.
- Modelos de recomendación que fueron construidos como ejercicio analítico pero nunca llegaron a producción, o que se degradaron con el tiempo sin un proceso de mantenimiento.
- Equipos de negocio que no pueden ajustar las reglas del motor sin depender del equipo técnico cada vez que cambia una política comercial.
- Plataformas que acumulan señales de comportamiento (clics, compras, búsquedas) sin aprovecharlas para personalizar la experiencia en tiempo real.

---

## Para quién es este servicio

### ICP corporativo (fijo)

- **Geografías prioritarias:** 1° Chile · 2° Perú y Colombia · 3° México, Costa Este EE.UU. y Canadá
- **Industrias válidas:** Retail · Aerolíneas · Banca · Salud · Minería
- **Perfil de empresa:** Organizaciones con áreas de datos, tecnología o producto establecidas, con un problema documentado que este servicio resuelve y con capacidad de patrocinar un proyecto (sponsor ejecutivo + referente técnico interno)

### Perfil específico para este servicio

- **Industrias más relevantes:** Retail y Aerolíneas son las industrias con mayor madurez de casos — volumen de catálogo extenso, comportamiento de usuario registrado y presión directa de la personalización en conversión y NPS. Banca también aplica para recomendación de productos financieros y campañas de fidelización. Salud y Minería tienen casos más acotados pero viables (recomendación de protocolos de atención, configuración de pedidos operacionales).
- **Rol del comprador:** Gerencia de Datos / Data & Analytics, Gerencia de Inteligencia Artificial / Advanced Analytics, Gerencia de Transformación Digital — perfiles con mandato de llevar modelos a producción y mejorar la experiencia del cliente final o del operador interno.
- **Síntomas que indica la contraparte:** "tenemos datos de comportamiento pero no los estamos usando para personalizar", "nuestro modelo de recomendación nunca llegó a producción", "el equipo de negocio no puede tocar el motor sin pasar por el equipo técnico cada vez que cambia una política comercial".
- **Trigger de activación:** iniciativa de personalización en canal digital que expone la ausencia de un motor productivo; modelo construido internamente que nunca llegó a producción o que se degradó sin proceso de mantenimiento; presión de negocio para mejorar conversión o ticket promedio con los datos de comportamiento ya disponibles.
- **Perfil mínimo de proyecto:** organización con datos históricos de interacciones de usuario (clics, compras, búsquedas, transacciones), un catálogo de productos, contenidos o servicios a recomendar, y un equipo técnico capaz de integrar una API en la plataforma digital del cliente.

### No es para

- Organizaciones que no tienen datos históricos de comportamiento de usuario ni interacciones en su plataforma, ya que el modelo requiere señales para aprender.
- Equipos que buscan únicamente un reporte o dashboard de análisis de comportamiento, sin intención de productizar el resultado.
- Organizaciones que no cuentan con capacidad técnica para integrar una API en su plataforma digital.

---

## Qué incluye

### Entregables posibles según el engagement

- Diagnóstico de datos y reporte de factibilidad del modelo.
- Arquitectura de datos y diseño del sistema de recomendación.
- Pipelines de datos productivos que alimentan el modelo.
- Modelo entrenado, versionado y desplegado en infraestructura cloud.
- API de recomendaciones documentada y lista para consumir.
- Dashboard de monitoreo con métricas de negocio y técnicas del modelo.
- Runbook de operación y guía de reentrenamiento.
- Sesiones de transferencia de conocimiento al equipo técnico y de negocio.

### Actividades principales

1. **Discovery & Data Assessment** — levantamiento del contexto de negocio, revisión de fuentes de datos disponibles (interacciones de usuario, catálogo, señales transaccionales), evaluación de calidad y cobertura, y definición del enfoque algorítmico más adecuado para el caso.
2. **Diseño del Modelo y Arquitectura** — selección del enfoque de recomendación (colaborativo, basado en contenido, híbrido, heurístico), diseño de la arquitectura de datos y de la API que expondrá las recomendaciones al sistema del cliente.
3. **Construcción de Pipelines de Datos** — desarrollo de los pipelines de ingesta, transformación y almacenamiento necesarios para generar los vectores de usuario e ítem que consume el modelo, integrados con las fuentes de datos existentes.
4. **Desarrollo y Entrenamiento del Modelo** — implementación del algoritmo, entrenamiento sobre datos históricos, ajuste de hiperparámetros y validación con métricas de negocio (conversión, relevancia, diversidad) y técnicas (precisión, recall, NDCG).
5. **Productización y Despliegue** — empaquetamiento como servicio (API REST o integración directa), despliegue en infraestructura cloud, configuración de monitoreo y alertas.
6. **Integración y Habilitación** — acompañamiento al equipo técnico del cliente en la integración de la API, configuración de reglas de negocio y parametrización del modelo.
7. **Definición del Ciclo de Vida** — establecimiento de criterios de evaluación continua, frecuencia de reentrenamiento y proceso para incorporar nuevas señales o cambios en el catálogo.

### Qué NO incluye

- Desarrollo del frontend o interfaz de usuario donde se muestran las recomendaciones (la API entrega los ítems; la presentación visual es responsabilidad del equipo del cliente).
- Gestión continua del catálogo de productos o contenidos del cliente.
- Soporte operacional permanente del modelo productivo, salvo que se contrate como servicio separado de Data Support & Monitoring.

---

## Resultados que puede esperar el cliente

| Métrica / Resultado | Valor de referencia (benchmark de mercado) | Notas |
|---|---|---|
| Incremento en tasa de conversión | 20-40% | Benchmark de industria en ecommerce con recomendaciones personalizadas vs. experiencias genéricas |
| Aumento en ticket promedio por sesión | 15-30% | Impulsado por recomendaciones de productos complementarios o de mayor valor |
| Reducción en tasa de abandono del catálogo | 20-35% | Al aumentar la relevancia de los ítems mostrados a cada usuario |
| Mejora en métricas de engagement | 10-25% | Tiempo en plataforma y páginas vistas por sesión en plataformas de contenido |
| Adherencia sostenida al sistema de recomendaciones | Superior al 20% | En contextos B2B donde la adopción es gradual |

:::info
En engagements de logística B2B, Acidlabs ha alcanzado adherencia sostenida del 20% a los sistemas de recomendación y reducción de la variación absoluta de demanda en 5% tras la puesta en producción.
:::

---

## Problemas que podría resolver

Extensiones naturales del servicio hacia contextos donde las capacidades actuales tienen potencial de aplicación directo, pero aún no hay casos implementados.

**Nuevas industrias del ICP:**
- **Banca:** Recomendación personalizada de productos financieros —créditos, seguros, inversiones— basada en el perfil transaccional del cliente, reemplazando campañas masivas por propuestas individualizadas con mayor tasa de activación.
- **Salud:** Recomendación de protocolos de atención, derivaciones clínicas o medicamentos alternativos basada en el historial del paciente y patrones de casos similares, apoyando la toma de decisión clínica sin reemplazarla.
- **Minería:** Recomendación de configuraciones de pedido de insumos y repuestos basada en el historial de operaciones y el plan de producción — patrón B2B directo, análogo al caso Koandina en logística de distribución.

**Evolución técnica del servicio:**
- **Recomendaciones en tiempo real con señales contextuales:** Pasar de modelos batch a motores que reaccionan a señales inmediatas —geolocalización, dispositivo, tiempo en sesión, evento en curso— para personalizar en el momento exacto de la decisión.
- **Recomendaciones conversacionales con LLMs:** Combinar el motor de recomendación con interfaces conversacionales para entregar sugerencias explicadas en lenguaje natural, aumentando la transparencia y la confianza del usuario en el resultado.
- **Recomendaciones cross-canal:** Unificar las señales de comportamiento del usuario a través de app, web y tienda física para producir una recomendación coherente independientemente del punto de contacto, eliminando la fragmentación de perfil por canal.

**Expansión hacia nuevos contextos de uso:**
- **Optimización de surtido en puntos de venta B2B:** Usar el motor para recomendar a distribuidores o puntos de venta qué productos incorporar o destacar según el comportamiento de compra de su zona o segmento, trasladando la personalización del usuario final al operador del canal.
- **Habilitación interna de equipos:** Adaptar el motor para recomendar documentación, casos de referencia, recursos de onboarding o formación interna a perfiles de colaboradores según su rol, BU y etapa en la organización, acelerando la transferencia de conocimiento.

---

## Duración y modalidad de engagement

| Aspecto | Detalle |
|---|---|
| **Duración orientativa** | Entre 3 y 8 meses, según la complejidad del catálogo, la madurez de los datos y el alcance de la integración |
| **Modalidad** | Proyecto cerrado con SOW / Sprints iterativos según el contexto del cliente |
| **Dedicación del equipo cliente** | Requiere un referente de negocio disponible para instancias de trabajo conjunto y un equipo técnico que pueda integrar la API resultante |
| **Formato de trabajo** | Remoto o híbrido según el contexto del cliente |
| **Estructura del engagement** | Discovery & Assessment → Diseño de Modelo y Arquitectura → Construcción de Pipelines → Desarrollo y Entrenamiento → Productización → Integración y Habilitación |

---

## Equipo de Acidlabs involucrado

| Rol | Responsabilidad en este servicio |
|---|---|
| Data Scientist / ML Engineer | Diseño y desarrollo del modelo de recomendación, selección del enfoque algorítmico, entrenamiento y validación |
| Data Engineer | Construcción de pipelines de datos y arquitectura de ingesta que alimenta el modelo |
| Delivery Lead | Gestión del engagement, alineación con el negocio del cliente y coordinación de entregables |
| Solutions Architect (en engagements amplios) | Diseño de la arquitectura cloud y definición del stack tecnológico |

:::info
Este servicio requiere al menos un perfil senior en modelado de ML y un perfil senior en ingeniería de datos, dado que la productización exige decisiones de arquitectura con impacto operacional directo.
:::

---

## Modalidad de contratación

:::info
Esta sección es de uso interno para el equipo comercial.
:::

La modalidad de contratación se define según el contexto del cliente en etapa de preventa. Los formatos más habituales son proyecto cerrado con SOW, sprints iterativos o retainer de mejora continua para el ciclo de vida del modelo.

---

## Servicios relacionados y cross-sell

**Servicios complementarios dentro de esta BU:**
- Data & ML Ops — para operacionalizar el ciclo de vida del modelo (monitoreo, reentrenamiento automatizado y versionamiento en producción) una vez desplegado.
- Forecast & Demand Planning — cuando el motor de recomendación se combina con predicción de demanda para optimizar disponibilidad del catálogo.

**Servicios de otras BUs que suelen combinarse:**
- Enterprise — Integración de sistemas: cuando la API de recomendaciones debe conectarse con ERP, CRM u otros sistemas core del cliente que no son puramente digitales.

---

## Preguntas frecuentes para el equipo comercial

**¿Cómo diferenciamos este servicio de soluciones de mercado como Salesforce Einstein, Dynamic Yield o Algolia?**
Las soluciones de mercado ofrecen recomendaciones genéricas con modelos de caja negra y licencias externas. Acidlabs construye un motor propio entrenado con los datos y señales específicas del cliente, con reglas de negocio a medida y desplegado en la infraestructura del cliente. Eso significa mayor control, mayor diferenciación competitiva y sin dependencia de proveedores externos para evolucionar el modelo.

**¿Cuáles son las objeciones más comunes y cómo responderlas?**

- *Objeción:* "Ya tenemos un equipo interno de Data Science, ¿para qué los necesitamos?"
  *Respuesta:* Trabajamos como extensión del equipo interno, aportando experiencia específica en productización de modelos de recomendación — una disciplina distinta al análisis exploratorio. El foco es llevar el modelo a producción con un ciclo de vida sostenible, algo que los equipos internos rara vez tienen tiempo de construir desde cero.

- *Objeción:* "No tenemos suficientes datos para que funcione."
  *Respuesta:* La evaluación de factibilidad se hace en el Discovery. En etapas tempranas, enfoques basados en contenido o modelos híbridos con componente heurístico permiten arrancar con menos datos y evolucionar hacia modelos más complejos a medida que crece el histórico.

- *Objeción:* "¿Funciona solo para B2C o también para B2B?"
  *Respuesta:* Funciona para ambos. La experiencia de Acidlabs incluye casos en logística y distribución donde el motor recomienda fechas de entrega, condiciones comerciales y configuraciones de pedido sobre transacciones B2B con alta variabilidad de demanda.

**¿Qué necesitamos del cliente para arrancar?**
Acceso a las fuentes de datos de comportamiento de usuario (interacciones, compras, búsquedas), disponibilidad de un referente de negocio con criterio sobre qué recomendar y a quién, y un equipo técnico que pueda integrar la API resultante en su plataforma digital. La alineación de stakeholders entre el área de negocio y el equipo técnico del cliente es clave para que el engagement avance sin fricciones.

---

## Stack tecnológico habitual

El stack se define según el entorno del cliente, pero las tecnologías que Acidlabs utiliza habitualmente en este tipo de servicio incluyen:

**Infraestructura cloud:** AWS (S3, Lambda, DynamoDB, SageMaker, API Gateway), GCP (Vertex AI, BigQuery, Cloud Run) o Azure (ML Studio, Azure Functions).

**Procesamiento de datos:** Apache Spark, DBT, AWS Glue, Dataflow, Athena.

**Desarrollo del modelo:** Python (scikit-learn, LightFM, Implicit, TensorFlow Recommenders), algoritmos de filtrado colaborativo, modelos basados en contenido, enfoques híbridos y heurísticos.

**Servicio y monitoreo:** FastAPI, Docker, Kubernetes, MLflow, Vertex AI Model Registry.

---

## Contacto y escalación

| Rol | Persona | Canal |
|---|---|---|
| **Owner del servicio** | Naoto Aguilar | gustavo.aguilar@acidlabs.com |
| **Consultas comerciales** | ⚠️ Pendiente de completar | — |
| **Referente técnico** | ⚠️ Pendiente de completar | — |

---

*Ficha generada con el Creador de Servicios Acidlabs. Para actualizaciones, contactar al owner.*
