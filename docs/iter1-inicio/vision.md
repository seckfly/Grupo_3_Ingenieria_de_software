# Documento de Visión v1 - Sistema de reservas de citas

> Estado: versión base (Base en la [matriz fase–artefacto](matriz-fase-artefacto.md)). No hay validación externa registrada. Los objetivos de la sección 5 son metas, no resultados obtenidos.

## 1. Propósito

Permitir que los pacientes reserven y cancelen citas médicas en línea.

## 2. Problema

Hoy las citas se piden por teléfono: hay filas de espera, errores de horarios y citas duplicadas.

## 3. Alcance

- Incluye: registro de pacientes, reserva de citas, cancelación de citas, confirmación por correo de cada cita reservada.
- No incluye: pagos en línea, historia clínica, telemedicina.

## 4. Interesados

| Rol | Necesidad |
|---|---|
| Paciente | Reservar rápido y sin llamar |
| Recepcionista | Consultar horarios y citas sin duplicados; esta necesidad aún no está vinculada a un requisito funcional y debe validarse antes de incorporarla al alcance comprometido |
| Administrador | Controlar horarios de los médicos |

## 5. Objetivos medibles

Metas del proyecto; todavía no se han medido ni alcanzado.

- Reducir a la mitad el tiempo de reserva (línea base por medir).
- Eliminar las citas duplicadas.

## 6. Requisitos de alto nivel

- REQ-001: Registrar paciente
- REQ-002: Reservar cita (incluye la confirmación por correo de la cita reservada)
- REQ-003: Cancelar cita

## 7. Restricciones

Debe funcionar en navegador. Primera versión en 7 semanas.

---

Términos oficiales: ver [glosario](glosario.md).
