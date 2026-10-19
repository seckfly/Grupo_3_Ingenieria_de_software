# Checklist de coherencia - ITER-1

Revisión documental de la [Visión](vision.md), el [SRS breve](srs-breve.md), la [matriz](matriz-fase-artefacto.md), el [roadmap](roadmap.md), el [glosario](glosario.md), los [riesgos](riesgos.md) y el [diagrama de CU-002](../../modelos/iter1/actividad-reservar-cita.png). Esta es una autorrevisión; **no sustituye la revisión por pares** ([revision-pares.md](revision-pares.md)) ni valida el proyecto con un cliente.

Leyenda: ✅ cumple · ⚠️ parcial o requiere validación.

| # | Verificación de la guía | Resultado | Observación |
|---|---|---|---|
| 1 | El actor principal se llama igual en Visión, SRS y diagramas | ✅ | El actor principal de CU-002 se denomina «Paciente» en los artefactos. |
| 2 | Cada REQ de la Visión tiene un caso de uso asociado | ✅ | REQ-001 → CU-001, REQ-002 → CU-002 y REQ-003 → CU-003 en el SRS breve. CU-001 y CU-003 siguen como lista preliminar; se detallarán en Elaboración. |
| 3 | Cada excepción del diagrama figura como flujo alterno en el CU | ✅ | El SRS breve resume E1 (horario ocupado), E2 (paciente no registrado), E3 (fallo de confirmación) y C1 (liberación del horario). |
| 4 | Nada modelado está fuera del alcance de la Visión | ⚠️ | La necesidad de la recepcionista de consultar horarios/citas aparece en la Visión, pero no está especificada como requisito funcional. El grupo debe validar si forma parte del alcance. |
| 5 | Los IDs siguen la convención (REQ-###, CU-###, RSK-###) | ✅ | REQ-001..003, CU-001..003 y RSK-001..005 usan el formato indicado. Los commits históricos no se reescribieron; los nuevos commits deben seguir la convención. |
| 6 | Todo lo que la Visión incluye aparece en algún artefacto | ⚠️ | Registro, reserva, confirmación y cancelación están vinculados a REQ/CU. La necesidad de la recepcionista requiere decisión de alcance antes de afirmar cobertura completa. |

## Hallazgos detectados

| # | Hallazgo | Corrección o acción | Estado |
|---|---|---|---|
| H1 | `vision.md` tenía caracteres de escape y saltos que afectaban títulos, listas y tabla | Se corrigió el Markdown conservando el contenido y los IDs | Corregido |
| H2 | La Visión usaba «agenda» pese al glosario | Se cambió a «horarios» y «citas» | Corregido |
| H3 | La confirmación por correo no estaba vinculada explícitamente a la reserva | Se vinculó a la cita reservada en el alcance y REQ-002 | Corregido |
| H4 | El diagrama usaba «reserva» como nombre de la cita | Se unificó el término a «cita» | Corregido |
| H5 | El contador de reintentos no estaba inicializado y el límite era ambiguo | El diagrama inicia el contador en cero y permite hasta tres reintentos después del primer envío fallido, siguiendo la secuencia descrita en la guía | Corregido |
| H6 | Un solo final mezclaba confirmación enviada y pendiente | Se separaron los finales de cita registrada y confirmación enviada/pendiente | Corregido |
| H7 | Los archivos no seguían la estructura y los nombres de la guía | Se movieron y renombraron a `docs/iter1-inicio` y `modelos/iter1` | Corregido |
| H8 | «Lista» aparece en la matriz de la guía, pero no estaba definida entre los estados | Se definió como inventario preliminar de casos de uso | Corregido |
| H9 | La meta de reducir a la mitad el tiempo de reserva no tenía línea base | Se identificó la línea base como pendiente de medir | Anotado |
| H10 | El diagrama dice «Enviar confirmación al paciente» y no especifica «por correo» en esa etiqueta | El SRS y el glosario sí lo especifican; se recomienda explicitarlo en el diagrama cuando se regenere su PNG desde el archivo fuente | Pendiente menor |
| H11 | El nombre del repositorio no sigue literalmente el ejemplo `Tema6_ApellidoNombre` | Se conserva el repositorio grupal actual para no cambiar su URL sin autorización; confirmar si el docente exige literalmente el patrón del ejemplo | Pendiente de confirmar |
| H12 | Faltaba el SRS breve y no existía una lista que vinculara REQ-001..003 con CU-001..003 | Se creó el SRS en Borrador con trazabilidad preliminar y los flujos E1, E2, E3 y C1 de CU-002 | Corregido; CU-001 y CU-003 se detallarán en ITER-2 |
| H13 | La necesidad de la recepcionista no se vincula a un requisito de alto nivel | No se inventó un requisito nuevo; el grupo debe validar si esa función entra en el alcance | Pendiente de validación |
| H14 | Roadmap y riesgos indicaban roles sin integrantes responsables | Se asignaron nombres a iteraciones y riesgos según la distribución propuesta por el grupo | Propuesto; confirmar con el grupo |
| H15 | El checklist incluía comprobaciones adicionales a las seis del paso 5 | Se ajustó el checklist principal a las seis verificaciones de la guía | Corregido |
