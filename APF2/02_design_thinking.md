# **2. Aplicación de Design Thinking**

Design Thinking es un proceso de innovación centrado en el ser humano que recorre cinco etapas iterativas: Empatizar, Definir, Idear, Prototipar y Testear (Riley, 2024). En este proyecto, las etapas de Prototipar y Testear se integran con el ciclo BML de Lean Startup (Bland & Osterwalder, 2019), de modo que el prototipo construido en Design Thinking es también el experimento de validación del MVP.

## **2.1. Equipo de trabajo**

Cada integrante del grupo asumió un rol específico según su especialidad. La siguiente tabla muestra cómo se distribuye la participación de cada uno a lo largo de las etapas de Design Thinking.

| Integrante         | Rol                                       | Etapas de Design Thinking                                                                                                  |
| :----------------- | :---------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| **Rel Guzmán**     | Product Owner / Innovation Lead           | Empatizar, Definir: facilita las actividades, sintetiza hallazgos del avance anterior y redacta el enunciado del problema. |
| **Carlos Mendoza** | Scrum Master / Jefe de Proyecto           | Todas: coordina la dinámica del equipo durante las sesiones de Design Thinking y gestiona tiempos y entregables.           |
| **María Torres**   | Diseñadora UX/UI                          | Idear, Prototipar: diseña la arquitectura de la información y los wireframes.                       |
| **Luis Ramírez**   | Tech Lead / CRM Specialist                | Idear, Prototipar: evalúa la viabilidad técnica de las soluciones y lidera el desarrollo del prototipo web.                |
| **Sofía Paredes**  | Diseñadora UX / Analista de Negocios / QA | Testear: diseña los criterios de éxito y verifica los resultados de las pruebas de usabilidad.                             |

---

## **2.2. Empatizar**

### **2.2.1. Resumen del proyecto / Contexto**

_Este análisis es un estudio simulado elaborado con fines académicos. La información sobre Coolbox proviene de fuentes públicas disponibles (sitio web institucional y canales corporativos). Los datos operativos, volúmenes y procesos internos descritos son supuestos informados, no datos reales de la empresa._

**Empresa:** Coolbox, empresa de retail especializado en tecnología (B2B y B2C), operada por Rash Perú S.R.L. Con más de 150 tiendas en Lima y provincias, y un canal corporativo B2B dedicado a empresas, instituciones y emprendimientos.

**Proceso analizado:** Ventas corporativas B2B, desde el primer contacto del cliente hasta el seguimiento post-venta.

**Problema central identificado en el avance anterior:** Los encargados de ventas corporativas gestionan entre 15 y 30 clientes corporativos de forma simultánea. Al no contar con un sistema de seguimiento automatizado, dependen de su memoria y de hojas de cálculo para recordar cuándo contactar a cada cliente después de una venta. Esto genera pérdida sistemática de oportunidades de recompra y up-selling, en especial en productos tecnológicos con ciclos de renovación predecibles (laptops, equipos de cómputo, cámaras de seguridad).

**Innovación propuesta:** Implementar alertas automáticas en un CRM B2B que notifiquen al encargado de ventas en el momento óptimo para contactar a cada cliente corporativo, calculadas en función de la vida útil estimada del producto adquirido.

### **2.2.2. Alcance del proyecto**

El alcance corresponde al desarrollo del **sistema completo de seguimiento post-venta corporativo** para Coolbox: una aplicación web propia que reemplaza el proceso manual actual con un sistema automatizado de alertas y gestión de clientes B2B. El sistema incluye:

| Incluido en el alcance                                                                                                       | Excluido del alcance                                          |
| :--------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------ |
| Pipeline de ventas B2B con etapas del proceso As-Is.                                                                         | Integración con ERP o sistema de facturación de Coolbox.      |
| Workflow automatizado de alertas: N días después del cierre de venta → tarea de seguimiento asignada al encargado de ventas. | Modelos de Inteligencia Artificial o Machine Learning.        |
| Dashboard del encargado de ventas con vista priorizada de alertas.                                                           | Envío automático de mensajes directos al cliente corporativo. |
| Ficha de cliente con historial de compras accesible desde cada alerta.                                                       | Limpieza de bases de datos históricas de clientes inactivos.  |
| Campo de ciclo de recompra editable por el encargado de ventas (default: 90 días).                                           | Dashboards gerenciales avanzados con análisis de cohortes.    |

