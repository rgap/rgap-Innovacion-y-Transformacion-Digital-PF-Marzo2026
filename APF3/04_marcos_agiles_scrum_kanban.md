# **4. Marco de ejecución ágil: Scrum + Kanban**

Scrum y Kanban se aplican cuando el proyecto entra a una etapa de desarrollo de software. En este capítulo se describe su aplicación para construir el **MVP v1.0**, correspondiente al primer ciclo de desarrollo funcional. Posteriormente, el mismo marco podrá reutilizarse para el **MVP v2.0**, pero con un nuevo alcance, un nuevo Sprint Backlog y nuevos objetivos de Sprint. El Ciclo 1 (prototipo navegable de diseño), el Ciclo 2 (entrevistas y encuesta) y el Ciclo 5 (demo en video) no requieren Sprint formal (Kniberg, 2015; Hammarberg & Sundén, 2014).

Scrum provee la estructura temporal mediante Sprints, los roles y los eventos de coordinación. Kanban provee la visibilidad diaria del flujo de trabajo y los límites de trabajo en progreso (WIP) dentro de cada Sprint.

## **4.1. Equipo de trabajo — roles en el Sprint**

Cada integrante asume un rol de Scrum definido para la ejecución de los Sprints. La siguiente tabla describe las responsabilidades de cada uno durante el desarrollo del MVP v1.0.

| Rol Scrum            | Persona        | Separación de responsabilidades (separation of concerns)                     |
| :------------------- | :------------- | :--------------------------------------------------------------------------- |
| **Product Owner**    | Rel Guzmán     | Define y prioriza las tareas del Sprint. Acepta los entregables al final.    |
| **Scrum Master**     | Carlos Mendoza | Facilita las reuniones. Elimina bloqueos del equipo.                         |
| **Development Team** | María Torres   | Diseño UX/UI del sistema y soporte en la implementación de vistas.           |
| **Development Team** | Luis Ramírez   | Desarrollo técnico del sistema: backend, base de datos y lógica de alertas.  |
| **Development Team** | Sofía Paredes  | Verificación de criterios de aceptación, testing y carga de datos de prueba. |

## **4.2. Eventos y artefactos de Scrum**

### **4.2.1. Eventos**

Los eventos Scrum se aplican en cada Sprint necesario para construir un MVP funcional. En este apartado se detallan para el desarrollo del **MVP v1.0**; cuando se desarrolle el MVP v2.0 se repetirá el mismo marco de trabajo, pero con un backlog y objetivos propios.

| Evento                   | Descripción general                                                        | Aplicación en el desarrollo del MVP v1.0 (Ciclo 3)                                                                                                                                                           |
| :----------------------- | :------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint**               | Ciclo de duración fija (1–4 semanas) que contiene todos los demás eventos. | El MVP v1.0 se desarrolla en **4 Sprints de 1 semana cada uno**. **Objetivo general:** construir una versión básica para registrar clientes, consultar clientes existentes y visualizar alertas de recompra. |
| **Sprint Planning**      | Reunión para planear qué construir en el Sprint actual.                    | El equipo selecciona del Product Backlog las funcionalidades del MVP v1.0, incorporando los ajustes de UX validados en el Ciclo 2.                                                                           |
| **Daily Scrum**          | Reunión diaria de 15 min para coordinar al equipo.                         | Cada día, el equipo revisa el avance en el tablero Kanban e identifica bloqueos técnicos o de despliegue.                                                                                                    |
| **Sprint Review**        | Mostrar el resultado del Sprint al cliente o stakeholders.                 | Al cierre de cada Sprint se muestra el incremento parcial; al finalizar el Sprint 4 se presenta el MVP v1.0 básico desplegado en entorno controlado.                                                         |
| **Sprint Retrospective** | Mejorar cómo trabaja el equipo al cerrar cada Sprint.                      | El equipo identifica mejoras al proceso de desarrollo para aplicarlas en el siguiente Sprint del MVP v1.0. Al finalizar el Sprint 4, los aprendizajes quedan como insumo para una versión posterior.         |

### **4.2.2. Artefactos**

