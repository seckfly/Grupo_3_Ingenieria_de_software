# Checklist de coherencia

Comprobación de coherencia entre la Visión, el SRS breve y los modelos de CU-002.

| # | Verificación | Resultado | Observación |
|---|---|---|---|
| 1 | El actor se llama igual en Visión, SRS y diagramas | Sí | Visión, SRS y diagrama utilizan el término oficial «Paciente». |
| 2 | Cada REQ de la Visión tiene un caso de uso asociado | Sí | REQ-001 → CU-001; REQ-002 → CU-002; REQ-003 → CU-003. |
| 3 | Cada excepción del diagrama figura como flujo alterno en el CU | Sí | CU-002 recoge E1, E2, E3 y la compensación C1. |
| 4 | Nada modelado está fuera del alcance de la Visión | Sí | El diagrama se limita al proceso de reservar cita; no incluye pagos ni historia clínica. |
| 5 | Los IDs siguen la convención (REQ-###, CU-###, RSK-###) | Sí | Los requisitos, casos de uso y riesgos utilizan los prefijos indicados. |
| 6 | Todo lo que la Visión incluye aparece en algún artefacto | Sí, para el alcance funcional | REQ-001 a REQ-003 se relacionan con CU-001 a CU-003; el diagrama detalla CU-002, el proceso crítico elegido. |

## Hallazgos y correcciones

| # | Hallazgo | Corrección | Estado |
|---|---|---|---|
| 1 | La Visión utilizaba «agenda», mientras el glosario establece «Horario» como término oficial | Se cambió a «horarios» en la Visión para mantener la terminología consistente | Corregido |
| 2 | El repositorio no tenía un SRS breve que relacionara los requisitos con los casos de uso | Se creó el SRS en borrador y se vinculó REQ-001 a CU-001, REQ-002 a CU-002 y REQ-003 a CU-003 | Corregido |
| 3 | El SRS breve debía registrar los flujos alternos del proceso crítico para contrastarlos con el diagrama | Se documentaron E1, E2, E3 y C1 en el SRS breve | Corregido |
