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

## 7. Opinión

Como grupo, consideramos que la automatizacion con IA es una ventaja competitiva real cuando se diseña con criterio de negocio y no solo como "moda tecnologica".

Fortalezas principales:

- Ahorro de tiempo en tareas repetitivas y mejor uso del talento humano.
- Mejor calidad de decision al combinar datos historicos y prediccion.
- Escalabilidad: la empresa puede crecer sin incrementar costes linealmente.

Limites y riesgos:

- Si el dato es pobre, el modelo amplifica errores.
- Existe riesgo de sesgo y decisiones opacas si no hay explicabilidad.
- La automatizacion mal planteada puede generar rechazo interno.

Impacto en empleo, etica y privacidad:

- Empleo: mas que sustitucion total, vemos una transformacion de roles hacia supervision, analisis y mejora de procesos.
- Etica: se requiere trazabilidad, auditorias periodicas y protocolos de revision humana.
- Privacidad: es obligatorio aplicar minimizacion de datos, control de acceso y cumplimiento normativo (RGPD/LOPDGDD).

Conclusión del grupo: la IA aporta mucho valor en empresa cuando se implementa con gobernanza del dato, supervision humana y objetivos medibles.


---

## Ejemplo real elegido

### Caso: IA asistida en radiologia para deteccion de cancer de mama

Se toma como ejemplo el uso de sistemas de IA como segundo lector en cribado mamografico. La IA analiza imagenes y prioriza casos sospechosos para apoyar al radiologo, reduciendo carga y mejorando consistencia.

### Como encaja con el tema

- Automatiza parte del proceso de analisis de imagen (tarea intensiva y repetitiva).
- Gestiona grandes volumenes de datos clinicos e imagenes.
- Refuerza la colaboracion humano-maquina: la decision final sigue siendo clinica.

### Arquitectura resumida del caso

1. Entrada de imagen DICOM desde el sistema hospitalario.
2. Preprocesado y analisis por modelo de IA.
3. Priorizacion de estudios y puntuacion de riesgo.
4. Revision por radiologo (validacion humana obligatoria).
5. Registro de resultado final y retroalimentacion para control de calidad.

### Metricas cuantitativas con fuente

- Reduccion de carga de lectura de radiologos del 30% al usar IA para triaje en cribado real.
- Incremento de deteccion de cancer del 13% en el despliegue reportado.
- Mantenimiento de seguridad clinica con validacion de especialista en el flujo final.

Fuente principal:

- Lánczky et al., "Evaluating the impact of AI on breast cancer screening workflow in Hungary", Nature Communications Medicine (2023).
	- Referencia divulgada por Kheiron Medical (Mia): https://www.kheironmed.com/news/kheirons-ai-integrated-into-hungarian-national-breast-screening-programme

Fuente complementaria (evidencia de rendimiento en lectura de mamografias):

- McKinney et al., "International evaluation of an AI system for breast cancer screening", Nature (2020).
	- https://www.nature.com/articles/s41586-019-1799-6

### Valor empresarial

- Mejora productividad del servicio (menos tiempo por estudio y mejor priorizacion).
- Mejora calidad asistencial al aumentar sensibilidad en deteccion.
- Reduce cuellos de botella en contextos con escasez de especialistas.

