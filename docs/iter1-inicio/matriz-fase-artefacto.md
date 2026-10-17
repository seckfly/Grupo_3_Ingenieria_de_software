# Matriz fase-artefacto - Sistema de reservas de citas

Indica qué artefacto se produce en cada fase RUP y con qué nivel de detalle.

**Estados:** Borrador (primera versión) · Base (acordado) · Refinado (mejorado) · Final (entregado) · — (no aplica)

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

- «Lista» en Casos de uso (Inicio) se conserva tal como figura en la guía, pero no está definido en la leyenda de estados.
- Coherencia con el [roadmap](roadmap.md): ITER-1 (Inicio), ITER-2 (Elaboración), ITER-3 (Construcción) e ITER-4 (Transición).

## Estado actual de los artefactos (fin de ITER-1)

| Artefacto | Existe en el repositorio | Ubicación |
| --- | --- | --- |
| Documento de Visión | Sí (v1) | [vision.md](vision.md) |
| Diagrama de actividad (CU-002) | Sí | [modelos/iter1](../../modelos/iter1/actividad-reservar-cita.png) |
| SRS breve | No | — |
| Casos de uso | No (solo se mencionan CU-001 y CU-002 en el diagrama) | — |
| Diagrama de clases, de secuencia y de estados (Cita) | No (fases posteriores) | — |
| Casos de prueba y manual de usuario | No (fases posteriores) | — |
