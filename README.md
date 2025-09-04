# 🚀 BeePayroll - Sistema de Facturación SaaS

## 📋 Resumen del Proyecto

Sistema dual de facturación para BeePayroll que incluye una vista cliente (SaaS) y una vista administrativa (ERP) con flujo de pago SPEI simplificado y cálculo automático de IVA.

## 🎯 Arquitectura de Funcionalidades

### Epic 1: Usuario SaaS Cliente
**"Como cliente de BeePayroll, quiero gestionar mi suscripción y pagos de manera transparente y sencilla"**

### Epic 2: Admin ERP  
**"Como administrador de BeePayroll, quiero gestionar eficientemente todos los clientes SaaS y sus facturaciones"**

---

## 📋 **EPIC 1: Usuario SaaS Cliente**

### **💰 Gestión de Facturación**

#### **JTBD-001**: Visualización de Resumen de Facturación
**Job to be Done**: Cuando necesito revisar mi facturación mensual, quiero ver un resumen claro del ciclo actual con desglose completo (empleados, servicios, IVA) para entender exactamente qué estoy pagando.

**User Story**: 
> Como cliente de BeePayroll, quiero acceder a un resumen detallado de mi facturación actual para revisar todos los cargos del periodo y planificar mi presupuesto mensual.

**Descripción**: 
El cliente puede ver en tiempo real su resumen de facturación que incluye: plan actual, costo por empleados activos, servicios adicionales contratados, créditos y prorrateos aplicados, subtotal, IVA (16%) y total a pagar. La información se presenta en un formato card con desglose visual claro y montos destacados.

---

#### **JTBD-002**: Proceso de Pago SPEI Simplificado
**Job to be Done**: Cuando llega mi fecha de pago, quiero un proceso SPEI simplificado con concepto único y botones "copiar" para realizar mi transferencia sin errores.

**User Story**: 
> Como cliente que debe realizar un pago, quiero un modal de transferencia SPEI con datos bancarios claros y concepto único para completar mi pago sin confusiones.

**Descripción**: 
Modal rediseñado que elimina la confusión de múltiples pestañas y presenta un flujo único: Cuenta CLABE, Beneficiario (ESSAD), Banco Destino (BBVA), y Concepto de Pago (obligatorio, formato ESS + 6 dígitos). Cada campo tiene botón "Copiar" y banner amarillo explicativo sobre la importancia del concepto.

---

#### **JTBD-003**: Acceso a Historial de Facturas
**Job to be Done**: Cuando necesito comprobantes fiscales, quiero acceder fácilmente a mi historial de facturas y poder descargar los PDF correspondientes.

**User Story**: 
> Como cliente que necesita comprobantes, quiero consultar mi historial de facturas con filtros de fecha y estatus para encontrar y descargar los documentos fiscales requeridos.

**Descripción**: 
Tabla de historial que muestra ID de factura, periodo facturado, monto total (con IVA), estatus (Pagada/Pendiente) y acción de descarga. Los montos se muestran con IVA incluido y se puede filtrar por diferentes criterios temporales.

---

#### **JTBD-004**: Sistema de Recordatorios de Pago
**Job to be Done**: Cuando se acerca mi fecha de pago, quiero recibir recordatorios amigables que me motiven a pagar a tiempo sin presión.

**User Story**: 
> Como cliente activo, quiero recibir recordatorios de pago oportunos y amigables que me permitan mantener mi servicio activo sin interrupciones.

**Descripción**: 
Sistema de modales de recordatorio con dos tipos: "3 días antes del vencimiento" con tono amigable (💙 Seguimos contigo) y "pago vencido" con información clara sobre consecuencias. Incluye botones de acción inmediata y opción de postergar.

---

### **🔄 Gestión de Planes**

#### **JTBD-005**: Comparación de Planes Disponibles
**Job to be Done**: Cuando mi negocio crece, quiero comparar planes disponibles y entender qué funcionalidades obtendré con cada uno antes de decidir.

**User Story**: 
> Como empresario en crecimiento, quiero comparar visualmente los diferentes planes (Starter, Growth, Enterprise) para elegir el que mejor se adapte a mis necesidades actuales y futuras.

**Descripción**: 
Sección "Gestionar Plan" con cards comparativas que muestran precio por empleado/mes, funcionalidades incluidas por plan, y indicador visual del plan actual. Diseño en formato de tarjetas delgadas y altas para fácil comparación lado a lado.

