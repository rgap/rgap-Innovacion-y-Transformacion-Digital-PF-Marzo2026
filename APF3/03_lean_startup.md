# **3. Aplicación de Lean Startup**

Lean Startup estructura la validación de la solución propuesta a través del ciclo **Build → Measure → Learn**, priorizando el aprendizaje rápido sobre la construcción perfecta (Bland & Osterwalder, 2019). La etapa de Construir se ejecuta con el equipo organizado en un Sprint de Scrum (Kniberg, 2015), gestionado con un tablero Kanban (Hammarberg & Sundén, 2014) (ver sección 5). Las etapas de Medir y Aprender completan el ciclo de validación.

## **3.1. Equipo de trabajo**

La siguiente tabla muestra cómo cada integrante del equipo participa en las fases del ciclo BML según su rol.

| Integrante         | Rol                                       | Fase del ciclo BML                                                                                                                                                                    |
| :----------------- | :---------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Rel Guzmán**     | Product Owner / Innovation Lead           | Preparación: formula las hipótesis y define los criterios de éxito a partir de los hallazgos de Design Thinking. Learn: lidera la revisión de aprendizajes y la decisión de producto. |
| **Carlos Mendoza** | Scrum Master / Jefe de Proyecto           | Build: facilita el Sprint, elimina bloqueos y garantiza el cumplimiento de las ceremonias Scrum.                                                                                      |
| **María Torres**   | Diseñadora UX/UI                          | Build: diseña e implementa el dashboard y la ficha del cliente en el prototipo web.                                                                                                   |
| **Luis Ramírez**   | Tech Lead / CRM Specialist                | Build: lidera el desarrollo técnico del prototipo web: backend, base de datos y lógica de alertas automáticas.                                                                        |
| **Sofía Paredes**  | Diseñadora UX / Analista de Negocios / QA | Build / Measure: prepara los datos de prueba y verifica los criterios de aceptación.                                                                                                  |

Este documento describe el **Ciclo 1** del proceso de validación. La planificación de los ciclos futuros se presenta al final en la sección 4.5.4.

---

## **3.2. Preparación**

### **3.2.1. Contexto del problema**

A partir de las etapas de Empatizar y Definir de Design Thinking, se consolidó el siguiente contexto del problema que motiva el experimento de validación:

**Empresa:** Coolbox, canal de ventas corporativas B2B.

**Problema validado:** El encargado de ventas no tiene un mecanismo sistematizado para saber cuándo contactar a un cliente corporativo tras una venta. La dependencia de la memoria y de hojas de cálculo genera pérdida estructural de oportunidades de recompra. La fricción es humana, no técnica: el encargado de ventas _quiere_ hacer el seguimiento, pero su volumen de cuentas lo hace imposible manualmente.

**Oportunidad:** Desarrollar un prototipo web con alertas automáticas basadas en la vida útil del producto vendido transformaría el proceso comercial de reactivo a proactivo, sin requerir un cambio conductual profundo en el encargado de ventas (el sistema trabaja por él).

### **3.2.2. Proto persona**

_(Ver sección 3.3, Design Thinking, para el detalle completo de las proto personas.)_

**Usuario principal del experimento:** Diego Salas, Encargado de Ventas Corporativas, gestiona entre 15 y 30 clientes corporativos, nunca ha utilizado un sistema de seguimiento comercial.

**Usuario secundario:** Rosa Flores, Gerente Comercial, necesita visibilidad del estado de seguimiento del equipo sin depender de consultas individuales a cada integrante.

### **3.2.3. Hipótesis de validación**

**Hipótesis 1:**

**Creemos que** Diego Salas
**tiene el problema de** perder oportunidades de recompra porque no recuerda cuándo contactar a sus clientes corporativos después de una venta
**y que** recibir una alerta automática en el sistema con la ficha de contexto del cliente en el momento exacto
**le ayudará a** realizar el seguimiento post-venta de forma proactiva sin depender de su memoria ni de hojas de cálculo.

**Hipótesis 2:**

**Creemos que** Rosa Flores
**tiene el problema de** no saber qué clientes están siendo atendidos y cuáles están siendo ignorados por su equipo sin hacer reuniones individuales
**y que** contar con un panel centralizado que muestre en tiempo real las alertas vencidas sin acción por encargado de ventas
**le ayudará a** supervisar el seguimiento comercial de su equipo y tomar decisiones correctivas antes de perder al cliente.

### **3.2.4. Plan de experimento**

