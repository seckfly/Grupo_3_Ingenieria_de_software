# SRS breve — Sistema de reservas de citas médicas

> **Estado:** Borrador de Inicio (ITER-1). Este documento organiza los requisitos de alto nivel de la [Visión](vision.md); no constituye una validación con un cliente ni evidencia de implementación.

## 1. Propósito y alcance

El sistema permitirá que los pacientes registren sus datos, reserven y cancelen citas médicas en línea y reciban por correo la confirmación de una cita registrada.

**Incluye:** registro de pacientes, reserva de citas, cancelación de citas y confirmación por correo.

**No incluye:** pagos en línea, historia clínica ni telemedicina.

## 2. Requisitos funcionales

| ID | Requisito | Caso de uso asociado |
|---|---|---|
| REQ-001 | El sistema permitirá registrar un paciente. | CU-001 Registrar paciente |
| REQ-002 | El sistema permitirá reservar una cita: comprobará la disponibilidad del horario, registrará la cita y enviará una confirmación por correo. | CU-002 Reservar cita |
| REQ-003 | El sistema permitirá cancelar una cita. | CU-003 Cancelar cita |

## 3. Restricciones y objetivos

- El sistema debe funcionar en un navegador.
- La Visión propone una primera versión en siete semanas; las fechas calendario se deben acordar en el grupo.
- Reducir a la mitad el tiempo de reserva y eliminar las citas duplicadas son objetivos del proyecto, no resultados medidos.

## 4. Lista preliminar de casos de uso

La lista corresponde al nivel **Lista** de la matriz fase–artefacto para Inicio. La especificación detallada de CU-001 y CU-003 se desarrollará en Elaboración.

| ID | Caso de uso | Actor principal | Requisito |
|---|---|---|---|
| CU-001 | Registrar paciente | Paciente | REQ-001 |
| CU-002 | Reservar cita | Paciente | REQ-002 |
| CU-003 | Cancelar cita | Paciente | REQ-003 |

## 5. Flujos preliminares de CU-002 — Reservar cita

**Flujo principal**

1. El paciente inicia sesión.
2. El sistema comprueba si está registrado.
3. El paciente elige especialidad, fecha y horario.
4. El sistema comprueba la disponibilidad y bloquea el horario libre.
5. El sistema registra la cita.
6. El sistema inicializa el contador de reintentos en cero y envía la confirmación por correo.
7. Si la confirmación se envía, finaliza el proceso con la cita registrada y confirmada.

**Excepciones y compensación**

- **E1 — Horario ocupado:** el sistema muestra horarios alternativos y el paciente elige otro.
- **E2 — Paciente no registrado:** se ejecuta CU-001 y, después del registro, el paciente vuelve al inicio de sesión para continuar.
- **E3 — Fallo de confirmación:** si el primer envío falla, el sistema puede realizar hasta tres reintentos adicionales. Si el envío sigue fallando, la cita queda registrada en estado **Pendiente** y se avisa al administrador.
- **C1 — Compensación:** si falla el registro de la cita después de bloquear el horario, el sistema libera el horario.

El diagrama de actividad asociado es [actividad-reservar-cita.drawio](../../modelos/iter1/actividad-reservar-cita.drawio) y su exportación [PNG](../../modelos/iter1/actividad-reservar-cita.png).

## 6. Punto por validar del alcance

La Visión identifica como interesado a la recepcionista y señala su necesidad de consultar horarios y citas sin duplicados, pero REQ-001 a REQ-003 no definen explícitamente esa función. No se agrega un requisito nuevo sin confirmación; el grupo debe decidir si esa necesidad forma parte del alcance funcional.
