# 📘 Lenguaje Ubicuo del Sistema

El **lenguaje ubicuo** define los términos compartidos entre negocio, desarrollo y producto.
Debe mantenerse **consistente** en:

* Código
* Base de datos
* Documentación
* Conversaciones del equipo

---

# Dominios del Sistema

## 1. Gestión Institucional

### Estructura territorial

| Término          | Descripción                                                                |
| ---------------- | -------------------------------------------------------------------------- |
| **Macroregión**  | Región natural de Colombia (Andina, Caribe, Pacífica, Orinoquía, Amazonía) |
| **Microregión**  | Departamento o agrupación dentro de una macroregión                        |
| **Departamento** | División político-administrativa                                           |
| **Municipio**    | División dentro de un departamento                                         |

### Estructura organizacional

| Término                  | Descripción                                            |
| ------------------------ | ------------------------------------------------------ |
| **Centro de Formación**  | Unidad principal donde se ejecutan procesos formativos |
| **Sede**                 | Unidad física (edificio, tecnoacademia, tecnoparque)   |
| **Unidad Institucional** | Espacio físico donde se desarrollan actividades        |
| **Ubicación**            | Dirección física con coordenadas                       |

### Configuración del sistema

| Término       | Descripción                                                  |
| ------------- | ------------------------------------------------------------ |
| **Catálogo**  | Valores de referencia (modalidades, jornadas, etc.)          |
| **Estado**    | Ciclo de vida de un registro                                 |
| **Parámetro** | Configuración global del sistema                             |
| **Jornada**   | Período del día (Mañana, Tarde, Noche)                       |
| **Modalidad** | Forma de formación (Presencial, Virtual, A Distancia, Mixta) |

---

## 2. Gestión Académica

### Estructura formativa

| Término                   | Descripción                                           |
| ------------------------- | ----------------------------------------------------- |
| **Programa de Formación** | Oferta educativa con estructura curricular            |
| **Tipo de Formación**     | Titulada, Complementaria, Especialización Tecnológica |
| **Diseño Curricular**     | Estructura de competencias, RAPs y horas              |

### Conocimiento y competencias

| Término         | Descripción                                                           |
| --------------- | --------------------------------------------------------------------- |
| **Competencia** | Capacidad técnica o transversal que el aprendiz debe desarrollar      |
| **RAP**         | Resultado de Aprendizaje — logro medible al finalizar una competencia |

### Organización del conocimiento

| Término                 | Descripción                                                   |
| ----------------------- | ------------------------------------------------------------- |
| **Línea Tecnológica**   | Nivel más alto de la jerarquía de conocimiento del SENA       |
| **Red Tecnológica**     | Agrupación técnica intermedia dentro de una línea tecnológica |
| **Red de Conocimiento** | Agrupación disciplinar que contiene programas de formación    |

### Gestión académica operativa

| Término    | Descripción                                                |
| ---------- | ---------------------------------------------------------- |
| **Ficha**  | Grupo de aprendices que cursan un mismo programa y jornada |
| **Oferta** | Programas disponibles en un centro de formación            |

---

## 3. Gestión de Recursos

### Infraestructura

| Término        | Descripción                                                     |
| -------------- | --------------------------------------------------------------- |
| **Ambiente**   | Espacio físico o virtual donde se desarrolla la formación       |
| **Inventario** | Conjunto de recursos disponibles en un ambiente                 |
| **Recurso**    | Equipo, mobiliario o herramienta (computador, proyector, silla) |

### Operación y mantenimiento

| Término            | Descripción                                                     |
| ------------------ | --------------------------------------------------------------- |
| **Mantenimiento**  | Actividad preventiva o correctiva sobre ambientes o recursos    |
| **Disponibilidad** | Estado actual del ambiente (Disponible, Ocupado, Mantenimiento) |

### Uso de recursos

| Término     | Descripción                                           |
| ----------- | ----------------------------------------------------- |
| **Reserva** | Asignación temporal de un ambiente para una actividad |

