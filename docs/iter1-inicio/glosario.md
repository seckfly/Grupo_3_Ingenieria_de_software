# Glosario - Sistema de reservas de citas

Cada concepto tiene **un solo nombre** en todos los documentos y en el diagrama.

| Término oficial | Significa | No usar |
|---|---|---|
| Paciente | Persona que solicita atención médica y usa el sistema para reservar citas | Usuario, Cliente |
| Cita | Reserva de un horario con un médico | Turno, Reserva (como nombre de la cita) |
| Horario | Franja de tiempo disponible de un médico | Slot, Agenda |
| Administrador | Rol que controla los horarios de los médicos y recibe el aviso de una cita Pendiente | Admin, Gestor |
| Recepcionista | Rol que consulta los horarios y las citas sin duplicados | Operador |
| Médico | Profesional de salud cuyos horarios se reservan | Doctor |
| Confirmación | Mensaje por correo que el sistema envía al paciente cuando su cita queda registrada | Notificación (para este fin) |
| Pendiente | Estado de una cita ya registrada cuya confirmación no pudo enviarse tras 3 reintentos | Fallida, En espera |
| Reintentos | Contador de reenvíos de la confirmación; se inicia en 0 y el límite es 3 | Intentos |
| Excepción (E1, E2, E3) | Camino alterno cuando algo sale distinto del flujo principal | Error |
| Compensación (C1) | Acción que deshace algo cuando el proceso falla a la mitad (liberar el horario bloqueado) | Rollback |

## Notas de uso

- «Reservar cita» (CU-002, REQ-002) y «reserva de citas» nombran la acción o función; no se usa «reserva» como sinónimo de Cita.
- «Sistema de reservas de citas» es el nombre del proyecto.
- IDs: ver [convenciones](../00-convenciones.md).
