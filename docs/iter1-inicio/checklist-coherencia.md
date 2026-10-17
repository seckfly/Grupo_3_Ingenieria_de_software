# Checklist de coherencia - ITER-1

Revisión hecha por la persona que prepara el repositorio, sobre los documentos que existen hoy: [Visión](vision.md), [matriz](matriz-fase-artefacto.md), [roadmap](roadmap.md), [glosario](glosario.md), [riesgos](riesgos.md) y el [diagrama de CU-002](../../modelos/iter1/actividad-reservar-cita.png). **No existen** SRS ni documento de casos de uso; las comprobaciones que dependen de ellos o de Trello quedan pendientes. Esto no sustituye la revisión por pares ([revision-pares.md](revision-pares.md)).

Leyenda: ✅ cumple · ❌ → ✅ inconsistencia detectada y corregida · ⏳ pendiente

| # | Verificación | Resultado | Observación |
|---|---|---|---|
| 1 | El actor se llama igual en Visión, SRS y diagramas | ✅ (Visión y diagrama) · ⏳ SRS | Visión y diagrama usan Paciente, Administrador y (solo la Visión) Recepcionista; no aparecen Usuario ni Cliente. El SRS no existe. |
| 2 | Cada REQ de la Visión tiene un caso de uso | ⏳ | No existe documento de casos de uso. Solo el diagrama cita CU-001 (REQ-001) y CU-002 (REQ-002); CU-003 (REQ-003) no figura en ningún artefacto. |
| 3 | Cada excepción del diagrama figura como flujo alterno en el CU | ⏳ | E1, E2, E3 y C1 están en el diagrama y en la descripción de la guía, pero no hay CU-002 escrito donde verificarlo. |
| 4 | Nada modelado está fuera del alcance de la Visión | ✅ | El diagrama no contiene pagos, historia clínica ni telemedicina. |
| 5 | Los IDs siguen la convención (REQ-###, CU-###, RSK-###) | ✅ | REQ-001..003, CU-001/002, RSK-001..005 e ITER-1..4 siguen la convención. Los commits anteriores ("Add files via upload") no la siguen; el historial no se reescribió. |
| 6 | Todo lo que la Visión incluye aparece en algún artefacto | ⏳ parcial | Reserva de citas y confirmación: en el diagrama. Registro de pacientes: solo referido como CU-001 (E2). Cancelación de citas (REQ-003): solo en la Visión, sin modelo ni CU. |
| 7 | La matriz es coherente con el roadmap | ✅ | Cuatro fases e iteraciones ITER-1..4; entregables del roadmap alineados con la matriz. |
| 8 | Roadmap y tablero de Trello corresponden | ⏳ | Fuera de alcance por ahora; no se ha accedido a Trello. |

## Hallazgos detectados

| # | Hallazgo | Corrección | Estado |
|---|---|---|---|
| H1 | `vision.md` tenía caracteres de escape (`\#`, `\-`) y líneas en blanco entre cada línea: títulos, listas y tabla de interesados no se renderizaban | Se reescribió el Markdown conservando el contenido y los IDs | Corregido |
| H2 | La Visión decía "errores de agenda" y "Ver la agenda", pero el glosario prohíbe "Agenda" para Horario | Se cambió a "errores de horarios" y "Ver los horarios y las citas sin duplicados" | Corregido |
| H3 | La confirmación por correo no estaba vinculada de forma explícita a la reserva | Alcance: "confirmación por correo de cada cita reservada"; REQ-002 la incluye | Corregido |
| H4 | El diagrama usaba "reserva" como nombre de cita ("Fin: reserva no completada") | Ahora "Fin: cita no registrada"; "Regresa a la reserva" pasó a "Regresa al inicio de sesión" | Corregido |
| H5 | El diagrama reintentaba con "intento + 1" pero el contador nunca se inicializaba, y "Intentos < 3" con "No (3 fallos)" era ambiguo | Se agregó "Inicializar contador reintentos = 0"; la decisión es "¿Reintentos < 3?" (hasta 3 reintentos tras el primer envío fallido) | Corregido |
| H6 | Un solo final "Fin: cita registrada" mezclaba la confirmación enviada con el estado Pendiente | Dos finales: "cita registrada y confirmación enviada" y "cita registrada, confirmación pendiente" (Pendiente = confirmación no enviada; la cita sí está registrada) | Corregido |
| H7 | Los archivos estaban en la raíz con nombres que no seguían la convención | Movidos y renombrados a la estructura de la guía | Corregido |
| H8 | El estado «Lista» (Casos de uso, Inicio) no está en la leyenda de estados de la matriz | Se conserva como en la guía y se anotó en la matriz | Observado, sin cambio |
| H9 | La Visión no documenta línea base para "reducir a la mitad el tiempo de reserva" | Se anotó "(línea base por medir)"; sin inventar cifras | Anotado |
| H10 | El diagrama dice "Enviar confirmación" sin precisar el canal (la Visión dice correo) | Sin cambio; el glosario define Confirmación como mensaje por correo | Observado |
| H11 | El repositorio no se llama `Tema6_ApellidoNombre` como pide la guía | Sin cambio (requiere decisión del usuario) | Pendiente |
