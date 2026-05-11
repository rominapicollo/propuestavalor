---
title: Forecasting & Demand Planning
sidebar_label: Forecasting & Demand Planning
description: Modelos de inteligencia artificial y series de tiempo para anticipar la demanda, reducir quiebres de stock y optimizar el inventario.
sidebar_position: 1
---

# Forecasting & Demand Planning
**BU:** Data & AI Evolution | **Servicio Cross:** Forecasting & Demand Planning | **Versión:** 1.1 | **Última actualización:** 2026-04-28 | **Owner:** ⚠️ Pendiente de completar

---

## Experiencia de Acidlabs en este servicio

- **Modelo ML mixto para recomendar fechas de entrega y reducir demanda en picos** ([Koandina](/docs/unidades-de-negocio/data-ai-evolution/casos-de-exito/catalogo-de-casos?empresa=Koandina)): modelo heurístico y de ML para suavizar picos de demanda y aumentar adherencia operativa; 20% de adherencia sostenida y 5% de reducción en variación absoluta de demanda.
- **Reducción de mermas en productos ultra-perecibles con modelo ML mixto** ([Cencosud](/docs/unidades-de-negocio/data-ai-evolution/casos-de-exito/catalogo-de-casos?empresa=Cencosud)): modelo mixto estadístico y de ML (forecast, clustering y clasificación) para anticipar riesgo de merma y generar accionables en productos perecibles de holding chileno con presencia regional.

---

## Qué es este servicio

Ayudamos a empresas con operaciones complejas a anticipar la demanda con modelos de inteligencia artificial y series de tiempo, reduciendo el exceso de inventario y los quiebres de stock. El resultado es una cadena de abastecimiento que responde al negocio real, no a la intuición ni a las planillas de cálculo.

---

## Qué problema resuelve

- Los equipos de planificación trabajan con métodos manuales o estadísticas básicas que no capturan la estacionalidad, las promociones ni los cambios del mercado, generando errores de forecast que impactan directamente en el capital de trabajo.
- El exceso de inventario inmoviliza capital y genera obsolescencia; los quiebres de stock generan ventas perdidas y erosionan la confianza del cliente. Las empresas oscilan entre uno y otro extremo sin un modelo que los equilibre.
- La planificación de la demanda consume horas de trabajo manual cada ciclo, es propensa a errores y depende de personas clave que concentran el conocimiento del negocio.
- Las decisiones de compra y producción se toman con información rezagada, sin visibilidad de señales externas como tendencias de mercado, clima o eventos que impactan la demanda real.

---

## Para quién es este servicio

<!-- ⚠️ Industrias mencionadas en contexto de casos históricos: Logística, Manufactura, Agroindustria, Distribución — se mantienen como referencia de experiencia implementada pero no forman parte del ICP vigente. Las industrias válidas del ICP corporativo son: Retail · Aerolíneas · Banca · Salud · Minería. -->

### ICP corporativo (fijo)

- **Geografías prioritarias:** 1° Chile · 2° Perú y Colombia · 3° México, Costa Este EE.UU. y Canadá
- **Industrias válidas:** Retail · Aerolíneas · Banca · Salud · Minería
- **Perfil de empresa:** Organizaciones con áreas de datos, tecnología o producto establecidas, con un problema documentado que este servicio resuelve y con capacidad de patrocinar un proyecto (sponsor ejecutivo + referente técnico interno)

### Perfil específico para este servicio

- **Industrias más relevantes:** Retail y Minería — industrias con alta variabilidad de demanda, múltiples SKUs o activos, y procesos de planificación con impacto directo en el capital de trabajo. Aerolíneas aplica en contextos de optimización de capacidad y demand planning de rutas. Banca y Salud tienen casos de uso puntuales en planificación de recursos o insumos.
- **Rol del comprador:** Gerencia de Operaciones / Logística / Supply Chain como dueño del dolor; Gerencia de Datos / Data & Analytics como referente técnico del engagement.
- **Síntomas que indica la contraparte:** "Tenemos quiebres de stock recurrentes en los productos que más rotan", "nuestro inventario creció sin que crecieran las ventas", "el equipo de planificación pasa días consolidando datos y el forecast igual sale mal", "acaban de implementar un ERP y quieren aprovechar los datos que ahora tienen centralizados".
- **Trigger de activación:** Presión por reducción de capital de trabajo, incidente recurrente de quiebres o sobrestock sin diagnóstico cuantitativo, o implementación reciente de un ERP que centraliza datos históricos que antes no estaban disponibles para modelado.
- **Perfil mínimo de proyecto:** Organización con datos históricos de ventas o demanda accesibles en sistemas digitales, un referente de negocio con conocimiento del proceso de planificación actual y un referente técnico con acceso a los sistemas de datos.

