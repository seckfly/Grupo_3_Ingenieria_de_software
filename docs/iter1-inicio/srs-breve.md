# SRS breve — Sistema de reservas de citas

> Estado: Borrador. La matriz fase–artefacto sitúa el SRS en Borrador durante Inicio y Base durante Elaboración.

## Requisitos y casos de uso

| ID | Requisito de alto nivel | Caso de uso |
|---|---|---|
| REQ-001 | Registrar paciente | CU-001 Registrar paciente |
| REQ-002 | Reservar cita | CU-002 Reservar cita |
| REQ-003 | Cancelar cita | CU-003 Cancelar cita |

## CU-002 — Reservar cita

**Flujo principal:** el paciente inicia sesión, elige especialidad, fecha y horario; el sistema comprueba la disponibilidad, bloquea el horario, registra la cita y envía la confirmación.

| Tipo | Descripción |
|---|---|
| Excepción E1 | Horario ocupado: el sistema muestra horarios alternativos y el paciente elige otro. |
| Excepción E2 | Paciente no registrado: se ejecuta CU-001 (Registrar paciente) y luego se vuelve al inicio de sesión para continuar con la reserva. |
| Excepción E3 | Falla el envío de la confirmación: el sistema reintenta hasta 3 veces; si sigue fallando, deja la cita en estado Pendiente y avisa al administrador. |
| Compensación C1 | Si falla el registro de la cita después de bloquear el horario, el sistema libera el horario. |

El diagrama de actividad correspondiente es [actividad-reservar-cita.drawio](../../modelos/iter1/actividad-reservar-cita.drawio) y su exportación es [actividad-reservar-cita.png](../../modelos/iter1/actividad-reservar-cita.png).