---

#### **JTBD-006**: Proceso de Cambio de Plan Informado
**Job to be Done**: Cuando decido cambiar de plan, quiero confirmación clara de las reglas (upgrade inmediato vs downgrade al siguiente ciclo) para evitar sorpresas.

**User Story**: 
> Como cliente que quiere cambiar de plan, quiero entender exactamente cuándo se aplicará el cambio y cómo afectará mi facturación actual y futura.

**Descripción**: 
Modal de confirmación que explica claramente: upgrades se aplican inmediatamente con facturación prorrateada, downgrades se aplican al siguiente ciclo. Incluye banner informativo sobre fecha de aplicación de cambios (ej: "1 de octubre de 2025").

---

#### **JTBD-007**: Flexibilidad de Facturación Mensual/Anual
**Job to be Done**: Cuando evalúo costos, quiero toggle entre precios mensuales y anuales para elegir la opción más conveniente.

**User Story**: 
> Como cliente consciente de costos, quiero ver las opciones de pago mensual y anual con descuentos aplicables para optimizar mi inversión en la plataforma.

**Descripción**: 
Switch "Mensual/Anual" en la sección de gestión de planes que actualiza dinámicamente los precios mostrados. Los precios anuales incluyen descuentos y se actualiza automáticamente el cálculo por empleado/mes o empleado/año.

---

### **🛍️ Servicios Adicionales**

#### **JTBD-008**: Exploración de Servicios Especializados
**Job to be Done**: Cuando necesito servicios especializados, quiero explorar opciones disponibles con descripciones detalladas y precios claros.

**User Story**: 
> Como cliente con necesidades específicas, quiero explorar servicios adicionales (Soporte, Legal, Fiscal, Integraciones, App, Multicompañía) para complementar mi plan base.

**Descripción**: 
Matriz de cards de servicios con imagen, título, descripción corta, precio "desde $X" y botón "Ver Detalles". Cada servicio incluye descripción larga (300+ caracteres) con beneficios específicos y casos de uso detallados.

---

#### **JTBD-009**: Solicitud de Demos Personalizadas
**Job to be Done**: Cuando me interesa un servicio, quiero solicitar una demo personalizada para evaluar si se ajusta a mis necesidades.

**User Story**: 
> Como prospecto de servicio adicional, quiero solicitar una demostración personalizada para entender mejor cómo el servicio resolverá mis necesidades específicas.

**Descripción**: 
Modal de detalles de servicio con imagen (40% width), descripción larga, y botón "Solicitar Demo" que conecta directamente con el equipo de ventas. Incluye mensaje informativo sobre el proceso de contacto y tiempos de respuesta.

---

### **📊 Transparencia Financiera**

#### **JTBD-010**: Comprensión de Reglas de Facturación
**Job to be Done**: Cuando reviso mi facturación, quiero entender las reglas de cobro para anticipar futuros cargos y planificar mi presupuesto.

**User Story**: 
> Como cliente informado, quiero acceder a las reglas de facturación detalladas para entender cómo se calculan mis cargos y planificar mejor mis finanzas.

**Descripción**: 
Modal "Reglas de Facturación" accesible desde ícono "?" que explica en 8 puntos: cálculo de periodos, definición de trabajador facturable, políticas de suspensión, aplicación de créditos, facturación de servicios adicionales, timing de cambios de plan, generación automática de facturas, y canales de soporte.

---

#### **JTBD-011**: Tracking de Créditos y Ajustes
**Job to be Done**: Cuando hay cambios en mi equipo, quiero ver cómo los créditos y prorrateos afectan mi facturación total.

**User Story**: 
> Como cliente con plantilla variable, quiero entender cómo las bajas de empleados durante el periodo se reflejan como créditos en mi facturación para optimizar mis costos.

**Descripción**: 
Sección dedicada en el resumen que muestra "Créditos y prorrateos" con montos negativos (descuentos) claramente identificados en color verde. Explica automáticamente cuando hay bajas de trabajadores y cómo se calculan los ajustes proporcionales.

---

## 📋 **EPIC 2: Admin ERP**

### **👥 Gestión de Clientes**

#### **JTBD-012**: Lista Filtrable de Clientes SaaS
**Job to be Done**: Cuando administro múltiples clientes, quiero una lista filtrable por estatus, fecha de pago y estatus de pago para priorizar mi atención.

