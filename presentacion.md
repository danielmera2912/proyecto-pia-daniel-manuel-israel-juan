# Guión de diapositivas — PowerPoint

---

## Diapositiva 1

Modelos de automatización con IA en la empresa

Gestión de recursos, datos y colaboración humano-máquina

Daniel Mera Sachse · Manuel Garrido Serrano · Israel Soto Cala · Juan Manuel Vega Carrillo

Programación de Inteligencia Artificial · Abril 2026

(imagen de fondo: red neuronal o nube, opacidad baja)

---

## Diapositiva 2

¿Qué problema resuelve la IA en la empresa?

- Procesos manuales y repetitivos que consumen tiempo y dinero
- Silos de información y baja calidad del dato
- Resistencia al cambio y escasez de perfiles analíticos
- Escalar con infraestructura propia es costoso y lento

La IA no es solo tecnología: también implica un cambio organizativo y cultural

---

## Diapositiva 3

Conceptos clave

(4 cuadros o tarjetas)

| Concepto | Descripción |
|----------|-------------|
| Dato como activo estratégico | La calidad del dato determina la calidad de las decisiones |
| Inteligencia colaborativa | La IA apoya; el humano decide en los puntos críticos |
| Aprendizaje continuo | Modelos y equipos mejoran con cada ciclo de retroalimentación |
| Mejora continua basada en métricas | Todo se mide y se ajusta con KPIs objetivos |

---

## Diapositiva 4

Tecnologías de soporte

| Tecnología | Para qué sirve |
|------------|----------------|
| Google Cloud Platform | Ecosistema de servicios gestionados en la nube |
| Google App Engine | Despliegue escalable: entorno estándar (APIs sin estado) y flexible (Docker) |
| BigQuery | Análisis de grandes volúmenes de datos en tiempo real |
| Docker | Contenedores personalizados con sus propias dependencias |
| Datastore / Memcache | Persistencia de datos y caché de alto rendimiento |

Modelo cloud: de Capex (infraestructura propia) a Opex (pago por uso)

---

## Diapositiva 5

Arquitectura propuesta

(6 capas apiladas con flechas entre ellas)

1. **Ingesta** — ERP, CRM, sensores, formularios
2. **Almacenamiento** — Data lake + BigQuery, control de acceso y trazabilidad
3. **Procesamiento** — ETL/ELT, limpieza y enriquecimiento de datos
4. **IA y decisión** — Clasificación, predicción de demanda, detección de anomalías
5. **Consumo** — APIs, paneles y alertas para operaciones, finanzas y dirección
6. **Observabilidad** — KPIs, detección de drift, reentrenamiento periódico

Flujo: Entrada → Preparación → Inferencia → Orquestación → Salida → Feedback

⚠ Validación humana obligatoria en decisiones de alto impacto

---

## Diapositiva 6

Caso real: radiología asistida con IA

IA como segundo lector en cribado mamográfico — Hungría, 2023

- La IA analiza mamografías y prioriza los casos con mayor riesgo
- El radiólogo revisa los estudios priorizados; la decisión clínica final siempre es humana
- Se integra en el flujo hospitalario existente sin sustituir al especialista

Flujo del caso:

1. Entrada de imagen DICOM desde el sistema hospitalario
2. Preprocesado y análisis por el modelo de visión artificial
3. Priorización automática y puntuación de riesgo
4. Revisión y validación por el radiólogo
5. Registro del resultado y retroalimentación al sistema

(imagen ilustrativa: mamografía o flujo hospitalario esquemático)

---

## Diapositiva 7

Resultados y beneficios

(3 cifras grandes destacadas)

**−30 %** de carga de lectura para radiólogos

**+13 %** de incremento en detección de cáncer

**✔** Seguridad clínica mantenida con validación humana final

Beneficios empresariales:

- Mayor productividad del servicio
- Mejor calidad en la detección diagnóstica
- Reduce el cuello de botella ante escasez de especialistas

Fuentes: Lánczky et al. (2023), Nature Commun. Medicine · McKinney et al. (2020), Nature

---

## Diapositiva 8

Nuestra opinión como grupo

Fortalezas:

- Ahorra tiempo en tareas repetitivas y libera talento humano para tareas de mayor valor
- Mejora la calidad de las decisiones al combinar datos históricos con predicción
- Permite escalar sin incrementar costes linealmente

Límites y riesgos:

- Si el dato es pobre, el modelo amplifica los errores
- Riesgo de sesgo y falta de explicabilidad si no se audita
- Una automatización mal planteada puede generar rechazo interno

Impacto ético y social:

- Empleo: transformación de roles, no sustitución total
- Privacidad: minimización de datos y cumplimiento del RGPD/LOPDGDD obligatorio
- Ética: trazabilidad y revisión humana periódica son innegociables

---

## Diapositiva 9

Conclusiones

- La IA aporta valor real cuando se integra con datos de calidad y objetivos medibles
- No sustituye a las personas: potencia la toma de decisiones humana
- Gobernanza del dato, ética y privacidad son condiciones obligatorias, no opcionales
- Recomendación: piloto controlado → medir con KPIs → escalar progresivamente

(cuadro destacado, texto grande):
"Automatizar con IA no es solo tecnología. Es estrategia de negocio + personas + datos."

Gracias por vuestra atención · ¿Preguntas?
