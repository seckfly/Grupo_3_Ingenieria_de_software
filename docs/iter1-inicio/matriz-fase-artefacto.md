# Matriz fase–artefacto - Sistema de reservas de citas

Indica qué artefacto se produce en cada fase RUP y con qué nivel de detalle.

**Estados:** Borrador (primera versión) · Base (acordado) · Refinado (mejorado) · Final (entregado) · Lista (inventario preliminar de casos de uso, tal como aparece en la tabla de la guía) · — (no aplica).

| Artefacto | Inicio | Elaboración | Construcción | Transición |
| --- | --- | --- | --- | --- |
| Documento de Visión | Base | Refinado | — | Final |
| SRS breve | Borrador | Base | Refinado | Final |
| Casos de uso | Lista | Base | Refinado | Final |
| Diagrama de actividad (proceso crítico) | Base | Refinado | — | — |
| Diagrama de clases | — | Base | Refinado | Final |
| Diagrama de secuencia | — | Base | Refinado | — |
| Diagrama de estados (Cita) | — | Borrador | Base | Final |
| Casos de prueba | — | Borrador | Base | Final |
| Manual de usuario | — | — | Borrador | Final |

La tabla es una **planificación** del nivel de detalle por fase. No demuestra que los artefactos ya existan.

- Coherencia con el [roadmap](roadmap.md): ITER-1 (Inicio), ITER-2 (Elaboración), ITER-3 (Construcción) e ITER-4 (Transición).

## Estado actual de los artefactos (fin de ITER-1)

| Artefacto | Estado actual | Ubicación |
|---|---|---|
| Documento de Visión | Existe (v1 base) | [vision.md](vision.md) |
| SRS breve | Existe como Borrador | [srs-breve.md](srs-breve.md) |
| Casos de uso | Lista preliminar CU-001 a CU-003; flujos de CU-002 resumidos | [srs-breve.md](srs-breve.md) |
| Diagrama de actividad (CU-002) | Existe | [PNG](../../modelos/iter1/actividad-reservar-cita.png) · [fuente .drawio](../../modelos/iter1/actividad-reservar-cita.drawio) |
| Diagrama de clases, de secuencia y de estados (Cita) | Pendientes de fases posteriores | — |
| Casos de prueba y manual de usuario | Pendientes de fases posteriores | — |

La especificación detallada de CU-001 y CU-003 está prevista para ITER-2, conforme a la matriz.
