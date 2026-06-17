# WheelsPe — Backlog Backend (`MOVEO-Backend`) — CONTRATO REAL

> Para el equipo de backend. Stack: **C# / ASP.NET Core (monolito)**, MySQL (EF Core) + MongoDB (logs).
> **Autenticación: SIN JWT — stateless por `userId`.** El login devuelve el objeto usuario; la sesión = guardar `id` y enviarlo como `?userId=` / `renterId=` / `ownerId=` / `payerId=`.
> Base URL: `http://<host>:8080/api/v1` · Swagger: `/swagger/index.html` · Repo: https://github.com/App-Moviles-MOVEO/MOVEO-Backend
> Actualizado 13/06/2026 contra el **código real** (reemplaza la versión anterior basada en el backlog).

Leyenda: ✅ Implementado · 🟡 Parcial · ⬜ No existe

> ⚠️ **Corrección importante:** la versión previa de este archivo (basada en el backlog) marcaba KYC, incidents e invoices como implementados. **No existen en el código.** Igualmente, las rutas reales difieren del backlog (`/rentals`, `/adventure-routes`, `/payments`, `/Reviews`, `/user-reviews`).

---

## 1. Inventario REAL de endpoints (11 controllers, todo bajo `/api/v1`)

### IAM / Auth — `/auth`
| Método | Ruta | Descripción | Cliente | Proveedor |
|---|---|---|:--:|:--:|
| POST | `/auth/register` | Registro (`role` = `renter`/`owner`); devuelve **usuario, no token** | ✅ | ✅ |
| POST | `/auth/login` | Login; devuelve **usuario, no token** | ✅ | ✅ |
| POST | `/auth/logout` | Logout simbólico | ✅ | ✅ |
| GET | `/auth/me?userId=` | Datos del usuario logueado | ✅ | ✅ |
| POST | `/auth/change-password` | Cambiar contraseña (requiere la actual) | ✅ | ✅ |

### Usuarios — `/users`
| Método | Ruta | Descripción |
|---|---|---|
| GET | `/users` · `/users?email=` · `/users/{id}` | Listar / buscar / perfil + reputación |
| POST / PUT / PATCH / DELETE | `/users[/{id}]` | Crear / editar / eliminar (hard delete) |

### Vehículos — `/vehicles` *(Rental)*
| Método | Ruta | Descripción | Cliente | Proveedor |
|---|---|---|:--:|:--:|
| GET | `/vehicles` | Catálogo + filtros | ✅ | ✅ (`?ownerId=`) |
| GET | `/vehicles/{id}` | Detalle (`ownerName`, `rating`, `reviewsCount`) | ✅ | ✅ |
| GET | `/vehicles/{id}/availability` | **Fechas ocupadas (calendario)** ⭐ | ✅ | ✅ |
| POST / PUT / PATCH / DELETE | `/vehicles[/{id}]` | Publicar / editar / eliminar | — | ✅ |

Filtros `GET /vehicles` (combinables): `ownerId`, `status`, `minPrice`, `maxPrice`, `district`, `bodyType`, `transmission`, `fuelType`, `startDate`+`endDate`, `lat`+`lng`+`sort=distance`, `page`+`pageSize`.

### Reservas / Alquileres — `/rentals` *(Rental)*
| Método | Ruta | Descripción | Cliente | Proveedor |
|---|---|---|:--:|:--:|
| GET | `/rentals?renterId=` / `?ownerId=` / `?vehicleId=` / `?status=` | Consultas | ✅ | ✅ |
| GET | `/rentals/{id}` · `/rentals/user/{userId}` · `/rentals/active` | Detalle / por usuario / activas | ✅ | ✅ |
| POST | `/rentals` | **Crear reserva** (valida solapamiento → 409) ⭐ | ✅ | — |
| PUT | `/rentals/{id}` | Actualizar | ✅ | ✅ |
| PATCH | `/rentals/{id}` | Estado: `accepted`/`active`/`completed`/`cancelled` | ✅ cancelar | ✅ aceptar/activar/completar |
| POST | `/rentals/{id}/pay` | **Pagar en un paso** | ✅ | — |
| DELETE | `/rentals/{id}` | Eliminar | ✅ | ✅ |

