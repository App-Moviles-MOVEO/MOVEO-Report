# MOVEO-Report

<p align="center">
    <strong>Universidad Peruana de Ciencias Aplicadas</strong><br>
    <img src="https://upload.wikimedia.org/wikipedia/commons/f/fc/UPC_logo_transparente.png"></img><br>
    <strong>Ingeniería de Software</strong><br>
    <strong>CICLO 2026-10</strong><br>
    <strong>Aplicaciones para Dispositivos Móviles</strong><br>
    <strong>3678</strong><br>
    <strong>Profesor: David Gerardo Quevedo Velasco</strong><br>
    <strong>Startup:</strong><br>
    <strong>Producto: </strong><br>
    <strong>INFORME DE TRABAJO FINAL</strong><br>
    <strong>AGOSTO 2026</strong><br>
</p>

## Relación de integrantes
| Integrante                              | Código         |
|-----------------------------------------|----------------|
| Barba Estrada, Bryan Eduardo            | U202323479     |
| Cotrina Siclla, Sofia Alessandra        | U20231B120     |
| Encalada Salazar, Alexis                | U20211G491     |
| Goñe Araccata, Esther Abigail           | U202318049     |
| Salazar Caballero, Alvaro Fabrizzio     | U202321941     |



# Registro de Versiones del Informe

| Versión | Fecha | Autor(es)  |  Descripción de Modificación |
|---------|-------|------------|------------------------------|


# Project Report Collaboration Insights 

# Contenido

