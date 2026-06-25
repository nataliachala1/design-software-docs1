# OpenAPI specs

Directorio para almacenar especificaciones OpenAPI en formato YAML/JSON.

Convenciones:

- Nombre de archivo: `<service>-openapi.yaml` (ej: `scheduling-openapi.yaml`).
- Mantener la especificación compacta y versionada en el repositorio.
- Incluir `info.version` siguiendo el versionado semántico.
- Usar el `servers` apropiado para entornos (local, staging, prod) sólo como ejemplos.

Uso:

- Las APIs públicas o contratos compartidos entre servicios deben colocarse aquí.
- Para contratos internos que cambian frecuentemente, referenciar el archivo desde el README del servicio.

Referencias:

- SpringDoc / OpenAPI para generación automática en tiempo de ejecución.