| Elemento                | Detalle                                                                                                                                           |
| :---------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Tipo de experimento** | Prototipo web navegable desarrollado por el equipo (demo funcional).                                                                              |
| **Duración**            | 2 semanas (Sprint 1, ejecutado con Scrum + Kanban).                                                                                               |
| **Participantes**       | 3 perfiles simulados: Diego (encargado de ventas con experiencia), Valeria (encargada de ventas nueva), Rosa (gerente comercial).                 |
| **Escenario de prueba** | 5 oportunidades de venta simuladas. 2 de ellas tienen alerta activa durante la sesión. El moderador presenta cada tarea y observa sin intervenir. |

### **3.2.5. Criterios de éxito**

| # | Métrica | Condición de éxito |
| :--- | :--- | :--- |
| 1 | Completación del flujo sin ayuda | Al menos 2 de 3 participantes completan su tarea sin solicitar ayuda al moderador. |
| 2 | Tiempo de tarea | Tiempo promedio entre los 3 participantes ≤ 3 minutos por tarea. |
| 3 | Satisfacción del usuario | Puntaje promedio ≥ 4 / 5 en la encuesta de satisfacción post-tarea. |

---

## **3.3. Construir (Build)**

_Solo los ciclos con MVPs (Ciclos 3 y 4) requieren un Sprint de Scrum para su construcción. El prototipo navegable (Ciclo 1) es un artefacto de diseño y no requiere desarrollo de software ni Sprint. Los artefactos ligeros (entrevistas, encuestas, demo en video) tampoco requieren Sprint. El detalle del Sprint y el tablero Kanban se describe en la sección 5._

El **artefacto mínimo de validación** es lo que el equipo construye en cada ciclo BML para responder la pregunta de validación con el menor esfuerzo posible. No tiene una forma fija: dependiendo del ciclo y de lo que se quiere aprender, puede tomar distintas formas:

| Tipo de artefacto     | Cuándo usarlo                                                                      |
| :-------------------- | :--------------------------------------------------------------------------------- |
| Prototipo navegable   | Cuando se quiere validar usabilidad antes de construir el sistema real.            |
| Entrevista / Encuesta | Cuando se quiere entender percepciones, actitudes o intenciones del usuario.       |
| MVP v1.0              | Primera versión funcional desplegada en entorno de prueba controlado, lista para ser usada por un grupo reducido de encargados de ventas.               |
| MVP v2.0              | Versión mejorada con ajustes derivados de la medición del MVP anterior.            |
| Demo en video         | Cuando se quiere comunicar el valor del sistema a stakeholders de forma eficiente. |

Para evitar confusiones, en este proyecto se diferencia entre artefactos mínimos de validación y MVP funcional. Los artefactos mínimos de validación pueden incluir entrevistas, encuestas, demos en video o prototipos navegables, mientras que el MVP funcional se entiende como una primera versión desarrollada del sistema, construida mediante uno o más Sprints de Scrum y desplegada inicialmente en un entorno de prueba controlado.

Lo que se construye en cada ciclo queda definido en la sección 4.6 (Planificación de ciclos BML).

### **3.3.1. Artefacto mínimo de validación del Ciclo 1**

Para el Ciclo 1, el artefacto es un **prototipo navegable de diseño**: un conjunto de pantallas interactivas que simulan el flujo del sistema sin ejecutar lógica real de backend. Se construye con herramientas de prototipado (no con desarrollo de software) y permite probar la usabilidad del flujo antes de construir el sistema real.

| Componente | Descripción | Responsable |
| :--- | :--- | :--- |
| Pantallas de alta fidelidad | Diseño visual de todas las vistas definidas en la arquitectura de información: dashboard, ficha del cliente, modal de registro y panel gerencial. | María Torres (Diseñadora UX/UI) |
| Flujo de navegación interactivo | Vínculos entre pantallas que permiten recorrer el Taskflow 1 (happy path) y el Taskflow 2 sin intervención del diseñador. | María Torres (Diseñadora UX/UI) |
| Datos estáticos para la demo | Nombres de empresas, montos, fechas y alertas representativas cargados como contenido fijo en el prototipo para simular un escenario real. | Sofía Paredes (Diseñadora UX / Analista de Negocios / QA) |
| Criterios de prueba | Definición de las 3 tareas y métricas que se aplicarán en las sesiones moderadas de la fase Medir. | Sofía Paredes (Diseñadora UX / Analista de Negocios / QA) |

### **3.3.2. Métricas a observar**

| Métrica | Cómo se mide | Fuente |
| :--- | :--- | :--- |
| Completación del flujo sin ayuda | El moderador anota si el participante completó la tarea sin pedir ayuda (Sí / No). | Observación directa |
| Tiempo de tarea | Tiempo transcurrido desde que el participante lee la instrucción hasta que declara la tarea completada. | Cronómetro del moderador |
| Satisfacción del usuario | Respuesta oral a: *"¿Qué tan fácil fue completar esta tarea?"* (escala 1–5), aplicada al terminar cada tarea. | Encuesta oral |

