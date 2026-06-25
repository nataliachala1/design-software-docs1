# Documentación de microservicios

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

Este documento define cuándo y cómo registrar documentación de microservicios en el repositorio.

## Regla de oro

> Sin ADR aprobada o decisión resuelta en `15-project-control/open-questions.md`, no existe carpeta de microservicio. Sin servicio real en código, no existe documentación.

## Regla crítica

No crear carpetas en `09-microservices/services/` hasta que el servicio exista en el repositorio de código o su creación esté formalmente aprobada por arquitectura.

Todo servicio nuevo requiere uno de estos artefactos antes de abrir PR:

- ADR en `05-architecture/decisions/records/`, o
- Decisión con estado `RESUELTA` en `15-project-control/open-questions.md`

Sin ese artefacto, el PR será rechazado sin revisión.

## Ubicación

```text
09-microservices/services/<nombre-del-servicio>/
```

El nombre de la carpeta debe coincidir exactamente con el nombre del repositorio de código.

## Flujo

### 1. Verificar catálogo

Confirmar que el servicio no exista en `09-microservices/service-catalog.md`.

### 2. Copiar plantilla

```bash
cp -r 09-microservices/_template/ 09-microservices/services/<nombre-servicio>/
```

### 3. Completar README del servicio

El `README.md` debe incluir:

- Responsabilidad del servicio
- Bounded context
- Owner
- Repositorio de código
- Dependencias
- Enlaces a contrato API, modelo de datos, eventos y runbook

### 4. Registrar en catálogo

Agregar fila en `09-microservices/service-catalog.md`:

```markdown
| <nombre-servicio> | <descripción> | <owner> | [repo](<url>) | 🟡 |
```

### 5. Completar archivos mínimos

| Archivo | Qué documentar |
|---------|----------------|
| `README.md` | Responsabilidad, owner, dependencias y links |
| `api-contract.md` | Endpoints, request, response y errores |
| `data-model.md` | Modelo transaccional propio del servicio |
| `events.md` | Eventos publicados y consumidos |
| `runbook.md` | Deploy, rollback, variables y troubleshooting |

`README.md` y `api-contract.md` deben estar en 🟡 mínimo antes del primer merge a `main` del código del servicio.

## Commits

```bash
git checkout -b feat/doc-service-<nombre-servicio>
git add 09-microservices/services/<nombre-servicio>/
git add 09-microservices/service-catalog.md
git commit -m "docs(09-microservices): register <service-name> service"
git push origin feat/doc-service-<nombre-servicio>
```

Un commit por microservicio cuando se documentan varios servicios en la misma sesión.

## Contrato API

- `09-microservices/services/<servicio>/api-contract.md` — contrato operativo del servicio.
- `07-api/contracts/openapi/` — archivos OpenAPI formales cuando existan.

Mantener enlaces cruzados entre ambos cuando aplique.