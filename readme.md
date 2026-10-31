Trabajo Práctico Integrador (TPI) - RPB S.A. (Baggio)

Sistema de Gestión Integral Agroindustrial y Comercial

**Universidad Tecnológica Nacional (UTN)**

**Tecnicatura Universitaria en Programación a Distancia (TUPad)**

**Asignatura:** Organización Empresarial

**Alumno:** Marcos Joaquín Gallardo

**Cuerpo Docente:** Prof. Carolina Bruno, Prof. Francisco A. Varberde Thompson

**Ciclo Lectivo:** 2026

Enlaces Rápidos del Proyecto

**Repositorio Público GitHub:** <https://github.com/Markiitooz/tpi-organizacion-empresarial-baggio>

**Tablero Ágil GitHub Projects:** <https://github.com/users/Markiitooz/projects/1>

Descripción del Sistema

Este proyecto documenta y modela la arquitectura conceptual, organizativa y de software para la firma agroindustrial **RPB S.A. (Baggio)**. El sistema integra el control transaccional desde las fincas citrícolas y viñedos hasta el cliente final, conectando:

1. **Trazabilidad y Stock:** Seguimiento de lotes de materia prima desde origen, balanza de recepción y control bromatológico de calidad.

2. **Facturación Automatizada:** Integración vía API con ARCA (ex-AFIP) para emisión electrónica de comprobantes fiscalizados.

3. **Logística y Despacho:** Programación de rutas de entrega y generación de remitos oficiales.

4. **Sincronización Offline:** Resiliencia de datos en zonas rurales con conectividad deficiente mediante persistencia en búfer local.

5. **Atención Postventa con IA:** Chatbot inteligente integrado para respuesta ágil de consultas B2B/B2C en tiempo récord.

Estructura del Repositorio

.
├── README.md                          # Portada principal y documentación técnica (este archivo)
├── docs/
│   ├── Gallardo_Marcos_TPI_Final.pdf  # Documento Integrador Consolidado (Entregas 1, 2, 3 y 4)
│   ├── Entrega_1_TGS.pdf              # Sistema Abierto y Módulos
│   ├── Entrega_2_FODA_SDLC.pdf        # Matriz FODA, Objetivos y Diagrama de Gantt
│   └── Entrega_3_IRAM_Diccionario.pdf # Organigrama IRAM 34501 y Diccionario de Datos
├── diagrams/
│   ├── organigrama_iram34501.svg      # Estructura jerárquica formal de RPB S.A.
│   └── proceso_bpmn_integral.svg      # Modelo BPMN 2.0 del flujo transaccional
└── src/
    └── database_schema.sql            # Scripts DD/E-R de las entidades del sistema


Flujo de Trabajo en Git y GitFlow Auditado

El desarrollo del proyecto siguió las buenas prácticas de versionado y control colaborativo:

* **Estrategia de Ramificación:** Se mantuvo la rama `main` protegida, trabajando la incorporación de funcionalidades mediante ramas secundarias del tipo `feature/*`.

* **Historial de Commits Descriptivos:**

  ```
  $ git checkout -b feature/bpmn-and-offline-sync
  $ git add .
  $ git commit -m "feat(bpmn): implementar modelado BPMN 2.0 y logica de sincronizacion offline"
  $ git push origin feature/bpmn-and-offline-sync
  
  ```

* **Pull Request (PR) y Revisión de Pares:**

  * **PR #4:** *"Integración del Proceso BPMN 2.0 y Módulo de Resiliencia Offline"*

  * **Estado:** Aprobado y fusionado (`Squash & Merge`) en `main`.

Backlog Ágil e Historias de Usuario (GitHub Projects)

Las tareas del proyecto se administraron a través de un tablero Kanban interactivo estructurado en tres estados (*Por Hacer*, *En Progreso*, *Listo*):

| ID | Historia de Usuario (Formato Estándar) | Criterio de Aceptación | Estado | 
| ----- | ----- | ----- | ----- | 
| **HU-01** | **Como** analista de planta, **quiero** registrar lotes de materia prima en recepción, **para** garantizar la trazabilidad bromatológica desde la finca. | Registro completo en < 2 min con validación de estado bromatológico. | `Listo (Done)` | 
| **HU-02** | **Como** responsable administrativo, **quiero** facturar automáticamente con ARCA, **para** agilizar el despacho legal de mercancías. | Obtención del CAE fiscal válido en menos de 5 segundos por transacción. | `Listo (Done)` | 
| **HU-03** | **Como** cliente minorista, **quiero** consultar el estado de mi envío mediante un Bot de IA, **para** obtener respuesta inmediata las 24 horas. | Respuesta autónoma en < 30s para el 70% de las consultas frecuentes. | `En Progreso` | 
| **HU-04** | **Como** transportista, **quiero** registrar entregas offline en fincas rurales, **para** no perder datos por caídas de red móvil. | Almacenamiento local automático y sincronización transparente al reconectar. | `Listo (Done)` | 

Mecanismos de Control e Indicadores de Desempeño (KPIs)

1. **Reducción de Mermas de Stock:** Disminución $\ge 15\%$ en pérdidas de insumos en depósitos (Medición mensual).

2. **Automatización Fiscal ARCA:** Alcanzar un $90\%$ de facturas emitidas sin intervención manual (Medición diaria).

3. **Eficiencia Postventa Bot IA:** Resolutividad autónoma $\ge 70\%$ con un tiempo de respuesta $\text{KPI} < 30\text{s}$ (Medición semanal).

4. **Disponibilidad y Resiliencia (Uptime):** Operatividad continua del $99.5\%$ asegurando cero pérdida de datos offline (Medición continua).

Declaración de Transparencia en el Uso de Inteligencia Artificial

De acuerdo con las pautas de la cátedra de **Organización Empresarial (UTN TUP AD)**, se declara el uso reflexivo y crítico de herramientas de IA Generativa:

1. **Propósito de Uso:** Asistencia en el trazado vectorial SVG de diagramas (BPMN 2.0 y Organigrama IRAM), verificación sintáctica de tipos de datos para el Diccionario de Datos y corrección de estilo técnico académico.

2. **Control y Responsabilidad Intelectual:** Todas las salidas generadas fueron revisadas, corregidas y adaptadas críticamente por el estudiante. Se verificó la consistencia conceptual del caso real RPB S.A. (Baggio) eliminando alucinaciones o incongruencias operativas.