---

## **3.4. Medir (Measure)**

_En esta fase se ejecutan las pruebas de usabilidad definidas en la sección 3.5 (Testear de Design Thinking) sobre el prototipo construido en el Build. Los resultados se contrastan con los criterios de éxito definidos en la sección 4.2.5._

### **3.4.1. Ejecución de las pruebas de usabilidad**

**Tarea 1: Gestión de alerta urgente — Diego Salas**

> _"Es lunes por la mañana. Abre el sistema y encuentra cuál es el cliente más urgente al que debes contactar hoy. Luego registra que lo llamaste y que está interesado en una nueva cotización."_

| Métrica                          | Resultado                                                                              | Estado |
| :------------------------------- | :------------------------------------------------------------------------------------- | :----- |
| Completación del flujo sin ayuda | Completó el flujo completo sin solicitar ayuda. Llegó a la ficha en 1 clic vía widget. | ✅     |
| Tiempo de tarea                  | 1 min 50 seg                                                                           | ✅     |
| Satisfacción del usuario         | 5 / 5                                                                                  | ✅     |

---

**Tarea 2: Identificación y registro de contacto fallido — Valeria**

> _"Sin que nadie te explique nada, encuentra cuándo debes contactar por primera vez a la empresa 'Tech Solutions SAC' y registra que intentaste llamarlos pero no contestaron."_

| Métrica                          | Resultado                                                                                                               | Estado |
| :------------------------------- | :---------------------------------------------------------------------------------------------------------------------- | :----- |
| Completación del flujo sin ayuda | Completó la tarea sin solicitar ayuda, aunque necesitó 5 clics porque el widget usaba solo color sin etiqueta de texto. | ⚠️     |
| Tiempo de tarea                  | 2 min 55 seg                                                                                                            | ✅     |
| Satisfacción del usuario         | 4 / 5                                                                                                                   | ✅     |

**Hallazgo:** El color sin etiqueta no comunica urgencia a usuarios nuevos. **Corrección:** Agregar etiqueta textual "Urgente / Próximo / En seguimiento" junto al indicador de color.

---

**Tarea 3: Supervisión del equipo desde el panel gerencial — Rosa Flores**

> _"Necesitas saber cuántas alertas de recompra lleva vencidas sin contacto tu equipo esta semana. Encuentra esa información en el sistema."_

| Métrica                          | Resultado                                                                                                                | Estado |
| :------------------------------- | :----------------------------------------------------------------------------------------------------------------------- | :----- |
| Completación del flujo sin ayuda | No encontró el Panel Gerencial sin ayuda; solicitó orientación al moderador para ubicarlo dentro del submenú "Reportes". | ❌     |
| Tiempo de tarea                  | 4 min 05 seg (incluyendo la intervención del moderador)                                                                  | ❌     |
| Satisfacción del usuario         | 4 / 5                                                                                                                    | ✅     |

**Hallazgo:** El Panel Gerencial es difícil de encontrar. **Corrección:** Agregar acceso directo en la barra lateral principal, visible en todo momento.

---

### **3.4.2. Resultados comparados con los criterios de éxito del Ciclo 1**

| Métrica | Condición de éxito | Resultado | Estado |
| :--- | :--- | :--- | :--- |
| Completación del flujo sin ayuda | ≥ 2 / 3 sin solicitar ayuda | 2 / 3 (Diego y Valeria; Rosa solicitó ayuda) | ✅ Cumplido |
| Tiempo de tarea | Promedio ≤ 3 min | Promedio: 2 min 57 seg | ✅ Cumplido |
| Satisfacción del usuario | Promedio ≥ 4 / 5 | 4.3 / 5 (Diego: 5, Valeria: 4, Rosa: 4) | ✅ Cumplido |

### **3.4.3. Resumen de hallazgos de usabilidad**

| #   | Hallazgo                                                          | Severidad | Corrección propuesta                                        |
| :-- | :---------------------------------------------------------------- | :-------- | :---------------------------------------------------------- |
| 1   | El color sin etiqueta no comunica urgencia a usuarios nuevos.     | Alta      | Agregar etiqueta textual junto al indicador de color.       |
| 2   | El Panel Gerencial está oculto dentro del submenú "Reportes".     | Alta      | Agregar acceso directo en la barra lateral principal.       |
| 3   | El botón "Sin oportunidad" generó confusión (¿borra al cliente?). | Media     | Renombrar a "Sin oportunidad actual" + tooltip explicativo. |