**User Story**: 
> Como administrador ERP, quiero una vista consolidada de todos los clientes SaaS con filtros avanzados para gestionar eficientemente la cartera y priorizar acciones.

**Descripción**: 
Tabla de clientes con columnas: Nombre comercial, RFC, Correo, Teléfono, Estatus (Activo/Suspendido), Fecha de pago, Referencia bancaria, y Estatus de pago (Pagada/Pendiente). Incluye filtros por cada columna y rango de fechas para identificar rápidamente problemas de cobranza.

---

#### **JTBD-013**: Control de Acceso de Clientes
**Job to be Done**: Cuando un cliente incumple pagos, quiero suspender/activar su acceso con confirmaciones de seguridad para proteger los ingresos.

**User Story**: 
> Como administrador de cuentas, quiero controlar el acceso de clientes morosos mediante suspensión/activación con confirmaciones de seguridad para proteger los ingresos de la empresa.

**Descripción**: 
Controles de suspensión/activación con modales de confirmación que incluyen checkboxes obligatorios: "Avisé al cliente de la suspensión" y "Confirmo que deseo impedir su acceso". Para activación: confirmación de reactivación y recomendación de actualizar facturas pagadas.

---

#### **JTBD-014**: Perfil Completo de Cliente
**Job to be Done**: Cuando necesito información completa de un cliente, quiero ver su perfil detallado con historial, plan actual y servicios contratados en una sola vista.

**User Story**: 
> Como gestor de cuentas, quiero acceder al perfil completo de cada cliente para revisar su información, plan actual, historial de movimientos y estado de facturación en una vista consolidada.

**Descripción**: 
Vista de detalle del cliente que incluye: información básica, referencia única, controles de estado, información del plan con funcionalidades, historial de movimientos de plan paginado, resumen del ciclo actual editable, historial de facturas con carga de ZIP, y controles de cierre de ciclo.

---

#### **JTBD-015**: Referencias Bancarias Únicas
**Job to be Done**: Cuando gestiono pagos bancarios, quiero asignar referencias únicas por cliente para identificar transferencias fácilmente.

**User Story**: 
> Como responsable de conciliación bancaria, quiero que cada cliente tenga una referencia única visible para identificar rápidamente sus transferencias SPEI.

**Descripción**: 
Cada cliente tiene una referencia única (formato REF + 9 dígitos) visible en su detalle y en la lista de clientes. Esta referencia facilita la identificación de transferencias bancarias y está separada del concepto de pago por factura individual.

---

### **💳 Control de Facturación**

#### **JTBD-016**: Validación y Cierre de Ciclos
**Job to be Done**: Cuando termina un ciclo de facturación, quiero validar y cerrar el periodo generando automáticamente la factura con concepto SPEI único.

**User Story**: 
> Como responsable de facturación, quiero validar los cargos del ciclo actual y cerrar formalmente el periodo para generar la factura correspondiente con concepto de pago único.

**Descripción**: 
Control de cierre de ciclo con checkbox de validación obligatorio que permite revisar: fechas del ciclo, empleados activos, servicios habilitados, ajustes aplicados, y total con IVA. Al cerrar se genera automáticamente factura "Pendiente" con concepto SPEI único (ESS + 6 dígitos).

---

#### **JTBD-017**: Generación de Conceptos SPEI Únicos
**Job to be Done**: Cuando los clientes realizan pagos SPEI, quiero que el sistema genere conceptos únicos que faciliten la conciliación bancaria.

**User Story**: 
> Como administrador financiero, quiero que cada factura tenga un concepto de pago único generado automáticamente para simplificar la conciliación bancaria y eliminar errores de identificación.

**Descripción**: 
Sistema automático que genera conceptos únicos (formato ESS + 6 dígitos aleatorios) al cerrar cada ciclo. Incluye modal de ayuda "?" que explica el proceso de generación, propósito del concepto, uso obligatorio en transferencias, y alineación con estándares SPEI mexicanos.

---

#### **JTBD-018**: Gestión de Comprobantes Fiscales
**Job to be Done**: Cuando recibo comprobantes fiscales, quiero cargar los archivos ZIP y marcar automáticamente las facturas como pagadas.

**User Story**: 
> Como responsable de documentación fiscal, quiero cargar archivos ZIP de facturas (PDF + XML) y que el sistema marque automáticamente las facturas como pagadas para mantener el control actualizado.