### **2.2.3. Análisis comparativo de la competencia**

Se aplicó un ejercicio de **benchmarking** para identificar cómo distintos tipos de referentes gestionan el seguimiento post-venta en contextos B2B, y determinar qué prácticas son replicables para Coolbox. Los referentes se clasifican en tres categorías: **competidor directo** (mismo mercado y segmento), **competidor indirecto** (segmento adyacente o canal diferente) y **referente análogo** (industria distinta pero práctica comparable).

| Empresa / Referente                     | Tipo               | Herramienta de seguimiento                    | Mecanismo post-venta                                                                                                           | Fortaleza identificada                                                                            | Brecha respecto a Coolbox                                                                                      |
| :-------------------------------------- | :----------------- | :-------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------- |
| **Falabella Empresas**                  | Directo            | Salesforce CRM + equipo corporativo           | Correos automáticos de renovación y llamadas programadas por agentes especializados.                                           | Automatización escalable respaldada por equipo dedicado.                                          | Requiere inversión alta en licencias y personal; no replicable como _quick win_.                               |
| **Ripley Corporativo**                  | Directo            | CRM interno + gestión por ejecutivo de cuenta | El ejecutivo agenda manualmente el seguimiento en su calendario.                                                               | Atención personalizada con ejecutivo asignado.                                                    | Igual que Coolbox: depende de la memoria del ejecutivo; no sistematizado.                                      |
| **Ingram Micro Perú**                   | Indirecto          | Zoho CRM + automatización de tareas           | Flujos de correo automatizados según ciclo de vida del producto y alertas internas al representante.                           | Ciclos configurados por línea de producto; bajo costo operativo.                                  | Orientado a distribuidores, no a retailers multiproducto; requiere adaptación.                                 |
| **HubSpot**                             | Análogo            | HubSpot CRM (gratuito)                        | Workflows de tareas automáticas + dashboard de actividades del encargado de ventas.                                            | Referente directo de las funcionalidades que el sistema propio debe replicar.                     | No permite adaptar el flujo exacto al proceso de Coolbox sin configuraciones complejas.                        |
| **Coolbox (estado actual – As-Is)**     | Referente interno  | Excel / agendas manuales                      | Seguimiento reactivo: el encargado de ventas contacta al cliente solo cuando este lo solicita o cuando lo recuerda.            | Flexibilidad inmediata.                                                                           | Sin sistematización: alta dependencia de la memoria del encargado de ventas; pérdida estructural de recompras. |
| **Sistema propio (solución propuesta)** | Solución propuesta | Sistema web desarrollado por el equipo        | Dashboard de alertas + ficha de cliente + lógica de seguimiento automatizado, diseñados a medida del proceso As-Is de Coolbox. | Control total sobre el flujo, los datos y la experiencia de usuario; sin dependencia de terceros. | Requiere desarrollo propio; el equipo asume la carga técnica de construcción.                                  |

**Conclusión del benchmarking:** El seguimiento post-venta sistematizado es una práctica ya adoptada por competidores directos de mayor madurez digital (Falabella) e indirectos con buenas prácticas replicables (Ingram Micro). Ripley evidencia que el problema no es exclusivo de Coolbox. El referente análogo (HubSpot) valida la viabilidad técnica del mecanismo de alertas. Coolbox tiene la oportunidad de cerrar esa brecha con un sistema propio diseñado a la medida de su proceso, sin depender de plataformas de terceros.

---

## **2.3. Definir**

### **2.3.1. Proto personas**

