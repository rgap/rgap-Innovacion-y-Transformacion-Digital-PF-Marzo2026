# **4. Marco de ejecución ágil: Scrum + Kanban**

Scrum y Kanban se aplican cuando el proyecto entra a una etapa de desarrollo de software. En este capítulo se describe su aplicación para construir el **MVP v1.0**, correspondiente al primer ciclo de desarrollo funcional. Posteriormente, el mismo marco podrá reutilizarse para el **MVP v2.0**, pero con un nuevo alcance, un nuevo Sprint Backlog y nuevos objetivos de Sprint. El Ciclo 1 (prototipo navegable de diseño), el Ciclo 2 (entrevistas y encuesta) y el Ciclo 5 (demo en video) no requieren Sprint formal (Kniberg, 2015; Hammarberg & Sundén, 2014).

Scrum provee la estructura temporal mediante Sprints, los roles y los eventos de coordinación. Kanban provee la visibilidad diaria del flujo de trabajo y los límites de trabajo en progreso (WIP) dentro de cada Sprint.

## **4.1. Equipo de trabajo — roles en el Sprint**

Cada integrante asume un rol de Scrum definido para la ejecución de los Sprints. La siguiente tabla describe las responsabilidades de cada uno durante el desarrollo del MVP v1.0.

| Rol Scrum            | Persona        | Separación de responsabilidades (separation of concerns)                          |
| :------------------- | :------------- | :-------------------------------------------------------------------------------- |
| **Product Owner**    | Rel Guzmán     | Define y prioriza las tareas del Sprint. Acepta los entregables al final.         |
| **Scrum Master**     | Carlos Mendoza | Facilita las reuniones. Elimina bloqueos del equipo.                              |
| **Development Team** | María Torres   | Diseño UX/UI del sistema, frontend y soporte en la implementación de vistas.      |
| **Development Team** | Luis Ramírez   | Desarrollo técnico del sistema: frontend, backend, base de datos y lógica.        |
| **Development Team** | Sofía Paredes  | Verificación de criterios de aceptación, testing, QA, y carga de datos de prueba. |

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

## **4.3. Tablero Kanban de los Sprints**

El tablero Kanban gestiona el flujo diario de tareas dentro de cada Sprint de desarrollo. Se encuentra publicado en [https://github.com/users/rgap/projects/24/views/2](https://github.com/rgap/Coolbox-B2B-WebApp)

Cada tarea avanza de izquierda a derecha por las columnas, con límites WIP que impiden acumular trabajo en progreso y hacen visibles los bloqueos el mismo día en que ocurren (Hammarberg & Sundén, 2014):

| 📋 Product Backlog                                       | 🔍 To Do (WIP ≤ 5)                                           | ⚙️ In Progress (WIP ≤ 3)                           | 🧪 Testing (WIP ≤ 3)                                  | ✅ Done                                |
| :------------------------------------------------------- | :----------------------------------------------------------- | :------------------------------------------------- | :---------------------------------------------------- | :------------------------------------- |
| _(historias o tareas priorizadas, aún fuera del Sprint)_ | _(tareas seleccionadas para el Sprint, listas para iniciar)_ | _(tareas en desarrollo backend, frontend o UX/UI)_ | _(verificación de criterios de aceptación y pruebas)_ | _(tareas terminadas con DoD cumplida)_ |

**Figura 1\. Tablero Kanban del Sprint 1 en GitHub Projects**

**![][image1]**

Esta imagen evidencia cómo Kanban se usa para visualizar el avance diario y detectar bloqueos dentro del Sprint.

**Figura 2\. Detalle de límites WIP y estados del tablero**

**![][image2]**

Esta evidencia permite justificar que el equipo no solo registra tareas, sino que controla la cantidad de trabajo simultáneo para evitar acumulación y pérdida de foco.

**Definición de Done (DoD):** Una tarea alcanza la columna Done del tablero Kanban cuando está implementada en el sistema, verificada por Sofía contra sus criterios de aceptación y demostrada informalmente al equipo. Ninguna tarea puede avanzar a Done sin pasar por la columna de testing.

## **4.4. Historias de usuario y gestión de tareas**

Para cada Sprint de desarrollo se definen **historias de usuario** que describen las funcionalidades desde la perspectiva del usuario final, y **tareas técnicas** derivadas de cada historia que el equipo ejecuta durante el Sprint.

**Figura 3\. Historia de usuario registrada para el MVP v1.0**

**![][image3]**

La tarjeta o issue incluye criterios de aceptación claros, tareas técnicas, estimación de esfuerzo y prioridad.

Cada historia se descompone en tareas concretas estimadas y asignadas a un integrante del Development Team.

**Figura 4\. Descomposición de la historia en tareas técnicas**

**![][image4]**

Las tareas técnicas conectan la necesidad del usuario con el trabajo concreto del Sprint.

Se agregan los miembros del equipo para asignar responsabilidades, distribuir tareas y dar seguimiento al avance de cada actividad durante el desarrollo del MVP.

**Figura 5\. Miembros del equipo agregados en GitHub Projects y en el repositorio de Github**

**![][image5]**

Con esto documentamos que el equipo fue incorporado dentro de la herramienta para facilitar la asignación de responsabilidades y la gestión de tareas del proyecto.

Las tareas registradas se asignan a los miembros del equipo según su rol y responsabilidad dentro del Sprint.

**Figura 6\. Asignación de tareas a los miembros del equipo en GitHub Projects**

**![][image6]**

Con esto documentamos que las tareas del proyecto son distribuidas entre los integrantes del equipo, permitiendo una mejor organización y control durante la construcción del MVP. Los issues que no aparecen en el tablero fueron archivadas temporalmente para visualizar solo los issues que se deben trabajar en el sprint actual.

## **4.5. Gestión de tareas incompletas y nuevos Sprints**

Si al finalizar un Sprint alguna tarea del Sprint Backlog no alcanzó el estado Done, se aplica el siguiente criterio:

- **Tareas bloqueadas o incompletas:** se devuelven al Product Backlog con una nota del motivo. El Product Owner decide si las reincorpora al siguiente Sprint o las reprioritiza.
- **Tareas parcialmente avanzadas:** se evalúan en la Sprint Retrospective. Si el avance es significativo y la tarea es crítica para el Sprint Goal, el Scrum Master puede proponer extender su ejecución al siguiente Sprint sin reiniciarla.
- **Sprint Goal no alcanzado:** si el incremento del Sprint no cumple con el Sprint Goal, el equipo no lo declara como incremento válido. Se planifica un nuevo Sprint o se reprioriza el alcance antes de cerrar el MVP v1.0.

El equipo puede crear Sprints adicionales si el alcance mínimo del MVP v1.0 no queda cubierto dentro de los 4 Sprints planificados. Cada Sprint adicional sigue el mismo proceso: Planning → Daily Scrum → Review → Retrospective, con su propio Sprint Backlog y tablero Kanban.