### No es para

- Organizaciones que recién están iniciando su proceso de digitalización y aún no cuentan con datos históricos de demanda accesibles en sistemas digitales.
- Empresas que buscan únicamente consultoría estratégica en supply chain sin implementación técnica de modelos.
- Operaciones sin variabilidad de demanda significativa, donde el forecast agrega poco valor frente a un método simple de reposición.

---

## Qué incluye

### Entregables posibles según el engagement

- Modelos de forecasting de demanda entrenados, validados y desplegados en producción, integrados con las fuentes de datos del cliente (ERP, WMS, sistemas de ventas).
- Pipelines de datos automatizados para la actualización y el reentrenamiento periódico de los modelos según la cadencia definida con el cliente.
- Dashboard de monitoreo de forecast con métricas de precisión (MAPE, sesgo, cobertura) para que el equipo de planificación evalúe y ajuste los modelos.
- Herramienta o reporte de planificación de la demanda que integra el output de los modelos al proceso operativo existente del cliente.
- Documentación técnica y de negocio: guías de interpretación del forecast, descripción de variables y lógica de los modelos.
- Sesiones de transferencia de conocimiento al equipo interno del cliente para operar y evaluar los modelos de forma autónoma.

### Actividades principales

1. **Discovery & Data Assessment** — Relevamiento de fuentes de datos históricas, calidad y granularidad de la información disponible, comprensión del proceso de planificación actual y definición de los casos de uso prioritarios.
2. **Feature Engineering & Diseño del Modelo** — Construcción de variables predictoras (estacionalidad, eventos, precios, canales), selección de algoritmos (series de tiempo clásicas, modelos de ML, enfoques híbridos) y definición de la arquitectura de solución.
3. **Entrenamiento, Validación & Ajuste** — Entrenamiento de modelos con datos históricos, backtesting con escenarios reales, comparación contra el método de forecast actual del cliente y ajuste fino según los hallazgos.
4. **Integración & Despliegue** — Integración del modelo con los sistemas del cliente, automatización de la actualización de predicciones y puesta en producción con el equipo técnico del cliente.
5. **Habilitación & Handover** — Transferencia de conocimiento, documentación operativa y definición del modelo de soporte o mejora continua post-implementación.

### Qué NO incluye

- Construcción o migración de la infraestructura de datos de base (esto corresponde al servicio de Data Platforms).
- Soporte operativo continuo de los modelos en producción, salvo que se contrate como servicio adicional de ML Ops.
- Gestión integral del proceso de supply chain o planificación de producción más allá del componente de forecasting.

---

## Resultados que puede esperar el cliente

| Métrica / Resultado | Valor de referencia (benchmark de mercado) | Notas |
|---|---|---|
| Mejora en precisión del forecast (reducción de error) | 20–50% de reducción del error | Benchmark McKinsey; varía según industria y calidad de datos base |
| Reducción de quiebres de stock | Hasta 65% menos | Benchmark de mercado para implementaciones de AI forecasting |
| Reducción de inventario inmovilizado | 20–30% promedio | Mejora en capital de trabajo de $15–20M por cada $1B de revenue |
| Reducción de costos de almacenamiento | 5–10% | Derivado de la optimización de niveles de inventario |
| Tiempo del ciclo de planificación | Reducción significativa | Automatización del proceso reemplaza consolidación manual de datos |
| Mejora en disponibilidad de producto en góndola | 2–4 puntos porcentuales | Representa ventas recuperadas previamente perdidas por quiebres |

:::info
En una empresa de distribución de bebidas, el modelo de forecasting implementado por Acidlabs logró una reducción del 5% en la variación absoluta de demanda y una adherencia sostenida del 20% en las recomendaciones operativas tras su puesta en producción.
:::

---

## Problemas que podría resolver