Las proto personas son representaciones sintéticas de los usuarios principales del sistema, construidas a partir del análisis del proceso As-Is del avance anterior y el análisis comparativo de la competencia. A diferencia de una persona completa basada en investigación primaria extensa, la proto persona se basa en supuestos informados que serán validados en la etapa de testeo (Riley, 2024).

---

**Proto Persona 1**

**Nombre y apellido:** Diego Salas
**Rol / tipo de usuario:** Encargado de Ventas Corporativas B2B
**Descripción del rol:** Persona responsable de gestionar la cartera de clientes corporativos de Coolbox, desde el primer contacto hasta el cierre de la venta y el seguimiento post-venta.
**Puntos de dolor:** Atiende entre 15 y 30 clientes corporativos de forma simultánea sin una herramienta que le indique cuándo contactar a cada cliente. Pierde oportunidades de recompra por olvido. Cuando recuerda llamar, el cliente ya cotizó con la competencia.
**Necesidades:** Un sistema que le notifique automáticamente cuándo contactar a cada cliente, con el contexto suficiente (empresa, producto comprado, monto, fecha) para personalizar la llamada en menos de un minuto, sin necesidad de buscar información en otra pantalla.

---

**Proto Persona 2**

**Nombre y apellido:** Rosa Flores
**Rol / tipo de usuario:** Gerente Comercial B2B
**Descripción del rol:** Responsable de supervisar al equipo de encargados de ventas, establecer metas de ventas recurrentes y tomar decisiones sobre la cartera de clientes corporativos.
**Puntos de dolor:** No tiene visibilidad del estado de seguimiento de su equipo sin hacer reuniones o consultar a cada encargado de ventas de forma individual. Se entera de los clientes perdidos cuando ya es tarde.
**Necesidades:** Un panel centralizado que muestre en tiempo real cuántas alertas están vencidas sin acción, qué encargados de ventas están al día y cuál es la tasa de conversión de seguimientos a nuevas cotizaciones, filtrable por encargado de ventas y período.

---

## **2.4. Idear**

### **2.4.1. Arquitectura de la información**

La arquitectura de la información define la estructura y organización del sistema de seguimiento comercial propuesto para Coolbox. Establece qué vistas existen, cómo se relacionan y qué información reside en cada una. Esta arquitectura se basa en el análisis comparativo de la competencia y en las necesidades de los usuarios identificados en las proto personas.

```text
Vista: Dashboard del Encargado de Ventas
	Sección: Barra superior
		Nombre del encargado activo
		Ícono: Notificaciones
		Ícono: Ayuda
	Sección: Alertas de recompra activas
		Contador: Urgentes (vencidas o con vencimiento hoy) -> Vista: Ficha del cliente
		Contador: Próximas (1–7 días) -> Vista: Ficha del cliente
		Contador: En seguimiento (8–30 días) -> Vista: Ficha del cliente
		Tarjeta de alerta
			Nombre de la empresa
			Producto de la última compra
			Monto
			Días restantes
			Botón: Ver ficha -> Vista: Ficha del cliente
			Botón: Posponer
	Sección: Actividades del día
		Lista de llamadas pendientes

Vista: Ficha del cliente
	Enlace: Volver al Dashboard -> Vista: Dashboard del Encargado de Ventas
	Nombre de la empresa
	RUC
	Contacto principal
		Nombre
		Teléfono
	Encargado asignado
	Sección: Última compra
		Producto
		Cantidad
		Monto
		Fecha de cierre
		Campo editable: Ciclo de recompra (días)
		Fecha de alerta calculada
	Sección: Notas del encargado de ventas
		Texto libre editable
	Sección: Acciones
		Botón: Registrar contacto -> Modal: Registro de contacto
		Botón: Posponer (N días)
		Botón: Sin oportunidad actual

Modal: Registro de contacto
	Ícono: Cerrar modal
	Selector: Resultado del contacto
		Opción: Interesado en recompra
		Opción: No interesado actualmente
		Opción: No contestó
	Campo: Notas del contacto
	Campo editable: Fecha del próximo seguimiento (default: fecha actual + ciclo de recompra)
	Botón: Guardar y cerrar
	Botón: Cancelar

Vista: Clientes
	Sección: Barra superior
		Nombre del encargado activo
		Ícono: Notificaciones
		Ícono: Ayuda
	Sección: Listado de empresas
		Buscador
		Tarjeta de empresa
			Nombre
			RUC
			Encargado asignado
			Enlace: Ver ficha -> Vista: Ficha del cliente

Vista: Pipeline de Ventas B2B
	Sección: Barra superior
		Nombre del encargado activo
		Ícono: Notificaciones
		Ícono: Ayuda
	Sección: Tablero de etapas
		Columna: Prospecto
		Columna: Cotización enviada
		Columna: Evaluación crediticia
		Columna: Venta cerrada (activa el workflow de alerta automáticamente)
		Columna: Seguimiento activo
		Tarjeta de oportunidad
			Nombre de la empresa
			Monto
			Fecha estimada de cierre

Vista: Panel Gerencial
	Sección: Barra superior
		Nombre del gerente activo
		Ícono: Notificaciones
		Ícono: Ayuda
	Sección: Métricas del equipo
		Contador: Alertas vencidas sin acción
		Contador: Contactos realizados esta semana
		Indicador: Tasa de conversión seguimiento → nueva cotización
	Sección: Filtros
		Selector: Filtrar por encargado de ventas
		Selector: Filtrar por período
	Sección: Tabla de seguimiento
		Fila por encargado de ventas
			Nombre del encargado de ventas
			Alertas vencidas
			Contactos registrados
			Conversión
```

