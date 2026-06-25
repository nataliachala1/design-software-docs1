# Gobierno documental

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

## Contenido

Reglas comunes para que todos los equipos documenten con el mismo criterio, sin duplicar información ni publicar datos sensibles.

## Reglas de oro

1. **Sin rama, sin cambio.** Ningún documento se edita directamente en `dev`, `qa` o `main`.
2. **Sin índice, no existe.** Todo archivo nuevo debe registrarse en el `README.md` de su sección antes de hacer PR.
3. **Sin fuente editable, el diagrama no vale.** Exportaciones sin fuente se rechazan en revisión.
4. **Secretos fuera del repo.** Credenciales, tokens, IPs de producción o datos personales nunca se publican aquí.
5. **Un documento, un propósito.** Si el contenido ya existe en otra sección, se enlaza; no se duplica.
6. **El historial es sagrado.** No se elimina historia sin acuerdo del equipo; los documentos deprecados van a `99-archive/`.

## Principios

- **Claridad sobre completitud:** un documento corto y claro es mejor que uno largo e incompleto.
- **Trazabilidad:** toda decisión de arquitectura tiene su ADR; toda HU tiene sus criterios de aceptación.
- **Seguridad por defecto:** ante la duda de si algo es sensible, no se publica.

## Archivos

| Archivo | Descripción | Estado |
|---------|-------------|--------|
| [documentation-rules.md](./documentation-rules.md) | Naming, estructura mínima, estados, índices y diagramas | 🟢 |
| [git-conventions.md](./git-conventions.md) | Ramas, ambientes, releases y commits | 🟢 |
| [microservices-documentation.md](./microservices-documentation.md) | Reglas para documentar microservicios reales | 🟢 |
| [security-rules.md](./security-rules.md) | Reglas contra fugas de información sensible | 🟢 |
| [definition-of-ready.md](./definition-of-ready.md) | Criterios para saber si un documento puede pasar a revisión | 🟢 |
| [definition-of-done.md](./definition-of-done.md) | Criterios para cerrar un documento como estable | 🟢 |