**Conclusión del Ciclo 1:** El concepto central (alerta con ficha de contexto) es intuitivo y valorado por los usuarios. Los tres hallazgos son de usabilidad superficial (etiquetas, accesos, nomenclatura), no de concepto. La solución avanza al siguiente ciclo con ajustes de UX definidos.

---

## **3.5. Aprender (Learn)**

### **3.5.1. Informe de aprendizaje validado: Ciclo 1**

**Aprendizajes clave:**

1. **El mecanismo técnico es confiable.** Los 5 workflows se activaron en la fecha exacta. La lógica de alertas automáticas del prototipo web funciona correctamente con los datos de prueba cargados.

2. **La ficha de contexto resuelve el problema de preparación.** Los tres participantes revisaron la ficha del cliente en menos de 60 segundos y confirmaron que la información presentada es suficiente para hacer la llamada sin buscar datos en otra pantalla.

3. **El color sin etiqueta no es suficiente para usuarios nuevos.** Valeria no identificó el significado de los colores del widget hasta leer el nombre del cliente. Se necesita etiqueta textual junto al indicador de color.

### **3.5.2. Conclusiones sobre las hipótesis**

| Hipótesis                                                                | Conclusión del Ciclo 1                                                                                                                                              |
| :----------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Hipótesis 1** (alertas automáticas → seguimiento proactivo de Diego)   | **Validada en entorno simulado.** El mecanismo funciona y Diego la valoró con 5/5. La tasa de contacto real se medirá en ciclos futuros con usuarios en producción. |
| **Hipótesis 2** (panel centralizado → supervisión sin reuniones de Rosa) | **Parcialmente validada.** Rosa encontró el panel y leyó las métricas sin problemas, pero el acceso estaba oculto. Se ajusta el menú antes del siguiente ciclo.     |

### **3.5.3. Decisión de producto**

| Dimensión                                                  | Decisión       | Acción para el siguiente ciclo                                 |
| :--------------------------------------------------------- | :------------- | :------------------------------------------------------------- |
| Concepto central (alertas automáticas en el prototipo web) | **Perseverar** | El concepto es válido. Continuar con el mismo enfoque.         |
| Indicador de urgencia (color sin etiqueta)                 | **Ajustar**    | Agregar etiqueta textual "Urgente / Próximo / En seguimiento". |
| Acceso al Panel Gerencial (oculto en "Reportes")           | **Ajustar**    | Mover acceso a la barra lateral principal.                     |

---

## **3.6. Planificación de ciclos BML**

Cada ciclo del proceso Construir → Medir → Aprender emplea un artefacto mínimo de validación distinto, elegido según la pregunta que se busca responder en ese momento del proyecto.

### **3.6.1. Descripción de MVPs por ciclo**

Los MVPs son las versiones desarrolladas del sistema. El MVP v1.0 se despliega en un entorno de prueba controlado; el MVP v2.0 avanza hacia un entorno con mayor alcance según los aprendizajes del ciclo anterior. Los demás ciclos (Ciclos 1, 2 y 5) emplean artefactos mínimos de validación más ligeros que no constituyen un MVP.

**MVP v1.0 (Ciclo 3):** Primera versión del sistema desplegada en un entorno de prueba controlado. Se construye en uno o más Sprints e incorpora los ajustes de UX validados en el Ciclo 2. Permite medir el impacto inicial del sistema con un grupo reducido de encargados de ventas de Coolbox.

**MVP v2.0 (Ciclo 4):** Segunda versión del sistema, construida en Sprints adicionales, con mejoras derivadas del Ciclo 3: ciclos de recompra diferenciados por categoría de producto, acceso directo al Panel Gerencial y ajustes adicionales de usabilidad.

### **3.6.2. Tabla de ciclos BML**

| Ciclo | Artefacto mínimo de validación | Objetivo de validación | Requiere Sprint | Estado |
| :--- | :--- | :--- | :--- | :--- |
| **Ciclo 1** | Prototipo navegable | Validar que el flujo es comprensible y usable antes de construir el sistema real. | No | ✅ Completado |
| **Ciclo 2** | Entrevistas + Encuesta | Validar que los ajustes de UX del Ciclo 1 resuelven los problemas de usabilidad con usuarios reales. | No | 🔜 Planificado |
| **Ciclo 3** | MVP v1.0 | Medir el impacto inicial del sistema con un grupo reducido de encargados de ventas en entorno de prueba controlado. | Sí | 🔜 Planificado |
| **Ciclo 4** | MVP v2.0 | Validar que las mejoras incrementales aumentan el uso diario y reducen alertas sin acción. | Sí | 🔜 Planificado |
| **Ciclo 5** | Demo en video | Validar la percepción de valor del sistema ante los stakeholders del proyecto. | No | 🔜 Planificado |