**Descripción**: 
Sistema de carga de archivos ZIP por factura individual con validación de formato. Al cargar exitosamente, la factura cambia automáticamente de "Pendiente" a "Pagada", se actualiza el estatus en todas las vistas, y se habilita la opción "Reemplazar factura ZIP" para futuras actualizaciones.

---

#### **JTBD-019**: Precios Promocionales Flexibles
**Job to be Done**: Cuando ofrezco promociones, quiero ajustar precios por empleado independientemente del plan estándar.

**User Story**: 
> Como gerente comercial, quiero aplicar precios promocionales por empleado a clientes específicos sin cambiar su plan base para manejar descuentos y ofertas especiales.

**Descripción**: 
Campo editable "Precio por empleado" en el detalle del cliente que permite establecer tarifas diferentes al plan estándar. Cuando el precio es menor al estándar, se muestra un banner de advertencia indicando descuento aplicado. Recalcula automáticamente totales proyectados.

---

### **🔧 Administración de Servicios**

#### **JTBD-020**: Confirmación de Entrega de Servicios
**Job to be Done**: Cuando confirmo la entrega de servicios adicionales, quiero habilitar el cobro con evidencia de la sesión proporcionada.

**User Story**: 
> Como responsable de servicios, quiero confirmar que se proporcionó correctamente un servicio adicional al cliente antes de habilitar su cobro en la facturación.

**Descripción**: 
Switch de habilitación por servicio que requiere confirmación modal: "Confirmo que se proporcionó este servicio al usuario satisfactoriamente". Incluye campo opcional para link de grabación de la sesión como evidencia. Banner azul explica que habilitar confirma entrega y autoriza cobro.

---

#### **JTBD-021**: Gestión de Evidencias de Servicio
**Job to be Done**: Cuando grabo sesiones de servicios, quiero vincular las grabaciones como comprobante de entrega del servicio.

**User Story**: 
> Como prestador de servicios especializados, quiero vincular grabaciones de sesiones como evidencia de la entrega del servicio para tener respaldo documental del trabajo realizado.

**Descripción**: 
Campo "Link de grabación del servicio" en el modal de confirmación que puede ser marcado como opcional mediante checkbox. Una vez guardado el link, aparece botón "Ver sesión" que abre la grabación en nueva pestaña. Sirve como evidencia para auditorías y disputas.

---

#### **JTBD-022**: Ajuste de Costos por Inclusión en Plan
**Job to be Done**: Cuando los servicios están incluidos en el plan, quiero ajustar costos a cero sin eliminar el servicio del sistema.

**User Story**: 
> Como administrador de precios, quiero establecer costo cero para servicios que están incluidos en el plan del cliente sin perder la trazabilidad del servicio en el sistema.

**Descripción**: 
Campos editables de costo por servicio que permiten establecer valor cero cuando el servicio está incluido en el plan base. Al establecer $0, el sistema muestra mensaje "incluido en el plan" y recalcula automáticamente los totales proyectados sin afectar la estructura de servicios.

---

### **📈 Monitoreo y Reporting**

#### **JTBD-023**: Supervisión de Ingresos por Cobranza
**Job to be Done**: Cuando necesito supervisar ingresos, quiero filtrar clientes por estatus de pago y fechas para identificar problemas de cobranza.

**User Story**: 
> Como responsable financiero, quiero identificar rápidamente clientes con pagos pendientes o vencidos para tomar acciones proactivas de cobranza y proteger el flujo de caja.

**Descripción**: 
Sistema de filtros avanzados que permite segmentar clientes por: estatus de pago (Pagada/Pendiente), rango de fechas de vencimiento, y estado del cliente (Activo/Suspendido). Los resultados se actualizan en tiempo real y permiten acciones masivas sobre los clientes filtrados.

---

#### **JTBD-024**: Análisis de Comportamiento de Clientes
**Job to be Done**: Cuando analizo comportamiento de clientes, quiero ver el historial completo de cambios de plan para identificar patrones.

**User Story**: 
> Como analista de negocio, quiero revisar el historial de movimientos de plan de cada cliente para identificar patrones de crecimiento, rotación y oportunidades de upselling.

**Descripción**: 
Tabla "Historial de Movimientos de Plan" paginada que muestra: fecha del cambio, plan origen, plan destino, tipo (upgrade/downgrade), fecha efectiva, y estatus. Ordenada por fecha más reciente y permite identificar tendencias de crecimiento o contracción por cliente.

