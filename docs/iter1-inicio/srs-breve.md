# SRS breve — Sistema de reservas de citas

Versión 1 — ITER-1, fase de Inicio.

## Requisitos y casos de uso

| ID | Requisito de alto nivel | Caso de uso |
|---|---|---|
| REQ-001 | Registrar paciente | CU-001 Registrar paciente |
| REQ-002 | Reservar cita, comprobar disponibilidad y enviar confirmación por correo | CU-002 Reservar cita |
| REQ-003 | Cancelar cita | CU-003 Cancelar cita |

El alcance funcional comprende estas tres operaciones. Los interesados Recepcionista y Administrador expresan necesidades del negocio en la Visión; su identificación no añade casos de uso independientes en ITER-1.

## Lista de casos de uso

| Caso de uso | Actor | Resultado |
|---|---|---|
| CU-001 Registrar paciente | Paciente | Paciente registrado para continuar con la reserva |
| CU-002 Reservar cita | Paciente; Administrador recibe el aviso de E3 | Cita registrada; confirmación enviada o aviso de confirmación no enviada |
| CU-003 Cancelar cita | Paciente | Cita cancelada |

## CU-002 — Reservar cita

**Flujo principal:** el paciente inicia sesión, elige especialidad, fecha y horario; el sistema verifica disponibilidad, bloquea el horario, registra la cita y envía la confirmación por correo al paciente.

| Tipo | Descripción |
|---|---|
| Excepción E1 | Horario ocupado: el sistema muestra horarios alternativos y el paciente elige otro. |
| Excepción E2 | Paciente no registrado: se ejecuta CU-001 Registrar paciente y se regresa al inicio de sesión para continuar la reserva. |
| Excepción E3 | Si falla el envío de la confirmación por correo, el sistema reintenta hasta tres veces; si sigue fallando, deja la cita en estado Pendiente y avisa al administrador. |
| Compensación C1 | Si falla el registro después de bloquear el horario, el sistema libera el horario para evitar que quede bloqueado sin propietario. |

**Control de E3:** el contador de reintentos se inicializa en cero antes del primer envío. Tras un fallo se comprueba si es menor que tres. Cada reintento incrementa el contador en uno y vuelve a ejecutar el envío. Se permiten un envío inicial y hasta tres reintentos. Tras el fallo del tercer reintento se registra el estado Pendiente y se avisa al administrador.

**Resultados del proceso:**

- Registro correcto y correo enviado: cita registrada y confirmación enviada.
- Registro correcto y correo no enviado tras los reintentos: cita registrada con confirmación pendiente; administrador avisado.
- Fallo del registro: cita no registrada y horario liberado mediante C1.

«Pendiente» designa una cita ya registrada cuya confirmación por correo no se pudo enviar. No representa una reserva inexistente.

## Restricciones

Funcionamiento en navegador y primera versión en siete semanas. Se excluyen pagos en línea, historia clínica y telemedicina.

## Modelo del proceso crítico

[Fuente editable draw.io](../../modelos/iter1/actividad-reservar-cita.drawio) · [Diagrama PNG](../../modelos/iter1/actividad-reservar-cita.png).