Extensiones naturales del servicio hacia contextos donde las capacidades actuales tienen potencial de aplicación directo, pero aún no hay casos implementados.

**Nuevas industrias del ICP:**
- **Minería:** Anticipar la demanda de insumos críticos —explosivos, combustibles, repuestos de maquinaria— donde un quiebre de stock detiene la operación con costos por hora muy elevados.
- **Salud:** Forecast de medicamentos e insumos con alta caducidad y demanda estacional volátil, donde el quiebre tiene consecuencias clínicas directas.
- **Banca:** Anticipar la carga operativa en cajeros, sucursales y call centers, y los picos de demanda de productos financieros por campaña.
- **Aerolíneas:** Demand planning de recursos de operación —tripulaciones, insumos de cabina, slots de mantenimiento— más allá del revenue management de asientos.

**Evolución técnica del servicio:**
- **Demand sensing en tiempo real:** Actualización continua de predicciones con señales de punto de venta, IoT o e-commerce para clientes con alta variabilidad intradiaria.
- **Forecasting multicanal:** Modelado integrado de demanda física y digital para optimizar la asignación de stock entre canales en operaciones omnicanal.
- **Simulación de escenarios:** Generar escenarios probabilísticos ante variables externas —tipo de cambio, eventos climáticos, movimientos de competidores— convirtiendo el forecast en una herramienta de planificación estratégica.

**Expansión en la cadena de valor:**
- **Planificación colaborativa con proveedores (CPFR/VMI):** Compartir el forecast con proveedores clave para sincronizar producción upstream y reducir el efecto bullwhip en la cadena completa.
- **Pricing dinámico asistido por forecast:** Usar las predicciones de demanda como insumo para activar acciones de precio anticipadas, ya sea para maximizar margen en picos o reducir sobrestock antes de que se materialice.

---

## Duración y modalidad de engagement

| Aspecto | Detalle |
|---|---|
| **Duración orientativa** | Entre 2 y 6 meses, según la complejidad del negocio, la cantidad de SKUs o categorías a modelar y la madurez de los datos disponibles |
| **Modelos de engagement aplicables** | Fixed Price · Consultoría — el patrón habitual es iniciar con una consultoría diagnóstica (Discovery & Data Assessment) y escalar a Fixed Price para la ejecución completa |
| **Dedicación del equipo cliente** | Requiere un referente de negocio con conocimiento del proceso de planificación y un referente técnico con acceso a los sistemas de datos |
| **Formato de trabajo** | Remoto con instancias de trabajo sincrónico en las fases de discovery, validación y handover |
| **Estructura del engagement** | Discovery & Data Assessment → Feature Engineering & Diseño → Entrenamiento & Validación → Integración & Despliegue → Habilitación & Handover |

---

## Equipo de Acidlabs involucrado

| Rol | Responsabilidad en este servicio |
|---|---|
| Data Scientist Lead | Diseña la estrategia de modelado, lidera el feature engineering, selecciona los algoritmos y es responsable de la precisión final del modelo |
| Data Engineer | Construye los pipelines de datos, automatiza la actualización del forecast e integra los modelos con los sistemas del cliente |
| Analytics Translator / Delivery Lead | Gestiona el engagement, traduce los resultados técnicos a lenguaje de negocio y asegura la alineación con los stakeholders del cliente |
| ML Engineer | Apoya el despliegue en producción, la automatización del reentrenamiento y la observabilidad de los modelos en operación |

:::info
Este servicio requiere al menos un perfil senior en modelado predictivo con experiencia en series de tiempo y machine learning aplicado a demanda, y un perfil senior en ingeniería de datos con experiencia en plataformas cloud.
:::

---

## Modalidad de contratación

:::info
Esta sección es de uso interno para el equipo comercial.
:::

Este servicio se ejecuta bajo modelos de proyecto. Los formatos más habituales son:

- **Fixed Price:** alcance definido, entregable claro y precio cerrado. Aplica cuando el scope del proceso de forecasting está acotado y se han validado las hipótesis de mejora. Requiere scoping workshop previo y proceso de change request para fuera de scope.
- **Consultoría:** diagnóstico del proceso de planificación, evaluación de calidad de datos y hoja de ruta de implementación. Engagement corto que reduce el riesgo antes de comprometer el engagement completo. Puerta de entrada natural a un Fixed Price de ejecución.

