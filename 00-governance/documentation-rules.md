# Reglas de documentación

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

Este documento define las reglas para crear, nombrar, enlazar y mantener documentos. Para ramas y commits ver [git-conventions.md](./git-conventions.md). Para seguridad ver [security-rules.md](./security-rules.md).

## Regla de oro

> Un documento que no está en el índice no existe. Un diagrama sin fuente editable no es válido. Un documento sin revisor no es estable.

## Naming

### Archivos

- Usar `kebab-case.md`.
- Nombres descriptivos: `data-model.md`, `api-contract.md`, `migration-strategy.md`.
- Prohibido: espacios, `snake_case`, `PascalCase`, nombres genéricos como `documento1.md`.

### Carpetas

- Las carpetas raíz usan prefijo numérico: `NN-nombre`.
- Carpetas raíz nuevas requieren aprobación de arquitectura.
- Toda carpeta nueva debe incluir `README.md`.

### ADRs

- Formato: `ADR-NNN-titulo-corto.md`.
- Ubicación: `05-architecture/decisions/records/`.
- Proceso completo en [05-architecture/decisions/README.md](../05-architecture/decisions/README.md).

## Estructura mínima

Todo documento `.md` debe iniciar con:

```markdown
# Título descriptivo

> Estado: 🔴 Pendiente | Última actualización: YYYY-MM-DD
> Autor: Nombre Apellido | Equipo: <nombre del equipo>

## Contexto

## Contenido

## Referencias
```

## Estados

| Estado | Uso |
|--------|-----|
| 🔴 Pendiente | Creado, sin contenido validado |
| 🟡 En progreso | Contenido parcial o en revisión |
| 🟢 Estable | Revisado, aprobado y vigente |
| ⚫ Deprecado | Ya no aplica |

**Criterio para documentos deprecados:**

| Situación | Acción |
|-----------|--------|
| Sustituido por otro documento | Cambiar estado a ⚫ y añadir `> Reemplazado por: [enlace]` al inicio |
| Sección eliminada o reestructurada | Mover a `99-archive/deprecated/` y registrar en `CHANGELOG.md` |
| ADR obsoleta | Nunca mover — cambiar estado a `DEPRECATED` y añadir `> Reemplazada por: ADR-NNN.md` |

Un documento pasa a 🟢 solo después de revisión por una persona distinta al autor.

## Índices obligatorios

- Todo archivo nuevo se enlaza desde el `README.md` de su carpeta.
- Toda carpeta nueva incluye `README.md`.
- Documentos movidos conservan trazabilidad mediante nota en `CHANGELOG.md`.
- ADRs se registran en `05-architecture/decisions/README.md`.
- Microservicios se registran en `09-microservices/service-catalog.md`.

## Documentos y carpetas

### Documento nuevo

1. Verificar que no exista en otra sección.
2. Crear el archivo en la sección correcta con la estructura mínima.
3. Enlazarlo desde el `README.md` de la sección.
4. Abrir PR con checklist completo.

### Carpeta nueva

Crear subcarpeta solo si:

- Agrupa varios documentos del mismo subtema.
- Tiene ciclo de vida propio.
- Facilita navegación frecuente para varios equipos.

Prohibido: `misc/`, `otros/`, `temp/`, carpetas con un solo documento.

## Diagramas y recursos visuales

| Tipo | Ubicación |
|------|-----------|
| Fuentes UML `.wsd` / `.puml` | `08-uml/diagrams/source/` |
| Exportaciones `.svg` / `.png` | `08-uml/diagrams/exports/` |
| Logos | `assets/logos/` |
| Capturas y mockups | `assets/images/` |

Reglas:

- Todo diagrama requiere fuente editable. Sin fuente, el PR se rechaza.
- SVG preferido sobre PNG.
- Registrar todo diagrama en `08-uml/diagram-index.md`.

## Errores comunes

| Error | Solución |
|-------|----------|
| Archivo sin registrar en el índice | Enlazar en el `README.md` de la sección |
| Subir solo exportación de diagrama | Subir fuente + exportación |
| Duplicar contenido entre secciones | Enlazar al documento canónico |
| Carpeta con nombre genérico | Usar nombre descriptivo |
| Eliminar historia documental | Deprecar o archivar en `99-archive/` |

## Revisión

- Listo para PR → [definition-of-ready.md](./definition-of-ready.md)
- Listo para cierre → [definition-of-done.md](./definition-of-done.md)