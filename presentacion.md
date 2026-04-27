# 🎤 Presentación: Modelos de automatización con IA en la empresa

## Grupo: Daniel Mera Sachse · Manuel Garrido Serrano - Israel Soto Cala - Juan Manuel Vega Carrillo

---

## Diapositiva 1. Introducción

- La IA está transformando cómo las empresas gestionan recursos y procesos.
- Automatizar no es solo tecnología: también implica cambios organizativos y culturales.
- Objetivo: mostrar cómo combinar nube, datos e inteligencia colaborativa.

---

## Diapositiva 2. Problema que abordamos

- Procesos repetitivos consumen tiempo y reducen productividad.
- Existen silos de información y baja calidad del dato.
- Escalar con infraestructura tradicional suele ser costoso y lento.

---

## Diapositiva 3. Conceptos clave

- Dato como activo estratégico.
- Inteligencia colaborativa humano-máquina.
- Aprendizaje continuo de equipos y modelos.
- Enfoque de mejora continua basado en métricas.

---

## Diapositiva 4. Tecnologías de soporte

- Google Cloud Platform para servicios gestionados.
- Google App Engine para despliegue y escalabilidad.
- BigQuery para analítica avanzada.
- Docker en escenarios de ejecución flexible.
- Datastore y Memcache para persistencia y rendimiento.

---

## Diapositiva 5. Arquitectura propuesta

- Ingesta de datos:
	- ERP/CRM, tickets, sensores, formularios.
- Almacenamiento y gobierno:
	- Data lake + BigQuery, control de acceso y trazabilidad.
- Procesamiento:
	- ETL/ELT, limpieza y enriquecimiento de datos.
- IA y decisión:
	- Modelos de clasificación, predicción y detección de anomalías.
- Consumo:
	- APIs, paneles y alertas para áreas de negocio.
- Observabilidad:
	- KPIs, detección de drift y reentrenamiento.

Flujo resumido: Entrada -> Preparación -> Inferencia -> Orquestación -> Salida -> Feedback.

Validación humana: revisión obligatoria en decisiones de alto impacto.

---

## Diapositiva 6. Ejemplo real: radiología asistida con IA

- Caso: IA como segundo lector en cribado mamográfico.
- Objetivo: priorizar casos sospechosos y apoyar al radiólogo.
- Encaje con el tema:
	- Automatiza tareas repetitivas de análisis.
	- Gestiona gran volumen de imágenes clínicas.
	- Mantiene colaboración humano-máquina (decisión clínica final).

Flujo del caso:

1. Entrada DICOM desde sistema hospitalario.
2. Preprocesado y análisis por IA.
3. Priorización por riesgo.
4. Revisión del radiólogo.
5. Registro de resultado y mejora continua.

---

## Diapositiva 7. Resultados y beneficios

Métricas del caso real:

- 30% de reducción de carga de lectura para radiólogos (triaje con IA).
- 13% de incremento en detección de cáncer en despliegue reportado.
- Seguridad clínica mantenida con validación humana final.

Beneficios empresariales:

- Mayor productividad del servicio.
- Mejor calidad en la detección.
- Menor cuello de botella cuando faltan especialistas.

Fuentes:

- Lánczky et al. (2023), Nature Communications Medicine.
- McKinney et al. (2020), Nature.

---

## Diapositiva 8. Conclusiones y cierre

- La IA aporta valor cuando se integra con datos de calidad y objetivos medibles.
- No sustituye completamente a las personas: potencia la toma de decisiones.
- La gobernanza del dato, la ética y la privacidad son condiciones obligatorias.
- Recomendación del grupo:
	- Empezar con pilotos controlados,
	- medir impacto con KPIs,
	- escalar progresivamente con validación humana.

Mensaje final: automatizar con IA no es solo tecnología, es estrategia de negocio + personas + datos.