**Patrón habitual para este servicio:** el punto de entrada más frecuente es una Consultoría diagnóstica (Discovery & Data Assessment) que valida la calidad de datos y el potencial de mejora antes de escalar a Fixed Price para el desarrollo, entrenamiento e integración de los modelos.

La modalidad final se define según el contexto del cliente en etapa de preventa.

---

## Servicios relacionados y cross-sell

**Servicios complementarios dentro de esta BU:**

- **Data & MLOps** — Para operacionalizar los modelos entrenados con pipelines de ciclo de vida completo, monitoreo y reentrenamiento automatizado en producción.
- **AI Agents & RAGs empresariales** — Para automatizar el proceso de planificación de la demanda a través de agentes que consumen el forecast y generan recomendaciones de compra o producción de forma autónoma.
- **Business Process Optimization** — Para rediseñar el proceso de planificación de la demanda end-to-end una vez que el forecast está disponible como insumo confiable.
- **Data as Product** — Cuando el cliente necesita primero consolidar y limpiar sus fuentes de datos antes de poder entrenar modelos confiables.

**Servicios de otras BUs que suelen combinarse:**

- **BU Enterprise — Integraciones empresariales** — Cuando el cliente requiere integrar el forecast con su ERP (SAP, Oracle, etc.) o sistemas de planificación existentes para automatizar las órdenes de compra o producción.

---

## Preguntas frecuentes para el equipo comercial

**¿Cómo diferenciamos este servicio de lo que hace la competencia?**

Acidlabs combina el entendimiento profundo del proceso de negocio con la implementación técnica de los modelos — no entregamos un modelo en un notebook sino una solución integrada al proceso operativo del cliente. Nuestro foco está en que el equipo de planificación adopte y confíe en el forecast, no solo en que el modelo tenga buen MAPE en backtesting. Adicionalmente, nuestra experiencia transversal en retail, consumo masivo y logística nos permite aportar benchmarks y aprendizajes de industria que acortan el tiempo de exploración inicial.

**¿Cuáles son las objeciones más comunes y cómo responderlas?**

- *Objeción:* "Ya tenemos un equipo de Data Science interno que debería hacer esto."
  *Respuesta:* "Perfecto, trabajamos como extensión de ese equipo. Aportamos experiencia específica en forecasting de demanda y metodologías probadas en industria, lo que acelera los tiempos y evita que el equipo interno tenga que aprender desde cero. El resultado queda en manos del equipo interno, que lo puede operar y evolucionar."

- *Objeción:* "Nuestros datos son muy malos o están incompletos para hacer forecasting con ML."
  *Respuesta:* "La calidad de los datos es parte de lo que evaluamos en el discovery. En muchos casos, con los datos disponibles se puede construir una primera versión del modelo que ya supera el método actual. El assessment inicial nos permite ser honestos sobre qué es posible y con qué nivel de precisión, antes de comprometer el engagement completo."

- *Objeción:* "Ya probamos con un proveedor antes y el modelo no lo usó nadie."
  *Respuesta:* "Es el riesgo más común en este tipo de proyectos. Por eso nuestra metodología incluye desde el inicio al equipo de planificación como parte activa del desarrollo — no solo como validadores al final. El adoption rate del forecast es una métrica que seguimos explícitamente durante el engagement."

**¿Qué necesitamos del cliente para arrancar?**

- Acceso a datos históricos de ventas o demanda en formato digital, preferentemente con granularidad de SKU, punto de venta y fecha.
- Un referente de negocio con conocimiento del proceso de planificación actual y capacidad para validar los resultados del modelo desde la perspectiva del negocio.
- Un referente técnico que conozca los sistemas de datos del cliente y pueda facilitar los accesos necesarios.
- Disponibilidad de stakeholders clave para sesiones de discovery, validación de hipótesis y revisión de resultados del modelo.

---

## Contacto y escalación

| Rol | Persona | Canal |
|---|---|---|
| **Owner del servicio** | Naoto Aguilar | gustavo.aguilar@acidlabs.com |
| **Consultas comerciales** | ⚠️ Pendiente de completar | ⚠️ Pendiente |
| **Referente técnico** | ⚠️ Pendiente de completar | ⚠️ Pendiente |

---

*Ficha generada con el Creador de Servicios Acidlabs. Para actualizaciones, contactar al owner.*
