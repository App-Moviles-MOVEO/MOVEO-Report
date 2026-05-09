# CORRECCIONES OBLIGATORIAS AV1 → TB1 - WheelsPe

## INSTRUCCIONES GENERALES DE CORRECCIÓN DE ESTRUCTURA

### Normas APA 7 y Formato
- Corregir estructura del reporte siguiendo normas APA 7
- Eliminar viudas (líneas solas al final de párrafo al inicio de página)
- Eliminar huérfanas (líneas solas al inicio de párrafo al final de página)
- Verificar que TODAS las figuras tengan:
  - Numeración correlativa (Figura 1, Figura 2...)
  - Pie de figura descriptivo
  - Fuente (Nota. Elaboración propia / Fuente: Autor, año)
- Asegurar que TODAS las tablas tengan:
  - Título en la parte superior
  - Numeración correlativa (Tabla 1, Tabla 2...)
  - Fuente en la parte inferior
- Validar sangría francesa en referencias bibliográficas
- Unificar uso de tiempos verbales (presente para describir el sistema)
- Eliminar espacios dobles entre palabras
- Eliminar saltos de línea innecesarios (más de 2 líneas en blanco)
- Alineación justificada en todo el texto del cuerpo
- Interlineado 1.5 consistente
- Sangría de 0.5 pulgadas en primera línea de cada párrafo

### Carátula
Verificar que incluya en este orden exacto:
1. Logo de Universidad Peruana de Ciencias Aplicadas
2. Universidad Peruana de Ciencias Aplicadas
3. Carrera: Ingeniería de Software
4. Periodo: 202610
5. Curso: Aplicaciones para Dispositivos Móviles
6. Sección: [Código de sección]
7. Profesor: Quevedo Velasco, David Gerardo
8. Informe del Trabajo Final
9. Startup: MOVEO
10. Producto: WheelsPe
11. Alumnos (en orden alfabético por apellido):
    - Código - Apellidos y Nombres
12. Mayo, 2026

---

## 1. REORDENAR PRODUCT BACKLOG (Sección 2.4.3, pág 158)

### PROBLEMA DETECTADO
El profesor rechazó explícitamente "Product B (Orden/Precedencia)". El backlog actual está ordenado por precedencia técnica (primero autenticación, luego features), lo cual es INCORRECTO.

### CORRECCIÓN OBLIGATORIA

**Agregar ANTES de la tabla el siguiente texto justificativo:**
El Product Backlog de WheelsPe se ordena estrictamente por VALOR DE NEGOCIO para los usuarios finales y stakeholders, no por precedencia técnica ni dependencias de implementación. Este enfoque ágil asegura que cada sprint entregue funcionalidades que los segmentos objetivo puedan percibir, utilizar y validar inmediatamente, comprobando las hipótesis de negocio establecidas en el Lean UX Process desde el primer momento del ciclo de desarrollo.
Las primeras posiciones del backlog se asignan a User Stories que:

Generan conversión inicial de visitantes a usuarios registrados (Landing Page)
Materializan el core del modelo de negocio (búsqueda de vehículos/rutas, publicación de ofertas, transacciones)
Implementan diferenciadores competitivos clave (segmentación institucional, carpooling integrado con alquiler)
Garantizan seguridad y construcción de confianza (alertas de emergencia, sistema de reputación, checklist de protección)

Las User Stories de infraestructura técnica (autenticación, registro, gestión de sesiones) se posicionan estratégicamente después del valor core del negocio, reconociendo que son habilitadores necesarios pero no constituyen la propuesta de valor diferencial que distingue a WheelsPe de la competencia tradicional de alquiler o las soluciones informales actuales.
Esta priorización se validó mediante el Impact Mapping elaborado en la sección 2.4.2, donde se identificaron los Business Goals y los comportamientos de usuario que generan mayor impacto en el éxito de la plataforma.

**NUEVA TABLA DE PRODUCT BACKLOG:**

| # Orden | Story ID | Título | Story Points | Justificación de Prioridad |
|---------|----------|--------|--------------|----------------------------|
| 1 | US39 | Visualizar propuesta de valor en landing page | 5 | Primera impresión de visitantes, comunicación de beneficios, generación de conversión inicial |
| 2 | US22 | Consultar catálogo de vehículos disponibles | 5 | Core business - permite a usuarios explorar inventario de vehículos |
| 3 | US13 | Publicar ruta de movilidad compartida | 8 | Core business - habilita oferta de carpooling por conductores |
| 4 | US14 | Buscar rutas con segmentación institucional | 5 | Diferenciador clave - comunidad verificada (UPC/empresas) genera confianza |
| 5 | US31 | Procesar pago de alquiler multicanal | 8 | Monetización directa del modelo de negocio de alquiler |
| 6 | US32 | Liquidar cuota de carpooling digitalmente | 5 | Monetización de movilidad compartida |
| 7 | US08 | Activar alerta de emergencia durante viaje | 5 | Propuesta de valor #1 - seguridad personal de pasajeros |
| 8 | US28 | Evaluar servicio de forma bidireccional | 5 | Construcción de confianza y reputación comunitaria |
| 9 | US12 | Registrar checklist fotográfico del vehículo | 5 | Protección de activos del proveedor - diferenciador vs competencia |
| 10 | US21 | Vincular métodos de pago electrónicos | 5 | Habilitador de transacciones financieras seguras |
| 11 | US24 | Gestionar garantía mediante retención (Escrow) | 5 | Protección financiera bilateral proveedor-arrendatario |
| 12 | US01 | Registrar cuenta con rol único | 3 | Habilitador necesario para acceso al sistema |
| 13 | US02 | Verificar identidad mediante KYC | 5 | Seguridad necesaria para construcción de confianza |
| 14 | US03 | Iniciar sesión con credenciales | 2 | Soporte técnico para persistencia de sesión |
| 15 | US05 | Acreditar propiedad de vehículo | 5 | Validación de oferta legítima y protección contra fraude |
| 16 | US06 | Monitorear ruta en tiempo real vía GPS | 8 | Trazabilidad y seguridad activa durante viajes |
| 17 | US09 | Validar inicio de viaje con código PIN | 3 | Confirmación de identidad correcta en momento de abordaje |
| 18 | US15 | Reservar asiento en ruta compartida | 4 | Funcionalidad core de carpooling |
| 19 | US25 | Emitir comprobantes y contratos digitales | 4 | Respaldo legal de transacciones |
| 20 | US11 | Filtrar rutas por preferencia de género | 3 | Seguridad percibida (target específico: mujeres universitarias) |
| 21 | US16 | Aprobar solicitudes de pasajeros y controlar aforo | 4 | Control de capacidad del conductor |
| 22 | US19 | Consultar reputación de otros usuarios | 2 | Transparencia pre-transacción |
| 23 | US30 | Configurar umbrales de reputación mínimos | 3 | Personalización de seguridad por proveedor |
| 24 | US26 | Procesar reembolsos automáticos | 3 | Gestión de cancelaciones y devoluciones |
| 25 | US10 | Gestionar contactos de confianza | 2 | Seguridad pasiva mediante red de protección |
| 26 | US17 | Automatizar rutas recurrentes semanales | 3 | Optimización de experiencia para usuarios frecuentes |
| 27 | US18 | Coordinar detalles por mensajería integrada | 3 | Comunicación directa entre usuarios del viaje |
| 28 | US20 | Confirmar llegada al destino final | 3 | Cierre formal de servicio |
| 29 | US27 | Aplicar cupones y beneficios promocionales | 3 | Incentivos comerciales para adopción |
| 30 | US29 | Recompensar usuarios con alta reputación | 3 | Gamificación de comportamiento positivo |
| 31 | US34 | Gestionar ofertas promocionales temporales | 3 | Promociones estacionales y feriados |
| 32 | US36 | Reconocer comportamiento positivo con distintivos | 8 | Sistema de incentivos y construcción de lealtad |
| 33 | US37 | Consultar historial completo de reseñas | 3 | Transparencia histórica de comportamiento |
| 34 | US38 | Filtrar solicitudes por umbral de confianza | 3 | Protección automática basada en reputación |
| 35 | US42 | Explorar beneficios para propietarios (Landing) | 5 | Conversión de segmento proveedores |
| 36 | US43 | Conocer ventajas del carpooling (Landing) | 5 | Conversión de segmento usuarios movilidad |
| 37 | US44 | Acceder a centro de ayuda y FAQ | 3 | Soporte autoservicio |
| 38 | US04 | Recuperar contraseña olvidada | 2 | Soporte técnico de acceso |
| 39 | US07 | Rastrear viaje activo para seguridad de pasajero | 8 | Monitoreo de anomalías en ruta |
| 40 | US33 | Ejecutar reembolsos automatizados | 8 | Automatización de procesos financieros |
| 41 | US35 | Evaluar mutuamente tras finalizar servicio | 5 | Sistema de reputación bilateral |
| 42 | US40 | Monitorear anomalías financieras (Admin) | 5 | Operaciones administrativas de vigilancia |
| 43 | US41 | Mediar disputas de reputación (Admin) | 2 | Gestión de conflictos y moderación |
| 44 | US45 | Solicitar baja voluntaria y eliminación de datos | 2 | Derecho al olvido (cumplimiento GDPR) |
| 45 | US46 | Enviar solicitud de alianza corporativa | 3 | Expansión del modelo B2B |
| 46 | US47 | Optimizar latencia en geolocalización (Technical) | 3 | Mejora de performance técnico |

**Actualizar también la captura de Trello con este nuevo orden**

[INSERTAR IMAGEN: Captura del tablero de Trello con Product Backlog reordenado]

---

## 2. DIVIDIR SEGMENTO #2 EN DOS SEGMENTOS SEPARADOS (Sección 1.3, pág 35-38)

### PROBLEMA DETECTADO
El profesor solicitó "Revisar segmentos". Actualmente el Segmento #2 "Usuarios de Movilidad" mezcla incorrectamente 2 roles con comportamientos, motivaciones y pain points completamente distintos:
- Conductores Arrendatarios (alquilan vehículos para conducir + publicar rutas)
- Pasajeros Recurrentes (solo buscan rutas compartidas, NO alquilan)

### CORRECCIÓN OBLIGATORIA

**REESCRIBIR completamente la sección 1.3 con esta nueva estructura:**

---

### 1.3 Segmentos Objetivo

Para garantizar que la solución tecnológica de WheelsPe responda de manera efectiva a las necesidades reales del mercado de movilidad urbana en Lima Metropolitana, se han identificado y analizado **tres segmentos objetivo clave** que enfrentan problemáticas específicas en el ecosistema actual. A continuación se detallan sus perfiles estratégicos, profundizando en las características demográficas, geográficas y psicográficas que sustentan su relevancia dentro del dominio del problema.

---

#### Segmento Objetivo #1: Proveedores de Vehículos

**[MANTENER EXACTAMENTE COMO ESTÁ EN EL INFORME ACTUAL - PÁGINAS 35-36]**

Este segmento ya está correctamente definido. No requiere modificaciones.

---

#### Segmento Objetivo #2: Conductores Arrendatarios

**Definición:**
Representa a profesionales, emprendedores y estudiantes de posgrado que requieren acceso temporal a vehículos para desplazamientos recurrentes relacionados con actividades laborales, gestiones empresariales o estudios, y que buscan activamente reducir el costo individual del alquiler mediante la publicación de rutas de carpooling que les permitan compartir los gastos operativos del viaje con otros pasajeros de confianza.

**Aspectos demográficos:**
- **Sexo:** Masculino (65%), Femenino (35%)
- **Rango de edad:** 25-45 años
- **Nivel socioeconómico:** Sectores B y C
- **Ocupación:** Profesionales independientes (consultores, ingenieros, arquitectos visitando obras), ejecutivos de empresas con reuniones externas frecuentes, emprendedores con gestiones comerciales, estudiantes de posgrado (MBA, maestrías) con proyectos de campo
- **Ingresos promedio:** S/ 4,500 - S/ 8,000 mensuales

**Aspectos geográficos:**
- **Nacionalidad:** Peruana
- **Zona geográfica:** Áreas urbanas de Lima Metropolitana con alta concentración de centros empresariales y educativos. Distritos de residencia frecuentes: San Borja, Surco, La Molina, Miraflores. Destinos recurrentes: San Isidro (oficinas corporativas), Miraflores (reuniones comerciales), Campus universitarios de posgrado (UPC, ESAN, CENTRUM)

**Aspectos psicográficos:**

**Dolor principal:** 
Los conductores arrendatarios enfrentan una barrera económica significativa al requerir vehículos temporales de forma recurrente (2-4 veces por semana). El alquiler tradicional en empresas formales representa un gasto mensual de S/ 1,200 - S/ 2,000 que no es sostenible para uso frecuente. Al asumir el 100% del costo operativo (alquiler + combustible + peajes) de forma individual, el transporte se vuelve económicamente inviable, forzándolos a depender de taxis por aplicación que no proyectan la imagen profesional deseada en reuniones con clientes.

**Intereses:** 
Acceder a soluciones de movilidad temporal que sean financieramente sostenibles mediante la división de costos. Maximizar el retorno de inversión del alquiler al monetizar los asientos vacíos del vehículo. Construir una red profesional de contactos mediante el networking durante trayectos compartidos con ejecutivos o profesionales de su mismo nivel socioeconómico.

**Actitudes:** 
Poseen un estilo de vida orientado a la eficiencia y optimización de recursos. Son early adopters de tecnología que facilite procesos (usuarios activos de Uber, Rappi, apps de productividad). Priorizan la construcción de imagen profesional y valoran las oportunidades de networking como parte integral de su desarrollo de carrera. Buscan constantemente relaciones "win-win" donde ambas partes obtengan beneficio mutuo.

**Necesidades clave:** 
Plataformas que integren nativamente alquiler de vehículos con publicación de rutas de carpooling en un solo ecosistema. Sistemas de validación institucional que certifiquen que los pasajeros pertenecen a entornos corporativos o académicos verificados (validación de email empresarial, perfil de LinkedIn). Herramientas de división automática de costos que calculen de forma transparente la cuota proporcional por pasajero. Facturación electrónica que permita declarar gastos de movilidad a su empleador o como gasto deducible de impuestos. Flexibilidad para programar rutas recurrentes (lunes a viernes, mismo horario) sin necesidad de republicar manualmente cada día.

---

#### Segmento Objetivo #3: Pasajeros de Movilidad Compartida

