# Overview

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

## Contexto institucional

El SENA (Servicio Nacional de Aprendizaje) opera una red nacional de centros de formación profesional integral organizados en macroregiones, microregiones y sedes. Cada centro gestiona múltiples programas de formación (fichas), instructores, ambientes de aprendizaje y aprendices de forma simultánea.

El programa **ADSO 314555** desarrolla el sistema **Horarios SENA** como solución tecnológica para centralizar y automatizar la programación académica de los centros de formación.

## Problema

La programación de horarios se realiza hoy de forma manual o con herramientas desconectadas: hojas de cálculo, correos electrónicos y tableros físicos. Esto genera:

- **Conflictos de asignación:** un mismo instructor, ambiente o ficha puede quedar programado en dos lugares al mismo tiempo.
- **Sobrecarga administrativa:** los coordinadores invierten tiempo excesivo en tareas de verificación y corrección manual.
- **Uso ineficiente de recursos:** ambientes subutilizados o instructores con cargas desbalanceadas.
- **Falta de trazabilidad:** no existe un registro centralizado y auditable de la ejecución de la formación.

El proyecto **Horarios SENA** resuelve estos problemas mediante una plataforma centralizada, con validación algorítmica de conflictos y control en tiempo real.

## Objetivos

1. **Gestionar la estructura institucional** del SENA: macroregiones, microregiones, departamentos, municipios, centros de formación y sedes.
2. **Administrar los catálogos base** del sistema: modalidades de formación, jornadas, estados, líneas tecnológicas y demás parámetros configurables.
3. **Gestionar los ambientes de aprendizaje:** infraestructura, inventario y disponibilidad en tiempo real.
4. **Gestionar los actores y sus perfiles:** instructores, aprendices y directivos con sus roles, competencias y disponibilidades.
5. **Programar horarios sin conflictos:** asignar instructor, ambiente, ficha y franja horaria con validación automática que elimine colisiones.
6. **Garantizar trazabilidad:** registrar toda la ejecución de la formación de forma centralizada y auditable.

## Referencias

- Manual de Diseño Curricular SENA
- Ley 119 de 1994 — Estructura y misión del SENA
- [scope.md](./scope.md) — Alcance detallado del proyecto
- [glossary.md](./glossary.md) — Glosario de términos