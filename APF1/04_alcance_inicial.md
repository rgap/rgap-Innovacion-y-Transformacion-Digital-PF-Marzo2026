# **4\. Alcance inicial del proyecto**

El alcance se delimita a la implementación y configuración de una plataforma **CRM B2B en la nube**, enfocada específicamente en resolver la fricción del seguimiento post-venta. A través de la adopción de herramientas de **Automatización de Procesos (Workflows)**, el proyecto se centrará en configurar reglas de negocio que calculen automáticamente la fecha óptima de reabastecimiento o renovación de los clientes corporativos. El entregable principal será un ecosistema capaz de generar **alertas proactivas** que notifiquen al equipo de ventas de manera automática en el momento exacto en que se presente una oportunidad de recompra o *up-selling*.

### **Limitaciones del proyecto**

Para asegurar que esta iniciativa se mantenga como un *Quick win* de rápida ejecución, el proyecto excluye explícitamente lo siguiente en esta fase inicial:

| Limitación (Fuera del alcance) | Justificación operativa |
| :--- | :--- |
| **Integración con ERP o Facturación** | El CRM funcionará de forma aislada para la gestión comercial. Conectar bases de datos financieras requeriría un esfuerzo técnico extenso que retrasa la salida a producción. |
| **Modelos de Inteligencia Artificial (IA)** | Las alertas se activarán por fórmulas matemáticas simples y fijas (ej. Compra + 90 días). No se implementará *Machine Learning* para ajustar dinámicamente estos tiempos de consumo. |
| **Contacto directo automático al cliente** | Las notificaciones llegarán de forma interna a los asesores. No se automatizará el envío de correos o mensajes directos al cliente para mantener la personalización B2B. |
| **Depuración histórica masiva** | No se realizará una limpieza exhaustiva de bases de datos de clientes inactivos de años anteriores; el enfoque será sobre clientes activos recientes y nuevas ventas. |