### **2.4.2. Diseño de interacción: Flujos de tareas**

Se definen los dos flujos de tarea principales que el sistema debe soportar para los usuarios identificados en las proto personas. El **Taskflow 1** representa el **happy path** del sistema: la ruta óptima y exitosa en la que el usuario completa su objetivo de principio a fin sin desvíos, errores ni decisiones alternativas. Es la base sobre la que se diseñan los wireframes. El Taskflow 2 describe el flujo del usuario secundario.

---

**Taskflow 1:** Revisión y acción sobre una alerta de recompra urgente _(Happy Path)_

**Rol / tipo de usuario:** Encargado de Ventas Corporativas B2B

**Objetivo del usuario dentro del sistema:** Identificar el cliente corporativo más urgente del día, revisar su contexto y registrar el resultado del contacto realizado sin desvíos ni errores

```text
1. Ingresa al CRM
2. Mira el Dashboard del Encargado de Ventas
3. Mira el widget "Alertas de recompra activas"
4. Identifica 2 alertas en rojo en el contador "Urgentes"
5. Hace clic en la tarjeta de la primera alerta urgente
6. Mira la Vista: Ficha del cliente
7. Lee el nombre de la empresa, el contacto, el producto, el monto y la fecha de la última compra
8. Realiza la llamada al cliente fuera del sistema
9. Hace clic en el botón "Registrar contacto"
10. Mira el Modal: Registro de contacto
11. Selecciona el resultado del contacto (ej. "Interesado en recompra")
12. Escribe una nota sobre la conversación
13. Confirma o edita la fecha del próximo seguimiento
14. Hace clic en "Guardar y cerrar"
15. Mira el Dashboard del Encargado de Ventas con la alerta cerrada y el contador actualizado
```

---

**Taskflow 2:** Supervisión del estado de seguimiento del equipo

**Rol / tipo de usuario:** Gerente Comercial B2B

**Objetivo del usuario dentro del sistema:** Revisar cuántas alertas están vencidas sin acción en el equipo y filtrar por encargado de ventas para identificar quién necesita seguimiento

```text
1. Ingresa al CRM
2. Hace clic en "Panel Gerencial" en la barra lateral
3. Mira la Vista: Panel Gerencial
4. Lee el contador de alertas vencidas sin acción (ej. 4 alertas)
5. Lee el contador de contactos realizados esta semana (ej. 12 contactos)
6. Lee el indicador de tasa de conversión (ej. 25%)
7. Selecciona un encargado de ventas en el filtro "Filtrar por encargado de ventas"
8. Mira la tabla de seguimiento filtrada por ese encargado de ventas
9. Identifica las 2 alertas vencidas sin registro de contacto del encargado de ventas seleccionado
10. Hace clic en una fila para ver el detalle del cliente sin contactar
11. Mira la Vista: Ficha del cliente
12. Agrega una nota interna dirigida al encargado de ventas
13. Vuelve al Panel Gerencial
```

