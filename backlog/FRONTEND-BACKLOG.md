# WheelsPe — Backlog Frontend Móvil — ESTADO REAL

> Dos apps sobre **un solo backend** (`MOVEO-Backend`, base `/api/v1`, **SIN JWT — sesión por `userId`**):
> - **App Cliente / Arrendatario → Kotlin** (Android nativo). Núcleo ya conectado al backend real.
> - **App Proveedor / Conductor → Flutter** (por iniciar en Sprint 3).
>
> Repo: https://github.com/App-Moviles-MOVEO/MOVEO-Frontend · Actualizado 13/06/2026.
> Contrato real de endpoints en [`BACKEND-BACKLOG.md`](BACKEND-BACKLOG.md).

Leyenda: ✅ Hecho y conectado al backend real · 🟡 A medias / demo / falta backend · 🔵 Solo UI (sin backend) · ⬜ Pendiente · ⛔ Otra app/rol

> ⚠️ **Correcciones frente a la versión anterior de este archivo:**
> 1. **No hay JWT.** No "guardar JWT": guardar el `userId` que devuelve `/auth/login` y enviarlo como `?userId=`/`renterId=`/`ownerId=`.
> 2. **Endpoints reales:** `/rentals`, `/adventure-routes`, `/payments` + `/rentals/{id}/pay`, `/Reviews` + `/user-reviews`, `/messages`, `/Notifications`, `/support-tickets`.
> 3. **Chat (US18) y notificaciones YA funcionan** (antes marcados pendientes).
> 4. **KYC, recuperar contraseña, escrow, métodos de pago, GPS, pánico, comprobantes, cupones NO tienen backend** → esas pantallas son UI/demo a la espera de la API.

---

## APP CLIENTE (Kotlin)

### 1. Núcleo ya hecho (Sprint 1 + Sprint 2)
| US | Función | Estado | Endpoint real |
|---|---|---|---|
| US01 | Registro con rol único | ✅ | `POST /auth/register` |
| US03 | Login + persistencia de sesión | ✅ | `POST /auth/login` (guardar `userId`, **sin JWT**) |
| US22 | Catálogo + detalle de vehículos | ✅ | `GET /vehicles`, `/vehicles/{id}` |
| — | Selección de fechas + disponibilidad | ✅ | `GET /vehicles/{id}/availability`, `POST /rentals` (409) |
| — | Mis reservas (lista + detalle) | ✅ | `GET /rentals?renterId=` |
| US14 | Buscar rutas de carpooling | ✅ | `GET /adventure-routes` (filtro comunidad 🟡) |
| US15 | Reservar asiento | ✅ | `POST /adventure-routes/{id}/book` |
| US28/US35 | Calificar servicio | ✅ | `POST /user-reviews`, `/Reviews` |
| US19/US37 | Reputación / reseñas | ✅ | `GET /users/{id}`, `/user-reviews` |
| US18 | Chat 1-a-1 | ✅ | `/messages` |
| — | Notificaciones | ✅ | `/Notifications` |
| US44 | Ayuda / FAQ | ✅ | `/support-tickets` |

### 2. A medias / demo (depende del backend)
| US | Función | Estado | Qué falta |
|---|---|---|---|
| US02 | Verificación KYC | 🟡 | App tiene UI; **el backend NO expone flujo KYC** (solo flags en `User`). Reconciliar. |
| US31 | Pago de alquiler | 🟡 | Stripe modo demo + Yape un paso; **falta pasarela real (SP01)** |
| US32 | Cuota de carpooling | 🟡 | Mismo límite de pasarela que US31 |
| US24 | Escrow / garantía | 🟡 | Solo visual en resumen; sin retención real |
| US04 | Recuperar contraseña | 🟡 | UI lista; backend no tiene `forgot/reset` |
| US11 | Filtro "Solo Mujeres" | 🟡 | Toggle en UI; backend tiene `onlyWomen` pero falta exponerlo en filtro |
| US29/US36 | Recompensas / badges | 🟡 | Puntos en UI; sin lógica de canje ni badges |

### 3. Solo UI / pendientes (cliente)
| US | Función | Estado | Qué falta |
|---|---|---|---|
| US06/US07 | GPS en tiempo real / desvíos | 🔵 | Pantalla simulada; falta `/trips` (WS/SSE) |
| US08 | Botón de pánico | 🔵 | Solo UI; falta `/incidents` + GPS + push |
| US10 | Contactos de confianza | 🔵 | Lista fija; falta backend |
| US21 | Vincular métodos de pago | 🔵 | Mock; falta tokenización |
| US25 | Comprobantes / contratos (PDF) | ⬜ | Falta `/invoices` y consumirlo |
| US26/US33 | Reembolsos (cliente) | ⬜ | Backend soporta `refunded`; falta UI |
| US27 | Cupones y beneficios | ⬜ | No implementado |
| US34 | Ofertas promocionales | ⬜ | No implementado |
| US45 | Baja / borrado de datos (GDPR) | ⬜ | Falta backend GDPR |

### 4. Fuera de alcance de la app Cliente (van en app Proveedor)
US05 (acreditar/publicar vehículo) · US13 (publicar ruta) · US16 (aprobar pasajeros/aforo) · publicar vehículo / mis publicaciones · US40/US41 (paneles admin → web). ⛔

---

## APP PROVEEDOR (Flutter) — Sprint 3, por iniciar

El backend **ya soporta** el núcleo del proveedor; no requiere backend nuevo para empezar.

| US | Función | Estado | Endpoint real |
|---|---|---|---|
| US01/US03 | Registro/login (rol `owner`) | ⬜ | `/auth/register`, `/auth/login` |
| US05 | Publicar / editar vehículo | ⬜ | `POST/PUT/DELETE /vehicles` |
| US13 | Publicar ruta de carpool | ⬜ | `POST /adventure-routes` |
| US16 | Aceptar/activar/completar reservas | ⬜ | `PATCH /rentals/{id}` |
| — | Ver reservas de mis autos | ⬜ | `GET /rentals?ownerId=` |
| — | Panel de ingresos | ⬜ | `GET /payments?recipientId=` |
| US19/US37 | Reputación recibida | ⬜ | `GET /user-reviews?reviewedUserId=` |
| US18 | Chat con clientes | ⬜ | `/messages` |
| — | Notificaciones | ⬜ | `/Notifications` |

> Campos de ingresos/banco ya existen en `User` (`TotalEarned`, `BankAccountNumber`, etc.); falta exponer endpoints dedicados si se quieren editar por separado.

---

## 5. Orden de trabajo recomendado
- **Cliente (Kotlin):** cerrar lo que tiene backend listo y aún no se consume → **US25 (comprobantes)** y **US26/US33 (reembolsos UI)**; luego retirar la validación de solapamiento propia y usar `/vehicles/{id}/availability` + 409.
- **Proveedor (Flutter):** empezar ya por registro/login (rol owner) → publicar vehículo → gestionar reservas (`PATCH /rentals`) → ingresos y reputación. Todo con endpoints existentes.
- **Bloqueadas por backend (no empezar UI definitiva):** KYC real, pánico/GPS, escrow, métodos de pago, recuperar contraseña, cupones. Abrir tickets de coordinación (ver pendientes P1–P9 en `BACKEND-BACKLOG.md`).
- **Sesión:** guardar `userId` de forma segura (EncryptedSharedPreferences en Kotlin / flutter_secure_storage en Flutter). **No** usar header `Authorization: Bearer`.
- **Fuente de verdad del contrato:** Swagger del backend (`/swagger/index.html`).
