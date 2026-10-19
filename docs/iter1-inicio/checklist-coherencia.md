# Checklist de coherencia

Comprobación de coherencia entre la Visión, el SRS breve y los modelos de CU-002.

| # | Verificación | Resultado | Observación |
|---|---|---|---|
| 1 | El actor se llama igual en Visión, SRS y diagramas | Corregido: Paciente | Se unificó el actor principal con el término oficial «Paciente». |
| 2 | Cada REQ de la Visión tiene un caso de uso asociado | Sí | REQ-001 → CU-001; REQ-002 → CU-002; REQ-003 → CU-003. |
| 3 | Cada excepción del diagrama figura como flujo alterno en el CU | Corregido: E3 documentada | CU-002 recoge E1, E2, E3 y la compensación C1. |
| 4 | Nada modelado está fuera del alcance de la Visión | Sí | El diagrama se limita al proceso de reservar cita; no incluye pagos ni historia clínica. |
| 5 | Los IDs siguen la convención (REQ-###, CU-###, RSK-###) | Sí | Los requisitos, casos de uso y riesgos utilizan los prefijos indicados. |
| 6 | Todo lo que la Visión incluye aparece en algún artefacto | Sí, para el alcance funcional | REQ-001 a REQ-003 se relacionan con CU-001 a CU-003; el diagrama detalla CU-002, el proceso crítico elegido. |

## Hallazgos y correcciones

| # | Hallazgo | Corrección | Estado |
|---|---|---|---|
| 1 | Los nombres del actor principal no eran uniformes en las versiones revisadas | Se unificó el término a «Paciente» en los artefactos | Corregido |
| 2 | La excepción E3 (fallo de confirmación) no estaba documentada como flujo alterno en el SRS breve | Se incorporó E3 con reintentos, estado Pendiente y aviso al administrador | Corregido |
| 3 | La Visión utilizaba «agenda», mientras el glosario establece «Horario» como término oficial | Se cambió a «horarios» para mantener la terminología consistente | Corregido |

