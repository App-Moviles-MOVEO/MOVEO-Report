# WheelsPe — Product Backlog & Estado de Implementación

> Documento de coordinación entre equipos. Fuente: `README.md` (Informe del Trabajo Final, secciones 2.4.1 User Stories, 2.4.3 Product Backlog y 4.2 Sprint 1).
> Última actualización: 2026-06-13.

## 1. Producto y arquitectura

**Producto:** WheelsPe — plataforma de movilidad colaborativa (alquiler de vehículos entre pares + carpooling) para Perú.

| Componente | Tecnología | Repositorio | Estado |
|---|---|---|---|
| Backend (API) | **C# / ASP.NET Core** (monolito), MySQL (EF Core) + MongoDB (logs), **SIN JWT — sesión por `userId`**, OpenAPI/Swagger | [MOVEO-Backend](https://github.com/App-Moviles-MOVEO/MOVEO-Backend) | Núcleo desplegado con Swagger |
| App móvil **Cliente/Arrendatario** | **Kotlin** (Android nativo) | [MOVEO-Frontend](https://github.com/App-Moviles-MOVEO/MOVEO-Frontend) | Núcleo conectado (Sprints 1–2) |
| App móvil **Proveedor/Conductor** | **Flutter / Dart** | [MOVEO-Frontend](https://github.com/App-Moviles-MOVEO/MOVEO-Frontend) | Por iniciar (Sprint 3) |
| Landing Page | HTML5 + CSS3 + JS vanilla | [MOVEO-Landing-Page](https://github.com/App-Moviles-MOVEO/MOVEO-Landing-Page) | ✅ Desplegada en GitHub Pages |

**Base URL API:** `/api/v1` · **Auth:** stateless por `userId` (NO Bearer/JWT) · **Formato:** JSON/HTTPS · **Swagger:** `/swagger/index.html`

> ⚠️ **Corrección 13/06/2026:** este documento maestro se generó inicialmente a partir del backlog y de las capturas de Swagger del Sprint 1. Tras revisar el **código real**, varias filas de la matriz cambiaron (KYC, incidents/pánico e invoices **NO existen**; chat y notificaciones **sí existen**; los nombres de endpoints son `/rentals`, `/adventure-routes`, `/payments`, `/Reviews`, `/user-reviews`). Las fuentes autoritativas y actualizadas son [`BACKEND-BACKLOG.md`](BACKEND-BACKLOG.md) y [`FRONTEND-BACKLOG.md`](FRONTEND-BACKLOG.md). La columna "Backend" de la matriz inferior ya refleja la realidad.

**Bounded Contexts (DDD):** IAM · Carpooling · Rental · Billing · Operations

### Cómo usar este backlog
- **Backend** → ver [`BACKEND-BACKLOG.md`](BACKEND-BACKLOG.md): endpoints ya implementados y los que faltan.
- **Frontend móvil (Kotlin y Flutter)** → ver [`FRONTEND-BACKLOG.md`](FRONTEND-BACKLOG.md): mismo set de User Stories para ambas apps, consumiendo la misma API.
- Este archivo es el **índice maestro + matriz de estado**.

---

## 2. Épicas

| Epic | Título |
|---|---|
| EP01 | Gestión de la identidad y acceso |
| EP02 | Seguridad y control operacional |
| EP03 | Inventario y ofertas de vehículos |
| EP04 | Experiencia de alquiler y reserva |
| EP05 | Movilidad compartida (carpooling) |
| EP06 | Operaciones financieras |
| EP07 | Reputación y núcleo de la plataforma |
| EP08 | Información y fidelización |
| SP   | Spike Stories (investigación técnica) |

---

## 3. Matriz de estado (Backend × Frontend)

Leyenda: ✅ Hecho · 🟡 Parcial · ⬜ Pendiente · — No aplica

| # | US | Título (Product Backlog) | Épica | SP | Backend | Mobile (Kotlin/Flutter) |
|---|----|--------------------------|-------|----|---------|--------------------------|
| 1 | US39 | Visualizar propuesta de valor (Landing) | EP08 | 5 | — | ✅ (Landing web) |
| 2 | US22 | Consultar catálogo de vehículos | EP03 | 5 | ✅ `GET /vehicles` | ✅ Sprint 1 |
| 3 | US13 | Publicar ruta de movilidad compartida | EP05 | 8 | ✅ `POST /routes` | ✅ Sprint 1 |
| 4 | US14 | Buscar rutas con segmentación institucional | EP05 | 5 | 🟡 `GET /routes` (falta filtro dominio) | ✅ Sprint 1 |
| 5 | US31 | Procesar pago de alquiler multicanal | EP06 | 8 | 🟡 `/rentals/{id}/pay` + `/payments` (sin pasarela real) | 🟡 demo |
| 6 | US32 | Liquidar cuota de carpooling | EP06 | 8 | 🟡 `/payments` (sin pasarela real) | 🟡 demo |
| 7 | US08 | Activar alerta de emergencia / pánico | EP02 | 5 | ⬜ (no hay `/incidents`) | 🔵 solo UI |
| 8 | US28 | Evaluar servicio (bidireccional) | EP07 | 5 | ✅ `POST /user-reviews` | ✅ Cliente |
| 9 | US12 | Checklist fotográfico del vehículo | EP02 | 5 | ⬜ | ⬜ |
| 10 | US21 | Vincular métodos de pago | EP06 | 5 | ⬜ | ⬜ |
| 11 | US24 | Garantía mediante retención (Escrow) | EP06 | 5 | ⬜ | ⬜ |
| 12 | US01 | Registrar cuenta con rol único | EP01 | 3 | ✅ `POST /auth/register` | ✅ Sprint 1 |
| 13 | US02 | Verificar identidad (KYC) | EP01 | 5 | ⬜ (solo flags en `User`, sin flujo) | 🟡 UI |
| 14 | US03 | Iniciar sesión + persistencia | EP01 | 2 | ✅ `POST /auth/login` (sin JWT, `userId`) | ✅ Sprint 1 |
| 15 | US05 | Acreditar propiedad de vehículo | EP03 | 5 | 🟡 `POST /vehicles` (falta validación docs) | ⬜ |
| 16 | US06 | Monitoreo de ruta en tiempo real (GPS) | EP02 | 8 | ⬜ | ⬜ |
| 17 | US09 | Validar inicio de viaje con código PIN | EP02 | 3 | ⬜ | ⬜ |
| 18 | US15 | Reservar asiento en ruta compartida | EP05 | 4 | ✅ `POST /adventure-routes/{id}/book` | ✅ Cliente |
| 19 | US25 | Emitir comprobantes y contratos | EP06 | 4 | ⬜ (no hay `/invoices`) | ⬜ |
| 20 | US11 | Filtro de preferencia de género | EP02 | 3 | ⬜ | ⬜ |
| 21 | US16 | Aprobar pasajeros y controlar aforo | EP05 | 4 | 🟡 `book` descuenta cupos (falta aprobar/rechazar) | ⬜ (Proveedor) |
| 22 | US19 | Consultar reputación de usuarios | EP07 | 2 | 🟡 `GET /users/{id}` | ⬜ |
| 23 | US30 | Configurar umbrales de reputación | EP07 | 3 | ⬜ | ⬜ |
| 24 | US26 | Procesar reembolsos automáticos | EP06 | 3 | 🟡 `PATCH /payments/{id}` (`status=refunded`, sin política) | ⬜ |
| 25 | US10 | Gestionar contactos de confianza | EP02 | 2 | ⬜ | ⬜ |
| 26 | US17 | Automatizar rutas recurrentes | EP05 | 3 | ⬜ | ⬜ |
| 27 | US18 | Coordinación por mensajería (chat) | EP05 | 3 | ✅ `/messages` | ✅ Cliente |
| 28 | US20 | Confirmar llegada al destino | EP05 | 3 | 🟡 `complete` (sin geo) | ⬜ |
| 29 | US27 | Aplicar cupones y beneficios | EP08 | 3 | ⬜ | ⬜ |
| 30 | US29 | Recompensar usuarios alta reputación | EP07 | 3 | ⬜ | ⬜ |
| 31 | US34 | Ofertas promocionales temporales | EP08 | 3 | ⬜ | ⬜ |
| 32 | US36 | Distintivos por comportamiento positivo | EP07 | 8 | ⬜ | ⬜ |
| 33 | US37 | Consultar historial de reseñas | EP07 | 3 | ✅ `GET /user-reviews`, `/users/{id}` | ✅ Cliente |
| 34 | US38 | Filtrar solicitudes por umbral de confianza | EP07 | 3 | ⬜ | ⬜ |
| 35 | US42 | Beneficios para propietarios (Landing) | EP08 | 5 | — | ✅ (Landing web) |
| 36 | US43 | Ventajas del carpooling (Landing) | EP08 | 5 | — | ✅ (Landing web) |
| 37 | US44 | Centro de ayuda y FAQ (Landing) | EP08 | 3 | — | ✅ (Landing web) |
| 38 | US04 | Recuperar contraseña olvidada | EP01 | 2 | ⬜ | ⬜ |
| 39 | US07 | Rastrear viaje activo (seguridad pasajero) | EP02 | 8 | ⬜ (no hay GPS/`incidents`) | 🔵 simulado |
| 40 | US33 | Ejecutar reembolsos automatizados | EP06 | 8 | 🟡 `PATCH /payments/{id}` (sin automatización) | ⬜ |
| 41 | US35 | Evaluación mutua tras servicio | EP07 | 5 | ✅ `/user-reviews` | ✅ Cliente |
| 42 | US40 | Monitorear anomalías financieras (Admin) | EP06 | 5 | ⬜ (no hay `/incidents`) | ⛔ web |
| 43 | US41 | Mediar disputas de reputación (Admin) | EP07 | 2 | ⬜ (no hay `/incidents`) | ⛔ web |
| 44 | US45 | Baja voluntaria / eliminación de datos | EP01 | 2 | ⬜ | ⬜ |
| 45 | US46 | Solicitar alianza corporativa | EP08 | 3 | — (Landing) | ⬜ |
| 46 | US47 | Optimizar latencia geolocalización (Técnica) | SP02 | 3 | ⬜ | ⬜ |
| 47 | SP01 | Spike: pasarelas de pago (Stripe/Yape/PayPal) | SP | 5 | ⬜ | — |
| 48 | SP02 | Spike: GPS y mapas (Google Maps vs Mapbox) | SP | 5 | ⬜ | ⬜ |
| 49 | SP03 | Spike: KYC con IA (Jumio/Onfido) | SP | 8 | 🟡 | — |
| 50 | SP04 | Spike: microservicios y contenedores | SP | 8 | 🟡 | — |

> **Nota de inconsistencia detectada en el informe:** en la tabla 2.4.1 (User Stories) el título de `US22` es *"Procesamiento de pago por alquiler"* y `US31` *"Procesamiento multicanal de pagos"*, mientras que en el Product Backlog 2.4.3 `US22` figura como *"Consultar catálogo de vehículos"*. Este documento usa los títulos del **Product Backlog (2.4.3)** como referencia canónica, que es la fuente priorizada. Conviene unificar en el README.

---

## 4. Resumen ejecutivo del estado

**Backend (`MOVEO-Backend`) — implementado realmente:**
- IAM: registro, login (sin JWT), CRUD de usuarios, cambiar contraseña. **KYC NO existe** (solo flags en `User`).
- Rental: catálogo de vehículos (CRUD + estado + **disponibilidad por fechas** ⭐), reservas `/rentals` (crear con anti-solapamiento 409, pagar en un paso, gestionar estado, consultas).
- Carpooling: `/adventure-routes` (CRUD, `book` de asiento, `onlyWomen`). Falta filtro por comunidad.
- Pagos: `/payments` (crear/actualizar/refund + consultas por payer/recipient). **Sin pasarela real.** **No hay `/invoices`.**
- Reseñas: `/Reviews` + `/user-reviews` (evaluación bidireccional). Chat `/messages` ✅. Notificaciones `/Notifications` ✅. Soporte `/support-tickets` ✅.
- **NO existen:** KYC, incidents (pánico/anomalías/disputas), invoices, escrow, métodos de pago, GPS/trips, recuperar contraseña, cupones.

**Frontend Cliente (Kotlin) — conectado al backend real (Sprints 1–2):** US01, US03, US22 (+ fechas/disponibilidad), US14, US15, US18 (chat), US28/US35, US19/US37, notificaciones, ayuda. Demo/parcial: US02 (KYC UI), US31/US32 (pago demo), US24 (escrow visual). Solo UI: GPS, pánico, contactos, métodos de pago.

**Frontend Proveedor (Flutter) — por iniciar (Sprint 3):** publicar vehículo/ruta, gestionar reservas, ingresos, reputación — todo con endpoints existentes.

> El detalle por User Story está en [`BACKEND-BACKLOG.md`](BACKEND-BACKLOG.md) y [`FRONTEND-BACKLOG.md`](FRONTEND-BACKLOG.md) (fuentes autoritativas).