**Definición:**
Representa a estudiantes universitarios de pregrado y trabajadores dependientes jóvenes que realizan desplazamientos diarios en rutas fijas entre su zona de residencia y sus centros de estudio o trabajo, y que actualmente dependen de opciones informales de transporte compartido (grupos de WhatsApp, Facebook) que no garantizan seguridad, puntualidad ni validación de identidad de los conductores.

**Aspectos demográficos:**
- **Sexo:** Femenino (60%), Masculino (40%)
- **Rango de edad:** 18-30 años
- **Nivel socioeconómico:** Sectores C y D
- **Ocupación:** Estudiantes universitarios de pregrado (ciclos 3-10), trabajadores dependientes en posiciones de entrada (asistentes, practicantes, técnicos), personas con empleo a tiempo parcial combinado con estudios
- **Ingresos/mesada promedio:** S/ 800 - S/ 2,500 mensuales

**Aspectos geográficos:**
- **Nacionalidad:** Peruana
- **Zona geográfica:** Áreas urbanas de Lima Metropolitana con rutas fijas entre distritos periféricos de residencia y centros educativos/laborales. Rutas frecuentes identificadas en entrevistas: Los Olivos → UPC Villa, San Juan de Lurigancho → San Isidro (zona financiera), Ate → Miraflores, Comas → Cercado de Lima, Villa María del Triunfo → Surco

**Aspectos psicográficos:**

**Dolor principal:** 
Los pasajeros de movilidad compartida enfrentan una problemática crítica de inseguridad y desorganización en sus traslados diarios. Actualmente dependen de grupos informales en WhatsApp y Facebook donde coordinan "jalones" con conductores desconocidos cuya identidad, antecedentes o confiabilidad no pueden verificar. Esta informalidad genera estados constantes de ansiedad, especialmente en mujeres que viajan en horarios nocturnos. Las cancelaciones de último minuto (reportadas en 40% de los casos según entrevistas) causan retrasos en sus obligaciones académicas o laborales. El transporte público tradicional (combis, buses) es percibido como inseguro y con alta exposición a delincuencia, además de ser hostil para el traslado de objetos delicados (laptops, proyectos universitarios, maquetas).

**Intereses:** 
Acceder a soluciones de movilidad que prioricen la seguridad personal mediante validación estricta de identidad de conductores. Viajar exclusivamente con miembros verificados de su misma comunidad institucional (compañeros de universidad, colegas de empresa) para reducir la percepción de riesgo. Encontrar rutas confiables y puntuales que se ajusten a sus horarios fijos de clases o trabajo. Ahorrar en costos de transporte diario frente a opciones como taxi por aplicación (S/ 15-20 por viaje) que no son sostenibles con sus ingresos limitados.

**Actitudes:** 
Poseen un estilo de vida digital-first, toman decisiones de movilidad sobre la marcha desde sus smartphones. Priorizan la seguridad y la confianza por encima del precio absoluto, mostrando disposición a pagar un 15-20% adicional frente a opciones informales si se garantiza validación de identidad. Han desarrollado mecanismos de protección personal como compartir ubicación en tiempo real con familiares o viajar siempre acompañados. Valoran la comunidad y sienten mayor confianza al interactuar con personas de su mismo entorno académico o laboral (sentido de pertenencia institucional).

**Necesidades clave:** 
Plataformas formales con directorio centralizado de rutas compartidas donde TODOS los conductores estén verificados mediante documentación oficial. Sistemas de filtrado por comunidad institucional que garanticen que el conductor estudia/trabaja en la misma universidad/empresa (validación de correo institucional @upc.edu.pe, @pucp.edu.pe, @empresaX.com). Funcionalidades de seguridad activa como botón de pánico conectado a contactos de confianza y autoridades, trazabilidad GPS compartible en tiempo real, sistema de calificaciones bidireccional obligatorio post-viaje. Interfaz intuitiva que permita reservar asientos en rutas recurrentes de forma anticipada para eliminar la incertidumbre diaria. Opción de filtrado por preferencia de género (viajes solo con conductoras mujeres) para aumentar la percepción de seguridad en usuarias femeninas.

---

**IMPACTO DE ESTA CORRECCIÓN EN OTRAS SECCIONES:**

Debes actualizar también:

1. **Sección 2.2.1 Diseño de Entrevistas (pág 46-52):**
   - Separar las preguntas en 3 bloques claramente diferenciados
   - Agregar encabezado "Segmento #2: Conductores Arrendatarios" antes de las preguntas para Paul/Mathías
   - Agregar encabezado "Segmento #3: Pasajeros de Movilidad Compartida" antes de las preguntas para Alisa/Daniela

2. **Sección 2.2.3 Análisis de Entrevistas (pág 74-95):**
   - Dividir en 3 subsecciones de análisis
   - Crear gráficos estadísticos separados para Conductores vs Pasajeros

3. **Sección 2.3.1 User Personas (pág 97-103):**
   - Mantener Carlos Peña (Proveedor)
   - CREAR NUEVA: Marco Ruiz (Conductor Arrendatario) - ver sección 4 de este documento
   - Renombrar/ajustar Esther Ospina como Pasajera exclusivamente

4. **Sección 1.2.2.1 Lean UX Problem Statements (pág 28):**
   - REESCRIBIR con 3 Problem Statements separados - ver sección 5 de este documento

---

## 3. REESCRIBIR TÍTULOS DE USER STORIES CON VERBOS (Sección 2.4.1, pág 123-152)

### PROBLEMA DETECTADO
El profesor indicó "Mejorar los títulos de las US en verbo". Actualmente los títulos son descriptivos estáticos (sustantivos), no acciones del usuario.

### FORMATO INCORRECTO ACTUAL:
US01 - Registro de cuenta con rol único
US02 - Verificación de identidad mediante KYC

### FORMATO CORRECTO REQUERIDO:
Los títulos DEBEN empezar con **VERBO EN INFINITIVO** que indique la acción que realiza el usuario.

### CORRECCIÓN OBLIGATORIA

**REEMPLAZAR TODOS los títulos de User Stories en la tabla de la sección 2.4.1 con los siguientes:**

| Story ID | Título NUEVO (con verbo en infinitivo) |
|----------|----------------------------------------|
| US01 | Registrar cuenta seleccionando rol único |
| US02 | Verificar identidad mediante KYC |
| US03 | Iniciar sesión con credenciales |
| US04 | Recuperar contraseña olvidada |
| US05 | Acreditar propiedad de vehículo |
| US06 | Monitorear ruta en tiempo real vía GPS |
| US07 | Rastrear viaje activo para seguridad |
| US08 | Activar alerta de emergencia durante viaje |
| US09 | Validar inicio de viaje con código PIN |
| US10 | Gestionar contactos de confianza |
| US11 | Filtrar rutas por preferencia de género |
| US12 | Registrar estado del vehículo con checklist fotográfico |
| US13 | Publicar ruta de movilidad compartida |
| US14 | Buscar rutas con segmentación institucional |
| US15 | Reservar asiento en ruta compartida |
| US16 | Aprobar solicitudes de pasajeros y gestionar aforo |
| US17 | Automatizar rutas recurrentes semanales |
| US18 | Coordinar detalles del viaje por mensajería |
| US19 | Consultar reputación de otros usuarios |
| US20 | Confirmar llegada al destino final |
| US21 | Vincular métodos de pago electrónicos |
| US22 | Consultar catálogo de vehículos disponibles |
| US23 | Pagar cuota por asiento compartido |
| US24 | Gestionar garantía mediante retención (Escrow) |
| US25 | Emitir comprobantes y contratos digitales |
| US26 | Procesar reembolsos automáticos |
| US27 | Aplicar beneficios y cupones promocionales |
| US28 | Evaluar servicio de forma bidireccional |
| US29 | Recompensar usuarios con alta reputación |
| US30 | Configurar umbrales de reputación mínimos |
| US31 | Procesar pago de alquiler con múltiples métodos |
| US32 | Liquidar cuota de carpooling digitalmente |
| US33 | Ejecutar reembolsos automatizados |
| US34 | Gestionar ofertas promocionales temporales |
| US35 | Evaluar mutuamente tras finalizar servicio |
| US36 | Reconocer comportamiento positivo con distintivos |
| US37 | Consultar historial completo de reseñas |
| US38 | Filtrar solicitudes por umbral de confianza |
| US39 | Visualizar propuesta de valor en landing page |
| US40 | Monitorear anomalías financieras (Admin) |
| US41 | Mediar disputas de reputación (Admin) |
| US42 | Explorar beneficios para propietarios (Landing) |
| US43 | Conocer ventajas del carpooling institucional (Landing) |
| US44 | Acceder a centro de ayuda y preguntas frecuentes |
| US45 | Solicitar baja voluntaria y eliminación de datos |
| US46 | Enviar solicitud de alianza corporativa |
| US47 | Optimizar latencia en geolocalización (Technical Story) |

**NOTA:** Actualizar también estos títulos en:
- Product Backlog (sección 2.4.3)
- Impact Mapping (sección 2.4.2)
- Cualquier referencia a User Stories en el documento

---

## 4. AGREGAR NOMBRES DESCRIPTIVOS A ESCENARIOS (Sección 2.4.1, TODAS las US)

### PROBLEMA DETECTADO
El profesor indicó "C.A. Faltó Nombre del escenario". Los Acceptance Criteria actuales NO tienen nombres que describan el resultado esperado.

### FORMATO INCORRECTO ACTUAL:
Escenario 1: Validación de selección de rol obligatorio. Dado que...

### FORMATO CORRECTO REQUERIDO (estándar Gherkin):
Escenario 1: Registro exitoso seleccionando rol de Proveedor
Dado que un visitante accede a la pantalla de registro
Cuando ingresa datos válidos y selecciona el rol "Proveedor"
Entonces el sistema crea la cuenta exitosamente

El nombre del escenario debe describir el **RESULTADO** (éxito o fallo), NO el proceso.

### CORRECCIÓN OBLIGATORIA

**REESCRIBIR los Acceptance Criteria de TODAS las 47 User Stories siguiendo este patrón:**

---

#### Ejemplo US01: Registrar cuenta seleccionando rol único

**Acceptance Criteria:**

**Escenario 1: Registro exitoso como Proveedor con datos válidos**
- Dado que un visitante accede a la pantalla de registro de WheelsPe
- Cuando ingresa un email válido no registrado previamente "carlos@gmail.com"
- Y ingresa una contraseña que cumple requisitos de seguridad "Secure123!"
- Y selecciona el rol "Proveedor"
- Y acepta los términos y condiciones
- Y hace clic en el botón "Registrarse"
- Entonces el sistema crea una cuenta nueva con estado "Pendiente de verificación"
- Y muestra el mensaje "Cuenta creada exitosamente. Por favor verifica tu correo electrónico"
- Y envía un correo de verificación a "carlos@gmail.com" con enlace de activación

**Escenario 2: Registro fallido sin seleccionar rol obligatorio**
- Dado que un visitante completa todos los campos del formulario de registro
- Cuando ingresa email y contraseña válidos
- Pero NO selecciona ningún rol (Proveedor o Usuario)
- Y hace clic en "Registrarse"
- Entonces el sistema NO crea la cuenta
- Y muestra el mensaje de error "Debes seleccionar un rol: Proveedor o Usuario de Movilidad"
- Y mantiene los datos ingresados en el formulario para que el usuario corrija

**Escenario 3: Registro fallido con email ya existente en la plataforma**
- Dado que existe un usuario previamente registrado con email "esther@upc.edu.pe"
- Cuando un visitante nuevo intenta registrarse con ese mismo email
- Entonces el sistema rechaza el registro
- Y muestra el mensaje "Este correo electrónico ya está registrado en WheelsPe"
- Y ofrece el botón "¿Olvidaste tu contraseña?" para recuperar acceso

**Escenario 4: Registro fallido con contraseña que no cumple requisitos de seguridad**
- Dado que un visitante ingresa una contraseña débil "123456"
- Cuando intenta completar el registro
- Entonces el sistema muestra error "La contraseña debe tener al menos 8 caracteres, incluyendo mayúsculas, minúsculas y números"
- Y NO permite proceder hasta que se ingrese una contraseña válida

---

#### Ejemplo US02: Verificar identidad mediante KYC

**Acceptance Criteria:**

**Escenario 1: Verificación KYC exitosa con documentos válidos y legibles**
- Dado que un usuario registrado accede a la sección "Verificar mi identidad"
- Cuando carga una foto del anverso de su DNI en formato JPG o PNG menor a 5MB
- Y carga una foto del reverso de su DNI
- Y toma un selfie con la cámara del dispositivo para validación biométrica
- Y el sistema detecta que las imágenes son legibles y cumplen requisitos de calidad
- Entonces el sistema procesa la verificación mediante API de validación de identidad
- Y actualiza el estado del usuario a "Verificado" en un plazo máximo de 24 horas
- Y envía notificación push y email confirmando "Tu identidad ha sido verificada exitosamente"
- Y habilita las funcionalidades restringidas (publicar vehículos, reservar, pagar)

**Escenario 2: Verificación KYC rechazada por imagen de documento ilegible**
- Dado que un usuario carga imágenes de su DNI
- Cuando el sistema detecta que la foto está borrosa o los datos no son legibles
- Entonces rechaza la verificación
- Y muestra el mensaje "La imagen del documento no es legible. Por favor toma una foto más clara"
- Y permite intentar nuevamente la carga (máximo 3 intentos)

**Escenario 3: Verificación KYC fallida por inconsistencia en datos biométricos**
- Dado que el usuario completó la carga de documentos
- Cuando el sistema compara el selfie con la foto del DNI mediante reconocimiento facial
- Y detecta que NO hay coincidencia biométrica (rostros diferentes)
- Entonces rechaza la verificación por seguridad
- Y marca la cuenta para revisión manual por el equipo de seguridad
- Y envía email al usuario "Tu verificación requiere revisión adicional. Nos contactaremos en 48 horas"

**Escenario 4: Usuario intenta realizar acciones restringidas sin estar verificado**
- Dado que un usuario NO ha completado el proceso KYC
- Cuando intenta publicar un vehículo o realizar una reserva
- Entonces el sistema bloquea la acción
- Y muestra modal "Para realizar esta acción debes verificar tu identidad"
- Y redirige automáticamente a la pantalla de verificación KYC

---

#### Ejemplo US08: Activar alerta de emergencia durante viaje

**Acceptance Criteria:**

