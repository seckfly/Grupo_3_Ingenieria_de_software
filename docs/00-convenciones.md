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

minusculas-con-guiones. Diagramas: tipo-tema.drawio / .png

## Commits

Formato: "ITERN: qué se hizo (IDs afectados)"
Ejemplo: "ITER1: agrega excepción E3 en CU-002"

Los commits anteriores a esta convención (por ejemplo, "Add files via upload") no se reescriben.

## Versiones (tags)

vX.Y-iterN  →  v1.0-iter1

El tag `v1.0-iter1` identifica el cierre de ITER-1 en `main`, después de integrar el PR conforme a los pasos 8 y 9 de la guía.
