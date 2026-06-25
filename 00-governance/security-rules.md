# Seguridad documental

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

Este repositorio puede ser consultado por varios equipos. Todo contenido publicado debe usar ejemplos seguros y nunca exponer información sensible.

## Regla de oro

> Ante la duda de si algo es sensible, no se publica. Rotar primero, avisar después.

## No publicar

- Credenciales, contraseñas, tokens o llaves privadas.
- Certificados o archivos `.env`, `.pem`, `.key`, `.p12`, `.pfx`.
- Datos personales reales: correos, teléfonos, documentos de identidad, nombres de usuarios reales.
- Capturas de pantalla con sesiones abiertas o datos operativos reales.
- URLs internas, IPs, nombres de host o rutas de red de ambientes reales.
- Procedimientos que permitan evadir controles de seguridad.

## Valores seguros para ejemplos

| Caso | Valor seguro |
|------|--------------|
| Correo | `usuario@example.com` |
| Token | `TOKEN_DE_EJEMPLO` |
| URL | `https://example.com/api` |
| Servicio | `sena-horarios-service` |
| Número de documento | `1234567890` — aclarar siempre que es ficticio |

## Antes de subir capturas

- Confirmar que no hay nombres, correos, tokens ni sesiones visibles.
- Validar que la captura aporta valor documental real.
- Guardar en `assets/images/` y referenciar desde el documento.

## Si se detecta una fuga

1. No crear más commits con el dato expuesto.
2. **Rotar la credencial de inmediato** si aplica — no esperar confirmación.
3. Avisar al responsable del repositorio y al equipo de arquitectura.
4. Abrir PR que reemplace el contenido por un ejemplo seguro.
5. Evaluar limpieza de historial de Git si el dato quedó versionado.

## Contacto de seguridad

| Rol | Canal |
|-----|-------|
| Responsable del repositorio | `@[completar]` |
| Equipo de arquitectura | `@equipo-arquitectura` → `[completar canal: Slack / Teams / email]` |

## Checklist pre-PR

- [ ] Sin credenciales ni tokens.
- [ ] Sin datos personales reales.
- [ ] Sin URLs o IPs de ambientes internos.
- [ ] Sin capturas con sesiones o datos reales.
- [ ] Todos los ejemplos usan valores ficticios.