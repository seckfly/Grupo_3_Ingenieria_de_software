# Riesgos por fase - Sistema de reservas de citas

Probabilidad: Baja, Media, Alta. Impacto: Bajo, Medio, Alto. Las mitigaciones siguen siendo planes hasta que se ejecuten y comprueben.

| ID | Fase | Riesgo | Prob. | Impacto | Mitigación (planificada) | Responsable |
|---|---|---|---|---|---|---|
| RSK-001 | Inicio | Alcance ambiguo, con exigencias nuevas a mitad del proyecto | Alta | Alto | Validar la Visión con quien aprueba el alcance y confirmar la lista «No incluye» | **Isaí Samuel Bejarano Benites — Analista** |
| RSK-002 | Elaboración | Doble reserva del mismo horario | Media | Alto | Modelar E1 y C1, definir bloqueo temporal del horario y probarlo con un prototipo | **Alejandro Horna Quezada — Arquitecto** |
| RSK-003 | Construcción | Retraso por dejar las pruebas para el final | Media | Medio | Preparar el checklist de pruebas desde Elaboración y ejecutarlo durante Construcción | **Cesar Jeremin Alonso Chuquimango Reyes — apoyo de pruebas** |
| RSK-004 | Transición | Los recepcionistas no adoptan el sistema | Media | Alto | Preparar un manual breve y una capacitación de uso | **Alonso Castillo Davalos — apoyo documental** |
| RSK-005 | Elaboración | Citas en estado Pendiente sin seguimiento cuando falla el envío de la confirmación (E3) | Media | Medio | Modelar E3 con hasta tres reintentos y aviso al administrador; probarlo con un prototipo | **Alejandro Horna Quezada — Arquitecto** |

## Estado

- Las mitigaciones están **planificadas**; no se presentan como implementadas ni validadas.
- E1, E2, E3 y C1 aparecen en el diagrama de actividad de CU-002. El bloqueo temporal y las pruebas con prototipo quedan para Elaboración.
- RSK-001 requiere validar el alcance con quien lo apruebe.
- **Pendiente de Trello:** crear una tarjeta por riesgo en la lista Riesgos, con la mitigación en checklist y la persona responsable; añadir «Mitigar RSK-00X» a la tarjeta de la iteración correspondiente.
