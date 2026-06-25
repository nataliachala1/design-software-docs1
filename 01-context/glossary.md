# Glosario

> Estado: 🟢 Estable | Última actualización: 2026-06-24
> Autor: ADSO 314555 | Equipo: Arquitectura

Vocabulario compartido del dominio SENA y del sistema Horarios SENA. Todos los equipos deben usar estos términos con el significado aquí definido.

## Términos

| Término | Definición | Contexto |
|---------|------------|----------|
| **Aprendiz** | Persona matriculada en un programa de formación del SENA. Se asocia a una ficha activa y tiene un estado dentro del proceso formativo. | SENA |
| **Ambiente de aprendizaje** | Espacio físico o virtual donde se desarrolla la formación. Tiene tipo (aula, laboratorio, taller, virtual), capacidad, ubicación y estado de disponibilidad. | SENA / Sistema |
| **Centro de formación** | Unidad operativa del SENA responsable de ejecutar programas de formación en una región. Agrupa sedes, instructores, ambientes y fichas. | SENA |
| **Competencia** | Unidad de aprendizaje que un instructor está habilitado para impartir. Define la especialidad técnica del instructor dentro de una línea tecnológica. | SENA |
| **Conflicto de horario** | Situación en la que un mismo recurso (instructor, ambiente o ficha) queda asignado a dos actividades simultáneas. El sistema lo detecta y bloquea automáticamente. | Sistema |
| **Coordinador** | Directivo del centro de formación responsable de gestionar la programación académica, asignar horarios y supervisar la ejecución de la formación. | SENA |
| **Ficha** | Grupo de aprendices matriculados en un mismo programa de formación durante un periodo específico. Se identifica con un número único (ej. ficha 3145555). | SENA |
| **Franja horaria** | Intervalo de tiempo definido por día de la semana, hora de inicio y hora de fin. Es la unidad mínima de programación del sistema. | Sistema |
| **Horario** | Asignación concreta de un instructor, un ambiente, una ficha y una franja horaria. Representa una sesión de formación programada. | Sistema |
| **Instructor** | Persona responsable de impartir formación a los aprendices. Puede ser de planta (vinculado directamente al SENA) o contratista. Tiene competencias, disponibilidad y estado. | SENA |
| **Jornada** | Turno académico en el que se ejecuta la formación. Valores posibles: Mañana, Tarde, Noche, Fin de Semana. | SENA |
| **Línea tecnológica** | Clasificación temática que agrupa programas y competencias por área de conocimiento técnico dentro del SENA (ej. Tecnología de la Información, Agroindustria). | SENA |
| **Macroregión** | Agrupación geográfica de mayor nivel dentro de la estructura organizacional del SENA. Contiene varias microregiones. | SENA |
| **Microregión** | Subdivisión de una macroregión. Agrupa centros de formación de una zona geográfica específica. | SENA |
| **Modalidad de formación** | Forma en que se imparte la formación. Valores posibles: Presencial, Virtual, A Distancia, Mixta. | SENA |
| **Red de conocimiento** | Agrupación de programas y competencias que comparten un área disciplinar común dentro del SENA. Relacionada con las líneas tecnológicas. | SENA |
| **Resultado de aprendizaje** | Logro concreto y verificable que un aprendiz debe demostrar al finalizar una competencia. Define los criterios de evaluación. | SENA |
| **Sede** | Instalación física perteneciente a un centro de formación. Un centro puede tener varias sedes con ambientes propios. | SENA |

## Convención de estados

Los siguientes estados aplican a múltiples entidades del sistema (fichas, instructores, ambientes, etc.):

| Estado | Significado |
|--------|-------------|
| Activo | Operativo y disponible para asignación |
| Inactivo | Deshabilitado temporalmente |
| Suspendido | Bloqueado por causa específica |
| Finalizado | Proceso concluido, sin posibilidad de reasignación |

## Referencias

- [overview.md](./overview.md) — Contexto y problema del proyecto
- [scope.md](./scope.md) — Alcance y restricciones del MVP