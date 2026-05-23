# **4. Marco de ejecución ágil: Scrum + Kanban**

Scrum y Kanban se aplican exclusivamente en los ciclos BML que requieren desarrollo de software: **Ciclo 3 (MVP v1.0)** y **Ciclo 4 (MVP v2.0)**. El Ciclo 1 (prototipo navegable de diseño), el Ciclo 2 (entrevistas y encuesta) y el Ciclo 5 (demo en video) no requieren Sprint formal (Kniberg, 2015; Hammarberg & Sundén, 2014).

Scrum provee la estructura temporal mediante Sprints, los roles y los eventos de coordinación. Kanban provee la visibilidad diaria del flujo de trabajo y los límites de trabajo en progreso (WIP) dentro de cada Sprint.

## **4.1. Equipo de trabajo — roles en el Sprint**

Cada integrante asume un rol de Scrum definido para la ejecución de los Sprints de construcción. La siguiente tabla describe las responsabilidades de cada uno durante el desarrollo de los MVPs.

| Rol Scrum            | Persona        | Responsabilidad en el Build                                                  |
| :------------------- | :------------- | :--------------------------------------------------------------------------- |
| **Product Owner**    | Rel Guzmán     | Define y prioriza las tareas del Sprint. Acepta los entregables al final.    |
| **Scrum Master**     | Carlos Mendoza | Facilita las ceremonias. Elimina bloqueos del equipo.                        |
| **Development Team** | María Torres   | Diseño UX/UI del sistema y soporte en la implementación de vistas.           |
| **Development Team** | Luis Ramírez   | Desarrollo técnico del sistema: backend, base de datos y lógica de alertas.  |
| **Development Team** | Sofía Paredes  | Verificación de criterios de aceptación, testing y carga de datos de prueba. |

## **4.2. Eventos y artefactos de Scrum**

### **4.2.1. Eventos**

Los eventos Scrum se aplican en cada Sprint de desarrollo (Ciclos 3 y 4). La columna de aplicación describe cómo se ejecutarán en el primer Sprint de desarrollo (Ciclo 3, MVP v1.0).

| Evento                   | Descripción general                                                        | Aplicación en el Sprint 1 de desarrollo (Ciclo 3)                                                                                                                                                                  |
| :----------------------- | :------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint**               | Ciclo de duración fija (1–4 semanas) que contiene todos los demás eventos. | Duración a definir según alcance del MVP v1.0. **Objetivo del Sprint (Sprint Goal):** desplegar el sistema en un entorno de prueba controlado, listo para ser usado por un grupo reducido de encargados de ventas. |
| **Sprint Planning**      | Reunión para planear qué construir en el Sprint actual.                    | El equipo selecciona del Product Backlog las funcionalidades del MVP v1.0, incorporando los ajustes de UX validados en el Ciclo 2.                                                                                 |
| **Daily Scrum**          | Reunión diaria de 15 min para coordinar al equipo.                         | Cada día, el equipo revisa el avance en el tablero Kanban e identifica bloqueos técnicos o de despliegue.                                                                                                          |
| **Sprint Review**        | Mostrar el resultado del Sprint al cliente o stakeholders.                 | Al cierre, se muestra el MVP v1.0 desplegado en entorno controlado a los stakeholders del proyecto.                                                                                                                |
| **Sprint Retrospective** | Mejorar cómo trabaja el equipo al cerrar cada Sprint.                      | El equipo identifica mejoras al proceso de desarrollo antes del Sprint del Ciclo 4 (MVP v2.0).                                                                                                                     |

### **4.2.2. Artefactos**

