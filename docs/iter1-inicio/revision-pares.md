# Revisión por pares — ITER-1

Pull Request revisado: [ITER1 — fase de Inicio](https://github.com/seckfly/Grupo_3_Ingenieria_de_software/pull/1).

**Revisor:** Marco Antonio Martell Alvarez.

## Checklist de revisión

| # | Pregunta | Resultado | Observación |
|---|---|---|---|
| 1 | ¿La Visión define claramente qué incluye y qué NO incluye? | Conforme | El alcance y las exclusiones están identificados en la sección 3 de la Visión. |
| 2 | ¿El roadmap tiene entregables y responsable en cada iteración? | Conforme | Las cuatro iteraciones incluyen objetivo, entregables, responsable y plazo. |
| 3 | ¿La matriz fase–artefacto es coherente con el roadmap? | Conforme | Los artefactos y su evolución se organizan según las cuatro fases RUP. |
| 4 | ¿El diagrama muestra el flujo principal y al menos dos excepciones? | Conforme | El modelo incluye el flujo principal, E1, E2, E3 y la compensación C1. |
| 5 | ¿Los nombres de actores y conceptos coinciden en todos los documentos? | Conforme | La terminología se contrasta con el glosario y los artefactos de Inicio. |
| 6 | ¿Cada riesgo tiene mitigación y responsable? | Conforme | RSK-001 a RSK-004 incluyen probabilidad, impacto, mitigación y responsable. |
| 7 | ¿Los IDs y los commits siguen las convenciones? | Conforme | Los artefactos utilizan REQ-###, CU-### y RSK-###; los nuevos commits usan el prefijo de iteración. |

## Hallazgos de revisión

| # | Hallazgo | Corrección aplicada |
|---|---|---|
| 1 | La Visión utilizaba «agenda», mientras el glosario establece «Horario» como término oficial | Se cambió a «horarios» en la Visión. |
| 2 | La confirmación por correo no estaba vinculada explícitamente a REQ-002 | Se vinculó la confirmación por correo con REQ-002 y CU-002. |
| 3 | El control de reintentos y el significado de Pendiente requerían detalle textual | Se precisaron en el SRS y en el glosario, en correspondencia con el modelo. |