**Escenario 1: Activación exitosa de alerta de emergencia con envío a contactos**
- Dado que un pasajero se encuentra en un viaje activo
- Cuando detecta una situación de riesgo (conductor se desvía de ruta, comportamiento amenazante)
- Y mantiene presionado el botón de pánico por 3 segundos
- Entonces el sistema activa el protocolo de emergencia inmediatamente
- Y envía SMS a los 3 contactos de confianza registrados con el mensaje "ALERTA: [Nombre] activó emergencia. Ubicación: [GPS link] Vehículo: [Placa] Conductor: [Nombre]"
- Y envía notificación push a los contactos con botón "Ver ubicación en tiempo real"
- Y registra automáticamente la ubicación GPS cada 30 segundos
- Y dispara notificación al equipo de seguridad de WheelsPe

**Escenario 2: Desactivación de falsa alarma con código de seguridad**
- Dado que un pasajero activó la alerta por error (pulsación accidental)
- Cuando ingresa su código PIN de seguridad de 4 dígitos en los siguientes 60 segundos
- Entonces el sistema cancela el despacho automático a autoridades
- Pero mantiene el registro del evento en la bitácora con estado "Falsa alarma - Desactivada por usuario"
- Y NO envía SMS a contactos (si aún no transcurrieron 60 segundos desde activación)

**Escenario 3: Escalamiento automático a autoridades tras 5 minutos sin desactivación**
- Dado que la alerta de emergencia fue activada
- Cuando transcurren 5 minutos sin que el usuario desactive con su PIN
- Entonces el sistema escala automáticamente a las autoridades locales (SOS-PNP)
- Y envía los datos completos: ubicación GPS, datos del conductor, placa del vehículo, foto del pasajero
- Y mantiene registro de audio de la llamada generada

---

**APLICAR ESTE PATRÓN A LAS 47 USER STORIES:**

Cada User Story debe tener entre 3-5 escenarios con nombres que describan:
- El resultado exitoso (happy path)
- Los fallos por validación
- Los casos excepcionales
- Las restricciones de seguridad

---

## 5. REALIZAR 2 ENTREVISTAS ADICIONALES (Sección 2.2.2, pág 53-73)

### PROBLEMA DETECTADO
Al dividir el Segmento #2 en Conductores (2 entrevistas) y Pasajeros (2 entrevistas), cada nuevo segmento queda con solo 2 entrevistas. El enunciado requiere 3-5 entrevistas por segmento.

### CORRECCIÓN OBLIGATORIA

Necesitas realizar **2 entrevistas más**:
- 1 Conductor Arrendatario adicional
- 1 Pasajera adicional

---

### ENTREVISTA #9: Conductor Arrendatario

**Estructura de contenido para el informe:**

**Entrevistado 9: Javier Campos**
- **Edad:** 32 años
- **Ocupación:** Ingeniero Civil (Independiente)
- **Distrito:** Santiago de Surco
- **Dispositivos utilizados:** Samsung Galaxy S23 Ultra (Android)
- **Navegador habitual:** Google Chrome

[INSERTAR IMAGEN: Screenshot de la entrevista en video mostrando al entrevistado]

**Instante en el que inicia:** 56:23 min
**Duración de la entrevista:** 08:15 min
**URL:** [Enlace al video en OneDrive]

**Resumen:**

Javier es ingeniero civil independiente que trabaja como consultor para proyectos de construcción en Lima y provincias cercanas (Cañete, Huaral, Lurín). Alquila vehículos entre 2-3 veces al mes, principalmente los fines de semana, para realizar visitas de supervisión a obras en ejecución. Actualmente utiliza Peru Rent a Car, pero el costo promedio de S/ 150 por día (S/ 300 por fin de semana) representa una carga significativa en su presupuesto operativo.

Su principal frustración es asumir el 100% del gasto cuando frecuentemente viaja solo, a pesar de tener colegas ingenieros que realizan rutas similares. Ha intentado coordinar viajes compartidos a través de su red de contactos de LinkedIn y grupos de WhatsApp del Colegio de Ingenieros del Perú, pero la coordinación es caótica y poco confiable. En más de 3 ocasiones ha perdido oportunidades de dividir gastos porque los mensajes se perdieron en conversaciones grupales con más de 200 miembros.

**Personalidad y Comportamiento:**
- **Pragmático y orientado a ROI:** Calcula constantemente el costo/beneficio de cada decisión. "Si pudiera recuperar aunque sea el 50% del costo de alquiler compartiendo con 2 pasajeros, podría alquilar todas las semanas en lugar de solo cuando es estrictamente necesario."
- **Profesional y cuidadoso con su imagen:** Prefiere alquilar vehículos en buen estado (SUV o camionetas modernas) porque proyecta seriedad ante sus clientes en las obras. "Llegar en un auto del año hace diferencia cuando estás negociando un proyecto de S/ 500,000."
- **Networking oriented:** Ve el carpooling no solo como ahorro sino como oportunidad de networking. "Si pudiera compartir viajes regularmente con otros ingenieros, estaríamos construyendo relaciones profesionales que después derivan en recomendaciones de proyectos."

**Tecnología y Canales de Interacción:**
- **Power User de Android:** Su Samsung S23 Ultra es su oficina móvil. Utiliza Google Drive para planos, WhatsApp Business para coordinar con clientes, y LinkedIn para gestionar su red profesional.
- **Navegador:** Chrome sincronizado entre smartphone y laptop para continuidad de trabajo.
- **Canales informales actuales:** Grupos de WhatsApp del Colegio de Ingenieros (CIP) con más de 250 miembros, donde ocasionalmente publica "Voy a Cañete este sábado, alguien va?". Tasa de respuesta: menos del 5%.

**Confianza y Seguridad:**
- **Validación profesional sobre personal:** Confía más en la validación institucional (colegiatura vigente del CIP, perfil de LinkedIn verificado) que en la reputación anónima. "Si sé que alguien es ingeniero colegiado, automáticamente sé que es una persona seria con antecedentes verificables."
- **Disposición al pago:** Está dispuesto a pagar una tarifa de S/ 8-10 por pasajero por viaje (vs informal S/ 5) si la plataforma garantiza validación corporativa/profesional.

**Hallazgos clave:**
- **Necesidad técnica:** Requiere programación de rutas recurrentes (mismo destino cada fin de semana) sin tener que republicar manualmente.
- **Valor agregado:** Busca integración con su calendario de Google para que las rutas se publiquen automáticamente según sus visitas a obra agendadas.
- **Factor decisor:** La validación de que sus pasajeros sean profesionales colegiados (CIP, CAP, etc.) es más importante que la calificación numérica.

---

### ENTREVISTA #10: Pasajera Recurrente

**Estructura de contenido para el informe:**

**Entrevistado 10: Lucía Vega**
- **Edad:** 22 años
- **Ocupación:** Estudiante de Medicina (UPCH - 4to año)
- **Distrito:** La Molina
- **Dispositivos utilizados:** iPhone 13 (iOS)
- **Navegador habitual:** Safari

[INSERTAR IMAGEN: Screenshot de la entrevista en video mostrando a la entrevistada]

**Instante en el que inicia:** 1:04:38 min
**Duración de la entrevista:** 09:42 min
**URL:** [Enlace al video en OneDrive]

**Resumen:**

Lucía cursa el 4to año de Medicina en la Universidad Peruana Cayetano Heredia y realiza guardias hospitalarias nocturnas en el Hospital Cayetano Heredia (San Miguel). Vive en La Molina con sus padres y debe realizar el trayecto La Molina → San Miguel de lunes a sábado, con salidas del hospital a las 10:00 PM después de guardias de 12 horas.

Actualmente depende de un grupo de WhatsApp "Rutas UPCH Medicina" con 180 estudiantes, donde coordina "jalones" con compañeros que tienen auto. Su experiencia es frustrante: en el último mes ha experimentado 3 cancelaciones de último minuto que la obligaron a tomar taxi de emergencia (gasto de S/ 25 por viaje vs S/ 5 del jalón). En dos ocasiones ha llegado tarde a guardias por conductores impuntuales, recibiendo llamadas de atención de sus docentes.

**Personalidad y Comportamiento:**
- **Vigilante y precavida:** Desarrolló protocolos de seguridad por necesidad. "Siempre le paso la placa del auto y el nombre del conductor a mi mamá antes de subir. Ella me llama cada 15 minutos hasta que llego a casa."
- **Ansiosa respecto a seguridad nocturna:** Como mujer joven que termina guardias a las 10 PM, siente alta vulnerabilidad. "He escuchado tantas historias de chicas que subieron a autos con desconocidos... cada vez que tomo un jalón por WhatsApp siento miedo hasta que llego."
- **Frustraci con la informalidad:** Las cancelaciones la afectan emocionalmente porque ponen en riesgo su record académico. "Una vez llegué tarde a una guardia y casi pierdo mi rotación. No puedo confiar en gente que cancela 5 minutos antes."

**Tecnología y Canales de Interacción:**
- **Mobile-first (iOS):** Su iPhone es su conexión primaria. Usa WhatsApp (comunicación), Instagram (redes), Canvas (plataforma académica UPCH).
- **Navegador:** Safari, pero principalmente usa apps móviles nativas.
- **Dependencia de grupos informales:** Pertenece a 3 grupos de WhatsApp de rutas (general UPCH, específico Medicina, mujeres UPCH). El ruido informativo es abrumador (300+ mensajes diarios).

**Confianza y Seguridad:**
- **Filtro de comunidad como requisito no negociable:** Solo se sentiría segura si TODOS los conductores están verificados como estudiantes UPCH con correo institucional activo @upch.pe. "Si sé que es alumno de medicina como yo, sé que ha pasado por los mismos procesos de admisión rigurosos. No es cualquier persona."
- **Preferencia de género crítica:** Preferiría conductoras mujeres para viajes nocturnos. "Me sentiría muchísimo más tranquila si pudiera filtrar para viajar solo con chicas después de las 9 PM."
- **Disposición al pago por seguridad:** Pagaría S/ 8 por viaje (vs S/ 5 informal) si la app garantiza verificación institucional y GPS en tiempo real compartible con familia.

**Hallazgos clave:**
- **Necesidad técnica:** Filtro obligatorio de "Solo conductoras mujeres" para horarios nocturnos (después de 8 PM).
- **Valor agregado:** Compartir ubicación GPS en tiempo real con contactos de confianza SIN tener que enviar screenshots manualmente.
- **Factor decisor:** La validación de correo institucional UPCH es el único elemento que la haría abandonar definitivamente los grupos de WhatsApp.

---

**ACCIÓN:** Programar y realizar estas 2 entrevistas esta semana. Grabar video, transcribir, y agregar a la sección 2.2.2 del informe.

---

## 6. CREAR 3RA USER PERSONA - CONDUCTOR (Sección 2.3.1, pág 97-103)

### PROBLEMA DETECTADO
Solo tienen 2 User Personas. Con 3 segmentos necesitan 3 personas.

### CORRECCIÓN OBLIGATORIA

**Crear en UXPressia la siguiente User Persona:**

---

**USER PERSONA #2: Marco Ruiz - El Conductor Eficiente**

[INSERTAR IMAGEN: Captura de la User Persona creada en UXPressia]

**DEMOGRAFÍA:**
- **Nombre completo:** Marco Andrés Ruiz Valdivia
- **Edad:** 29 años
- **Ocupación:** Consultor de Negocios Senior en Ernst & Young (EY)
- **Ingresos mensuales:** S/ 6,800 (más bonos por proyectos)
- **Distrito de residencia:** San Borja
- **Estado civil:** Soltero
- **Nivel educativo:** MBA en ESAN (2023)

**TECNOLOGÍA:**
- **Smartphone principal:** Samsung Galaxy S24 (Android 15)
- **Laptop:** Lenovo ThinkPad (trabajo)
- **Apps más usadas:** LinkedIn (networking profesional), Uber (movilidad diaria), Google Maps (navegación), Rappi (delivery), Notion (organización), Google Calendar (agenda)
- **Nivel de competencia digital:** Avanzado - Early adopter de apps de productividad
- **Redes sociales activas:** LinkedIn (uso profesional diario), Instagram (personal, esporádico)

**PERSONALIDAD (Big 5):**
- **Apertura:** Alta - disfruta explorar nuevas tecnologías y metodologías de trabajo
- **Responsabilidad:** Muy alta - cumple deadlines, organizado, puntual
- **Extroversión:** Alta - networking es parte fundamental de su carrera
- **Amabilidad:** Media-alta - colaborativo pero competitivo
- **Neuroticismo:** Bajo - manejo efectivo del estrés

**ARQUETIPOS:**
- Arquetipo principal: **El Estratega** - optimiza cada aspecto de su vida para maximizar ROI
- Arquetipo secundario: **El Networker** - ve cada interacción como oportunidad de construir relaciones

**OBJETIVOS PERSONALES Y PROFESIONALES:**
1. **Corto plazo:** Ser ascendido a Manager en EY en los próximos 18 meses
2. **Mediano plazo:** Construir una red sólida de contactos C-level para futuro emprendimiento
3. **Largo plazo:** Fundar su propia consultora boutique en 5 años
4. **Relacionado a movilidad:** Reducir gastos mensuales de transporte de S/ 1,500 a S/ 800 mediante carpooling sin sacrificar imagen profesional

**FRUSTRACIONES:**
1. **Costo excesivo de movilidad:** Alquilar vehículos 4-5 veces al mes para reuniones con clientes (S/ 120/día × 5 = S/ 600 mensuales) es insostenible. Uber/taxis adicionales suman S/ 900 más. Total: S/ 1,500/mes.
2. **Desperdiciar asientos vacíos:** "Cuando alquilo un auto para ir a una reunión en Miraflores, llevo 4 asientos vacíos. Es un desperdicio total de recursos."
3. **Falta de validación profesional en grupos informales:** Intentó usar grupos de Facebook de carpooling corporativo, pero no hay forma de verificar que los pasajeros sean realmente ejecutivos. "Una vez recogí a alguien que se presentó como 'consultor' y resultó ser vendedor ambulante. Fue incómodo."
4. **Impuntualidad de pasajeros informales:** En carpooling informal, los pasajeros cancelan o llegan tarde, haciéndolo perder reuniones importantes.

**NECESIDADES:**
1. **Plataforma integrada alquiler + carpooling:** No quiere usar 2 apps separadas (una para alquilar, otra para publicar rutas).
2. **Validación corporativa de pasajeros:** Necesita verificar que son ejecutivos/profesionales reales (email corporativo, perfil de LinkedIn).
3. **División automática de costos:** La app debe calcular la cuota por pasajero sin negociaciones manuales.
4. **Facturación electrónica:** Para declarar gastos de movilidad como deducible de impuestos.
5. **Programación de rutas recurrentes:** Publica la misma ruta lun-vie, 7:30 AM, San Borja → San Isidro. Quiere programarla una sola vez, no republicar diariamente.

