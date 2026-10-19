# Checklist de coherencia - ITER-1

Revisión documental realizada por quien prepara el repositorio sobre la [Visión](vision.md), el [SRS breve](srs-breve.md), la [matriz](matriz-fase-artefacto.md), el [roadmap](roadmap.md), el [glosario](glosario.md), los [riesgos](riesgos.md) y el [diagrama de CU-002](../../modelos/iter1/actividad-reservar-cita.png). **Esto no sustituye la revisión por pares** ([revision-pares.md](revision-pares.md)) ni valida el proyecto con un cliente.

Leyenda: ✅ cumple · ⚠️ parcial o requiere validación · ⏳ pendiente.

| # | Verificación | Resultado | Observación |
|---|---|---|---|
| 1 | Los actores y conceptos se nombran coherentemente en Visión, SRS y diagrama | ⚠️ Parcial | Paciente y Administrador se usan de forma coherente. Recepcionista aparece como interesado en la Visión, pero su necesidad de consultar horarios y citas no está vinculada a un requisito funcional; validar si forma parte del alcance. |
| 2 | Cada REQ de la Visión tiene un caso de uso asociado | ✅ | REQ-001 → CU-001, REQ-002 → CU-002 y REQ-003 → CU-003 en el SRS breve. CU-001 y CU-003 permanecen como lista preliminar hasta ITER-2. |
| 3 | Cada excepción del diagrama figura como flujo alterno en CU-002 | ✅ | El SRS breve resume E1 (horario ocupado), E2 (paciente no registrado), E3 (fallo de confirmación) y C1 (liberación del horario). |
| 4 | Nada modelado está fuera del alcance de la Visión | ✅ | El diagrama no incluye pagos, historia clínica ni telemedicina. |
| 5 | Los IDs siguen las convenciones (REQ-###, CU-###, RSK-###, ITER-#) | ✅ | REQ-001..003, CU-001..003, RSK-001..005 e ITER-1..4 respetan el formato. Los commits históricos no se reescribieron; los nuevos commits deben seguir la convención. |
| 6 | Todo lo que la Visión incluye aparece en algún artefacto | ⚠️ Parcial | Registro, reserva, confirmación y cancelación aparecen en el SRS y la lista de casos de uso; el detalle de CU-001 y CU-003 se prevé para ITER-2. La necesidad de la recepcionista requiere validación de alcance. |
| 7 | La matriz fase–artefacto es coherente con el roadmap | ✅ | Las cuatro fases y los niveles previstos de SRS/casos de uso coinciden con el roadmap actualizado. |
| 8 | Roadmap y tablero de Trello corresponden | ⏳ Pendiente | El tablero correcto no está confirmado. No se ha realizado ni documentado la sincronización con Trello. |

## Hallazgos detectados

| # | Hallazgo | Corrección o acción | Estado |
|---|---|---|---|
| H1 | `vision.md` tenía caracteres de escape y saltos que afectaban títulos, listas y tabla | Se corrigió el Markdown conservando el contenido y los IDs | Corregido |
| H2 | La Visión usaba «agenda» pese al glosario | Se cambió a «horarios» y «citas» | Corregido |
| H3 | La confirmación por correo no estaba vinculada explícitamente a la reserva | Se vinculó a la cita reservada en el alcance y REQ-002 | Corregido |
| H4 | El diagrama usaba «reserva» como nombre de la cita | Se unificó el término a «cita» | Corregido |
| H5 | El contador de reintentos no estaba inicializado y el límite era ambiguo | Se inicializa en cero y se documentan hasta tres reintentos posteriores al primer envío fallido | Corregido |
| H6 | Un solo final mezclaba confirmación enviada y pendiente | Se separaron los finales de cita registrada y confirmación enviada/pendiente | Corregido |
| H7 | Los archivos no seguían la estructura y los nombres de la guía | Se movieron y renombraron a `docs/iter1-inicio` y `modelos/iter1` | Corregido |
| H8 | «Lista» aparece en la matriz de la guía, pero no estaba definida entre los estados | Se definió como inventario preliminar de casos de uso | Corregido |
| H9 | La meta de reducir a la mitad el tiempo de reserva no tenía línea base | Se identificó la línea base como pendiente de medir | Anotado |
| H10 | El diagrama dice «Enviar confirmación al paciente» sin repetir «por correo» en esa etiqueta | El glosario define Confirmación como correo; puede hacerse explícito al exportar una nueva versión del diagrama | Observado |
| H11 | El nombre del repositorio no sigue literalmente el ejemplo `Tema6_ApellidoNombre` | Se conserva el repositorio grupal actual para no romper su enlace sin autorización | Pendiente de decisión |
| H12 | Faltaba el SRS breve y no existía una lista que vinculara REQ-001..003 con CU-001..003 | Se creó este SRS en Borrador con trazabilidad preliminar y los flujos E1, E2, E3 y C1 de CU-002 | Corregido; CU-001 y CU-003 se detallarán en ITER-2 |
| H13 | La necesidad de la recepcionista no se vincula a un requisito de alto nivel | No se inventó un REQ nuevo; se dejó indicada la necesidad de validar el alcance | Pendiente de validación |