| Artefacto           | Descripción                                                                                                                                 | Contenido en este proyecto                                                                                                                                                                                                         |
| :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Product Backlog** | Lista ordenada y priorizada de todo lo que el sistema debe tener al finalizar el proyecto. Gestionado por el Product Owner.                 | Para el MVP v1.0 se priorizan registro básico de clientes, lista de clientes, ficha básica, alertas de recompra y datos de prueba. Funcionalidades como registro de contactos y panel gerencial quedan para versiones posteriores. |
| **Sprint Backlog**  | Subconjunto del Product Backlog seleccionado en el Sprint Planning para el Sprint actual. Responsabilidad del **Development Team**.         | Para cada Sprint del MVP v1.0 se seleccionan funcionalidades del alcance definido, organizadas dentro de un plan de 4 Sprints de 1 semana.                                                                                         |
| **Incremento**      | Resultado funcional del Sprint que cumple con el **Sprint Goal**. Cada incremento es una versión del sistema usable de forma independiente. | Resultado funcional y usable producido durante un Sprint. Incluye solo el trabajo que cumple la Definition of Done (DoD) y que puede formar parte de una versión potencialmente entregable del producto.                           |

### **4.2.3. MVP v1.0 a desarrollar**

El **MVP v1.0** es una versión simple del sistema de seguimiento post-venta B2B para Coolbox. Se desarrolla en **4 Sprints de 1 semana cada uno** y se enfoca únicamente en el registro de clientes y la generación de alertas de recompra.

**Funcionalidades incluidas en el MVP v1.0:**

- Registro básico de clientes.
- Lista básica de clientes.
- Ficha básica del cliente.
- Lista de alertas de recompra.
- Datos de prueba con clientes existentes y compras anteriores.

**Resultado esperado:** Al final de los 4 Sprints debe existir una versión básica donde se puedan registrar clientes, ver clientes existentes y visualizar alertas de recompra.

El **registro de contactos no se incluye en esta versión**. Esa funcionalidad queda planificada para el MVP v2.0 o para un Sprint posterior al cierre del MVP v1.0.

## **4.3. Tablero Kanban de los Sprints**

El tablero Kanban gestiona el flujo diario de tareas dentro de cada Sprint de desarrollo. Cada tarea avanza de izquierda a derecha por las columnas, con límites WIP que impiden acumular trabajo en progreso y hacen visibles los bloqueos el mismo día en que ocurren (Hammarberg & Sundén, 2014):

| 📋 Product Backlog                                       | 🔍 To Do / Sprint Backlog (WIP ≤ 5)                          | ⚙️ In Progress (WIP ≤ 3)                           | 🧪 Testing (WIP ≤ 3)                                  | ✅ Done                                |
| :------------------------------------------------------- | :----------------------------------------------------------- | :------------------------------------------------- | :---------------------------------------------------- | :------------------------------------- |
| _(historias o tareas priorizadas, aún fuera del Sprint)_ | _(tareas seleccionadas para el Sprint, listas para iniciar)_ | _(tareas en desarrollo backend, frontend o UX/UI)_ | _(verificación de criterios de aceptación y pruebas)_ | _(tareas terminadas con DoD cumplida)_ |

**Figura 4.1. Tablero Kanban del Sprint 1 en GitHub Projects**

![Captura del tablero Kanban del Sprint 1 con las columnas Product Backlog, To Do / Sprint Backlog, In Progress, Testing y Done](./imagenes/04_01_tablero_kanban_sprint1.png)

**Descripción:** La captura debe mostrar la vista tipo tablero de **GitHub Projects** configurada para el Sprint 1 de desarrollo del MVP v1.0. Deben verse las columnas del flujo de trabajo definidas para el proyecto, desde el Product Backlog hasta Done, junto con las tarjetas distribuidas según su estado. Esta imagen evidencia cómo Kanban se usa para visualizar el avance diario y detectar bloqueos dentro del Sprint.

**Figura 4.2. Detalle de límites WIP y estados del tablero**

![Captura del tablero Kanban con límites WIP visibles y tarjetas agrupadas por estado](./imagenes/04_02_limites_wip_tablero.png)

**Descripción:** La captura debe enfocar la configuración operativa del tablero, mostrando los estados del flujo y los límites de trabajo en progreso: **To Do / Sprint Backlog (WIP ≤ 5)**, **In Progress (WIP ≤ 3)** y **Testing (WIP ≤ 3)**. Esta evidencia permite justificar que el equipo no solo registra tareas, sino que controla la cantidad de trabajo simultáneo para evitar acumulación y pérdida de foco.