[Student Outcome (ver anexo A)](#student-outcome-ver-anexo-a)

[Objetivos SMART](#objetivos-smart)

# Capítulo I: Presentación

[1.1. Startup Profile](#11-startup-profile)

[1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)

[1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)

[1.2. Solution Profile](#12-solution-profile)

[1.2.1. Antecedentes y problemática](#121-antecedentes-y-problemática)

[1.2.2. Lean UX Process](#122-lean-ux-process)

[1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)

[1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)

[1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)

[1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)

[1.3. Segmentos objetivo](#13-segmentos-objetivo)

# Capítulo II: Requirements Development and Software Solution Design

[2.1. Competidores](#21-competidores)

[2.1.1. Análisis competitivo](#211-análisis-competitivo)

[2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)

[2.2. Entrevistas](#22-entrevistas)

[2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)

[2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)

[2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)

[2.3. Needfinding](#23-needfinding)

[2.3.1. User Personas](#231-user-personas)

[2.3.2. User Task Matrix](#232-user-task-matrix)

[2.3.3. User Journey Mapping](#233-user-journey-mapping)

[2.3.4. Empathy Mapping](#234-empathy-mapping)

[2.3.5. Big Picture EventStorming](#235-big-picture-eventstorming)

[2.3.6. Ubiquitous Language](#236-ubiquitous-language)

[2.4. Requirements specification](#24-requirements-specification)

[2.4.1. User Stories](#241-user-stories)

[2.4.2. Impact Mapping](#242-impact-mapping)

[2.4.3. Product Backlog](#243-product-backlog)

[2.5. Strategic-Level Domain-Driven Design](#25-strategic-level-domain-driven-design)

[2.5.1. EventStorming](#251-eventstorming)

[2.5.1.1. Candidate Context Discovery](#2511-candidate-context-discovery)

[2.5.1.2. Domain Message Flows Modeling](#2512-domain-message-flows-modeling)

[2.5.1.3. Bounded Context Canvases](#2513-bounded-context-canvases)

[2.5.2. Context Mapping](#252-context-mapping)

[2.5.3. Software Architecture](#253-software-architecture)

[2.5.3.1. Software Architecture Context Level Diagrams](#2531-software-architecture-context-level-diagrams)

[2.5.3.2. Software Architecture Container Level Diagrams](#2532-software-architecture-container-level-diagrams)

[2.5.3.3. Software Architecture Deployment Diagrams](#2533-software-architecture-deployment-diagrams)

[2.6. Tactical-Level Domain-Driven Design](#26-tactical-level-domain-driven-design)

[2.6.1. Bounded Context: Identity & Access Management (IAM)](#261-bounded-context-identity--access-management-iam)

[2.6.1.1. Domain Layer](#2611-domain-layer)

[2.6.1.2. Interface Layer](#2612-interface-layer)

[2.6.1.3. Application Layer](#2613-application-layer)

[2.6.1.4. Infrastructure Layer](#2614-infrastructure-layer)

[2.6.1.5. Bounded Context Software Architecture Component Level Diagrams](#2615-bounded-context-software-architecture-component-level-diagrams)

[2.6.1.6. Bounded Context Software Architecture Code Level Diagrams](#2616-bounded-context-software-architecture-code-level-diagrams)

[2.6.1.6.1. Bounded Context Domain Layer Class Diagrams](#26161-bounded-context-domain-layer-class-diagrams)

[2.6.1.6.2. Bounded Context Database Design Diagram](#26162-bounded-context-database-design-diagram)

[2.6.2. Bounded Context: Carpooling](#262-bounded-context-carpooling)

[2.6.2.1. Domain Layer](#2621-domain-layer)

[2.6.2.2. Interface Layer](#2622-interface-layer)

[2.6.2.3. Application Layer](#2623-application-layer)

[2.6.2.4. Infrastructure Layer](#2624-infrastructure-layer)

[2.6.2.5. Bounded Context Software Architecture Component Level Diagrams](#2625-bounded-context-software-architecture-component-level-diagrams)

[2.6.2.6. Bounded Context Software Architecture Code Level Diagrams](#2626-bounded-context-software-architecture-code-level-diagrams)

[2.6.2.6.1. Bounded Context Domain Layer Class Diagrams](#26261-bounded-context-domain-layer-class-diagrams)

[2.6.2.6.2. Bounded Context Database Design Diagram](#26262-bounded-context-database-design-diagram)

[2.6.3. Bounded Context: Rental](#263-bounded-context-rental)

[2.6.3.1. Domain Layer](#2631-domain-layer)

[2.6.3.2. Interface Layer](#2632-interface-layer)

[2.6.3.3. Application Layer](#2633-application-layer)

[2.6.3.4. Infrastructure Layer](#2634-infrastructure-layer)

[2.6.3.5. Bounded Context Software Architecture Component Level Diagrams](#2635-bounded-context-software-architecture-component-level-diagrams)

[2.6.3.6. Bounded Context Software Architecture Code Level Diagrams](#2636-bounded-context-software-architecture-code-level-diagrams)

[2.6.3.6.1. Bounded Context Domain Layer Class Diagrams](#26361-bounded-context-domain-layer-class-diagrams)

[2.6.3.6.2. Bounded Context Database Design Diagram](#26362-bounded-context-database-design-diagram)

[2.6.4. Bounded Context: Billing](#264-bounded-context-billing)

[2.6.4.1. Domain Layer](#2641-domain-layer)

[2.6.4.2. Interface Layer](#2642-interface-layer)

[2.6.4.3. Application Layer](#2643-application-layer)

[2.6.4.4. Infrastructure Layer](#2644-infrastructure-layer)

[2.6.4.5. Bounded Context Software Architecture Component Level Diagrams](#2645-bounded-context-software-architecture-component-level-diagrams)

[2.6.4.6. Bounded Context Software Architecture Code Level Diagrams](#2646-bounded-context-software-architecture-code-level-diagrams)

[2.6.4.6.1. Bounded Context Domain Layer Class Diagrams](#26461-bounded-context-domain-layer-class-diagrams)

[2.6.4.6.2. Bounded Context Database Design Diagram](#26462-bounded-context-database-design-diagram)

[2.6.5. Bounded Context: Operations](#265-bounded-context-operations)

[2.6.5.1. Domain Layer](#2651-domain-layer)

[2.6.5.2. Interface Layer](#2652-interface-layer)

[2.6.5.3. Application Layer](#2653-application-layer)

[2.6.5.4. Infrastructure Layer](#2654-infrastructure-layer)

[2.6.5.5. Bounded Context Software Architecture Component Level Diagrams](#2655-bounded-context-software-architecture-component-level-diagrams)

[2.6.5.6. Bounded Context Software Architecture Code Level Diagrams](#2656-bounded-context-software-architecture-code-level-diagrams)

[2.6.5.6.1. Bounded Context Domain Layer Class Diagrams](#26561-bounded-context-domain-layer-class-diagrams)

[2.6.5.6.2. Bounded Context Database Design Diagram](#26562-bounded-context-database-design-diagram)

# Capítulo III: Solution UI/UX Design

[3.1. Product design](#31-product-design)

[3.1.1. Style Guidelines](#311-style-guidelines)

[3.1.1.1. General Style Guidelines](#3111-general-style-guidelines)

[3.1.2. Information Architecture](#312-information-architecture)

[3.1.2.1. Organization Systems](#3121-organization-systems)

[3.1.2.2. Labelling Systems](#3122-labelling-systems)

[3.1.2.3. SEO Tags and Meta Tags](#3123-seo-tags-and-meta-tags)

[3.1.2.4. Searching Systems](#3124-searching-systems)

[3.1.2.5. Navigation Systems](#3125-navigation-systems)

[3.1.3. Landing Page UI Design](#313-landing-page-ui-design)

[3.1.3.1. Landing Page Wireframe](#3131-landing-page-wireframe)

[3.1.3.2. Landing Page Mock-up](#3132-landing-page-mock-up)

[3.1.4. Mobile Applications UX/UI Design](#314-mobile-applications-uxui-design)

[3.1.4.1. Mobile Applications Wireframes](#3141-mobile-applications-wireframes)

[3.1.4.2. Mobile Applications Wireflow Diagrams](#3142-mobile-applications-wireflow-diagrams)

[3.1.4.3. Mobile Applications Mock-ups](#3143-mobile-applications-mock-ups)

[3.1.4.4. Mobile Applications User Flow Diagrams](#3144-mobile-applications-user-flow-diagrams)

[3.1.4.5. Mobile Applications Prototyping](#3145-mobile-applications-prototyping)

# Capítulo IV: Product Implementation & Validation

[4. Product Implementation & Validation](#4-product-implementation--validation)

[4.1. Software Configuration Management](#41-software-configuration-management)

[4.1.1. Software Development Environment Configuration](#411-software-development-environment-configuration)

[4.1.2. Source Code Management](#412-source-code-management)

[4.1.3. Source Code Style Guide & Conventions](#413-source-code-style-guide--conventions)

[4.1.4. Software Deployment Configuration](#414-software-deployment-configuration)

[4.2. Landing Page & Mobile Application Implementation](#42-landing-page--mobile-application-implementation)

[4.2.1. Sprint n](#421-sprint-n)

[4.2.1.1. Sprint Planning n](#4211-sprint-planning-n)

[4.2.1.2. Sprint Backlog n](#4212-sprint-backlog-n)

[4.2.1.3. Development Evidence for Sprint Review](#4213-development-evidence-for-sprint-review)

[4.2.1.4. Testing Suite Evidence for Sprint Review](#4214-testing-suite-evidence-for-sprint-review)

[4.2.1.5. Execution Evidence for Sprint Review](#4215-execution-evidence-for-sprint-review)

[4.2.1.6. Services Documentation Evidence for Sprint Review](#4216-services-documentation-evidence-for-sprint-review)

[4.2.1.7. Software Deployment Evidence for Sprint Review](#4217-software-deployment-evidence-for-sprint-review)

[4.2.1.8. Team Collaboration Insights during Sprint](#4218-team-collaboration-insights-during-sprint)

[4.3. Validation Interviews](#43-validation-interviews)

[4.3.1. Diseño de Entrevistas](#431-diseño-de-entrevistas)

[4.3.2. Registro de Entrevistas](#432-registro-de-entrevistas)

[4.3.3. Evaluaciones según heurísticas](#433-evaluaciones-según-heurísticas)

# Conclusiones

[Conclusiones y recomendaciones](#conclusiones-y-recomendaciones)

[Video App Validation](#video-app-validation)

[Video About the product](#video-about-the-product)

[Video About the team](#video-about-the-team)

[Glosario](#glosario)

[Bibliografía](#bibliografía)

[Anexos](#anexos)


# Student Outcome

<table>
  <tr>
    <td><b>Criterio específico</b></td>
    <td><b>Acciones realizadas</b></td>
    <td><b>Conclusiones</b></td>
  </tr>

  <!-- PRIMER CRITERIO: Trabaja en equipo para proporcionar liderazgo en forma conjunta -->

  <tr>
    <td>
      <p>Trabaja en equipo para proporcionar liderazgo en forma conjunta</p>
    </td>
    <td>
      <p><strong>TB1</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Facilité todas las reuniones de planning del Sprint 1 donde coordiné la distribución de HU entre desarrolladores, propuse la metodología de seguimiento en Trello que adoptamos como equipo y medié los conflictos que surgieron sobre la priorización de features, logrando que todos llegáramos a consensos constructivos.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Lideré el análisis exhaustivo de nuestros competidores Peru Rent A Car, Kayak y Budget Car Rental, coordiné todas las sesiones de user research y testing de usabilidad, facilité workshops de ideación para UX/UI donde todos aportamos ideas creativas, y representé constantemente la voz del usuario en las decisiones técnicas para mantener el foco en la experiencia.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Organicé las reuniones iniciales del equipo para definir roles y responsabilidades, coordiné la creación del repositorio GitHub y la estructura de carpetas del proyecto, facilité las sesiones de brainstorming para definir el alcance del landing page y medié en la toma de decisiones sobre qué secciones incluir en la primera versión de MOVEO.</p>
    </td>
    <td>
      <p><strong>TB1</strong></p>
      <p>En conclusión: La comunicación efectiva y constante entre los miembros favoreció la coordinación y el avance armónico del proyecto.</p>
    </td>
  </tr>

  <tr>
    <td>
      <p>Trabaja en equipo para proporcionar liderazgo en forma conjunta</p>
    </td>
    <td>
      <p><strong>TP1</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Facilité todas las reuniones de planning del Sprint 1 donde coordiné la distribución de HU entre desarrolladores, propuse la metodología de seguimiento en Trello que adoptamos como equipo y medié los conflictos que surgieron sobre la priorización de features, logrando que todos llegáramos a consensos constructivos.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Lideré el análisis exhaustivo de nuestros competidores Peru Rent A Car, Kayak y Budget Car Rental, coordiné todas las sesiones de user research y testing de usabilidad, facilité workshops de ideación para UX/UI donde todos aportamos ideas creativas, y representé constantemente la voz del usuario en las decisiones técnicas para mantener el foco en la experiencia.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Organicé las reuniones iniciales del equipo para definir roles y responsabilidades, coordiné la creación del repositorio GitHub y la estructura de carpetas del proyecto, facilité las sesiones de brainstorming para definir el alcance del landing page y medié en la toma de decisiones sobre qué secciones incluir en la primera versión de MOVEO.</p>
    </td>
    <td>
      <p><strong>TP1</strong></p>
      <p>En conclusión: El liderazgo compartido y la distribución equitativa de responsabilidades permitieron consolidar un equipo cohesionado, capaz de tomar decisiones conjuntas y responder de forma ágil a los desafíos del proyecto.</p>
    </td>
  </tr>

  <tr>
    <td>
      <p>Trabaja en equipo para proporcionar liderazgo en forma conjunta</p>
    </td>
    <td>
      <p><strong>TB2</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Facilité las reuniones de planning del Sprint 3, coordinando la distribución de tareas para la implementación de los módulos de Usuario, Vehículo y Alquiler en el backend. Propuse y ayudé a configurar la integración de CI/CD en GitHub Actions para automatizar las pruebas y despliegues. Medié discusiones técnicas sobre la arquitectura DDD, guiando al equipo hacia soluciones prácticas y alineadas con los objetivos del sprint.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Lideré la definición de los esquemas de datos para los modelos de dominio en el backend, asegurando consistencia y alineación con la lógica de negocio. Coordiné las sesiones de validación de la API con el frontend, actuando como puente entre ambos equipos de desarrollo y representando el enfoque en la experiencia de usuario desde la perspectiva del backend.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Organicé y coordiné reuniones para alinear el desarrollo del backend con los requerimientos del frontend, facilitando la comunicación entre ambos equipos. Lideré la configuración inicial del repositorio <code>MOVEO-backend</code>, la estructura base del proyecto .NET y la integración con el sistema de control de versiones y la documentación.</p>
    </td>
    <td>
      <p><strong>TB2</strong></p>
      <p>En conclusión: El liderazgo compartido se mantuvo y se fortaleció, permitiendo una distribución efectiva de tareas técnicas complejas y una toma de decisiones colaborativa y eficiente durante el desarrollo del backend en el Sprint 3.</p>
    </td>
  </tr>

  <tr>
    <td>
      <p>Trabaja en equipo para proporcionar liderazgo en forma conjunta</p>
    </td>
    <td>
      <p><strong>TF1</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Facilité las reuniones finales de integración del Sprint 4, coordinando la alineación entre frontend y backend para entregar una solución completamente funcional. Lideré la implementación del módulo de soporte técnico con notificaciones en tiempo real y medié en la priorización final de bugs críticos antes del cierre del proyecto.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Lideré la integración completa de la API REST con el frontend, implementando el flujo de autenticación basado en JWT y tokens HTTP-only. Coordiné la validación técnica de todos los endpoints con Swagger y aseguré que la documentación reflejara con precisión la funcionalidad desplegada en producción.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Organicé la entrega final del proyecto, incluyendo la redacción de las secciones técnicas del informe, la consolidación del repositorio y la validación del CI/CD en GitHub Actions. Lideré el despliegue del backend en Railway y del frontend en Render, asegurando que ambos componentes funcionaran en conjunto en el entorno de staging.</p>
    </td>
    <td>
      <p><strong>TF1</strong></p>
      <p>En conclusión: El liderazgo compartido permitió cerrar el proyecto con una solución integrada, bien documentada y desplegada, reflejando un alto nivel de madurez técnica y coordinación entre los miembros del equipo.</p>
    </td>
  </tr>

  <!-- SEGUNDO CRITERIO: Crea un entorno colaborativo e inclusivo... -->

  <tr>
    <td>
      <p><b>Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos.</b></p>
    </td>
    <td>
      <p><strong>TB1</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Creé el workspace de Trello completo y definí el flujo de trabajo que seguimos actualmente, establecí junto al equipo la Definition of Ready y Done que nos guía en cada tarea, organicé daily standups virtuales diarios e implementé retrospectivas semanales donde todos participamos para mejorar continuamente nuestros procesos.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Diseñé wireframes de forma colaborativa involucrando a todo el equipo en las decisiones de diseño, establecí métricas UX específicas como tiempo de carga menor a 3 segundos y usabilidad superior al 85%, organicé sesiones de testing con usuarios reales para validar nuestras hipótesis y creé un design system unificado que mantiene la coherencia visual en todo el proyecto.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Creé el canal de comunicación principal del equipo en WhatsApp y Discord, establecí las metas iniciales de completar el landing page y la documentación básica para la primera entrega, planifiqué la distribución de tareas entre compañeros según sus fortalezas e implementé reuniones de seguimiento diarias para mantener a todos alineados con los objetivos.</p>
    </td>
    <td>
      <p><strong>TB1</strong></p>
      <p>En conclusión: La comunicación interdisciplinaria permitió un mejor desarrollo y entendimiento del proyecto en todas sus fases.</p>
    </td>
  </tr>

  <tr>
    <td>
      <p><b>Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos.</b></p>
    </td>
    <td>
      <p><strong>TP1</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Creé el workspace de Trello completo y definí el flujo de trabajo que seguimos actualmente, establecí junto al equipo la Definition of Ready y Done que nos guía en cada tarea, organicé daily standups virtuales diarios e implementé retrospectivas semanales donde todos participamos para mejorar continuamente nuestros procesos.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Diseñé wireframes de forma colaborativa involucrando a todo el equipo en las decisiones de diseño, establecí métricas UX específicas como tiempo de carga menor a 3 segundos y usabilidad superior al 85%, organicé sesiones de testing con usuarios reales para validar nuestras hipótesis y creé un design system unificado que mantiene la coherencia visual en todo el proyecto.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Creé el canal de comunicación principal del equipo en WhatsApp y Discord, establecí las metas iniciales de completar el landing page y la documentación básica para la primera entrega, planifiqué la distribución de tareas entre compañeros según sus fortalezas e implementé reuniones de seguimiento diarias para mantener a todos alineados con los objetivos.</p>
    </td>
    <td>
      <p><strong>TP1</strong></p>
      <p>En conclusión: El enfoque colaborativo, la planificación clara y el compromiso colectivo con las metas definidas fueron clave para cumplir con los objetivos de esta entrega de manera eficaz y con calidad.</p>
    </td>
  </tr>

  <tr>
    <td>
      <p><b>Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos.</b></p>
    </td>
    <td>
      <p><strong>TB2</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Actualicé el workspace de Trello para el Sprint 3, definiendo columnas específicas para tareas de backend (DDD, API, Despliegue). Establecí junto al equipo metas claras para la implementación de los módulos de Usuario, Vehículo y Alquiler, y las tareas de despliegue en Railway y Render. Organicé daily standups enfocados en el avance del backend y coordiné retrospectivas para mejorar el flujo de trabajo del equipo técnico.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Colaboré en la definición de los objetivos técnicos del backend, enfocados en la correcta implementación de la lógica de negocio. Establecí metas de calidad para los esquemas de datos y la documentación de la API. Planifiqué y participé en sesiones de integración entre el backend y el frontend para garantizar que los servicios cumplieran con los requisitos de la interfaz de usuario.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Establecí como meta principal la creación de un backend robusto y bien documentado. Planifiqué la integración con los servicios de nube (Railway, Render) y coordiné tareas para la configuración de CI/CD. Organicé reuniones de seguimiento para alinear el avance del backend con el cronograma del sprint y los objetivos generales del proyecto.</p>
    </td>
    <td>
      <p><strong>TB2</strong></p>
      <p>En conclusión: La planificación meticulosa, la definición clara de metas técnicas y el mantenimiento de un entorno colaborativo permitieron al equipo avanzar de manera cohesiva y eficiente en la implementación del backend durante el Sprint 3, cumpliendo con los objetivos establecidos.</p>
    </td>
  </tr>

  <tr>
    <td>
      <p><b>Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos.</b></p>
    </td>
    <td>
      <p><strong>TF1</strong></p>
      <p><strong>Luna Morales, Gianfranco:</strong> Actualicé el tablero de Trello con las tareas críticas del Sprint 4, incluyendo pruebas de integración, corrección de bugs y preparación de la documentación final. Establecí metas diarias para garantizar la entrega a tiempo y organicé las sesiones de validación con usuarios reales para retroalimentar el producto final.</p>
      <p><strong>Huang Liu, Franco Gabriel:</strong> Definí los criterios de calidad para la API final, incluyendo cobertura de pruebas unitarias, documentación Swagger y manejo de errores coherente. Planifiqué y ejecuté pruebas de extremo a extremo con Postman para validar todos los flujos del negocio antes del despliegue.</p>
      <p><strong>Santiago Peña, Andreow Jomark:</strong> Establecí como meta entregar un sistema completamente funcional con autenticación, verificación de identidad, reservas, pagos simulados, notificaciones y soporte. Coordiné las pruebas finales, la redacción del informe técnico y la preparación de los videos demostrativos, asegurando coherencia entre el código, la documentación y la experiencia del usuario.</p>
    </td>
    <td>
      <p><strong>TF1</strong></p>
      <p>En conclusión: La planificación rigurosa, la comunicación constante y el enfoque en la calidad permitieron al equipo entregar una solución final robusta, validada y lista para producción, cumpliendo con todos los objetivos del curso y las expectativas del profesor.</p>
    </td>
  </tr>
</table>

# Objetivos SMART

# Capítulo I: Introducción
# 1.1. Startup Profile
### 1.1.1. Descripción de la Startup

Nuestro proyecto consiste en un servicio digital diseñado para conectar a personas que poseen un vehículo con quienes necesitan uno por un tiempo determinado. A diferencia de una compañía de alquiler tradicional, nuestra propuesta no requiere contar con un parque automotor propio, lo que reduce significativamente los costos iniciales. En lugar de ello, los autos registrados por los mismos usuarios son los que conforman la oferta disponible en la plataforma, generando así una red colaborativa similar a una flota virtual.
El modelo se centra en la intermediación: los dueños obtienen ingresos únicamente cuando su vehículo es efectivamente arrendado, mientras que los arrendatarios acceden a precios más accesibles que en el mercado convencional. De esta manera, se construye un sistema rentable, flexible y equitativo para ambas partes.

Misión: Ofrecer una solución moderna y segura que simplifique el acceso a un vehículo de alquiler, generando confianza y beneficios tanto para el propietario como para el arrendatario. Buscamos que nuestra plataforma sea percibida como una alternativa práctica, clara y orientada a las necesidades reales de los usuarios.

Visión: Aspiramos a consolidarnos como la plataforma más reconocida en el Perú para la renta de automóviles entre particulares. Queremos ser identificados por la innovación de nuestro modelo, la seguridad de nuestras operaciones y la facilidad de uso del sistema. Nuestra meta es que, al pensar en alquiler de autos sin trámites complicados, las personas recurran primero a nosotros.

### 1.1.2. Perfiles de integrantes del equipo
| Integrantes                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                               | Conocimientos                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <img src="Assets/img/cover/Andreow.jpg " width="100" height="100"> <br>Alison Jimena Arrieta Quispe u202317362         | Soy estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Mi principal meta es especializarme en la creación de agentes inteligentes y soluciones basadas en Inteligencia Artificial, con enfoque en aprendizaje automático, procesamiento del lenguaje natural y sistemas autónomos. | Tengo experiencia en múltiples lenguajes de programación como Python, C#, Java, JavaScript y SQL, y estoy familiarizado con frameworks como Vue.js, ASP.NET Core y TensorFlow/Keras. Me apasiona aprender tecnologías emergentes y aplicarlas en proyectos reales que generen impacto. |
| <img src="Assets/Alexis.png " width="100" height="100"> <br>Alexis Encalada Salazar u20211g491                         | Soy estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Mi principal meta es especializarme en la creación de agentes inteligentes y soluciones basadas en Inteligencia Artificial, con enfoque en aprendizaje automático, procesamiento del lenguaje natural y sistemas autónomos. | Tengo experiencia en múltiples lenguajes de programación como Python, C#, Java, JavaScript y SQL, y estoy familiarizado con frameworks como Vue.js, ASP.NET Core y TensorFlow/Keras. Me apasiona aprender tecnologías emergentes y aplicarlas en proyectos reales que generen impacto. |
| <img src="Assets/img/cover/Andreow.jpg " width="100" height="100"> <br>Esther Abigail Goñe Araccata u202318049         | Soy estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Mi principal meta es especializarme en la creación de agentes inteligentes y soluciones basadas en Inteligencia Artificial, con enfoque en aprendizaje automático, procesamiento del lenguaje natural y sistemas autónomos. | Tengo experiencia en múltiples lenguajes de programación como Python, C#, Java, JavaScript y SQL, y estoy familiarizado con frameworks como Vue.js, ASP.NET Core y TensorFlow/Keras. Me apasiona aprender tecnologías emergentes y aplicarlas en proyectos reales que generen impacto. |
| <img src="Assets/img/cover/Andreow.jpg " width="100" height="100"> <br>Alvaro Fabrizzio Salazar Caballero  u2023211941 | Soy estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Mi principal meta es especializarme en la creación de agentes inteligentes y soluciones basadas en Inteligencia Artificial, con enfoque en aprendizaje automático, procesamiento del lenguaje natural y sistemas autónomos. | Tengo experiencia en múltiples lenguajes de programación como Python, C#, Java, JavaScript y SQL, y estoy familiarizado con frameworks como Vue.js, ASP.NET Core y TensorFlow/Keras. Me apasiona aprender tecnologías emergentes y aplicarlas en proyectos reales que generen impacto. |
| <img src="Assets/Andreow.png " width="100" height="100"> <br>Andreow Jomark Santiago Peña u202317362                   | Soy estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Mi principal meta es especializarme en la creación de agentes inteligentes y soluciones basadas en Inteligencia Artificial, con enfoque en aprendizaje automático, procesamiento del lenguaje natural y sistemas autónomos. | Tengo experiencia en múltiples lenguajes de programación como Python, C#, Java, JavaScript y SQL, y estoy familiarizado con frameworks como Vue.js, ASP.NET Core y TensorFlow/Keras. Me apasiona aprender tecnologías emergentes y aplicarlas en proyectos reales que generen impacto. |

# 1.2. Solution Profile

## 1.2.1. Antecedentes y Problemática
Para explicar los fundamentos de nuestra startup utilizaremos una adaptación de la técnica de análisis 5W + 2H, que permite organizar la información respondiendo a las preguntas clave de cualquier iniciativa.

**Antecedentes**

- En los últimos años la necesidad de soluciones de movilidad temporal ha crecido considerablemente, especialmente en zonas urbanas donde adquirir un vehículo propio no siempre es viable. Ante ello surge la oportunidad de una plataforma digital que facilite el contacto directo entre propietarios de automóviles y personas interesadas en alquilarlos, optimizando el proceso a través de un aplicativo accesible.

**Problemática**

- La ausencia de servicios que ofrezcan un alquiler directo entre dueños y arrendatarios dificulta satisfacer la demanda de transporte temporal. Esto genera dos consecuencias principales: los usuarios que requieren un vehículo de manera inmediata encuentran limitaciones, y los propietarios pierden la posibilidad de generar ingresos adicionales con sus autos.

Aplicación del método 5W + 2H

**¿Qué?**

El proyecto busca responder a la falta de un sistema eficiente que conecte a quienes desean rentabilizar sus vehículos con quienes necesitan arrendarlos. La iniciativa está directamente relacionada con dos tipos de clientes: propietarios con autos disponibles y arrendatarios que requieren alternativas accesibles y confiables.

**¿Cuándo?**

La problemática se presenta en el momento en que un propietario desea alquilar su vehículo, pero no cuenta con un canal formal ni seguro para hacerlo. A su vez, los arrendatarios se ven afectados cuando requieren un vehículo por un tiempo limitado —sea por un viaje, una urgencia o una necesidad puntual— y no encuentran opciones adecuadas.
El uso de la plataforma se da justamente en esos escenarios: el dueño publica su vehículo y el arrendatario selecciona la opción que mejor se adapta a su situación.

**¿Dónde?**

El servicio puede utilizarse en cualquier lugar con acceso a internet, ya sea desde casa, el trabajo o en desplazamiento.
La propuesta está dirigida principalmente a contextos urbanos donde la demanda de movilidad es más alta y, paradójicamente, la oferta de plataformas colaborativas de alquiler es todavía reducida.

**¿Quiénes?**

Participan dos grupos principales: los propietarios que desean ofrecer su auto en alquiler y los arrendatarios que buscan una solución práctica sin trámites extensos.
El problema afecta sobre todo a los dueños que no logran monetizar sus vehículos y a las personas que necesitan movilidad temporal pero no encuentran opciones seguras y confiables.
En consecuencia, el público objetivo que hará uso del servicio corresponde a ambos segmentos, integrados en una misma plataforma.

**¿Por qué?**

La raíz del problema se encuentra en la falta de un canal especializado y confiable que asegure la interacción entre dueños y arrendatarios. Esta ausencia limita la rentabilidad de los primeros y restringe la variedad de opciones para los segundos.

**¿Cómo?**

El servicio se utiliza cuando los dueños desean generar ingresos con su vehículo o cuando un arrendatario necesita resolver rápidamente una necesidad de transporte.
Los usuarios llegan a la plataforma a través de campañas digitales, publicidad segmentada en redes sociales y recomendaciones de otros clientes.
En general, el detonante es la búsqueda de una alternativa segura, flexible y accesible frente a los servicios tradicionales de alquiler.

**¿Cuánto cuesta?**

Para los propietarios no existen costos de inscripción ni inversión inicial; únicamente se descuenta una comisión en caso de concretarse el alquiler.
Los arrendatarios, en cambio, acceden a tarifas variables y flexibles, con opciones que resultan más económicas en comparación con las agencias de renta tradicionales.


## 1.2.2. Lean UX Process

### 1.2.2.1. Lean UX Problem Statement

MOVEO tiene como objetivo ofrecer un servicio de alquiler de vehículos accesible, flexible y rentable, conectando de manera segura y eficiente a propietarios y arrendatarios a través de una plataforma digital. Sin embargo, el mercado actual se caracteriza por la falta de innovación, modelos de negocio rígidos, altos costos para los usuarios y una fuerte dependencia de flotas propias, lo que limita la escalabilidad y reduce la diversidad de la oferta. Ante esta situación, se plantea la necesidad de mejorar el modelo de servicio mediante un sistema más adaptable e inclusivo, que permita ampliar la participación de propietarios particulares y optimizar la experiencia de alquiler sin requerir una inversión directa en vehículos.

Consideramos que habremos alcanzado un avance significativo cuando logremos que el número de propietarios inscritos crezca de forma constante y que la oferta de vehículos disponibles se adapte a la demanda real del mercado.

### 1.2.2.2. Lean UX Assumptions

**Segmento de Usuarios:**

**¿Quién es el usuario?**

Nuestros principales usuarios son dos: los dueños de vehículos que desean generar ingresos pasivos sin tener que involucrarse en la gestión diaria de sus autos, y las personas que buscan alternativas de alquiler de vehiculos seguras, cómodas y accesibles.

**¿Dónde se integra el servicio en su vida?**

Para los propietarios, el servicio se convierte en un medio para obtener ingresos extra sin esfuerzo operativo. Para los inquilinos, representa la posibilidad de acceder a un vehículo en el momento en que lo necesitan, sin asumir compromisos de propiedad ni altos costos.

**¿Cuándo y cómo se utiliza el servicio?**

Los dueños lo usan al registrar su vehículo y seguir sus ganancias, mientras que los inquilinos lo emplean cuando requieren transporte para viajes, mudanzas, diligencias o necesidades puntuales de movilidad.

**¿Qué problemas enfrenta el servicio?**

El mayor reto es garantizar la seguridad y confianza de los propietarios respecto al uso de sus vehículos, al mismo tiempo que se asegura que los inquilinos disfruten de una experiencia rápida, sencilla y sin complicaciones.

**Resultados de Negocio (Business Outcomes):**

- Anticipamos que los propietarios valorarán una plataforma que les permita alquilar sin preocuparse de la gestión operativa.
- Creemos que los arrendatarios encontrarán en nuestro servicio una alternativa más económica y variada que las opciones tradicionales.
- Reconocemos que existen competidores en el sector, pero nuestro modelo —sin flota propia— nos permitirá mantener precios atractivos y una mejor experiencia de usuario.
- Sabemos que para mantener la confianza, debemos reforzar la calidad del servicio con pruebas constantes, mejoras continuas y canales abiertos de comunicación con nuestros clientes.

### 1.2.2.3. Lean UX Hypothesis Statements

1. Consideramos que los propietarios interesados en generar ingresos pasivos, sin realizar grandes inversiones ni dedicar demasiado tiempo a la gestión, verán en MOVEO una alternativa confiable para monetizar sus vehículos. Consideraremos que hemos alcanzado el éxito cuando estos propietarios incrementen el uso de la plataforma y obtengan ingresos recurrentes mediante el alquiler de sus autos, evidenciando confianza y satisfacción en el servicio.

2. Creemos que los arrendatarios que buscan opciones de alquiler más flexibles, asequibles y seguras optarán por MOVEO gracias a su facilidad de uso, precios competitivos y garantías de protección. Consideraremos que hemos alcanzado el éxito cuando la frecuencia de alquiler y la tasa de retención de usuarios aumenten, junto con una mejora perceptible en los niveles de satisfacción reportados.

3. Suponemos que al implementar un modelo operativo sin una flota propia de vehículos, podremos destinar mayores recursos a la innovación tecnológica y a la optimización de la experiencia de usuario. Consideraremos que hemos alcanzado el éxito cuando los indicadores de eficiencia operativa y de experiencia del cliente reflejen una reducción de costos, estabilidad en las tarifas y un incremento sostenido en el número de transacciones exitosas.

### 1.2.2.4. Lean UX Canvas.
En el apartado de Lean UX Canvas se desarrolló una estructuración completa y académica de las principales hipótesis estratégicas que sustentan la propuesta de valor y la arquitectura de la plataforma Moveo

Cada hipótesis fue traducida en un Lean UX Canvas formal, siguiendo un enfoque científico-experimental que articula: el problema de negocio detectado (Business Problem ), las soluciones propuestas a nivel funcional y técnico (Solutions ), los resultados esperados a nivel organizacional (Business Outcomes ), la caracterización de los usuarios objetivos (Users ), los beneficios esperados para estos usuarios (User Outcomes & Benefits ), la formulación de hipótesis de aprendizaje (Hypotheses ), y el diseño de experimentos estratégicos para validar o refutar dichas hipótesis (What's the most important thing we need to learn first? y What's the least amount of work we need to do to learn the next most important thing? ).

Este trabajo metodológico permitió no solo establecer un marco claro de experimentación y validación temprana de las decisiones de diseño y tecnología, sino también alinear todos los esfuerzos de desarrollo a métricas de éxito específicas y medibles. Así, el apartado de Lean UX Canvas representa una pieza fundamental dentro del enfoque de construcción iterativa, ágil y centrada en el usuario de Moveo, asegurando que cada funcionalidad propuesta responde a necesidades reales, riesgos priorizados y oportunidades de negocio tangibles.

![Lean ux Canva](Assets/Leanuxcanva.png)

<a id="segmentos-objetivo"></a>
# 1.3. Segmentos objetivos 
**Segmento 1: Proveedores de vehículos**

Datos demográficos:
- Género: hombres y mujeres.
- Rango etario: de 18 a 70 años.
- Condición socioeconómica: sectores A, B y C (clase media o clase alta).

Datos geográficos:
- Nacionalidad: peruana.
- Área de residencia: zonas urbanas.
- Ubicación principal: Lima Metropolitana.

Datos psicográficos:
- Individuos (naturales o jurídicos) que poseen un vehículo que permanece sin uso la mayor parte del tiempo.
- Personas interesadas en generar ingresos adicionales a través de un recurso que ya poseen, sin necesidad de destinar grandes cantidades de tiempo a la gestión.
- Propietarios que aún no cuentan con un mecanismo práctico, seguro y rápido para ofrecer sus autos en alquiler.

**Segmento 2: Clientes**

Datos demográficos:
- Género: tanto masculino como femenino.
- Edad: entre 18 y 50 años.
- Nivel socioeconómico: clases A, B y C (clase media, media alta y alta).

Datos geográficos:
- Nacionalidad: peruana.
- Lugar de residencia: zonas urbanas.
- Departamento: Lima Metropolitana.

Datos psicográficos:
- Personas que pasan una cantidad considerable de horas en transporte público o en el tráfico y buscan alternativas más cómodas y flexibles.
- Usuarios que no cuentan con los recursos para adquirir un auto propio (nuevo o de segunda mano), pero que requieren movilidad en situaciones específicas.
- Personas que necesitan disponer de un vehículo particular por un período corto, ya sea para actividades puntuales, compromisos laborales o viajes.

# Capítulo II: Requirements Elicitation & Analysis
## 2.1. Competidores 

Previo al desarrollo de la aplicación, hicimos una búsqueda de las opciones que ya existen en el mercado, para ver que es lo que ofrecen y como podemos diferenciarnos de ellos.
- **Peru Rent A Car:**
  Esta plataforma se especializa en el alquiler de coches en Perú. Ofrece una amplia gama de vehículos y opciones de alquiler, así como información sobre destinos turísticos en Perú.
  La plataforma también permite a los usuarios comparar precios y reservar coches en línea.
  <div style="text-align: center;">
 <img src="Assets/PeruRentACar.png" width=310  alt="">
  </div>

- **Kayak:**
  Kayak es una de las plataformas de búsqueda de viajes más grandes del mundo. Permite a los usuarios buscar y comparar precios de vuelos, hoteles y alquiler de coches en una sola plataforma.
  Kayak también ofrece herramientas para planificar viajes, como alertas de precios y recomendaciones personalizadas.
  <div style="text-align: center;">
<img src="Assets/Kayak.png" width=310  alt="">
  </div>

- **Budget Car Rental Peru:**
  A diferencia de Peru Rent A Car, Budget Car Rental es una empresa internacional que ofrece servicios de alquiler de coches en Perú.
  La plataforma permite a los usuarios buscar y comparar precios de coches de alquiler en diferentes ubicaciones y reservar en línea. Budget Car Rental también ofrece opciones de alquiler a largo plazo y programas de fidelización.
  <div style="text-align: center;">
<img src="Assets/Budget.png" width=310  alt="">
  </div>

### 2.1.1. Análisis competitivo.

En esta sección tiene como objetivo que su startup conozca mejor a sus competidores, en contraste con la idea inicial que pudiera tener sobre ellos. Se debe desarrollar el siguiente Landscape:  
**Se realiza un mapeo estratégico comparativo entre nuestra propuesta (Moveo) y los principales actores del mercado, evaluando su perfil, marketing, producto y análisis SWOT, con el fin de identificar brechas de mercado, fortalezas propias y oportunidades de posicionamiento diferenciado.**

**¿Por qué llevar a cabo este análisis?**  
*Objetivo: Comprender a fondo el posicionamiento de nuestra startup frente a competidores clave en el mercado de alquiler de autos en Perú, identificando sus fortalezas, debilidades y estrategias, para definir con precisión nuestra ventaja competitiva y oportunidades de diferenciación.*


<table border="1" style="text-align: center;">
	<tbody>
		<tr><td colspan="6">Análisis de competidores</td></tr>
		<tr><td colspan="2"></td><td>Moveo</td><td>Kayak</td><td>Peru Rent A Car</td><td>Budget Car Rental Peru</td></tr>
		<tr><td rowspan="2">Perfil</td><td>Resumen</td>
			<td>Una aplicación que busca ofrecer una plataforma rápida y ágil para el alquiler de autos, con un fuerte enfoque en la seguridad de ambas partes.</td>
			<td>Kayak es una plataforma líder de búsqueda tanto de vuelos, como cuartos de hotel, alquiler de vehículos, etc.</td>
			<td>Esta plataforma web presenta parte de un catálogo establecido de vehículos para alquilar, con una atención mediante WhatsApp y dirigido solo a clientes.</td>
			<td>Plataforma de similar funcionamiento que Rent A Car Peru, orientado a clientes con un énfasis en cuidar el presupuesto de los mismos.</td></tr>
		<tr><td>Ventaja competitiva</td>
			<td>Ofrecer una plataforma tanto para dueños de vehículos como a clientes interesados en alquilar.</td>
			<td>Es la aplicación líder en la búsqueda de servicios por su variedad y robusta plataforma web.</td>
			<td>Líder local del servicio de alquiler de autos, con una amplia flota y rápida atención al usuario</td>
			<td>Ofrece una alternativa de alquiler económica velando por el bolsillo de sus clientes. </td></tr>
		<tr><td rowspan="2">Perfil de Marketing</td><td>Mercado objetivo</td>
			<td>Jóvenes y adultos desde los 20 a los 50 años.</td>
			<td>Turistas o viajeros que necesiten cualquier tipo de servicio de comodidad.</td>
			<td>Adultos peruanos que busquen alquilar un vehiculo.</td>
			<td>Adultos peruanos que busquen alquilar un vehiculo económico.</td></tr>
		<tr><td>Estrategias de marketing</td>
			<td>Marketing digital en redes sociales y colaboraciones con influencers.</td>
			<td>Alianza con Google Ads, tanto en Youtube como Chrome.</td>
			<td>Patrocinio mediante búsquedas de Chrome.</td>
			<td>Patrocinio mediante búsquedas de Chrome.</td></tr>
		<tr><td rowspan="3">Perfil de Producto</td>
			<td>Productos y Servicios</td>
			<td>Aplicación destinada a la oferta de vehículos en alquiler, como la demanda de los mismos.</td>
			<td>Aplicación móvil y web que cuenta con una enorme variedad de servicios esenciales para viajeros y turistas</td>
			<td>Aplicación web rápida e intuitiva que permite consultar parte del catálogo de vehículos disponibles para alquiler.</td>
			<td>Aplicación web ágil y amigable que permite consultar una limitada oferta de vehículos económicos en alquiler</td></tr>
		<tr><td>Precios y Costos</td>
			<td>Costos por publicación de vehículos mediante una suscripción.</td>
			<td>Modelo gratuito, con cobro de comisión a las empresas referidas.</td>
			<td>Ingreso directo mediante el alquiler.</td>
			<td>Ingreso directo mediante el alquiler.</td></tr>
		<tr><td>Canales de distribución</td>
			<td>Disponible en línea a través de la aplicación web.</td>
			<td>Descargable en Google Play y App Store y la plataforma web.</td>
			<td>Disponible en línea a través de la aplicación web.</td>
			<td>Disponible en línea a través de la aplicación web.</td></tr>
		<tr><td rowspan="4">Análisis SWOT</td><td>Fortalezas</td><td><ul>
                    <li>Orientado a jóvenes y adultos peruanos</li><li>Facilidades para alquilar, como ofrecer alquiler</li><li>Énfasis en la seguridad y garantía</li></ul></td>
			<td><ul>
                    <li>Gran cantidad de usuarios</li><li>Referente del sector</li><li>Plataformas ágiles e intuitivas</li></ul></td>
			<td><ul><li>Plataforma local</li><li>Excelente atención al cliente</li></ul></td>
			<td><ul><li>Plataforma web amigable</li><li>Todo el catálogo está disponible para cualquier usuario</li></ul></td></tr>
		<tr><td>Debilidades</td>
            <td><ul><li>Nuevo competidor</li><li>Sector con competidores fuertes ya establecidos</li></ul></td>
			<td><ul><li>Pobre atención al cliente</li></ul></td>
			<td><ul><li>Solo se puede consultar parte del catálogo de vehículos</li></ul></td>
			<td><ul><li>Opta por un nicho muy concreto</li><li>No cuenta con tanta relevancia como su competencia</li></ul></td></tr>
		<tr><td>Oportunidades</td>
            <td><ul><li>Sin competidores a nivel nacional</li><li>Ofrece servicio para ambas partes involucradas en el alquiler</li></ul></td>
			<td><ul><li>Fuerte presencia internacional</li><li>Referente del sector</li></ul></td>
			<td><ul><li>Flota amplia y en crecimiento</li><li>Atención personalizada</li></ul></td>
			<td><ul><li>Excelente interfaz</li></ul></td></tr>
		<tr><td>Amenazas</td>
            <td><ul><li>Competencia ya establecida</li><li>Sector muy competitivo</li></ul></td>
			<td><ul><li>Oferta demasiado ámplia</li><li>Sin control de calidad</li></ul></td>
			<td><ul><li>Oferta fija y poco variada</li><li>Sin opciones para dueños interesados en alquilar</li></ul></td>
<td><ul><li>Se ve opacado por la competencia</li><li>Oferta aún más limitada que la competencia</li></ul></td>
</tr></tbody></table>

### 2.1.2. Estrategias y tácticas frente a competidores. 
Moveo se diferenciará mediante un enfoque local y seguro, integrando tanto a dueños de vehículos como a arrendatarios.
Para contrarrestar la falta de reconocimiento como nuevo competidor, se aplicarán tácticas de marketing digital y alianzas con influencers, generando confianza y visibilidad rápida.
Aprovechando la ausencia de un líder nacional en movilidad tipo Airbnb, la estrategia será posicionarse como la primera opción peruana especializada en alquiler de autos.
Frente a amenazas de grandes plataformas, Moveo enfocará sus esfuerzos en segmentos desatendidos y en brindar soporte inmediato y flexibilidad en precios, destacando su cercanía y adaptabilidad frente a la oferta internacional y tradicional.

## 2.2. Entrevistas

En esta sección se presenta la investigación cualitativa realizada mediante entrevistas profundas a representantes de nuestros dos segmentos objetivo: **propietarios de vehículos** (Segmento 1) e **inquilinos o usuarios que desean alquilar autos** (Segmento 2). El objetivo es comprender sus necesidades reales, frustraciones, hábitos de consumo y expectativas frente a una plataforma de alquiler de autos, validando así los supuestos del modelo de negocio y ajustando la propuesta de valor de Moveo a lo que el mercado realmente demanda.

### 2.2.1. Diseño de entrevista 
Esta sección incluye preguntas demográficas, conductuales y psicográficas dirigidas a cada segmento, con el fin de construir arquetipos (personas) basados en evidencia real. Se aplican buenas prácticas de diseño de entrevistas: preguntas abiertas, no sugestivas, orden lógico (de lo general a lo específico) y enfoque en comportamientos reales, no hipotéticos.

Antes de realizar las entrevistas profundas, se aplicó un formulario digital (Google Forms) a todos los participantes con el objetivo de recolectar información demográfica y conductual básica. Esto permitió segmentar adecuadamente a los entrevistados, personalizar el enfoque de cada entrevista según su perfil, y optimizar el tiempo durante las sesiones cualitativas.

Formulario segmento Proveedores de Vehiculos: https://forms.gle/uyVSkqSiuiKx1nb69


Formulario segmento Inquilinos: https://forms.gle/kz3BdxPoZHKNgqUg9
#### **Segmento 1: Proveedores de Vehiculos** 

**Demográficas (para arquetipo):**
- ¿Cuál es tu nombre completo?
- ¿Qué edad tienes?
- ¿En qué distrito resides?
- ¿Cuál es tu género?
- ¿Cuál es tu estado civil?
- ¿Vives solo, con pareja, con hijos u otros familiares?
- ¿A qué te dedicas (trabajo, estudios, negocio propio)?

**Psicográficas y comportamentales (para arquetipo):**
- ¿Cómo describirías tu personalidad cuando se trata de prestar algo valioso (precavido, confiado, flexible, exigente)?
- ¿Qué marcas de autos confías más para alquilar? ¿Por qué?
- ¿Qué influencers, blogs, canales o redes sociales te influyen a la hora de tomar decisiones sobre tu auto o negocios?
- ¿Qué dispositivos usas con más frecuencia (celular, laptop, tablet)? ¿Qué apps o navegadores prefieres?
- ¿Por qué canales digitales sueles informarte o resolver dudas (WhatsApp, Instagram, Facebook, Google, foros)?

> *Nota: Estas preguntas fueron incluidas en el formulario inicial para identificar patrones de comportamiento digital y afinidades, lo que permitió guiar mejor las entrevistas profundas y construir arquetipos más precisos.*


**Necesidades y comportamiento (preguntas principales):**
- ¿Qué tipo de unidades sueles alquilar (auto, SUV, camioneta, moto, otro)?
- ¿Cuál es el tiempo mínimo y máximo que normalmente estás dispuesto a prestar tu vehículo?
- ¿Qué requisitos solicitas a una persona antes de entregarle tu vehículo?
- ¿Dónde publicas actualmente tus vehículos para alquilarlos (apps, redes sociales, conocidos)?
- ¿Cómo gestionas el control de tus autos disponibles y en uso (anotaciones, Excel, aplicación, otro)?
- ¿Qué tan confiable consideras que son las plataformas actuales para validar a los clientes?
- ¿Qué tan útil sería para ti ver comentarios de otros dueños sobre un cliente antes de alquilar?
- ¿Te interesaría contar con un panel digital donde registres todos tus autos y su estado?
- ¿Qué tan importante consideras poder calificar a los clientes después de cada alquiler?
- ¿Has tenido malas experiencias alquilando tu auto? Cuéntame qué pasó y qué aprendiste.

---
#### **Segmento 2: Clientes**

**Demográficas (para arquetipo):**
- ¿Cuál es tu nombre completo?
- ¿Qué edad tienes?
- ¿En qué distrito vives?
- ¿Cuál es tu género?
- ¿Cuál es tu estado civil?
- ¿Vives solo, con pareja, con hijos u otros familiares?
- ¿Cuál es tu ocupación principal?

**Psicográficas y comportamentales (para arquetipo):**
- ¿Cómo describirías tu estilo al tomar decisiones de consumo (espontáneo, investigador, influenciable, ahorrativo)?
- ¿Qué marcas de autos o servicios de alquiler prefieres o evitas? ¿Por qué?
- ¿Qué personas, influencers o medios digitales te ayudan a decidir antes de alquilar un auto?
- ¿Qué dispositivos usas con más frecuencia (celular, laptop, tablet)? ¿Qué apps o navegadores prefieres?
- ¿Por qué canales digitales sueles buscar soluciones o servicios (WhatsApp, Instagram, Google Maps, TikTok, foros)?

> *Nota: La información recolectada en el formulario permitió identificar segmentos de comportamiento digital y afinidades de marca, facilitando la construcción de arquetipos realistas y la personalización de las preguntas durante la entrevista.*


**Necesidades y comportamiento (preguntas principales):**
- ¿Qué documentos te han solicitado en tus experiencias previas al alquilar un auto?
- ¿Qué tipo de vehículo prefieres alquilar según tu necesidad (trabajo, viaje, ocasión especial)?
- ¿Qué requisitos o condiciones suelen ponerte antes de alquilar (edad mínima, tarjeta de crédito, otros)?
- ¿Qué factores te desaniman al momento de querer alquilar un auto (precio, desconfianza, restricciones, otro)?
- ¿Dónde sueles buscar opciones de autos en alquiler (apps, redes, páginas web, conocidos)?
- ¿Qué tan confías en que las aplicaciones muestran información real de los dueños y autos?
- ¿Qué tan valioso sería para ti revisar reseñas de otros usuarios sobre el dueño antes de alquilar?
- ¿Te resultaría útil poder reservar un vehículo con anticipación directamente desde la app?
- ¿Qué tan importante es para ti dejar una opinión sobre tu experiencia con el dueño o el vehículo?
- ¿Cuál ha sido tu peor experiencia alquilando un auto? ¿Qué cambiarías para evitarlo?


### 2.2.2. Registro de entrevistas

### 2.2.3. Análisis de Entrevistas 


## 2.3. Needfinding


### 2.3.1. User Persona


### 2.3.2. User Task Matrix


### 2.3.3. User Journey Mapping

### 2.3.4. Empathy Mapping 

### 2.3.5. As-is Scenario Mapping 

## 2.4. Ubiquitous Language

Arrendador:	Usuario que publica su vehículo para alquiler.

Arrendatario:	Usuario que alquila un vehículo disponible en la app.

Vehículo:	Entidad principal registrada por un arrendador.

Reserva:	Proceso mediante el cual un arrendatario aparta un vehículo en una fecha.

Publicación:	Objeto que contiene los datos visibles de un vehículo (precio, fotos, reglas).

Reseña:	Valoración escrita o numérica sobre el arrendador o vehículo.

Framework:	Conjunto de herramientas y librerías que usamos para construir la aplicación .

Entidad:	Objeto del dominio que tiene identidad propia .

Repositorio: Componente de software que gestiona la persistencia de

## 2.4. Requirements specification
### 2.4.1. User Stories
### 2.4.2. Impact Mapping
### 2.4.3. Product Backlog

## 2.5. Strategic-Level Domain-Driven Design
### 2.5.1. EventStorming
#### 2.5.1.1. Candidate Context Discovery
#### 2.5.1.2. Domain Message Flows Modeling
#### 2.5.1.3. Bounded Context Canvases
### 2.5.2. Context Mapping
### 2.5.3 Software Architecture

#### 2.5.3.1 Software Architecture Context Level Diagrams

El **Diagrama de Contexto** constituye el primer nivel de abstracción del Modelo C4. Su propósito fundamental es delimitar el alcance del sistema a construir, en este caso **WheelsPe**, y definir con claridad sus fronteras mediante la interacción con actores humanos y sistemas externos de terceros. Este diagrama proporciona una visión de alto nivel que permite comprender el rol estratégico de WheelsPe en el ecosistema de movilidad compartida sin profundizar en su complejidad técnica interna, lo que lo convierte en una herramienta de comunicación esencial tanto para los desarrolladores como para los inversionistas y demás partes interesadas del proyecto.

<p align="center">
  <img src="WheelsPe System Context.jpg" alt="WheelsPe System Context Diagram" width="100%">
</p>
<p align="center">
  <b>Figura 1:</b> Diagrama de Contexto del Sistema WheelsPe.
</p>

El diagrama de contexto de WheelsPe ilustra la dinámica entre los actores principales y las dependencias tecnológicas externas que hacen posible el servicio. Se identifican dos roles de usuario críticos:

* **Arrendatario / Pasajero:** Utiliza la plataforma para consultar el *Catálogo*, realizar *Reservas* y efectuar el *Pago*.
* **Proveedor / Conductor:** Responsable de registrar el *Vehículo*, publicar la *Ruta* y gestionar la *Liquidación* de sus ingresos.

En el ámbito de las integraciones, WheelsPe delega funciones especializadas en sistemas externos para garantizar la robustez del servicio. Se utiliza una **Pasarela de Pagos** para procesar transacciones y gestionar la *Comisión de plataforma*, mientras que el **Servicio de Verificación** asegura que cada perfil alcance el estado de *Usuario verificado* mediante el proceso de *Verificación de identidad*. Asimismo, se integra el **Servicio de Notificaciones** para el envío de *Alertas de emergencia* y el cumplimiento del protocolo de seguridad, junto con una **API de Mapas** para optimizar la *Coincidencia de ruta* en los trayectos compartidos. Toda la comunicación entre estos componentes se realiza bajo protocolos seguros, garantizando la confidencialidad de la *Bitácora de eventos* y la integridad de la información del usuario.

---

#### 2.5.3.2 Software Architecture Container Level Diagrams

En esta vista, se observa que la **WheelsPe Platform** está compuesta por tres contenedores principales que interactúan de forma desacoplada:

1.  **Mobile Application:** (Desarrollada en Kotlin/Swift) Actúa como la interfaz de usuario donde el Arrendatario y el Proveedor gestionan el *Catálogo*, sus *Rutas* y su *Reputación*.
2.  **API Application:** El núcleo de la plataforma construido sobre **C# y ASP.NET Core**. Este contenedor es el responsable de orquestar la lógica de negocio compleja, incluyendo la *Reserva de asiento*, el cálculo de *Precio dinámico* y la *Coincidencia de ruta*. Se comunica con el frontend mediante el protocolo **JSON/HTTPS**.
3.  **Database:** (MySQL) Donde se resguarda la *Bitácora de eventos*, el historial de *Pagos* y la persistencia de toda la información del sistema.

<p align="center">
  <img src="WheelsPe Containers.jpg" alt="WheelsPe Containers Diagram" width="100%">
</p>
<p align="center">
  <b>Figura 2:</b> Diagrama de Contenedores de la plataforma WheelsPe.
</p>

Finalmente, la **API Application** es la encargada de consumir los sistemas externos, enviando peticiones para la *Verificación de identidad (KYC)*, consultando trayectos en la **API de Mapas** y gestionando la *Liquidación al proveedor* a través de la **Pasarela de Pagos**, asegurando un entorno operativo integrado y eficiente.

---

#### 2.5.3.3 Software Architecture Deployment Diagrams

Dentro de la **API Application**, la arquitectura se organiza en tres capas claramente diferenciadas:

* **Capa de Interfaz:** Expone los controladores *User & Auth*, *Vehicle* y *Rental & Carpool*, los cuales gestionan los endpoints para procesos como la *Acreditación de vehículo* y la *Confirmación de reserva*.
* **Capa de Aplicación y Dominio:** Donde el *Identity Service* valida el estado de *Usuario verificado* mediante tokens **JWT** y la *WheelsPe Domain Logic* aplica las reglas críticas de *Reputación*, *Precio dinámico* y *Coincidencia de ruta*.
* **Capa de Infraestructura:** Utiliza el *Data Repository* para centralizar el acceso a la *Database* mediante **Entity Framework Core**, mientras coordina las salidas hacia sistemas externos: el *Servicio de Verificación* para el proceso KYC, la *API de Mapas* para la navegación y la *Pasarela de Pagos* para ejecutar la *Liquidación al proveedor*.

<p align="center">
  <img src="WheelsPe Component.jpg" alt="WheelsPe Component Diagram" width="100%">
</p>
<p align="center">
  <b>Figura 3:</b> Diagrama de Componentes de la API Application.
</p>

Esta estructura garantiza que la lógica central de WheelsPe permanezca aislada de los detalles de implementación tecnológica, facilitando la evolución independiente de cada componente.

## 2.6. Tactical-Level Domain-Driven Design

### 2.6.1. Bounded Context: Identity & Access Management (IAM)

#### 2.6.1.1. Domain Layer

* **Usuario (Entity):** Es la entidad principal que representa a la persona en la plataforma. Posee una identidad persistente y es el corazón del agregado GestionIdentidad.
    * **Atributos:** `idUsuario`, `nombreCompleto`, `correoElectronico`, `telefono`, `rol` (Proveedor o Usuario), `estadoVerificacion`.
    * **Métodos:**
        * `actualizarPerfilBasico(nuevoNombre, nuevoTelefono)`: Modifica datos de contacto validando que no sean nulos y cumplan el formato telefónico.
        * `cambiarRol(nuevoRol)`: Ejecuta la transición de funciones asegurando que no haya servicios activos y reiniciando el estado de verificación si es necesario.
        * `actualizarEstadoVerificacion(nuevoEstado)`: Cambia la fase del proceso KYC (Pendiente, Verificado, Rechazado).

* **DocumentoIdentidad (Value Object):** Contiene la información inmutable de los documentos legales para la acreditación de confianza.
    * **Atributos:** `tipoDocumento`, `numero`, `fechaVencimiento`, `urlImagenFrontal`.
    * **Métodos:** `validarVigencia()`.

* **Reputacion (Entity):** Entidad que encapsula el comportamiento histórico del usuario para generar confianza digital.
    * **Atributos:** `idReputacion`, `puntajePromedio`, `totalCalificaciones`.
    * **Métodos:** `recalcularPromedio(puntos)`, `evaluarEstadoCritico()`.

* **GestionIdentidad (Aggregate):** Raíz que agrupa al Usuario, su Reputacion y sus Documentos. Asegura que solo usuarios verificados realicen acciones críticas.
    * **Métodos:** `iniciarProcesoKYC()`, `validarCapacidadOperativa()`.

* **ValidadorIdentidad (Domain Service):** Lógica compleja que compara los datos del DNI con la identidad del perfil para prevenir suplantaciones.

* **UsuarioRepository (Repository):** Define el contrato para persistir perfiles y buscar usuarios por credenciales.

#### 2.6.1.2. Interface Layer

* **RegistroController (Controller):** Expone el endpoint para la creación de perfiles con selección de rol.
    * **Métodos:** `registrarUsuario(UserDTO)`.
* **PerfilController (Controller):** Gestiona la visualización y edición de la información del usuario.
    * **Métodos:** `obtenerPerfil()`, `editarPerfilBasico()`.
* **VerificacionController (Controller):** Interfaz para el envío de documentos de identidad.
    * **Métodos:** `enviarEvidenciaKYC()`.
* **UserResponse (DTO):** Objeto que retorna al frontend los datos del perfil, ocultando información sensible como hashes de contraseñas.

#### 2.6.1.3. Application Layer

* **AutenticacionService (Application Service):** Orquesta el flujo de login comunicándose con el proveedor de seguridad externo.
    * **Métodos:** `iniciarSesion()`, `renovarToken()`.
* **GestionPerfilService (Application Service):** Coordina la actualización de datos llamando a los métodos del dominio y persistiendo en el repositorio.
    * **Métodos:** `actualizarDatosContacto()`.
* **NotificadorSeguridadHandler (Event Handler):** Reacciona a eventos como `IdentidadVerificada` para enviar notificaciones push de éxito al usuario.

#### 2.6.1.4. Infrastructure Layer

* **MySqlUserRepository (Implementation):** Implementación técnica del repositorio que utiliza un ORM para realizar operaciones CRUD en la base de datos MySQL.
* **FirebaseAuthAdapter (External Service):** Adaptador que conecta con Firebase para delegar la autenticación robusta y la gestión de sesiones.
* **S3StorageAdapter (External Service):** Implementación encargada de subir y recuperar las imágenes de los documentos en el almacenamiento en la nube.

#### 2.6.1.5 Bounded Context Software Architecture Component Level Diagrams

Este diagrama representa la arquitectura del Bounded Context de **IAM** (Identity & Access Management) bajo el enfoque de Domain-Driven Design...

<p align="center">
  <img src="WheelsPe Bounded Context Iam.png" alt="IAM Component Diagram" width="100%">
</p>
<p align="center">
  <b>Figura 5:</b> Diagrama de Componentes del Bounded Context IAM.
</p>

#### 2.6.1.6 Bounded Context Software Architecture Code Level Diagrams

##### 2.6.1.6.1 Bounded Context Domain Layer Class Diagrams

Este diagrama representa la arquitectura de clases del dominio para IAM, detallando la relación entre el Agregado de Usuario, sus Objetos de Valor y la Reputación...

<p align="center">
  <img src="Bounded Context Domain Layer Class Diagrams IAM.jpeg" alt="IAM Domain Class Diagram" width="100%">
</p>
<p align="center">
  <b>Figura 6:</b> Diagrama de Clases de la Capa de Dominio - IAM.
</p>

##### 2.6.1.6.2 Bounded Context Database Design Diagram

Este diagrama representa el modelo lógico de datos para el Bounded Context de IAM, diseñado bajo un enfoque relacional que prioriza la integridad de la identidad...

<p align="center">
  <img src="Bounded Context Database Design Diagram IAM.jpeg" alt="IAM Database Design" width="100%">
</p>
<p align="center">
  <b>Figura 7:</b> Modelo Entidad-Relación para el Bounded Context IAM.
</p>

### 2.6.2. Bounded Context: Carpooling
#### 2.6.2.1. Domain Layer
#### 2.6.2.2. Interface Layer
#### 2.6.2.3. Application Layer
#### 2.6.2.4. Infrastructure Layer
#### 2.6.2.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.2.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.2.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.2.6.2. Bounded Context Database Design Diagram

### 2.6.3. Bounded Context: Rental
#### 2.6.3.1. Domain Layer
#### 2.6.3.2. Interface Layer
#### 2.6.3.3. Application Layer
#### 2.6.3.4. Infrastructure Layer
#### 2.6.3.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.3.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.3.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.3.6.2. Bounded Context Database Design Diagram

### 2.6.4. Bounded Context: Billing
#### 2.6.4.1. Domain Layer
#### 2.6.4.2. Interface Layer
#### 2.6.4.3. Application Layer
#### 2.6.4.4. Infrastructure Layer
#### 2.6.4.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.4.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.4.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.4.6.2. Bounded Context Database Design Diagram

### 2.6.5. Bounded Context: Operations
#### 2.6.5.1. Domain Layer
#### 2.6.5.2. Interface Layer
#### 2.6.5.3. Application Layer
#### 2.6.5.4. Infrastructure Layer
#### 2.6.5.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.5.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.5.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.5.6.2. Bounded Context Database Design Diagram