---

## **2.5. Prototipar**

_Esta etapa se integra con la fase de Construir (Build) del ciclo Lean Startup. Los wireframes y los flujos representan el experimento mínimo de validación que el equipo construye para probar la hipótesis principal._

### **2.5.1. Wireframes de baja fidelidad**

Los wireframes describen la disposición visual de los elementos en cada pantalla clave, sin aplicar estilos ni colores. El objetivo es validar la estructura y jerarquía de la información antes de construir el sistema real.

---

**Wireframe 1: Dashboard del Encargado de Ventas (pantalla de inicio)**

```text
┌─────────────────────────────────────────────────────────┐
│ Sistema Coolbox B2B [Diego ▾] [🔔 3] [?] │
├───────────────┬─────────────────────────────────────────┤
│ │ │
│ MENÚ │ ALERTAS DE RECOMPRA ACTIVAS │
│ │ ┌──────────┬────────────┬────────────┐ │
│ 🏠 Dashboard │ │ 🔴 URGENTE│ 🟡 PRÓXIMO │ 🟢 SEGUIM.│ │
│ 👥 Clientes │ │ 2 │ 5 │ 12 │ │
│ 📊 Pipeline │ └──────────┴────────────┴────────────┘ │
│ ✅ Tareas │ │
│ 📈 Reportes │ ┌─────────────────────────────────────┐│
│ │ │ 🔴 Empresa ABC – vence hoy ││
│ │ │ Laptops HP (x10) · S/. 45,000 ││
│ │ │ [Ver ficha] [Posponer] ││
│ │ ├─────────────────────────────────────┤│
│ │ │ 🔴 Tech Solutions SAC – vence hoy ││
│ │ │ Cámaras Hikvision (x5) · S/8,500 ││
│ │ │ [Ver ficha] [Posponer] ││
│ │ └─────────────────────────────────────┘│
└───────────────┴─────────────────────────────────────────┘
```

---

**Wireframe 2: Ficha de alerta del cliente**

```text
┌─────────────────────────────────────────────────────────┐
│ ← Volver al Dashboard │
│ │
│ EMPRESA ABC S.A.C. RUC: 20XXXXXXX │
│ Contacto: Juan Quispe | 📞 987-XXX-XXX │
│ Encargado asignado: Diego │
├─────────────────────────────────────────────────────────┤
│ ÚLTIMA COMPRA │
│ Producto: Laptops HP EliteBook 840 (x10 unidades) │
│ Monto: S/. 45,000 │
│ Fecha: 14/02/2026 │
│ Ciclo de recompra: 90 días [Editar] │
│ Fecha de alerta: 15/05/2026 ← HOY │
├─────────────────────────────────────────────────────────┤
│ NOTAS DEL ENCARGADO │
│ "Empresa de contabilidad. Renuevan equipos por área. │
│ Próximamente área de RRHH podría necesitar tablets." │
├─────────────────────────────────────────────────────────┤
│ [✅ Registrar contacto] [⏰ Posponer 3 días] [✖ Sin oportunidad] │
└─────────────────────────────────────────────────────────┘
```

---

**Wireframe 3: Modal de registro de contacto**

```text
┌─────────────────────────────────────────┐
│ REGISTRAR CONTACTO: Empresa ABC │
│ │
│ Resultado: │
│ ◉ Interesado en recompra │
│ ○ No interesado actualmente │
│ ○ No contestó │
│ │
│ Notas del contacto: │
│ ┌─────────────────────────────────┐ │
│ │ Ej.: "Pidió cotización de │ │
│ │ tablets para junio" │ │
│ └─────────────────────────────────┘ │
│ │
│ Próximo seguimiento (auto: +90 días): │
│ 📅 13/08/2026 [Editar fecha] │
│ │
│ [Guardar y cerrar] [Cancelar] │
└─────────────────────────────────────────┘
```

