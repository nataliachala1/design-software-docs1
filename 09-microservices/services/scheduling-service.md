# Scheduling Service

Descripción: Servicio responsable de la gestión de horarios, asignaciones y detección de conflictos.

Responsabilidades principales:

- CRUD de `horarios`, `asignaciones` y `franjas`.
- Validación de conflictos (instructor/ambiente/ficha).
- Publicación de eventos: `assignment.created`, `assignment.conflict`, `schedule.updated`.
- API para consumo por frontend y por otros microservicios.

Referencias:

- Contrato API: `../_template/api-contract.md` (usar como guía y generar `scheduling-api.md`).
- Modelo de datos: `../_template/data-model.md`.
- Runbook: `../_template/runbook.md`.

Notas operativas:

- Mantener compatibilidad hacia atrás en versiones menores del contrato. Versionar cambios incompatibles.
- Documentar ejemplos de payload en el `api` contract y en `events`.