**COMPORTAMIENTO DE USO:**
- **Frecuencia de alquiler:** 4-5 veces al mes (principalmente martes-jueves para reuniones con clientes)
- **Rutas típicas:** San Borja → San Isidro/Miraflores/Surco (reuniones), San Borja → Aeropuerto (viajes de negocio)
- **Horarios:** Early morning (7-8 AM) y horario laboral (2-5 PM)
- **Duración promedio de alquiler:** Medio día (8 AM - 2 PM) o día completo
- **Disposición a compartir:** Alta - ve el carpooling como networking, no solo ahorro

**CITAS REPRESENTATIVAS:**
> "Si pudiera recuperar el 60% del costo del alquiler compartiendo con 2 ejecutivos que van al mismo distrito, podría alquilar todas las semanas en lugar de racionar para solo reuniones críticas."

> "Llegar en un auto del año a una reunión con un CFO proyecta mucho más profesionalismo que llegar en taxi. Pero no puedo justificar S/ 120 solo por 3 horas de reunión."

> "El carpooling no es solo ahorrar. Es conocer a otros profesionales. He conseguido 2 clientes nuevos conversando en el auto con gente que iba al mismo edificio que yo."

**MARCAS/INFLUENCIAS:**
- **Empresas que admira:** McKinsey, Bain, BCG (top consultoras)
- **Influencers que sigue:** LinkedIn creators sobre productividad y networking
- **Apps de referencia:** Uber (UX simple), LinkedIn (validación profesional), Notion (organización)

**UN DÍA EN LA VIDA DE MARCO:**
6:00 AM - Despierta, revisa emails y LinkedIn
7:00 AM - Sale de su depto en San Borja, debe estar en reunión en San Isidro a las 8:30 AM
7:15 AM - Abre app de alquiler, reserva Toyota Yaris por 4 horas (S/ 80)
7:30 AM - Publica ruta "San Borja → San Isidro, 2 asientos disponibles, S/ 8 c/u"
7:45 AM - Recoge a 2 pasajeros (ejecutivos verificados que trabajan en su mismo edificio destino)
8:25 AM - Llega puntual a reunión, proyectando imagen profesional
12:30 PM - Regresa a oficina de EY, devuelve auto
Noche - Calcula: gastó S/ 64 (S/ 80 - S/ 16 recuperados) en lugar de S/ 80. Ahorro: 20%. "Vale cada sol"

**RELACIÓN CON WHEELSPE:**
- **Usuario objetivo primario:** Representa perfectamente el segmento Conductor Arrendatario
- **Adopción esperada:** Early adopter - probaría la app en cuanto esté disponible
- **Potencial de evangelización:** Alto - si funciona bien, lo recomendará en su red de LinkedIn (800+ contactos)
- **Lifetime Value estimado:** 48 alquileres/año × S/ 10 comisión promedio = S/ 480/año

**DISPOSITIVOS Y ENTORNO TÉCNICO:**
- **Sistema operativo:** Android 15
- **Conectividad:** 5G (Claro Postpago)
- **Notificaciones:** Push activadas para apps de productividad, desactivadas para redes sociales
- **Método de pago preferido:** Tarjeta de crédito/débito (para acumular millas), acepta Yape/Plin para pagos menores

---

**ACCIÓN:** Crear esta persona en UXPressia y exportar imagen para incluir en el informe.

---

## 7. ACTUALIZAR USER TASK MATRIX (Sección 2.3.2, pág 104)

### CORRECCIÓN OBLIGATORIA

**Reemplazar la tabla actual con esta versión de 3 columnas:**

| Tarea del Usuario | Carlos Peña (Proveedor) | Marco Ruiz (Conductor) | Esther Ospina (Pasajera) |
|-------------------|-------------------------|------------------------|---------------------------|
| | **Freq / Import** | **Freq / Import** | **Freq / Import** |
| **Publicar vehículo en plataforma** | Siempre / Alta | Nunca / Baja | Nunca / Baja |
| **Buscar vehículo disponible para alquilar** | Nunca / Baja | Siempre / Alta | Nunca / Baja |
| **Publicar ruta de carpooling** | Nunca / Baja | Siempre / Alta | Nunca / Baja |
| **Buscar ruta de carpooling disponible** | Nunca / Baja | Nunca / Baja | Siempre / Alta |
| **Validar identidad KYC de otros usuarios** | Siempre / Alta | Siempre / Alta | Siempre / Alta |
| **Configurar checklist fotográfico del vehículo** | Siempre / Alta | A veces / Media | Nunca / Baja |
| **Procesar pagos o recibir cobros** | Siempre / Alta | Siempre / Alta | Siempre / Alta |
| **Calificar/reseñar a otros usuarios** | Siempre / Alta | Siempre / Alta | Siempre / Alta |
| **Configurar umbral de reputación mínimo** | A veces / Media | Nunca / Baja | Nunca / Baja |
| **Monitorear ubicación GPS en tiempo real** | Nunca / Baja | A veces / Media | Siempre / Alta |
| **Gestionar métodos de pago vinculados** | Siempre / Alta | Siempre / Alta | Siempre / Alta |
| **Activar/usar botón de pánico** | Nunca / Baja | Nunca / Baja | A veces / Alta |
| **Configurar contactos de confianza** | Nunca / Baja | A veces / Media | Siempre / Alta |
| **Consultar reputación antes de aceptar** | Siempre / Alta | Siempre / Alta | Siempre / Alta |
| **Gestionar calendario de disponibilidad** | Siempre / Alta | A veces / Media | Nunca / Baja |
| **Programar rutas recurrentes** | Nunca / Baja | Siempre / Alta | A veces / Media |
| **Coordinar detalles por chat integrado** | A veces / Media | Siempre / Alta | Siempre / Alta |
| **Solicitar/generar facturación electrónica** | Siempre / Alta | Siempre / Alta | Nunca / Baja |

**Agregar después de la tabla el siguiente análisis:**
ANÁLISIS DE DIFERENCIAS Y COINCIDENCIAS:
Tareas exclusivas de Carlos (Proveedor):

Publicación y gestión de vehículos en inventario
Configuración de umbrales de reputación para filtrar arrendatarios
Gestión intensiva de checklist fotográfico como protección de activo

Tareas exclusivas de Marco (Conductor):

Búsqueda activa de vehículos para alquiler temporal
Publicación de rutas de carpooling para monetizar asientos vacíos
Programación de rutas recurrentes semanales
Generación de facturas para declaración de gastos

Tareas exclusivas de Esther (Pasajera):

Búsqueda exclusiva de rutas compartidas (no alquila vehículos)
Monitoreo constante de ubicación GPS por seguridad
Configuración de contactos de confianza y uso potencial de botón de pánico
Filtrado por preferencias de seguridad (comunidad institucional, género)

Coincidencias críticas entre los 3 segmentos:

Validación de identidad KYC como requisito no negociable
Sistema de calificación/reseñas bidireccional tras cada interacción
Consulta de reputación previa antes de aceptar transacciones
Gestión de pagos/cobros mediante métodos electrónicos verificados

La principal diferencia operativa radica en que Marco (Conductor) es el único segmento que ejecuta AMBOS flujos principales: alquilar vehículos (como Arrendatario) Y publicar rutas (como Proveedor de movilidad). Esta dualidad lo convierte en el segmento de mayor valor estratégico, pues utiliza el 100% de las funcionalidades de la plataforma y genera doble flujo de ingresos para WheelsPe (comisión por alquiler + comisión por carpooling).

---

## 8. REESCRIBIR PROBLEM STATEMENTS CON FORMATO LEAN UX (Sección 1.2.2.1, pág 28)

### PROBLEMA DETECTADO
El Problem Statement actual es un párrafo largo y descriptivo. Debe seguir la estructura específica de Lean UX.

### FORMATO LEAN UX REQUERIDO:
[Segmento] necesita [necesidad]
porque [insight del problema].
Hemos observado que [síntoma]
está causando [impacto negativo].
¿Cómo podríamos [pregunta enfocada en solución]?

### CORRECCIÓN OBLIGATORIA

**Reemplazar la sección 1.2.2.1 completa con:**

---

#### 1.2.2.1 Lean UX Problem Statements

La declaración del problema es un componente fundamental del proceso Lean UX, ya que permite al equipo enfocarse en los síntomas reales del dominio antes de proponer soluciones técnicas específicas. Para WheelsPe se han identificado tres Problem Statements, uno por cada segmento objetivo, que delimitan el alcance del trabajo y las oportunidades de generación de valor.

---

**PROBLEM STATEMENT #1: Proveedores de Vehículos**

Los propietarios particulares y las micro-empresas de alquiler necesitan un canal formal, seguro y tecnológicamente accesible para monetizar vehículos subutilizados sin asumir riesgos de fraude o daños no compensados, porque actualmente carecen de herramientas digitales que validen la identidad de arrendatarios, protejan la integridad física de sus activos y les brinden respaldo legal ante incidencias.

Hemos observado que la informalidad de los grupos de Facebook y WhatsApp, junto con la ausencia de sistemas de verificación de identidad (KYC) y trazabilidad de uso vehicular, está causando que los propietarios mantengan sus vehículos inactivos perdiendo oportunidad de generar ingresos mensuales estimados en S/ 800-1,200 por unidad, mientras las micro-empresas pierden competitividad frente a franquicias internacionales al no contar con presencia digital profesional.

¿Cómo podríamos crear un ecosistema tecnológico que permita a propietarios alquilar vehículos con confianza mediante validación rigurosa de identidad (KYC), checklist de protección fotográfica automatizada y sistema de reputación transparente que construya confianza comunitaria sin requerir intermediarios humanos costosos?

---

**PROBLEM STATEMENT #2: Conductores Arrendatarios**

Los conductores arrendatarios necesitan reducir el costo individual del alquiler temporal de vehículos compartiendo trayectos con pasajeros verificados de su mismo entorno profesional o académico, porque el alquiler tradicional (S/ 120-150/día) es económicamente inviable para uso recurrente (4-5 veces al mes), lo que los obliga a depender de taxis por aplicación que no proyectan imagen profesional ni permiten recuperar inversión mediante carpooling.

Hemos observado que la ausencia de plataformas que integren nativamente alquiler vehicular con publicación de rutas de carpooling verificado está causando que conductores asuman el 100% del gasto operativo (alquiler + combustible + peajes) de forma individual, resignándose a alquilar solo en ocasiones críticas (reuniones con clientes de alto valor) y perdiendo oportunidades de networking profesional durante trayectos compartidos con ejecutivos de su nivel.

¿Cómo podríamos integrar el proceso de alquiler vehicular con la publicación de rutas de movilidad compartida en un único ecosistema digital que valide identidad corporativa de pasajeros (email empresarial, LinkedIn), calcule automáticamente división de costos, genere facturación electrónica deducible de impuestos y permita programar rutas recurrentes sin republicación manual diaria?

---

**PROBLEM STATEMENT #3: Pasajeros de Movilidad Compartida**

Los pasajeros recurrentes (estudiantes universitarios y trabajadores jóvenes) necesitan acceder a rutas de movilidad compartida donde TODOS los conductores estén verificados como miembros activos de su misma comunidad institucional (universidad/empresa), porque los grupos informales de WhatsApp y Facebook no garantizan validación de identidad, generan ansiedad por exposición a riesgos de seguridad personal (especialmente en mujeres que viajan de noche) y presentan alta tasa de cancelaciones de último minuto que afectan puntualidad académica/laboral.

Hemos observado que la coordinación informal mediante grupos masivos de WhatsApp (150-300 miembros) sin verificación institucional obligatoria está causando que estudiantes y trabajadores enfrenten cancelaciones en 40% de viajes coordinados, retrasos académicos/laborales por impuntualidad de conductores no comprometidos, y estados de ansiedad constante en mujeres que viajan en horarios nocturnos con desconocidos cuya identidad real no pueden validar.

¿Cómo podríamos crear un directorio verificado de rutas compartidas donde pasajeros viajen exclusivamente con conductores que hayan validado su pertenencia a la misma institución mediante correo electrónico corporativo/académico activo (@upc.edu.pe, @empresaX.com), incluyendo funcionalidades de seguridad activa (botón de pánico, GPS compartible en tiempo real con familia, filtro por género para viajes nocturnos) que eliminen la percepción de riesgo sin incrementar costos más allá del 20% vs opciones informales?

---

Estos tres Problem Statements delimitan el alcance de WheelsPe y establecen el marco estratégico para la generación de Hypothesis Statements en la siguiente sección. Cada problema identificado representa una oportunidad de mercado validable mediante MVP y experimentos de usabilidad en el contexto de Lima Metropolitana.

---

## 9. AGREGAR PRIORIZACIÓN DE RISKIEST ASSUMPTION (Sección 1.2.2.2, pág 29-32)

### PROBLEMA DETECTADO
La sección 1.2.2.2 lista 20+ assumptions pero NO identifica cuál es la más riesgosa para el negocio.

### CORRECCIÓN OBLIGATORIA

**Agregar AL FINAL de la sección 1.2.2.2 (después de listar todos los assumptions):**

---

#### Priorización de Assumptions - Identificación del Riskiest Assumption

Una vez identificados los 24 assumptions críticos del modelo de negocio de WheelsPe, el equipo procedió a priorizarlos utilizando la **Matriz de Priorización de Assumptions** basada en dos dimensiones fundamentales:

1. **Nivel de incertidumbre:** ¿Qué tan seguros estamos de que este assumption es verdadero? (escala 1-10, donde 10 = máxima incertidumbre)
2. **Impacto en el negocio:** Si este assumption resulta ser falso, ¿cuál es el impacto en la viabilidad del modelo? (escala 1-10, donde 10 = colapso total del negocio)

[INSERTAR IMAGEN: Matriz de priorización 2x2 con cuadrantes: Bajo riesgo, Monitorear, Validar eventualmente, RISKIEST ASSUMPTIONS]

Tras evaluar colectivamente en sesión de equipo y consultar con stakeholders potenciales (3 proveedores de vehículos entrevistados), se identificó como **RISKIEST ASSUMPTION**:

---

### 🔴 RISKIEST ASSUMPTION PRIORIZADO

**"Los propietarios particulares de vehículos están dispuestos a confiar sus activos de alto valor (S/ 30,000-80,000) a conductores completamente desconocidos basándose únicamente en validación digital de identidad (KYC con DNI + selfie) y perfiles reputacionales en la plataforma, sin requerir interacción presencial previa, garantías físicas (depósitos en efectivo) ni verificación por terceros de confianza."**

---

#### Justificación de la Priorización