| Artefacto           | Descripción                                                                                                                                 | Contenido en este proyecto                                                                                                                                                                               |
| :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Product Backlog** | Lista ordenada y priorizada de todo lo que el sistema debe tener al finalizar el proyecto. Gestionado por el Product Owner.                 | Pipeline B2B, lógica de alertas, dashboard, ficha de cliente, modal de registro, panel gerencial y datos de prueba. Se actualiza entre ciclos con los aprendizajes validados.                            |
| **Sprint Backlog**  | Subconjunto del Product Backlog seleccionado en el Sprint Planning para el Sprint actual. Responsabilidad del **Development Team**.         | Para el primer Sprint de desarrollo (Ciclo 3): funcionalidades del MVP v1.0 con los ajustes de UX del Ciclo 2 incorporados.                                                                              |
| **Incremento**      | Resultado funcional del Sprint que cumple con el **Sprint Goal**. Cada incremento es una versión del sistema usable de forma independiente. | Resultado funcional y usable producido durante un Sprint. Incluye solo el trabajo que cumple la Definition of Done (DoD) y que puede formar parte de una versión potencialmente entregable del producto. |

## **4.3. Tablero Kanban del Sprint**

El tablero Kanban gestiona el flujo diario de tareas dentro de cada Sprint de desarrollo. Cada tarea avanza de izquierda a derecha por las columnas, con límites WIP que impiden acumular trabajo en progreso y hacen visibles los bloqueos el mismo día en que ocurren (Hammarberg & Sundén, 2014):

| 📋 Sprint Backlog                | 🔍 En diseño/análisis (WIP ≤ 5)  | ⚙️ En desarrollo (WIP ≤ 8)        | 🧪 En testing (WIP ≤ 5)       | ✅ Done                     |
| :------------------------------- | :------------------------------- | :-------------------------------- | :---------------------------- | :-------------------------- |
| _(tareas pendientes de iniciar)_ | _(ajustes UX, diseño de vistas)_ | _(desarrollo backend y frontend)_ | _(verificación de criterios)_ | _(tareas con DoD cumplida)_ |

**Definición de Done (DoD):** Una tarea alcanza la columna Done del tablero Kanban cuando está implementada en el sistema, verificada por Sofía contra sus criterios de aceptación y demostrada informalmente al equipo. Ninguna tarea puede avanzar a Done sin pasar por la columna de testing.

## **4.4. Historias de usuario y gestión de tareas**

- Para cada Sprint de desarrollo se definen **historias de usuario** que describen las funcionalidades desde la perspectiva del usuario final, y **tareas técnicas** derivadas de cada historia que el equipo ejecuta durante el Sprint.

- Cada historia se descompone en tareas concretas estimadas y asignadas a un integrante del Development Team.

- Las historias de usuario y sus tareas se registran y gestionan en **GitHub Projects**, que permite organizar el Product Backlog, el Sprint Backlog y el tablero Kanban en un mismo espacio. El equipo puede optar por otra herramienta de gestión ágil equivalente (como Trello, Jira o Linear) siempre que soporte la visibilidad del flujo y los límites WIP definidos en la sección 5.3.

## **4.5. Gestión de tareas incompletas y nuevos Sprints**

Si al finalizar un Sprint alguna tarea del Sprint Backlog no alcanzó el estado Done, se aplica el siguiente criterio:

- **Tareas bloqueadas o incompletas:** se devuelven al Product Backlog con una nota del motivo. El Product Owner decide si las reincorpora al siguiente Sprint o las reprioritiza.
- **Tareas parcialmente avanzadas:** se evalúan en la Sprint Retrospective. Si el avance es significativo y la tarea es crítica para el Sprint Goal, el Scrum Master puede proponer extender su ejecución al siguiente Sprint sin reiniciarla.
- **Sprint Goal no alcanzado:** si el incremento del Sprint no cumple con el Sprint Goal, el equipo no lo declara como incremento válido. Se planifica un nuevo Sprint para completarlo antes de avanzar al siguiente ciclo BML.

El equipo puede crear Sprints adicionales dentro de un ciclo BML si el alcance del MVP lo requiere. Cada Sprint adicional sigue el mismo proceso: Planning → Daily Scrum → Review → Retrospective, con su propio Sprint Backlog y tablero Kanban.
