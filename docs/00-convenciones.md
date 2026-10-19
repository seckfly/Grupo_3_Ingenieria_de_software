# Convenciones del proyecto

## IDs (únicos y permanentes)

REQ-### requisito · CU-### caso de uso · RSK-### riesgo  
ITER-# iteración · CLS-Nombre clase

## Carpetas

```text
docs/iterN-fase/   documentos de cada iteración
modelos/iterN/     diagramas (fuente y exportación)
```

## Nombres de archivo

Minúsculas con guiones. Diagramas: tipo-tema.drawio / .png.

## Commits

Formato: `ITERN: qué se hizo (IDs afectados)`.

Ejemplo: `ITER1: agrega excepción E3 en CU-002`.

Los commits anteriores a esta convención no se reescriben.

## Versiones (tags)

Formato: `vX.Y-iterN`. La versión de cierre de Inicio es `v1.0-iter1`.