### Actores

| Término              | Descripción                                             |
| -------------------- | ------------------------------------------------------- |
| **Instructor**       | Persona que orienta la formación (planta o contratista) |
| **Aprendiz**         | Persona que recibe formación en una ficha               |
| **Directivo**        | Persona con rol de coordinación o dirección             |
| **Empresa**          | Entidad donde el aprendiz realiza la etapa productiva   |
| **Etapa Productiva** | Período de práctica del aprendiz en una empresa         |

---

## 4. Gestión de Horarios

### Planificación

| Término            | Descripción                                                  |
| ------------------ | ------------------------------------------------------------ |
| **Horario**        | Asignación de instructor + ambiente + ficha + franja horaria |
| **Franja Horaria** | Bloque de tiempo definido por día, hora inicio y hora fin    |

### Ejecución y control

| Término             | Descripción                                     |
| ------------------- | ----------------------------------------------- |
| **Sesión de Clase** | Ejecución real de una sesión de formación       |
| **Asignación**      | Registro histórico de una asignación de horario |

### Gestión de incidencias

| Término         | Descripción                                                             |
| --------------- | ----------------------------------------------------------------------- |
| **Conflicto**   | Cruce de horario (instructor, ambiente o ficha en dos lugares a la vez) |
| **Observación** | Registro de novedades sobre un horario (ej. "Instructor ausente")       |
| **Incidencia**  | Problema reportado que afecta la ejecución del horario                  |

---

## 5. Gestión de Proyectos Formativos

### Estructura del proyecto

| Término                | Descripción                                                  |
| ---------------------- | ------------------------------------------------------------ |
| **Proyecto Formativo** | Proyecto que integra competencias y RAPs en un contexto real |
| **Fase**               | Etapa del proyecto (Análisis, Diseño, Construcción, Pruebas) |
| **Actividad**          | Tarea específica dentro de una fase                          |

### Resultados

| Término        | Descripción                                            |
| -------------- | ------------------------------------------------------ |
| **Entregable** | Producto o resultado de una actividad                  |
| **Evidencia**  | Soporte digital de un entregable (PDF, imagen, código) |

### Control y dependencias

| Término         | Descripción                                           |
| --------------- | ----------------------------------------------------- |
| **Dependencia** | Relación entre fases (una fase depende de otra)       |
| **Hito**        | Punto de control importante en el avance del proyecto |

---

## 6. Transversal / Soporte

### Seguridad y acceso

| Término     | Descripción                                                            |
| ----------- | ---------------------------------------------------------------------- |
| **Usuario** | Persona con acceso al sistema (Coordinador, Instructor, Administrador) |
| **Rol**     | Conjunto de permisos (COORDINADOR, INSTRUCTOR, ADMINISTRADOR)          |
| **Permiso** | Acción específica que puede realizar un rol                            |

### Autenticación

| Término    | Descripción                     |
| ---------- | ------------------------------- |
| **Token**  | JWT generado para autenticación |
| **Sesión** | Registro de login de un usuario |

### Auditoría y comunicación

| Término          | Descripción                                                     |
| ---------------- | --------------------------------------------------------------- |
| **Auditoría**    | Registro inmutable de todas las acciones críticas               |
| **Notificación** | Mensaje enviado a un usuario (email, app, dashboard)            |
| **Alerta**       | Notificación de alto impacto (ej. conflicto de horario crítico) |

---

# Referencias

* `entities-and-rules.md` — Detalle de entidades y reglas de negocio
* `domain-events.md` — Eventos de dominio
* `09-microservices/service-catalog.md` — Catálogo de microservicios
* `01-context/glossary.md` — Glosario general del proyecto

---

# Buenas prácticas

* Usar los términos de forma **exacta en todo el sistema**
* Evitar sinónimos (ej: no usar “grupo” en vez de “Ficha”)
* Cada término debería mapear a:

  * Una entidad (BD)
  * Una clase (Java)
  * Un agregado (DDD)