---

#### **JTBD-025**: Navegación Eficiente de Grandes Volúmenes
**Job to be Done**: Cuando manejo grandes volúmenes de datos, quiero paginación y ordenamiento en todas las tablas para navegar eficientemente.

**User Story**: 
> Como usuario del sistema ERP, quiero navegar eficientemente por grandes cantidades de datos mediante paginación y ordenamiento para encontrar rápidamente la información que necesito.

**Descripción**: 
Sistema de paginación estándar implementado en todas las tablas (clientes, facturas, movimientos de plan) con controles de navegación, indicadores de página actual/total, y opción de ordenamiento por columnas relevantes (fecha, monto, nombre, etc.).

---

#### **JTBD-026**: Reportes Fiscales Precisos
**Job to be Done**: Cuando genero reportes financieros, quiero datos precisos con IVA incluido y desgloses detallados para cumplir con regulaciones fiscales.

**User Story**: 
> Como responsable fiscal, quiero generar reportes financieros con cálculos precisos de IVA (16%) y desgloses detallados para cumplir con las obligaciones fiscales mexicanas.

**Descripción**: 
Todos los montos del sistema incluyen cálculo automático de IVA al 16%. Los reportes muestran: subtotal, IVA desglosado, y total final. Las facturas generadas incluyen ambos campos (subtotal para cálculos internos y total con IVA para presentación al cliente) asegurando precisión fiscal.

---

## 🔗 **Interconexiones Clave del Sistema**

### **SPEI Simplificado**
- **Cliente** (JTBD-002): Proceso simplificado de pago
- **Admin** (JTBD-016/017): Generación de conceptos únicos
- **Resultado**: Flujo de pago infalible alineado con bancos mexicanos

### **Transparencia Financiera**
- **Cliente** (JTBD-001/010): Comprensión clara de cargos
- **Admin** (JTBD-019/022): Control flexible de precios
- **Resultado**: Confianza mutua y gestión transparente

### **Gestión de Servicios**
- **Cliente** (JTBD-008/009): Exploración y solicitud de servicios
- **Admin** (JTBD-020/021): Confirmación y evidencia de entrega
- **Resultado**: Ciclo completo de venta y entrega de servicios

### **Control de Acceso**
- **Cliente** (JTBD-004): Recordatorios amigables de pago
- **Admin** (JTBD-013): Control de suspensión por mora
- **Resultado**: Protección de ingresos con experiencia positiva

---

## 🛠️ **Tecnologías Utilizadas**

- **Frontend**: HTML5, Tailwind CSS, Vanilla JavaScript
- **Diseño**: Responsive design con tema dual (cliente/admin)
- **Funcionalidades**: Modales dinámicos, filtros avanzados, paginación
- **Cálculos**: IVA automático (16%), totales con desglose
- **UX/UI**: Flujo SPEI simplificado, confirmaciones de seguridad

---

## 📊 **Métricas Clave del Sistema**

- **26 Jobs to be Done** implementados
- **2 Epics principales** (Cliente SaaS + Admin ERP)
- **11 Modales interactivos** para diferentes flujos
- **Flujo SPEI único** eliminando confusión de referencia/concepto
- **Cálculo automático de IVA** en todos los precios
- **Sistema de filtros avanzados** para gestión eficiente
- **Paginación completa** para grandes volúmenes de datos

---

## 🚀 **Instalación y Uso**

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/edcas/pantalla-de-factura-mensual.git
   cd pantalla-de-factura-mensual
   ```

2. **Abrir el archivo**:
   ```bash
   open index.html
   ```

3. **Navegación**:
   - **Vista Cliente**: Gestión de facturación, planes y servicios
   - **Vista Admin**: Switch en la barra superior para acceder al ERP
   - **Simulaciones**: Botones de testing para modales de pago

---

## 📝 **Notas de Implementación**

- **IVA**: Tasa fija del 16% aplicada automáticamente
- **SPEI**: Conceptos únicos formato ESS + 6 dígitos
- **Referencias**: Formato REF + 9 dígitos por cliente
- **Facturas**: Soporte para subtotal y total con IVA
- **Temas**: Cliente (claro) y Admin (oscuro) diferenciados
- **Responsive**: Optimizado para desktop y mobile

---

*Desarrollado para ESSAD - BeePayroll System* 🐝
