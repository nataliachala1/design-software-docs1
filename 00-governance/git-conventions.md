# Convenciones de Git

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

Este repositorio usa ramas protegidas, Pull Requests y Conventional Commits para mantener trazabilidad documental.

## Regla de oro

> Ningún cambio va directo a `dev`, `qa` o `main`. Sin PR, sin revisión, sin merge.

## Ramas protegidas

| Rama | Propósito | Regla |
|------|-----------|-------|
| `dev` | Integración de trabajo en desarrollo | Recibe PRs desde ramas hijas |
| `qa` | Validación funcional y técnica | Recibe PRs o cherry-picks aprobados desde `dev` |
| `main` | Documentación estable | Recibe solo PRs desde `release/*` |

## Ramas documentales

| Tipo | Cuándo usarla | Ejemplo |
|------|---------------|---------|
| `feat/doc-*` | Documento nuevo | `feat/doc-api-guidelines` |
| `fix/doc-*` | Corrección de contenido | `fix/doc-scope` |
| `chore/doc-*` | Reorganización o renombrado | `chore/doc-move-adr-003` |
| `docs/doc-*` | Actualización de documento existente | `docs/doc-service-catalog` |

## Ramas por historia de usuario

| Caso | Formato | Ejemplo |
|------|---------|---------|
| Desarrollo de HU | `hu-<numero>-dev` | `hu-01-dev` |
| Ajuste o validación QA | `hu-<numero>-qa` | `hu-01-qa` |
| Release de iteración | `release/<iteracion>` | `release/iteration-01` |

## Flujo hacia dev

```bash
git checkout dev && git pull origin dev
git checkout -b hu-01-dev
git add <archivos>
git commit -m "docs(04-requirements): add scheduling availability user story"
git push origin hu-01-dev
```

Abrir PR de `hu-01-dev` → `dev`.

## Flujo hacia qa

```bash
git checkout qa && git pull origin qa
git checkout -b hu-01-qa

# Merge completo
git merge origin/hu-01-dev

# O cherry-pick selectivo
git cherry-pick <commit-sha>

git push origin hu-01-qa
```

Abrir PR de `hu-01-qa` → `qa`.

## Release hacia main

```bash
git checkout main && git pull origin main
git checkout -b release/iteration-01

git cherry-pick <commit-hu-01>
git cherry-pick <commit-hu-02>
git cherry-pick <commit-hu-03>

git push origin release/iteration-01
```

Abrir PR de `release/iteration-01` → `main`.

## Conventional Commits

Formato obligatorio:

```text
<type>(NN-section): short description in English
```

| Tipo | Uso |
|------|-----|
| `docs` | Crear o actualizar documentación |
| `fix` | Corregir contenido incorrecto |
| `chore` | Mover, renombrar o actualizar metadatos |
| `refactor` | Reestructurar sin cambiar significado |

No usar `feat`, `style`, `test`, `perf`, `build` ni `ci` en este repositorio.

Ejemplos:

```bash
docs(04-requirements): add scheduling user stories
docs(09-microservices): register auth service
fix(01-context): clarify project scope
chore(08-uml): export sequence diagrams to SVG
refactor(00-governance): split contribution rules by topic
```

## Reglas de commits

- Descripción en inglés; contenido de documentos en español.
- Commits pequeños y trazables.
- Un commit por microservicio cuando se documentan varios.
- No mezclar cambios de secciones distintas sin razón justificada.

## Hotfix en main

Para errores críticos que no pueden esperar el flujo normal:

```bash
git checkout main && git pull origin main
git checkout -b fix/doc-broken-api-contract
git add <archivos>
git commit -m "fix(07-api): correct broken endpoint reference in contract"
git push origin fix/doc-broken-api-contract
```

Abrir PR de `fix/doc-*` → `main`. Una vez mergeado, propagar a `qa` y `dev`:

```bash
git checkout qa && git pull origin qa
git cherry-pick <commit-sha>
git push origin qa
# Repetir para dev
```