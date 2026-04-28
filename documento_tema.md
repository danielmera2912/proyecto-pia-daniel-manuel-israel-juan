# Documento de tema y ejemplo

## Grupo
- Daniel Mera Sachse
- Manuel Garrido Serrano
- Israel Soto Cala
- Juan Manuel Vega Carrillo
## Tema

Modelos de automatización con IA en la empresa: gestión de recursos, datos y colaboración humano-máquina.

---

## 1. Problema

Muchas organizaciones quieren incorporar IA, pero se encuentran con tres barreras principales:

- Procesos manuales y repetitivos que consumen tiempo y dinero.
- Falta de una estrategia clara para gestionar el dato como activo principal.
- Resistencia al cambio cultural y escasez de perfiles con capacidades de análisis de datos.

Además, las empresas necesitan escalar soluciones con rapidez sin disparar los costes de infraestructura.


---

## 2. Tecnologías

Para abordar este problema, se plantea un enfoque apoyado en nube e IA:

- Google Cloud Platform como ecosistema de servicios.
- Google App Engine para desplegar aplicaciones de forma escalable.
- Docker en entornos flexibles para personalizar ejecución.
- BigQuery para análisis de grandes volúmenes de datos.
- Datastore y Memcache para persistencia y acceso rápido a información.
- Modelos de IA para clasificación, detección de patrones y recomendación.


---

## 3. Arquitectura

La arquitectura propuesta combina automatizacion operativa con supervisión humana:

### 3.1 Capas

- Capa de ingesta de datos:
	- Captura de eventos operativos (ERP/CRM, tickets, sensores o formularios).
	- Subida de datos estructurados y no estructurados a almacenamiento cloud.
- Capa de almacenamiento y gobierno:
	- Data lake para historico bruto y BigQuery para analitica.
	- Catalogacion, control de acceso por roles y trazabilidad.
- Capa de procesamiento:
	- Limpieza y transformacion (ETL/ELT).
	- Enriquecimiento con reglas de negocio y features para modelos.
- Capa de IA y decision:
	- Modelos para clasificacion, prediccion de demanda y deteccion de anomalias.
	- Motor de recomendaciones para priorizar acciones.
- Capa de aplicacion y consumo:
	- APIs y paneles para equipos de operaciones, finanzas y direccion.
	- Alertas en tiempo real y flujos de aprobacion.
- Capa de observabilidad y mejora continua:
	- Monitorizacion de calidad de dato, drift de modelo y KPIs.
	- Reentrenamiento periodico y versionado de modelos.

### 3.2 Flujo de datos

1. Entrada: llegan datos desde sistemas internos y externos.
2. Preparacion: se validan, normalizan y consolidan.
3. Inferencia: los modelos generan predicciones o clasificaciones.
4. Orquestacion: reglas de negocio convierten la salida en acciones.
5. Salida: paneles, alertas y tareas automatizadas para cada equipo.
6. Feedback: resultados reales vuelven al sistema para medir impacto y mejorar.

### 3.3 Validacion humana

- Human-in-the-loop en decisiones de alto impacto (riesgo, calidad, clientes sensibles).
- Muestreo de casos para auditoria de sesgo y errores.
- Modo "recomendacion" antes de modo "automatizacion completa" para reducir riesgo operativo.


---

## 4. Caso de uso real: IA asistida en radiología para detección de cáncer de mama

Se toma como ejemplo el despliegue del sistema Mia de Kheiron Medical en el programa nacional de cribado mamográfico de Hungría (2023). La IA actúa como segundo lector: analiza las imágenes y prioriza los casos sospechosos para apoyar al radiólogo, reduciendo la carga de lectura y mejorando la consistencia diagnóstica.

### 4.1 Encaje con el tema

- Automatiza una tarea intensiva y repetitiva (análisis de imagen diagnóstica).
- Gestiona grandes volúmenes de datos clínicos e imágenes DICOM.
- Refuerza la colaboración humano-máquina: la decisión clínica final sigue siendo responsabilidad del especialista.

### 4.2 Arquitectura del caso

1. Entrada de imagen DICOM desde el sistema de información hospitalario (HIS/PACS).
2. Preprocesado y análisis por el modelo de visión artificial de la IA.
3. Priorización automática de estudios y asignación de puntuación de riesgo.
4. Revisión y validación por el radiólogo (validación humana obligatoria).
5. Registro del resultado final y retroalimentación para control de calidad continuo.

---

## 5. Resultados y métricas

Las siguientes métricas proceden del despliegue documentado en Hungría y del estudio de validación internacional:

| Indicador | Resultado | Fuente |
|-----------|-----------|--------|
| Reducción de carga de lectura | −30 % en tiempo de triaje | Lánczky et al., 2023 |
| Incremento de detección de cáncer | +13 % en sensibilidad diagnóstica | Lánczky et al., 2023 |
| Seguridad clínica | Mantenida con validación humana final | McKinney et al., 2020 |

**Fuente principal:**
- Lánczky et al., *"Evaluating the impact of AI on breast cancer screening workflow in Hungary"*, Nature Communications Medicine (2023).
  - Referencia divulgada por Kheiron Medical (Mia): https://www.kheironmed.com/news/kheirons-ai-integrated-into-hungarian-national-breast-screening-programme

**Fuente complementaria:**
- McKinney et al., *"International evaluation of an AI system for breast cancer screening"*, Nature (2020).
  - https://www.nature.com/articles/s41586-019-1799-6

---

## 6. Valor empresarial y transferibilidad

El caso de radiología demuestra beneficios que son transferibles a otros sectores con procesos de revisión masiva de datos:

- **Productividad**: reducción del tiempo por estudio y mejor priorización de la carga de trabajo.
- **Calidad**: aumento de la sensibilidad diagnóstica sin degradar la especificidad clínica.
- **Escalabilidad**: permite atender mayor volumen de casos sin incrementar proporcionalmente la plantilla especializada.
- **Transferibilidad**: el mismo patrón arquitectónico (ingesta → análisis por IA → validación humana → feedback) es aplicable en control de calidad industrial, detección de fraude financiero o clasificación de incidencias en soporte técnico.

---

## 7. Opinión del grupo

Como grupo, consideramos que la automatización con IA es una ventaja competitiva real cuando se diseña con criterio de negocio y no solo como "moda tecnológica".

**Fortalezas principales:**

- Ahorro de tiempo en tareas repetitivas y mejor uso del talento humano.
- Mejor calidad de decisión al combinar datos históricos y predicción.
- Escalabilidad: la empresa puede crecer sin incrementar costes linealmente.

**Límites y riesgos:**

- Si el dato es pobre, el modelo amplifica errores.
- Existe riesgo de sesgo y decisiones opacas si no hay explicabilidad.
- La automatización mal planteada puede generar rechazo interno.

**Impacto en empleo, ética y privacidad:**

- *Empleo*: más que sustitución total, vemos una transformación de roles hacia supervisión, análisis y mejora de procesos.
- *Ética*: se requiere trazabilidad, auditorías periódicas y protocolos de revisión humana.
- *Privacidad*: es obligatorio aplicar minimización de datos, control de acceso y cumplimiento normativo (RGPD/LOPDGDD).

**Conclusión del grupo:** la IA aporta mucho valor en la empresa cuando se implementa con gobernanza del dato, supervisión humana y objetivos medibles.

