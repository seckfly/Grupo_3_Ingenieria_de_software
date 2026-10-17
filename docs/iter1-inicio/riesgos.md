# Riesgos por fase - Sistema de reservas de citas

Probabilidad: Baja, Media, Alta. Impacto: Bajo, Medio, Alto. Los responsables se indican por **rol**; la asignación personal está **por confirmar**.

| ID | Fase | Riesgo | Prob. | Impacto | Mitigación (planificada) | Responsable (rol) |
|---|---|---|---|---|---|---|
| RSK-001 | Inicio | Alcance ambiguo, con exigencias nuevas a mitad del proyecto | Alta | Alto | Validar la Visión con el cliente y firmar la lista "No incluye" | Analista |
| RSK-002 | Elaboración | Doble reserva del mismo horario | Media | Alto | Modelar E1 y C1; bloqueo temporal del horario; probarlo con prototipo | Arquitecto |
| RSK-003 | Construcción | Retraso por dejar las pruebas para el final | Media | Medio | Escribir casos de prueba desde la iteración 2 | Desarrollador |
| RSK-004 | Transición | Los recepcionistas no adoptan el sistema | Media | Alto | Capacitación corta y manual de una página | Líder de proyecto |
| RSK-005 | Elaboración | Citas Pendientes sin seguimiento cuando falla el envío de la confirmación (E3) | Media | Medio | Modelar E3 con límite de 3 reintentos y aviso al administrador; probarlo con prototipo | Arquitecto |

## Estado

- Las mitigaciones están **planificadas**; ninguna se ha implementado ni validada.
- RSK-002 y RSK-005 ya cuentan con E1, C1 y E3 modelados en el [diagrama](../../modelos/iter1/actividad-reservar-cita.png); el bloqueo temporal y la prueba con prototipo siguen pendientes (ITER-2).
- RSK-001: la validación de la Visión con el cliente no se ha realizado.
- **Pendiente:** tarjetas por riesgo en la lista Riesgos de Trello e ítems "Mitigar RSK-00X" en las tarjetas de iteración (fuera de alcance por ahora).