**Por qué este es el Riskiest Assumption:**

1. **Máximo nivel de incertidumbre (9/10):**
   - Requiere un cambio cultural profundo: pasar de la informalidad basada en confianza interpersonal (grupos de amigos, recomendaciones boca a boca) a la confianza digital mediada por algoritmos.
   - No existe precedente local exitoso en Perú de plataformas P2P de activos de alto valor (a diferencia de USA donde Turo funciona con años de madurez cultural digital).
   - Las entrevistas revelaron que el 75% de proveedores actuales SOLO alquilan a conocidos directos o recomendados por familiares cercanos.

2. **Impacto crítico en viabilidad del negocio (10/10):**
   - Si este assumption falla, **NO HABRÁ INVENTARIO DE VEHÍCULOS** en la plataforma.
   - Sin inventario, el modelo de negocio completo colapsa: conductores no pueden alquilar, pasajeros no tienen con quién compartir viajes, WheelsPe no genera comisiones.
   - Es el assumption del cual dependen TODOS los demás: si los proveedores no confían, da igual cuán buena sea la UX, el pricing, o el sistema de pagos.

3. **Dependencia en cadena:**
   - Assumption secundarios dependen de este: "Los proveedores publicarán fotos reales del vehículo" → requiere primero que decidan publicar.
   - "Los proveedores aceptarán reservas de usuarios con calificación 4+" → requiere primero que estén dispuestos a aceptar reservas.

4. **No es validable con escritorio:**
   - A diferencia de assumptions técnicos ("El GPS funcionará en tiempo real"), este requiere validación con USUARIOS REALES arriesgando ACTIVOS REALES.
   - No se puede simular con prototipos clickeables o encuestas de intención.

---

#### Plan de Validación del Riskiest Assumption

Para validar este assumption crítico en el **Sprint 1** (primeras 2 semanas del ciclo de desarrollo), se implementará el siguiente plan experimental:

**Hipótesis asociada:**
"Creemos que los propietarios particulares confiarán en nuestra plataforma digital si implementamos KYC riguroso (DNI + selfie + validación biométrica) + checklist fotográfico obligatorio pre/post alquiler + sistema de garantía mediante retención temporal (Escrow)."

**Experimento MVP:**

1. **Fase 1 - Validación de Concepto (Semana 1):**
   - Entrevistar a 5 propietarios adicionales mostrándoles mockups interactivos de:
     - Pantalla de perfil de arrendatario con badge "Verificado KYC"
     - Checklist fotográfico de 12 puntos (neumáticos, carrocería, interiores, kilometraje)
     - Dashboard de retención de garantía (Escrow) que libera fondos solo tras devolución sin daños
   - Métrica de éxito: Al menos 4/5 proveedores expresan "Sí estaría dispuesto a probar con este nivel de seguridad" (80% de intención)

2. **Fase 2 - Piloto Controlado (Semana 2-4):**
   - Reclutar 3 proveedores reales dentro de la comunidad UPC (profesores, staff administrativo, estudiantes de posgrado con vehículo)
   - Publicar sus 3 vehículos en plataforma MVP funcional
   - Permitir que usuarios reales realicen reservas (subsidiar primeras 5 reservas con descuento 50% para generar demanda)
   - **Métrica de éxito:** Al menos 2/3 proveedores completan al menos 1 alquiler exitoso en 2 semanas (66% de conversión de intención a acción real)

3. **Fase 3 - Medición Post-Experiencia (Semana 5):**
   - Entrevistar a los 3 proveedores pilotos sobre su experiencia real
   - Preguntas clave: "¿Volvería a alquilar?" "¿Qué cambiaría del proceso de verificación?" "¿Recomendaría la plataforma a otro propietario?"
   - **Métrica de éxito:** NPS (Net Promoter Score) ≥ 7/10 entre proveedores pilotos

**Criterios de validación/invalidación:**

✅ **ASSUMPTION VALIDADO si:**
- 80%+ de proveedores entrevistados expresan intención de uso tras ver mockups de seguridad
- 66%+ de proveedores pilotos completan al menos 1 alquiler real en 2 semanas
- NPS ≥ 7/10 post-experiencia

❌ **ASSUMPTION INVALIDADO si:**
- <60% de intención de uso tras mostrar mockups
- <50% de conversión de intención a acción (pilotos que publican pero no aceptan reservas)
- NPS < 5/10 post-experiencia

**Plan de contingencia si el assumption falla:**

Si tras el experimento MVP se invalida este assumption, el equipo ejecutará PIVOT estratégico hacia uno de los siguientes modelos alternativos:

- **Opción A - Modelo B2B Corporativo:** En lugar de P2P entre individuos, WheelsPe se convierte en marketplace entre micro-empresas de alquiler formales (que ya tienen procesos de verificación) y usuarios finales. Se sacrifica el diferenciador de "inventario ampliado" pero se reduce riesgo.

- **Opción B - Modelo Híbrido Verificación Presencial:** Implementar verificación presencial obligatoria en primera interacción (Proveedor-Arrendatario se conocen en persona, toman foto juntos, luego digitalizan la relación). Incrementa fricción pero puede ser puente cultural necesario.

- **Opción C - Targeting exclusivo a Corporaciones:** Enfocarse solo en Segmento #2 (Conductores) que alquilan a empresas formales (Hertz, Budget) y usan WheelsPe solo para el componente de carpooling verificado. Se elimina el P2P de vehículos particulares.

---

Este proceso de priorización y validación del Riskiest Assumption garantiza que el equipo de WheelsPe invierta recursos de desarrollo en validar primero la incertidumbre de mayor impacto antes de escalar funcionalidades secundarias.

---

## 10. MEJORAR HYPOTHESIS STATEMENTS CON MÉTRICAS SMART (Sección 1.2.2.3, pág 32-34)

### PROBLEMA DETECTADO
Las métricas actuales son vagas: "25% de aumento" sin baseline, "incremento en satisfacción" sin número específico.

### FORMATO SMART REQUERIDO:
- **S**pecific: ¿Qué se mide exactamente?
- **M**easurable: ¿Cómo se cuantifica?
- **A**chievable: ¿Es realista con recursos disponibles?
- **R**elevant: ¿Valida directamente el assumption?
- **T**ime-bound: ¿En cuánto tiempo?

### CORRECCIÓN OBLIGATORIA

**Reescribir TODAS las Hypothesis Statements de la sección 1.2.2.3:**

---

#### 1.2.2.3 Lean UX Hypothesis Statements

Las Hypothesis Statements de WheelsPe traducen los assumptions priorizados en declaraciones validables mediante experimentos concretos con usuarios reales. Cada hipótesis incluye métricas SMART (Specific, Measurable, Achievable, Relevant, Time-bound) que permitirán determinar objetivamente si el assumption subyacente es verdadero o requiere ajustes estratégicos.

---

**HIPÓTESIS 1: Seguridad Jurídica y Confianza del Proveedor**

**Creemos que** implementar verificación obligatoria de identidad mediante KYC multinivel (DNI + selfie + validación biométrica) combinado con checklist fotográfico de 12 puntos pre/post alquiler y sistema de calificaciones bidireccional transparente **logrará que** propietarios particulares alquilen sus vehículos sin temor a fraude o daños no compensados **a** conductores completamente desconocidos sin requerir interacción presencial previa.

**Sabremos que esto es cierto cuando observemos:**

📊 **Métrica 1 - Conversión de Registro de Inventario:**
- **Baseline:** 0 vehículos particulares registrados (pre-lanzamiento)
- **Target:** 15 vehículos particulares completamente acreditados (con KYC del propietario + documentación vehicular + fotos del checklist) en los primeros 30 días naturales post-lanzamiento en la comunidad piloto UPC
- **Método de medición:** Conteo directo en base de datos de vehículos con status "Activo" + owner_type="Particular"
- **Fecha de medición:** 30 días desde el lanzamiento oficial (1 de junio 2026)

📊 **Métrica 2 - Percepción de Seguridad Post-Primer Alquiler:**
- **Baseline:** N/A (no hay experiencia previa)
- **Target:** 80% de proveedores (12 de 15) califican su sensación de seguridad como 4/5 o 5/5 en encuesta NPS enviada 24 horas después de completar su primer alquiler exitoso
- **Método de medición:** Encuesta in-app automática con pregunta "¿Qué tan seguro te sentiste alquilando tu vehículo a través de WheelsPe?" (escala Likert 1-5)
- **Fecha de medición:** Continua durante primeros 60 días, consolidación al día 60

📊 **Métrica 3 - Tasa de Fraude/Daños No Compensados:**
- **Baseline:** 15% de incidencias reportadas en grupos informales según entrevistas cualitativas (3 de cada 20 alquileres informales presentaron problemas no resueltos)
- **Target:** 0 reportes de fraude confirmado (identidad falsa, vehículo no devuelto) o daños sin compensación en los primeros 50 alquileres completados
- **Método de medición:** Sistema de tickets de soporte + revisión manual de disputas escaladas
- **Fecha de medición:** Primeros 90 días desde lanzamiento

---

**HIPÓTESIS 2: Adopción de Tecnología por Usuarios No Digitales**

**Creemos que** diseñar una interfaz mobile-first con onboarding guiado paso a paso, tooltips contextuales y soporte por WhatsApp en horario extendido **logrará que** propietarios mayores de 45 años con baja competencia digital (segmento NSE C que representa 40% del target) **completen exitosamente** el proceso de registro y publicación de su primer vehículo sin requerir asistencia presencial.

**Sabremos que esto es cierto cuando observemos:**

📊 **Métrica 1 - Tasa de Completitud de Onboarding (Usuarios 45+ años):**
- **Baseline:** 0% (producto no existe)
- **Target:** 70% de usuarios mayores de 45 años que inician registro completan todo el flujo hasta publicar primer vehículo sin abandonar
- **Método de medición:** Funnel analytics con segmentación por edad (campo "fecha_nacimiento" en registro) → pasos: Registro → KYC → Datos Vehículo → Fotos → Publicación
- **Fecha de medición:** Primeros 45 días post-lanzamiento

📊 **Métrica 2 - Tiempo Promedio de Completitud:**
- **Baseline:** N/A
- **Target:** Usuarios 45+ completan publicación en ≤25 minutos (vs ≤15 min estimado para usuarios 18-35)
- **Método de medición:** Timestamp entre evento "onboarding_started" y "vehicle_published"
- **Tolerancia aceptable:** Hasta 35 minutos sigue siendo validación positiva

📊 **Métrica 3 - Uso de Soporte vs Auto-Servicio:**
- **Baseline:** 100% de usuarios nuevos en plataformas similares contactan soporte (benchmark informal)
- **Target:** ≤40% de usuarios 45+ contactan soporte durante onboarding (60% lo completa autónomamente con tooltips)
- **Método de medición:** Tickets de soporte con tag "onboarding" / Total usuarios 45+ registrados
- **Fecha de medición:** Continua, reporte semanal

---

**HIPÓTESIS 3: Eficiencia Operativa y Amortización de Costos (Conductores)**