## **2.6. Testear**

_En esta etapa se define el plan de pruebas: qué se va a evaluar, con quién y bajo qué criterios. La ejecución real de las pruebas y el registro de resultados ocurren durante la fase de Medir (Measure) del ciclo Lean Startup (sección 4.3), una vez que el prototipo está construido._

### **2.6.1. Plan de pruebas de usabilidad moderadas basadas en tareas**

Se diseñan pruebas moderadas en las que un integrante del equipo conduce cada sesión: presenta la tarea, observa, cronometra y aplica una pregunta de satisfacción al terminar, pero no interviene durante la ejecución de la tarea (Riley, 2024). El participante piensa en voz alta mientras avanza.

**Perfil de participantes:** 3 participantes con los perfiles de las proto personas (2 encargados de ventas con distinta experiencia, 1 gerente comercial).

**Moderador:** Sofía Paredes (Diseñadora UX / Analista de Negocios / QA).

**Métricas fijas aplicadas en cada tarea:**

| Métrica                              | Descripción                                                                                | Instrumento                             |
| :----------------------------------- | :----------------------------------------------------------------------------------------- | :-------------------------------------- |
| **Completación del flujo sin ayuda** | El participante llega al final de la tarea sin solicitar ayuda al moderador.               | Observación directa                     |
| **Tiempo de tarea**                  | Tiempo desde que el participante lee la instrucción hasta que declara la tarea completada. | Cronómetro del moderador                |
| **Satisfacción del usuario**         | Pregunta post-tarea: _"¿Qué tan fácil fue completar esta tarea?"_ (escala 1–5).            | Encuesta oral aplicada por el moderador |

---

**Tarea 1: Gestión de alerta urgente**
Participante: Diego Salas (encargado de ventas con experiencia)

> _"Es lunes por la mañana. Abre el sistema y encuentra cuál es el cliente más urgente al que debes contactar hoy. Luego registra que lo llamaste y que está interesado en una nueva cotización."_

| Métrica                          | Criterio de éxito                                                      |
| :------------------------------- | :--------------------------------------------------------------------- |
| Completación del flujo sin ayuda | Completa la tarea de principio a fin sin solicitar ayuda al moderador. |
| Tiempo de tarea                  | ≤ 3 minutos.                                                           |
| Satisfacción del usuario         | Puntaje ≥ 4 / 5.                                                       |

---

**Tarea 2: Identificación y registro de contacto fallido**
Participante: Valeria (encargada de ventas nueva, 3 meses en el puesto)

> _"Sin que nadie te explique nada, encuentra cuándo debes contactar por primera vez a la empresa 'Tech Solutions SAC' y registra que intentaste llamarlos pero no contestaron."_

| Métrica                          | Criterio de éxito                                                      |
| :------------------------------- | :--------------------------------------------------------------------- |
| Completación del flujo sin ayuda | Completa la tarea de principio a fin sin solicitar ayuda al moderador. |
| Tiempo de tarea                  | ≤ 3 minutos.                                                           |
| Satisfacción del usuario         | Puntaje ≥ 4 / 5.                                                       |

---

**Tarea 3: Supervisión del equipo desde el panel gerencial**
Participante: Rosa Flores (gerente comercial)

> _"Necesitas saber cuántas alertas de recompra lleva vencidas sin contacto tu equipo esta semana. Encuentra esa información en el sistema."_

| Métrica                          | Criterio de éxito                                                      |
| :------------------------------- | :--------------------------------------------------------------------- |
| Completación del flujo sin ayuda | Completa la tarea de principio a fin sin solicitar ayuda al moderador. |
| Tiempo de tarea                  | ≤ 3 minutos.                                                           |
| Satisfacción del usuario         | Puntaje ≥ 4 / 5.                                                       |