Estados: `pending` → `accepted` → `active` → `completed`, o `cancelled`.

### Carpooling / Rutas — `/adventure-routes` *(Adventure)*
> Una sola entidad sirve rutas de aventura y carpool. Campos carpool: `departureDate`, `departureTime`, `seatsTotal`, `seatsAvailable`, `pricePerSeat`, `onlyWomen`, `community`, `lat`, `lng`, `status`.

| Método | Ruta | Descripción | Pasajero | Conductor |
|---|---|---|:--:|:--:|
| GET | `/adventure-routes` · `/adventure-routes/{id}` | Buscar / detalle | ✅ | ✅ (`?ownerId=`) |
| POST | `/adventure-routes` | **Publicar ruta/viaje** | — | ✅ |
| POST | `/adventure-routes/{id}/book` | **Reservar asiento(s)** | ✅ | — |
| PUT / DELETE | `/adventure-routes/{id}` | Editar / eliminar | — | ✅ |

Filtros: `ownerId`, `type`, `difficulty`, `featured`, `onlyWomen`. **Falta** filtro por `community`/dominio (US14 → 🟡).

### Pagos — `/payments` *(Payment — registro en BD, sin pasarela real)*
| Método | Ruta | Descripción |
|---|---|---|
| GET | `/payments?payerId=` / `?recipientId=` / `?rentalId=` / `?status=` / `?type=` | Mis pagos / ingresos / filtros |
| GET | `/payments/{id}` · `/payer/{id}` · `/recipient/{id}` · `/rental/{id}` | Consultas |
| POST / PUT / PATCH / DELETE | `/payments[/{id}]` | Crear / actualizar / **reembolsar** (`status="refunded"`) / eliminar |

### Reseñas — `/Reviews` (de vehículo) · `/user-reviews` (entre usuarios)
| Método | Ruta | Descripción |
|---|---|---|
| GET/POST/PUT/DELETE | `/Reviews[/{id}]` (`?vehicleId=`/`?rentalId=`/`?reviewerId=`/`?revieweeId=`) | Reseñas de vehículo |
| GET/POST/PUT/DELETE | `/user-reviews[/{id}]` (`?reviewedUserId=`/`?reviewerId=`/`?rentalId=`/`?type=`) | Calificación mutua (`owner_to_renter`/`renter_to_owner`) |

> Cubre evaluación bidireccional y reputación: **US28 / US35 / US19 / US37 ✅**.

### Notificaciones — `/Notifications` · Chat — `/messages` · Soporte — `/support-tickets`
| Módulo | Endpoints clave | US |
|---|---|---|
| Notificaciones | `GET /Notifications?userId=` (+`&read=false`), `POST`, `PUT /{id}/read`, `PUT /user/{id}/read-all`, `DELETE` | — ✅ |
| Chat 1-a-1 | `GET /messages?userId=&otherUserId=`, `GET /messages/conversations/{userId}`, `POST`, `PUT /{id}/read` | US18 ✅ |
| Soporte / ayuda | `GET/POST /support-tickets` (+`/{id}`, `/user/{id}`, `/status/{s}`, `PATCH /{id}/close`, `/{ticketId}/messages`) | US44 ✅ |

---

## 2. Disponibilidad por fechas (avance de Sprint 2 — implementado ⭐)
- **Solapamiento al crear reserva:** `POST /rentals` rechaza dobles reservas con **409 `vehicle_not_available`** (+ `conflictingRanges`). Valida: `endDate<=startDate`→400, fecha pasada→400, `renterId==ownerId`→400, vehículo inexistente→404, no `active`→409 `vehicle_not_active`.
- `GET /vehicles/{id}/availability` → `busyRanges` para bloquear días en calendario.
- `GET /vehicles?startDate=&endDate=` → solo autos libres en el rango.
- Filtros `transmission` y `fuelType`; expiración automática de `pending` a los 30 min; orden por cercanía + paginación; cancelar libera fechas.
- Convención: **UTC**, rangos `[start, end)`; bloquean `pending/accepted/active`; liberan `cancelled/completed`.

