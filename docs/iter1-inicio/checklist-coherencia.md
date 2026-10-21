# Checklist de coherencia

Comprobación de coherencia entre la Visión, el SRS breve y los modelos de CU-002.

| # | Verificación | Resultado | Observación |
|---|---|---|---|
| 1 | El actor se llama igual en Visión, SRS y diagramas | Sí | Visión, SRS y diagrama utilizan el término oficial «Paciente». |
| 2 | Cada REQ de la Visión tiene un caso de uso asociado | Sí | REQ-001 → CU-001; REQ-002 → CU-002; REQ-003 → CU-003. |
| 3 | Cada excepción del diagrama figura como flujo alterno en el CU | Sí | CU-002 recoge E1, E2, E3 y la compensación C1. |
| 4 | Nada modelado está fuera del alcance de la Visión | Sí | El diagrama se limita al proceso de reservar cita; no incluye pagos ni historia clínica. |
| 5 | Los IDs siguen la convención (REQ-###, CU-###, RSK-###) | Sí | Los requisitos, casos de uso y riesgos utilizan los prefijos indicados. |
| 6 | Todo lo que la Visión incluye aparece en algún artefacto | Sí | Registro y cancelación figuran en REQ/CU-001 y REQ/CU-003; reserva y confirmación por correo figuran en REQ/CU-002 y su diagrama. |

## Hallazgos y correcciones

| # | Hallazgo | Corrección | Estado |
|---|---|---|---|
| 1 | La Visión utilizaba «agenda», mientras el glosario establece «Horario» como término oficial | Se cambió a «horarios» en la Visión para mantener la terminología consistente | Corregido |
| 2 | El repositorio no tenía un SRS breve que relacionara los requisitos con los casos de uso | Se creó el SRS breve y se vinculó REQ-001 a CU-001, REQ-002 a CU-002 y REQ-003 a CU-003 | Corregido |
| 3 | El SRS breve debía registrar los flujos alternos del proceso crítico para contrastarlos con el diagrama | Se documentaron E1, E2, E3 y C1 en el SRS breve | Corregido |
| 4 | El significado de Pendiente y el número de reintentos debían estar expresos en la documentación | Se añadieron las definiciones al glosario y el control del contador al SRS, en correspondencia con el diagrama | Corregido |
| 5 | El roadmap debía relacionar las mitigaciones con cada iteración | Se consolidó el plan de siete semanas y se vincularon RSK-001 a RSK-004 con ITER-1 a ITER-4 | Corregido |
prueba
