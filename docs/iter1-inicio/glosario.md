# Glosario

| Término oficial | Significa | No usar |
|---|---|---|
| Paciente | Persona que solicita atención médica | Usuario, Cliente |
| Cita | Reserva de un horario con un médico | Turno, Reserva (como nombre de la cita) |
| Horario | Franja de tiempo disponible de un médico | Slot, Agenda |

| Administrador | Interesado que controla horarios y recibe el aviso cuando falla la confirmación | No confundir con Paciente |
| Recepcionista | Interesado que necesita consultar horarios sin duplicados | No confundir con el actor Paciente de CU-002 |
| Confirmación | Correo que informa al paciente de la cita registrada | No confundir envío del correo con registro de la cita |
| Pendiente | Estado de una cita registrada cuya confirmación por correo no se pudo enviar tras los reintentos | No interpretar como cita no registrada |
| Reintento | Nuevo envío después de un envío fallido; se permiten hasta tres | No contar el envío inicial como reintento |