---

## 3. User Stories — estado real en el backend

### ✅ Soportadas por endpoint real
US01 (register) · US03 (login, sin JWT) · US22 (catálogo+detalle) · disponibilidad por fechas ⭐ · US13 (publicar ruta) · US15 (book) · US11 (`onlyWomen=true`) · US28/US35 (`/user-reviews`,`/Reviews`) · US19/US37 (reputación) · US18 (chat) · notificaciones · mis reservas/ventas · soporte · flujo completo crear/pagar/gestionar reserva.

### 🟡 Parciales
| US | Qué hay / qué falta |
|---|---|
| US05 | `POST /vehicles` sí; falta validación de documentos/SOAT |
| US14 | Campo `community` existe; falta filtro por query param |
| US16 | `book` descuenta cupos y marca `full`; falta lista de pasajeros y aprobar/rechazar |
| US20 | Se puede pasar ruta a `completed`; sin geolocalización ni confirmación formal |
| US31 / US32 | `/rentals/{id}/pay` + `/payments` registran pago; **sin pasarela real (SP01)** |
| US26 / US33 | `PATCH /payments/{id}` `status="refunded"`; sin flujo/política automática |
| US45 | `DELETE /users/{id}` (hard delete); no es borrado GDPR (soft + purge) |

### ⬜ Sin endpoint (NO marcar como hechas)
US02 KYC (solo flags `DniVerified`/`LicenseVerified` en `User`) · US04 recuperar contraseña (solo `change-password`) · US06/US07 GPS · US08 pánico (no hay `/incidents`) · US09 PIN · US10 contactos de confianza · US12 checklist · US17 rutas recurrentes · US21 métodos de pago · US24 escrow · US25 invoices · US27 cupones · US29/US36 badges · US30/US38 umbrales · US34 ofertas · US40/US41 admin (no hay `/incidents`) · SP01–SP04.

### Campos en `User` sin endpoint propio
Verificación: `EmailVerified`, `PhoneVerified`, `DniVerified`, `LicenseVerified` (sin flujo KYC). Bancarios: `BankName`, `BankAccountType`, `BankAccountNumber`, `BankAccountVerified`. Stats: `TotalRentals`, `TotalSpent`, `TotalEarned`, `ActiveRentals`, `CompletedRentals`, `CanceledRentals`, `Avatar`.

---

## 4. Pendientes priorizados (backend nuevo a construir)
| Prio | US | Funcionalidad | Propuesta de endpoint |
|---|---|---|---|
| P1 | US02 | Flujo KYC real | `POST /users/{id}/kyc/upload`, `GET /status`, `POST /verify`, `POST /reject` |
| P2 | SP01/US31/US32 | Pasarela de pago real | integrar Stripe/Yape/Plin sobre `/payments` |
| P3 | US24 | Escrow (hold/release) | `POST /rentals/{id}/hold`, `POST /release` |
| P4 | US04 | Recuperar contraseña | `POST /auth/password/forgot`, `POST /reset` |
| P5 | US06/07/08 | GPS en vivo + pánico | `/trips/{id}/location` (WS/SSE), `/incidents` |
| P6 | US21 | Métodos de pago tokenizados | `POST /users/{id}/payment-methods` |
| P7 | US25/27/34 | Comprobantes, cupones, ofertas | `/invoices`, `/coupons/validate`, `/vehicles/{id}/promotions` |
| P8 | US14 | Filtro por comunidad en rutas | query param en `GET /adventure-routes` |
| P9 | US16 | Lista de pasajeros + aprobar/rechazar | `/adventure-routes/{id}/passengers` |

### Spikes
SP01 pasarelas de pago · SP02 GPS/mapas (Google Maps vs Mapbox) · SP03 KYC con IA (Jumio/Onfido) · SP04 microservicios (hoy el backend es **monolito**).