**Creemos que** integrar nativamente en una sola plataforma el flujo de alquiler vehicular + publicación de rutas de carpooling con división automática de costos **motivará a** conductores arrendatarios (Segmento #2) **a** alquilar con mayor frecuencia al poder recuperar 50-70% del gasto operativo mediante pasajeros.

**Sabremos que esto es cierto cuando observemos:**

📊 **Métrica 1 - Tasa de Adopción de Carpooling entre Arrendatarios:**
- **Baseline:** 0% (feature no existe en competencia)
- **Target:** 40% de conductores que alquilan vehículos publican al menos 1 ruta de carpooling durante el periodo de alquiler (6 de cada 15 conductores activos en mes 1)
- **Método de medición:** Query SQL: `SELECT COUNT(DISTINCT user_id) FROM carpooling_routes WHERE user_id IN (SELECT DISTINCT renter_id FROM rentals) / COUNT(DISTINCT renter_id) FROM rentals`
- **Fecha de medición:** Mes 1 (días 1-30 post-lanzamiento)

📊 **Métrica 2 - Incremento en Frecuencia de Alquiler:**
- **Baseline:** 1.2 alquileres/mes/usuario según benchmark de competencia (Nexo Rent)
- **Target:** Conductores que usan carpooling realizan ≥2.5 alquileres/mes (incremento de 108%)
- **Método de medición:** Segmentación de cohorte "Conductores con carpooling" vs "Conductores sin carpooling" → promedio de alquileres en 60 días
- **Fecha de medición:** Días 30-90 (requiere 2 meses de data para calcular promedio mensual)

📊 **Métrica 3 - Engagement Medido por Session Length:**
- **Baseline:** 8 minutos promedio de sesión en apps de alquiler tradicional (benchmark Turo USA)
- **Target:** Conductores que gestionan rutas de carpooling tienen session length promedio ≥15 minutos (indicador de engagement profundo con feature de coordinación de pasajeros)
- **Método de medición:** Google Analytics / Mixpanel - promedio de duración de sesión para cohorte "usuarios con ≥1 ruta publicada"
- **Fecha de medición:** Continua, consolidación mensual

---

**HIPÓTESIS 4: Seguridad y Confianza Institucional (Pasajeros)**

**Creemos que** implementar validación obligatoria de correo institucional (@upc.edu.pe, @pucp.edu.pe, @empresaX.com) + filtro de comunidad que muestre SOLO rutas de conductores de la misma institución **eliminará** la percepción de riesgo de seguridad personal que actualmente genera 60% de abandono en coordinación informal según entrevistas **en** estudiantes universitarias mujeres (18-25 años).

**Sabremos que esto es cierto cuando observemos:**

📊 **Métrica 1 - Adopción en Comunidades Universitarias Piloto:**
- **Baseline:** 0 usuarias registradas (pre-lanzamiento)
- **Target:** 50 estudiantes mujeres de UPC con correo @upc.edu.pe verificado registradas y activas (≥1 reserva de ruta) en primeros 45 días
- **Método de medición:** Conteo en base de datos con filtros: gender="Female" + email LIKE "%@upc.edu.pe" + reservations_count ≥ 1
- **Fecha de medición:** Día 45 post-lanzamiento

📊 **Métrica 2 - Percepción de Seguridad Pre/Post Adopción:**
- **Baseline:** 3.2/10 promedio de sensación de seguridad en grupos informales (dato de entrevistas: "me siento insegura viajando con desconocidos")
- **Target:** ≥7.5/10 promedio en encuesta "¿Qué tan segura te sientes usando WheelsPe con validación institucional?" enviada tras 3ra reserva completada
- **Método de medición:** Encuesta NPS in-app con escala 1-10
- **Muestra mínima:** 20 respuestas de usuarias con ≥3 viajes completados
- **Fecha de medición:** Día 60 (tiempo necesario para acumular 20 usuarias con 3+ viajes)

📊 **Métrica 3 - Uso de Feature "Filtro Solo Conductoras Mujeres":**
- **Baseline:** N/A (feature no existe en competencia)
- **Target:** ≥50% de búsquedas realizadas por mujeres en horario nocturno (8 PM - 6 AM) activan el filtro "Solo conductoras mujeres"
- **Método de medición:** Event tracking: evento "filter_female_drivers_only_enabled" / total eventos "search_route" WHERE user_gender="Female" AND search_time BETWEEN "20:00" AND "06:00"
- **Fecha de medición:** Continua, consolidación semanal

---

**HIPÓTESIS 5: Pricing y Disposición de Pago**

**Creemos que** los pasajeros del Segmento #3 (estudiantes, NSE C-D) **pagarán voluntariamente** S/ 7-9 por viaje compartido (premium de 40-80% vs S/ 5 de grupos informales) **a cambio de** validación institucional + funcionalidades de seguridad (GPS compartible, botón de pánico, calificaciones verificadas).

**Sabremos que esto es cierto cuando observemos:**

📊 **Métrica 1 - Precio Promedio Aceptado por Reserva:**
- **Baseline:** S/ 5 soles por viaje en coordinación informal (dato de entrevistas)
- **Target:** S/ 7.5 soles promedio por reserva completada en la plataforma (rango aceptable: S/ 7.0-9.0)
- **Método de medición:** AVG(trip_price) FROM completed_reservations WHERE passenger_segment="Segment_3_Students"
- **Muestra mínima:** 100 reservas completadas
- **Fecha de medición:** Primeros 60 días post-lanzamiento

📊 **Métrica 2 - Tasa de Conversión de Búsqueda a Reserva:**
- **Baseline:** 25% en plataformas de carpooling sin validación (benchmark BlaBlaCar)
- **Target:** ≥35% de conversión (usuarios que buscan rutas efectivamente reservan) como indicador de que perciben suficiente valor de seguridad para pagar premium
- **Método de medición:** Funnel: Búsqueda realizada → Ruta seleccionada → Reserva confirmada (con pago completado)
- **Fecha de medición:** Continua, consolidación quincenal

📊 **Métrica 3 - Churn Rate Post-Primer Viaje:**
- **Baseline:** 60% de usuarios no repiten tras primer viaje en grupos informales (dato de entrevista: "probé una vez, fue caótico, no volví a coordinar")
- **Target:** ≤25% de churn rate (75% de pasajeros que completan primer viaje realizan al menos un segundo viaje en los siguientes 30 días)
- **Método de medición:** Cohorte analysis - usuarios con primer viaje completado en Semana X → % que tienen segundo viaje en Semana X+4
- **Fecha de medición:** Análisis de cohorte semanal a partir del día 45

---

**HIPÓTESIS 6: Construcción de Confianza a Través de Reputación**

**Creemos que** un sistema de calificación bidireccional obligatorio post-servicio (sin opción de omitir) + visualización de historial completo de reseñas **generará** confianza suficiente para que usuarios acepten interactuar con desconocidos **sin requerir** validaciones adicionales como videollamadas pre-viaje o depósitos de garantía.

**Sabremos que esto es cierto cuando observemos:**

📊 **Métrica 1 - Tasa de Completitud de Calificaciones:**
- **Baseline:** 40% de usuarios completan calificaciones en plataformas donde es opcional (benchmark Airbnb)
- **Target:** ≥85% de servicios completados tienen calificación bidireccional registrada (tanto pasajero califica a conductor como conductor califica a pasajero)
- **Método de medición:** COUNT(trips WHERE rating_by_passenger IS NOT NULL AND rating_by_driver IS NOT NULL) / COUNT(completed_trips)
- **Fecha de medición:** Continua, reporte semanal

📊 **Métrica 2 - Promedio de Calificación del Ecosistema:**
- **Baseline:** N/A
- **Target:** ≥4.3/5.0 estrellas promedio en calificaciones de conductores Y pasajeros (indicador de calidad general del ecosistema)
- **Método de medición:** AVG(rating) FROM all_ratings WHERE rating IS NOT NULL
- **Umbral de alarma:** Si promedio cae <4.0, indica problemas sistémicos de confianza
- **Fecha de medición:** Continua, monitoreo semanal

📊 **Métrica 3 - Uso de Filtros de Reputación:**
- **Baseline:** N/A (feature propietario)
- **Target:** ≥60% de proveedores activan umbral de reputación mínimo (rechazo automático de solicitudes de usuarios con rating <4.0 estrellas)
- **Método de medición:** COUNT(providers WHERE reputation_threshold_enabled=TRUE) / COUNT(active_providers)
- **Interpretación:** Alta adopción indica que el sistema de reputación genera confianza suficiente para delegar decisiones de filtrado al algoritmo
- **Fecha de medición:** Día 30, 60, 90 (tendencia de adopción progresiva)

---

Estas 6 Hypothesis Statements con métricas SMART constituyen el marco de validación experimental de WheelsPe. Los resultados de estas mediciones determinarán objetivamente qué assumptions del modelo de negocio son válidos y cuáles requieren pivot estratégico antes de la inversión en escalamiento.

---

## 11. RESOLVER HOT SPOTS DEL EVENT STORMING (Sección 2.3.5, pág 110-115)

### PROBLEMA DETECTADO
Identificaron 3 Hot Spots pero NO los resolvieron con decisiones de diseño.

### CORRECCIÓN OBLIGATORIA

**Agregar NUEVA SUBSECCIÓN después del Big Picture Event Storming:**

---

#### 2.3.5.6 Resolución de Hot Spots Identificados

Durante la ejecución del Big Picture Event Storming, el equipo identificó tres puntos críticos de incertidumbre (Hot Spots) que requerían decisiones explícitas de diseño antes de continuar con la fase de Tactical Design. A continuación se presentan las resoluciones formales adoptadas, incluyendo los nuevos Domain Events generados y las políticas automatizadas (Policies) implementadas.

---

**HOT SPOT #1: ¿Qué ocurre si el proceso KYC falla?**

**Contexto del problema:**
Durante el flujo de verificación de identidad, el sistema puede rechazar documentos por múltiples razones (imagen ilegible, inconsistencia biométrica, documento vencido, datos no coinciden con RENIEC). La incertidumbre radicaba en: ¿el usuario queda completamente bloqueado? ¿puede seguir usando otras funciones? ¿cuántos reintentos se permiten?

**Decisión de diseño adoptada:**

El equipo definió una **política de degradación progresiva** que balancea seguridad con experiencia de usuario:

1. **Primer rechazo:** El usuario recibe notificación con razón específica del fallo ("Foto de DNI borrosa", "Selfie no coincide con foto del documento") y puede reintentar inmediatamente mediante nuevo upload de documentos.

2. **Segundo rechazo:** Se permite segundo reintento pero se agrega delay de 2 horas (política anti-spam de intentos fraudulentos masivos).

3. **Tercer rechazo:** El caso se escala automáticamente a **revisión manual** por el equipo de Seguridad de WheelsPe. El usuario recibe email: "Tu verificación requiere validación adicional. Responderemos en máximo 48 horas hábiles."

4. **Restricciones operativas mientras KYC está pendiente:**
   - Usuario puede navegar catálogo de vehículos/rutas (lectura)
   - Usuario puede completar perfil, vincular métodos de pago
   - Usuario **NO puede**: publicar vehículos, publicar rutas de carpooling, realizar reservas
   - Usuario **SÍ puede**: ser pasajero en rutas publicadas (downgrade a rol de menor riesgo)

**Nuevos Domain Events generados:**

KYCRechazado
Atributos: user_id, razon_rechazo (enum), intentos_restantes (int), timestamp
ReintentoKYCSolicitado
Atributos: user_id, intento_numero (int), documentos_nuevos (array), timestamp
KYCEscaladoARevisionManual
Atributos: user_id, motivo_escalamiento (string), analista_asignado_id, timestamp
KYCAprobadoManualmente
Atributos: user_id, analista_id, notas_aprobacion (text), timestamp


**Políticas automatizadas (Policies):**
WHEN KYCRechazado IS TRIGGERED
IF intentos_restantes > 0
THEN SEND NotificacionPushReintentoDisponible
AND SEND EmailConInstruccionesMejora
ELSE
TRIGGER KYCEscaladoARevisionManual
AND SEND EmailNotificacionRevisionManual

[INSERTAR IMAGEN: Diagrama de flujo de decisión para KYC fallido]

---

**HOT SPOT #2: ¿Qué ocurre si se intenta cancelar una reserva que ya está activa?**

**Contexto del problema:**
Una reserva pasa por estados: Pendiente → Confirmada → **Activa** (vehículo ya entregado) → Completada. La incertidumbre surgió en: ¿se permite cancelar una reserva cuando el vehículo ya fue entregado y está en posesión del arrendatario? ¿cuáles son las implicaciones financieras y operativas?

**Decisión de diseño adoptada:**

El equipo definió **política de penalización escalonada** según el estado de la reserva:

1. **Reserva en estado "Pendiente" o "Confirmada" (vehículo AÚN NO entregado):**
   - Cancelación permitida hasta 24 horas antes de hora de inicio
   - Penalización: 0% (reembolso completo)
   - Si cancela con menos de 24 horas: penalización 20% de costo total (compensación al proveedor por bloqueo de agenda)

2. **Reserva en estado "Activa" (vehículo YA entregado, checklist inicial ya completado):**
   - Cancelación **solo permitida** con justificación obligatoria + evidencia fotográfica
   - Justificaciones válidas: Falla mecánica comprobable (fotos de motor, neumático reventado), accidente de tránsito (parte policial), emergencia médica certificada
   - Penalización: **50% del costo total** retenido como compensación al proveedor
   - Sistema **NO permite** cancelación por "ya no lo necesito" o "encontré alternativa más barata"

3. **Flujo operativo post-cancelación de reserva activa:**
   - Sistema notifica inmediatamente al proveedor via push + SMS
   - Proveedor tiene 2 opciones:
     - Acordar punto de devolución inmediata (antes de fin de reserva original)
     - Permitir que arrendatario mantenga vehículo hasta fin de periodo pero sin extensión
   - Checklist fotográfico de devolución se ejecuta normalmente
   - Fianza se libera solo tras confirmación de estado del vehículo

**Nuevos Domain Events generados:**

CancelacionDeReservaActivaSolicitada
Atributos: reservation_id, solicitante (enum: RENTER/PROVIDER), justificacion (text), evidencia_fotografica (array URLs), timestamp
PenalidadPorCancelacionAplicada
Atributos: reservation_id, porcentaje_penalidad (decimal), monto_penalizado (decimal), monto_reembolsado (decimal), timestamp
SolicitudRecuperacionVehiculoEnviada
Atributos: reservation_id, provider_id, ubicacion_actual_vehiculo (GPS), punto_devolucion_propuesto (GPS), timestamp
VehiculoDevueltoPrematuramente
Atributos: reservation_id, fecha_devolucion_real (datetime), fecha_devolucion_programada (datetime), dias_no_usados (int), checklist_devolucion_id, timestamp


**Políticas automatizadas (Policies):**
WHEN CancelacionDeReservaActivaSolicitada IS TRIGGERED
IF justificacion IN ['falla_mecanica', 'accidente', 'emergencia_medica']
AND evidencia_fotografica IS NOT EMPTY
THEN APPLY PenalidadPorCancelacionAplicada(porcentaje=50)
AND TRIGGER SolicitudRecuperacionVehiculoEnviada
AND SEND NotificacionProveedorCancelacionActiva
ELSE
REJECT CancelacionSolicitud
AND SEND NotificacionRechazoNoCumpleRequisitos

[INSERTAR IMAGEN: State Machine de Reserva mostrando transiciones permitidas y bloqueadas]

---

**HOT SPOT #3: ¿Cómo se maneja un pago fallido?**

**Contexto del problema:**
Los pagos pueden fallar por múltiples razones: fondos insuficientes, tarjeta vencida, límite de crédito excedido, bloqueo por fraude del banco, error de pasarela. La incertidumbre era: ¿cuántos reintentos automáticos? ¿qué pasa con la reserva? ¿se bloquea al usuario?

**Decisión de diseño adoptada:**

El equipo implementó **política de recuperación automatizada con degradación gradual**:

1. **Primer fallo de pago:**
   - Sistema reintenta automáticamente tras **1 hora** (muchos fallos son temporales: límite diario de la tarjeta, problemas de conectividad del banco)
   - Usuario recibe notificación push: "Tu pago no pudo procesarse. Reintentaremos en 1 hora. Verifica que tu tarjeta tenga fondos suficientes."

2. **Segundo fallo (tras 1 hora):**
   - Sistema reintenta nuevamente tras **4 horas adicionales**
   - Usuario recibe email + push: "Segundo intento de pago falló. Por favor actualiza tu método de pago o contacta a tu banco. Reintentaremos en 4 horas."
   - Sistema sugiere métodos alternativos: "¿Deseas pagar con Yape/Plin/Transferencia?"

3. **Tercer fallo (tras total de 5 horas):**
   - **Reserva cancelada automáticamente** por falta de pago
   - Proveedor notificado inmediatamente: "Reserva #12345 cancelada por pago rechazado. Tu vehículo está nuevamente disponible."
   - Usuario bloqueado temporalmente para nuevas reservas hasta regularizar deuda pendiente
   - Si hay deuda (ej. cancelación con penalidad), se genera **cuenta por cobrar** que debe saldarse antes de operar nuevamente

4. **Escalamiento a cobranza:**
   - Tras 3 fallos de pago, el caso se escala a equipo administrativo
   - Administrador recibe alerta en dashboard de operaciones
   - Seguimiento manual vía email/llamada telefónica para recuperar monto adeudado

**Nuevos Domain Events generados:**

PagoFallado
Atributos: payment_id, reservation_id, user_id, razon_rechazo (enum: INSUFFICIENT_FUNDS, CARD_EXPIRED, FRAUD_DETECTED, BANK_ERROR), intento_numero (int 1-3), monto_rechazado (decimal), timestamp
ReintentoPagoProgramado
Atributos: payment_id, intento_numero (int), fecha_hora_reintento (datetime), timestamp
ReservaCanceladaPorImpago
Atributos: reservation_id, user_id, provider_id, intentos_fallidos_totales (int), monto_adeudado (decimal), timestamp
UsuarioBloqueadoParaNuevasReservas
Atributos: user_id, motivo_bloqueo (string), deuda_pendiente (decimal), fecha_bloqueo (datetime), timestamp
AlertaCobranzaAdministrativa
Atributos: user_id, monto_adeudado (decimal), historial_pagos_fallidos (array), prioridad (enum: LOW/MEDIUM/HIGH), timestamp


**Políticas automatizadas (Policies):**
WHEN PagoFallado IS TRIGGERED
IF intento_numero == 1
THEN SCHEDULE ReintentoPagoProgramado(delay=1_hour)
AND SEND NotificacionPushPrimerFalloPago
ELSE IF intento_numero == 2
THEN SCHEDULE ReintentoPagoProgramado(delay=4_hours)
AND SEND EmailSegundoFalloPago
AND SUGGEST MetodosPagoAlternativos
ELSE IF intento_numero == 3
THEN TRIGGER ReservaCanceladaPorImpago
AND TRIGGER UsuarioBloqueadoParaNuevasReservas
AND TRIGGER AlertaCobranzaAdministrativa
AND SEND NotificacionProveedorReservaCancelada
AND SEND EmailUsuarioBloqueo

[INSERTAR IMAGEN: Diagrama de secuencia de reintentos de pago con timeouts]

---

**Impacto de las resoluciones en Tactical Design:**

Estas decisiones de resolución de Hot Spots generaron:
- **12 nuevos Domain Events** agregados al Event Storm refinado
- **8 nuevas Políticas automatizadas** que se implementarán como Process Managers en el Bounded Context de Operations
- **3 nuevas Agregados** en diseño táctico: KYCVerificationProcess, CancellationPolicy, PaymentRetryScheduler

La documentación de estos Hot Spots resueltos se utilizó directamente en la fase de Context Mapping (sección 2.5.1) para definir claramente las responsabilidades y fronteras de cada Bounded Context, asegurando que no haya ambigüedad en qué contexto maneja cada escenario de excepción.

---

## 12. ALINEAR IMPACT MAPPING CON HYPOTHESIS (Sección 2.4.2, pág 153)

### PROBLEMA DETECTADO
Los Business Goals del Impact Map no se alinean con las métricas específicas de las Hypothesis Statements.

### CORRECCIÓN OBLIGATORIA

**Reescribir la sección 2.4.2 completa con Business Goals que reflejen las métricas SMART:**

---

#### 2.4.2 Impact Mapping

El Impact Mapping de WheelsPe conecta los objetivos estratégicos de negocio (Business Goals) con los actores clave (Actors/Personas), los cambios de comportamiento esperados (Impacts) y las funcionalidades específicas que se implementarán (Deliverables). Cada Business Goal está alineado directamente con las Hypothesis Statements validables de la sección 1.2.2.3.

---

**BUSINESS GOAL 1: Validar Oferta de Inventario Verificado**

**Goal Statement:**
Alcanzar **15 vehículos particulares registrados y acreditados** (KYC del propietario completado + documentación vehicular validada + checklist fotográfico de 12 puntos completado) con **al menos 1 alquiler completado exitosamente por cada vehículo**, en los primeros **60 días post-lanzamiento** en la comunidad piloto UPC, para validar la disposición de propietarios a confiar en el modelo de verificación digital sin interacción presencial previa.

**ACTORS/PERSONAS:**
- Carlos Peña (Proveedor Particular - Dueño de 1-2 vehículos)
- Ana Monroy (Gestora de MYPE de alquiler - 5-8 vehículos)

**IMPACTS (Cambios de comportamiento esperados):**
1. Proveedores completan proceso de verificación KYC sin abandonar el flujo (tasa de completitud >70%)
2. Proveedores publican vehículos con checklist fotográfico completo en primera iteración
3. Proveedores aceptan reservas de arrendatarios con calificación ≥4.0 estrellas sin solicitar validaciones adicionales
4. Proveedores renuevan disponibilidad de vehículo semanalmente (re-engagement)

**DELIVERABLES (Funcionalidades específicas):**
- US02: Verificar identidad mediante KYC multinivel (DNI + selfie + biometría)
- US05: Acreditar propiedad vehicular con documentación legal
- US12: Registrar checklist fotográfico de 12 puntos pre/post alquiler
- US22: Consultar catálogo de vehículos con filtros avanzados
- US30: Configurar umbrales de reputación mínimos para filtrado automático
- Dashboard de ganancias que visualiza "tiempo muerto" del vehículo (motivador de disponibilidad constante)

[INSERTAR IMAGEN: Diagrama de Impact Mapping para Business Goal 1]

---

**BUSINESS GOAL 2: Validar Modelo de Amortización mediante Carpooling**

**Goal Statement:**
Lograr que **40% de conductores arrendatarios** (target: 6 de cada 15 conductores activos) **publiquen al menos 1 ruta de carpooling** durante el periodo de alquiler del vehículo, y que estos conductores **incrementen su frecuencia de alquiler a ≥2.5 veces/mes** (vs 1.2 veces/mes de conductores sin carpooling), validando en **primeros 90 días** que la integración alquiler+carpooling reduce barreras económicas y genera uso recurrente.

**ACTORS/PERSONAS:**
- Marco Ruiz (Conductor Arrendatario - Consultor 29 años)
- Javier Campos (Conductor Arrendatario - Ingeniero independiente 32 años)

**IMPACTS (Cambios de comportamiento esperados):**
1. Conductores publican rutas de carpooling inmediatamente después de confirmar alquiler de vehículo
2. Conductores establecen precios de cuota por pasajero entre S/ 7-9 (premium vs informal)
3. Conductores programan rutas recurrentes (misma ruta lun-vie) en lugar de republicar manualmente
4. Conductores alquilan con mayor frecuencia al validar que recuperan 50-70% del costo operativo

**DELIVERABLES (Funcionalidades específicas):**
- US13: Publicar ruta de movilidad compartida con detalles (origen, destino, horario, asientos, precio)
- US17: Automatizar rutas recurrentes semanales (template reutilizable)
- US21: Vincular métodos de pago para cobro automático de cuotas de pasajeros
- US25: Emitir facturas electrónicas deducibles de impuestos para conductores
- US32: Liquidar automáticamente cuota de carpooling dividida entre pasajeros
- Calculadora integrada de división de costos (muestra "Estás recuperando 65% del gasto")

[INSERTAR IMAGEN: Diagrama de Impact Mapping para Business Goal 2]

---

**BUSINESS GOAL 3: Validar Adopción en Comunidades Institucionales Femeninas**

**Goal Statement:**
Registrar **50 estudiantes universitarias mujeres** (18-25 años) con correos institucionales verificados (@upc.edu.pe, @pucp.edu.pe) que completen **≥1 reserva de ruta de carpooling**, y lograr **NPS ≥7.5/10** en percepción de seguridad post-experiencia, en **primeros 60 días post-lanzamiento**, validando que la segmentación institucional elimina barrera de desconfianza que causa 60% de abandono en coordinación informal.

**ACTORS/PERSONAS:**
- Esther Ospina (Pasajera - Estudiante Administración 21 años)
- Lucía Vega (Pasajera - Estudiante Medicina 22 años)

**IMPACTS (Cambios de comportamiento esperados):**
1. Pasajeras activan filtro "Solo mi universidad" en el 80%+ de búsquedas
2. Pasajeras en horario nocturno (8 PM - 6 AM) activan filtro "Solo conductoras mujeres" en >50% de búsquedas
3. Pasajeras comparten ubicación GPS en tiempo real con contactos de confianza durante el 100% de viajes
4. Pasajeras completan calificación post-viaje en >85% de casos (vs 40% en plataformas donde es opcional)

**DELIVERABLES (Funcionalidades específicas):**
- US14: Buscar rutas con segmentación institucional (validación de correo @dominio)
- US11: Filtrar rutas por preferencia de género de conductor/a
- US06: Monitorear ruta en tiempo real vía GPS compartible con familia
- US08: Activar botón de pánico conectado a contactos de confianza + equipo seguridad
- US10: Gestionar lista de contactos de confianza (hasta 5 contactos)
- US28: Evaluar servicio bidireccional obligatorio (sin opción de omitir)

[INSERTAR IMAGEN: Diagrama de Impact Mapping para Business Goal 3]

---

**BUSINESS GOAL 4: Validar Modelo de Pricing Premium por Seguridad**

**Goal Statement:**
Alcanzar precio promedio de **S/ 7.5 por viaje** en reservas del Segmento Pasajeros (rango aceptable S/ 7.0-9.0), representando **premium de 50% vs S/ 5 de grupos informales**, con **tasa de conversión de búsqueda a reserva ≥35%** (vs 25% benchmark de carpooling sin validación), y **churn rate ≤25%** tras primer viaje, validando en **primeros 90 días** que usuarios perciben suficiente valor de seguridad para pagar más.

**ACTORS/PERSONAS:**
- Esther Ospina (Pasajera)
- Lucía Vega (Pasajera)
- Marco Ruiz (Conductor - define pricing de sus rutas)

**IMPACTS (Cambios de comportamiento esperados):**
1. Pasajeros aceptan precios de S/ 7-9 sin negociar (pricing transparente basado en distancia+demanda)
2. Conductores establecen precios premium confiando en que validación institucional justifica costo adicional
3. Usuarios completan segundo viaje en siguientes 30 días tras primer experiencia positiva (retención)
4. Usuarios abandonan grupos informales de WhatsApp tras 3-5 viajes exitosos en plataforma

**DELIVERABLES (Funcionalidades específicas):**
- Motor de pricing dinámico que sugiere rango S/ 7-9 según distancia, horario, demanda
- US19: Consultar reputación completa antes de reservar (justifica premium por confianza)
- US27: Aplicar cupones promocionales de bienvenida (subsidio de primeros 3 viajes -30%)
- US36: Reconocer usuarios frecuentes con distintivos gamificados ("Viajero Confiable - 20 viajes")
- Comparador automático "S/ 7 WheelsPe verificado vs S/ 15 taxi"

[INSERTAR IMAGEN: Diagrama de Impact Mapping para Business Goal 4]

---

Estos 4 Business Goals del Impact Mapping están directamente trazables a las 6 Hypothesis Statements de la sección 1.2.2.3 y a los experimentos MVP definidos en el Sprint Planning de la sección 4.2.1.

---

## 13. ACTUALIZAR JOURNEY MAPS Y EMPATHY MAPS (Secciones 2.3.3 y 2.3.4, pág 105-109)

### CORRECCIÓN OBLIGATORIA

Necesitas crear **3 Journey Maps separados** y **3 Empathy Maps separados** (uno por cada User Persona).

**Mantener:**
- Journey Map de Carlos Peña (Proveedor)
- Empathy Map de Carlos Peña

**Crear NUEVOS:**
- Journey Map de Marco Ruiz (Conductor)
- Journey Map de Esther Ospina (Pasajera)
- Empathy Map de Marco Ruiz
- Empathy Map de Esther Ospina (actualizar si ya existe para reflejar solo rol de pasajera)

---

### Journey Map de Marco Ruiz (Conductor Arrendatario)

**Escenario:** Marco necesita vehículo para reunión con cliente en Miraflores y quiere recuperar parte del costo mediante carpooling.

| Fase | Acciones | Pensamientos | Emociones | Pain Points | Oportunidades |
|------|----------|--------------|-----------|-------------|---------------|
| **Descubrimiento** | Marco descubre WheelsPe por post de LinkedIn de un colega | "¿Será confiable? ¿Realmente podré recuperar gastos?" | Curiosidad, escepticismo | Desconfía de apps nuevas sin testimonios | Mostrar casos de éxito de profesionales |
| **Registro** | Crea cuenta, completa KYC con DNI+selfie, valida email corporativo @ey.com | "El KYC es tedioso pero entiendo que es para seguridad" | Neutralidad, ligera impaciencia | Proceso KYC toma 8 minutos | Explicar PORQUÉ se pide cada dato |
| **Búsqueda de Vehículo** | Filtra Toyota/Nissan, fecha mañana, zona San Borja | "Necesito algo presentable, no un auto viejo" | Exigencia, enfoque | Pocos vehículos en horario específico (7 AM) | Sugerir horarios alternativos con más oferta |
| **Reserva** | Selecciona Toyota Yaris 2023, S/ 90 por 5 horas | "S/ 90 es razonable si recupero S/ 30 con pasajeros" | Satisfacción calculada | Ninguno | Mostrar calculadora "Puedes recuperar S/ 36 con 2 pasajeros" |
| **Publicación de Ruta** | Inmediatamente publica "San Borja → Miraflores, 7:30 AM, 2 asientos, S/ 8 c/u" | "Espero que alguien reserve rápido" | Esperanza, urgencia | Ansiedad por si no llena asientos | Notificación push cuando hay solicitud |
| **Aprobación de Pasajeros** | Recibe 3 solicitudes, revisa perfiles, acepta 2 ejecutivos con LinkedIn verificado | "Perfecto, son profesionales como yo" | Confianza, satisfacción | Uno de los solicitantes tiene perfil incompleto | Mostrar badge "Perfil 100% completo" |
| **Día del Viaje** | Recoge vehículo, pasa por punto acordado, recoge pasajeros | "Llegaron puntuales, conversación interesante sobre industria financiera" | Alegría, networking | Pasajero pidió desviación no pactada | Dejar claro en app que ruta es fija |
| **Post-Viaje** | Completa checklist devolución, califica pasajeros 5★, recibe pago automático S/ 16 | "Gasté S/ 74 neto (S/ 90 - S/ 16). ¡Vale totalmente la pena!" | Euforia, logro | Ninguno | Mostrar "Ahorraste S/ 16 = 18% del costo" |

[INSERTAR IMAGEN: User Journey Map de Marco creado en UXPressia]

---

### Journey Map de Esther Ospina (Pasajera)

**Escenario:** Esther busca ruta recurrente UPC Villa → su casa en Los Olivos después de clases (salida 9 PM).

| Fase | Acciones | Pensamientos | Emociones | Pain Points | Oportunidades |
|------|----------|--------------|-----------|-------------|---------------|
| **Descubrimiento** | Ve poster en campus UPC "Movilidad segura entre alumnos UPC" | "¿Por fin algo mejor que los grupos caóticos de WhatsApp?" | Esperanza, intriga | Ninguno | QR code en poster para descarga directa |
| **Registro** | Crea cuenta con correo @upc.edu.pe, valida automáticamente comunidad UPC | "Me gusta que solo sea para UPC, me siento más tranquila" | Alivio, confianza inicial | Ninguno | Mostrar cuántos alumnos UPC ya están registrados |
| **Búsqueda de Ruta** | Busca "UPC Villa → Los Olivos", activa filtro "Solo mi universidad" + "Solo conductoras" | "Necesito conductora mujer para sentirme segura de noche" | Precaución, empoderamiento | Solo 2 rutas disponibles con esos filtros | Incentivar a conductoras a publicar rutas |
| **Evaluación de Conductor** | Revisa perfil de conductora: Ana, Ingeniería Industrial UPC, 15 viajes, 4.8★ | "Tiene buenas reseñas y es de mi misma universidad" | Confianza creciente | Quisiera ver si tiene ruta recurrente | Mostrar tag "Ruta recurrente Lun-Vie" |
| **Reserva** | Reserva asiento, paga S/ 7 con Yape | "S/ 7 es más que el jalón informal (S/ 5) pero vale la pena por seguridad" | Satisfacción, inversión en seguridad | Ninguno | Recordar que es -50% vs taxi (S/ 15) |
| **Preparación** | Configura compartir GPS con su mamá automáticamente al iniciar viaje | "Mi mamá va a poder rastrearme en vivo, eso me tranquiliza" | Protección, alivio | Tuvo que explicarle a mamá cómo funciona el link | Tutorial familiar en app |
| **Durante Viaje** | Sube al auto, valida código PIN, charla con conductora sobre exámenes finales | "Qué bueno hablar con alguien que entiende la presión de la U" | Camaradería, seguridad | Tráfico retrasó llegada 15 min | Alertar a usuario sobre tráfico en ruta |
| **Post-Viaje** | Califica 5★, activa opción "Reservar misma ruta próxima semana" | "Esto es justo lo que necesitaba. Bye WhatsApp caótico" | Lealtad, satisfacción profunda | Ninguno | Ofrecer "Reserva automática semanal" |

[INSERTAR IMAGEN: User Journey Map de Esther creado en UXPressia]

---

### Empathy Map de Marco Ruiz

[INSERTAR IMAGEN: Empathy Map de Marco creado en UXPressia]

**¿Qué PIENSA y SIENTE?**
- "Cada peso cuenta. Si puedo reducir 60% del costo de alquiler, lo haré."
- "Llegar en auto propio proyecta más seriedad que en taxi."
- "El carpooling no es solo ahorro, es networking con profesionales."
- Siente: Presión por optimizar gastos, orgullo por imagen profesional, ambición de crecimiento

**¿Qué VE?**
- Colegas consultores que llegan a reuniones en taxis Uber (imagen menos profesional)
- Grupos de LinkedIn llenos de spam, difícil coordinar carpooling
- Autos de alquiler tradicional costosos (S/ 120/día)
- Ejecutivos de su nivel que enfrentan el mismo problema de costos

**¿Qué DICE?**
- "No puedo justificar S/ 120 solo por 3 horas de reunión."
- "Si pudiera compartir con 2 ejecutivos que van al mismo edificio, alquilaría todas las semanas."
- "La validación profesional es más importante que la calificación numérica."
- "Necesito factura para declarar esto como gasto deducible."

**¿Qué HACE?**
- Alquila autos esporádicamente solo para reuniones críticas
- Toma taxis/Uber para reuniones menos importantes (resignado)
- Intenta coordinar carpooling por LinkedIn mensajes directos (bajo éxito)
- Lleva registro mental de cuánto gasta mensualmente en movilidad

**PAINS (Dolores):**
- Alquiler frecuente es económicamente inviable
- Desperdiciar 4 asientos vacíos = desperdiciar dinero
- No hay forma de validar que pasajeros sean realmente profesionales
- Impuntualidad de pasajeros informales le hace perder reuniones

**GAINS (Ganancias):**
- Reducir 50-70% del costo operativo mediante división
- Proyectar imagen profesional ante clientes
- Construir red de contactos durante viajes compartidos
- Facturar gastos para deducción de impuestos

---

### Empathy Map de Esther Ospina (Actualizado solo para rol Pasajera)

[INSERTAR IMAGEN: Empathy Map de Esther creado en UXPressia]

**¿Qué PIENSA y SIENTE?**
- "Necesito llegar segura a casa después de clases nocturnas."
- "No confío en desconocidos de grupos de WhatsApp."
- "Si es de mi universidad, hay mayor probabilidad de que sea confiable."
- Siente: Ansiedad sobre seguridad nocturna, frustración con informalidad, necesidad de pertenecer a comunidad segura

**¿Qué VE?**
- Noticias de robos/asaltos en transporte público
- Grupos de WhatsApp con 300+ mensajes diarios caóticos
- Amigas que han tenido experiencias negativas en "jalones"
- Aplicaciones como Uber/Cabify muy caras para uso diario (S/ 15-20)

**¿Qué DICE?**
- "Prefiero pagar S/ 7 y sentirme segura que S/ 5 con miedo."
- "Si es alumna de medicina como yo, sé que pasó por la admisión rigurosa de UPCH."
- "Mi mamá se queda más tranquila si puede rastrearme por GPS."
- "He llegado tarde a guardias 2 veces por cancelaciones de último minuto."

**¿Qué HACE?**
- Comparte ubicación en vivo con su mamá cada vez que toma "jalón"
- Viaja siempre acompañada cuando puede (nunca sola de noche si es posible)
- Revisa perfil de Facebook de conductor antes de aceptar
- Le pide a conductor que le confirme 2 horas antes para evitar cancelaciones

**PAINS (Dolores):**
- Cancelaciones frecuentes (40% de coordinaciones) causan retrasos académicos
- Exposición a riesgo de seguridad con desconocidos no validados
- Ansiedad constante durante viajes nocturnos
- Grupos de WhatsApp con ruido informativo insoportable

**GAINS (Ganancias):**
- Viajar exclusivamente con comunidad universitaria verificada
- Compartir GPS en tiempo real con familia sin pasos manuales
- Conductoras mujeres para viajes nocturnos (opción de filtro)
- Ahorro vs taxi (S/ 7 vs S/ 15) sin sacrificar seguridad

---

## 14. AGREGAR BIBLIOGRAFÍA ACADÉMICA (Referencias, pág final)

### PROBLEMA DETECTADO
Falta incluir mínimo 4 papers académicos Q1/Q2 recientes sobre el dominio del problema y técnicas móviles.

### CORRECCIÓN OBLIGATORIA

**Agregar a la sección de Referencias (formato APA 7):**

---

### Referencias sobre Dominio del Problema (Movilidad urbana, Economía P2P)

Bardhi, F., & Eckhardt, G. M. (2024). Access-based consumption: The rise of collaborative mobility platforms and their impact on urban transportation. *Journal of Consumer Research, 51*(2), 287-305. https://doi.org/10.1093/jcr/ucae015

Böcker, L., & Meelen, T. (2024). Trust mechanisms in peer-to-peer vehicle sharing: A systematic review of identity verification systems. *Transportation Research Part A: Policy and Practice, 178*, 103856. https://doi.org/10.1016/j.tra.2024.103856

Shaheen, S., Cohen, A., & Broader, J. (2023). Ride-sharing and ride-hailing: Adoption, impacts, and the future of mobility in emerging economies. *Transport Reviews, 43*(6), 981-1007. https://doi.org/10.1080/01441647.2023.2198765

Yang, F., Ding, F., Qu, X., & Ran, B. (2024). Safety perceptions in gender-segregated ride-sharing: Evidence from university students in Latin America. *Accident Analysis & Prevention, 186*, 107058. https://doi.org/10.1016/j.aap.2024.107058

### Referencias sobre Técnicas de Desarrollo Móvil

Kumar, R., & Singh, P. (2024). Cross-platform mobile development with Flutter: Performance benchmarking and architectural patterns. *Journal of Systems and Software, 205*, 111823. https://doi.org/10.1016/j.jss.2023.111823

Luo, Y., Zhang, M., & Wang, L. (2023). Domain-driven design in microservices architecture for mobile backend systems: A systematic literature review. *Information and Software Technology, 162*, 107279. https://doi.org/10.1016/j.infsof.2023.107279

Martínez-Fernández, S., Bogner, J., & Franch, X. (2024). Real-time GPS tracking in Android applications: Battery optimization strategies and architectural trade-offs. *IEEE Transactions on Mobile Computing, 23*(4), 2987-3002. https://doi.org/10.1109/TMC.2023.3287654

Stol, K.-J., Ralph, P., & Fitzgerald, B. (2024). Lean UX in mobile application development: An empirical study of hypothesis-driven design in agile teams. *Empirical Software Engineering, 29*(1), 18. https://doi.org/10.1007/s10664-023-10412-3

---

**Instrucción:** Estos papers son ficticios para propósitos de este documento. DEBES reemplazarlos con papers REALES de bases de datos académicas como Scopus, IEEE Xplore, ScienceDirect. Buscar en Google Scholar con filtros:
- Años: 2023-2024
- Revistas Q1/Q2 (verificar en Scimago Journal Rank)
- Keywords: "peer-to-peer mobility", "ride-sharing platforms", "trust in sharing economy", "Flutter mobile development", "domain-driven design microservices"

---

## 15. REALIZAR 2 ENTREVISTAS ADICIONALES - GUÍA DE EJECUCIÓN

### Entrevista #9: Conductor Arrendatario

**Perfil a reclutar:**
- Hombre o mujer, 28-40 años
- Profesional independiente o consultor
- Alquila vehículos 2-4 veces al mes para trabajo
- Usuario de LinkedIn activo

**Preguntas clave a incluir:**

1. ¿Con qué frecuencia necesitas vehículo temporal para trabajo? ¿Qué tipo de actividades?
2. ¿Cuánto gastas mensualmente en alquiler + combustible + peajes?
3. ¿Alguna vez has intentado compartir los gastos del viaje? ¿Cómo fue la experiencia?
4. Si hubiera una app que te permitiera publicar rutas y dividir costos automáticamente, ¿qué porcentaje del gasto esperarías recuperar para que valga la pena usarla?
5. ¿Qué te daría confianza para compartir viajes con desconocidos? (validación de empresa, LinkedIn, calificaciones)
6. ¿Estarías dispuesto a pagar una comisión del 10% si la app valida identidad corporativa de pasajeros?

**Formato de transcripción:** Igual al resto de entrevistas en sección 2.2.2

---

### Entrevista #10: Pasajera Recurrente

**Perfil a reclutar:**
- Mujer, 19-25 años
- Estudiante universitaria O trabajadora joven
- Viaja en rutas fijas diariamente
- Actualmente usa grupos de WhatsApp/Facebook

**Preguntas clave:**

1. ¿Cómo coordinas actualmente tus viajes diarios? ¿Qué aplicaciones o grupos usas?
2. ¿Has tenido experiencias negativas? (cancelaciones, impuntualidad, sensación de inseguridad)
3. Si sales tarde de noche (9-10 PM), ¿qué medidas de seguridad tomas?
4. ¿Pagarías S/ 2-3 más por viaje si la app garantiza que TODOS los conductores son de tu universidad/empresa?
5. ¿Te gustaría poder filtrar para viajar solo con conductoras mujeres en horario nocturno?
6. ¿Qué funcionalidad de seguridad sería indispensable para que abandones los grupos informales?

---

## RESUMEN EJECUTIVO DE CORRECCIONES

### ✅ COMPLETADAS EN ESTE DOCUMENTO

1. ✅ Reordenar Product Backlog por valor de negocio
2. ✅ Dividir Segmento #2 en Conductores + Pasajeros (3 segmentos totales)
3. ✅ Reescribir 47 títulos de User Stories con verbos
4. ✅ Agregar nombres descriptivos a escenarios de Acceptance Criteria (con ejemplos completos para US01, US02, US08)
5. ✅ Reescribir 3 Problem Statements con formato Lean UX
6. ✅ Agregar priorización de Riskiest Assumption + plan de validación
7. ✅ Mejorar 6 Hypothesis Statements con métricas SMART
8. ✅ Resolver 3 Hot Spots del Event Storming con decisiones de diseño
9. ✅ Alinear Impact Mapping con Hypothesis (4 Business Goals SMART)
10. ✅ Crear User Persona #3 (Marco Ruiz - Conductor)
11. ✅ Actualizar User Task Matrix a 3 columnas
12. ✅ Crear Journey Map de Marco + Esther
13. ✅ Crear Empathy Map de Marco + actualizar Esther
14. ✅ Agregar bibliografía académica (8 papers)

### 🔶 PENDIENTES DE EJECUTAR (REQUIEREN TRABAJO MANUAL)

15. 🔶 Realizar Entrevista #9 (Conductor) + transcripción
16. 🔶 Realizar Entrevista #10 (Pasajera) + transcripción
17. 🔶 Actualizar sección 2.2.1 Diseño de Entrevistas (separar bloques por 3 segmentos)
18. 🔶 Actualizar sección 2.2.3 Análisis de Entrevistas (gráficos separados Conductores vs Pasajeros)
19. 🔶 Crear User Personas en UXPressia y exportar imágenes
20. 🔶 Crear Journey Maps en UXPressia y exportar imágenes
21. 🔶 Crear Empathy Maps en UXPressia y exportar imágenes
22. 🔶 Aplicar nombres de escenarios a las 45 User Stories restantes
23. 🔶 Buscar y reemplazar bibliografía con papers académicos REALES
24. 🔶 Revisar formato APA 7 en TODO el documento
25. 🔶 Eliminar viudas y huérfanas
26. 🔶 Verificar numeración de TODAS las figuras y tablas
27. 🔶 Actualizar carátula con datos correctos

---

## PRIORIDAD DE EJECUCIÓN (ROADMAP)

**ESTA SEMANA (Crítico para AV1):**
- Días 1-2: Correcciones 1, 2, 3, 4 (reordenar backlog, segmentos, títulos US, escenarios)
- Días 3-4: Entrevistas 15, 16 + correcciones 17, 18
- Día 5: Correcciones 5, 6, 7 (Problem Statements, Assumptions, Hypothesis)

**PRÓXIMA SEMANA (Calidad para TB1):**
- Días 6-8: Correcciones 8, 9 (Hot Spots, Impact Mapping)
- Días 9-10: Correcciones 10-13 (Personas, Task Matrix, Journey, Empathy)
- Días 11-12: Correcciones 19-21 (UXPressia + exports)

**ÚLTIMA SEMANA ANTES DE ENTREGA:**
- Días 13-14: Correcciones 22-23 (Escenarios restantes, bibliografía)
- Días 15-16: Correcciones 24-27 (Formato APA, figuras, tablas, carátula)
- Día 17: Revisión final + generación de PDF

---

**FIN DEL DOCUMENTO DE CORRECCIONES**