**Definición de Done (DoD):** Una tarea alcanza la columna Done del tablero Kanban cuando está implementada en el sistema, verificada por Sofía contra sus criterios de aceptación y demostrada informalmente al equipo. Ninguna tarea puede avanzar a Done sin pasar por la columna de testing.

## **4.4. Historias de usuario y gestión de tareas**

- Para cada Sprint de desarrollo se definen **historias de usuario** que describen las funcionalidades desde la perspectiva del usuario final, y **tareas técnicas** derivadas de cada historia que el equipo ejecuta durante el Sprint.

**Figura 4.3. Historia de usuario registrada para el MVP v1.0**

![Captura de una historia de usuario en GitHub Projects o GitHub Issues con criterios de aceptación](./imagenes/04_03_historia_usuario_mvp1.png)

**Descripción:** La captura debe mostrar una historia de usuario priorizada del Sprint, por ejemplo: _"Como encargado de ventas corporativas, quiero recibir una alerta automática cuando un cliente esté cerca de su fecha estimada de recompra, para identificar oportunamente una nueva oportunidad comercial"_. La tarjeta o issue debe incluir criterios de aceptación claros, como visualización de alerta, acceso a la ficha básica del cliente y consulta de la compra anterior asociada.

- Cada historia se descompone en tareas concretas estimadas y asignadas a un integrante del Development Team.

**Figura 4.4. Descomposición de la historia en tareas técnicas**

![Captura de las tareas técnicas derivadas de una historia de usuario y asignadas al equipo](./imagenes/04_04_tareas_tecnicas_historia.png)

**Descripción:** La captura debe mostrar cómo una historia de usuario se divide en tareas ejecutables, estimadas y asignadas a integrantes del Development Team. Por ejemplo: diseño de la lista de alertas, creación de datos de prueba, implementación de la lógica de fechas, desarrollo de la ficha básica del cliente y validación de criterios de aceptación. Esta imagen conecta la necesidad del usuario con el trabajo concreto del Sprint.

- Las historias de usuario y sus tareas se registran y gestionan en **GitHub Projects**, que permite organizar el Product Backlog, el Sprint Backlog y el tablero Kanban en un mismo espacio.

**Figura 4.5. Gestión integrada de historias y tareas en GitHub Projects**

![Captura de GitHub Projects con historias de usuario, tareas técnicas, responsables y estados de avance](./imagenes/04_05_github_projects_historias_tareas.png)

**Descripción:** La captura debe mostrar la vista general de **GitHub Projects** donde se gestionan conjuntamente el Product Backlog, el Sprint Backlog y el tablero Kanban. Deben apreciarse las tarjetas con responsables, estado, prioridad o Sprint asociado. Esta evidencia documenta que el equipo utiliza una herramienta centralizada para dar seguimiento a las historias de usuario y tareas durante la construcción del MVP.

## **4.5. Gestión de tareas incompletas y nuevos Sprints**

Si al finalizar un Sprint alguna tarea del Sprint Backlog no alcanzó el estado Done, se aplica el siguiente criterio:

- **Tareas bloqueadas o incompletas:** se devuelven al Product Backlog con una nota del motivo. El Product Owner decide si las reincorpora al siguiente Sprint o las reprioritiza.
- **Tareas parcialmente avanzadas:** se evalúan en la Sprint Retrospective. Si el avance es significativo y la tarea es crítica para el Sprint Goal, el Scrum Master puede proponer extender su ejecución al siguiente Sprint sin reiniciarla.
- **Sprint Goal no alcanzado:** si el incremento del Sprint no cumple con el Sprint Goal, el equipo no lo declara como incremento válido. Se planifica un nuevo Sprint o se reprioriza el alcance antes de cerrar el MVP v1.0.

El equipo puede crear Sprints adicionales si el alcance mínimo del MVP v1.0 no queda cubierto dentro de los 4 Sprints planificados. Cada Sprint adicional sigue el mismo proceso: Planning → Daily Scrum → Review → Retrospective, con su propio Sprint Backlog y tablero Kanban.
