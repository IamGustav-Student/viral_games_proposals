# Arquitectura Técnica: L2 Multiverse

## Stack Tecnológico Propuesto
- **Frontend (Lobby & UI):** Next.js 14+ (React) con TailwindCSS para una interfaz moderna y rápida.
- **Motor de Juegos:** Phaser.js o PixiJS para los minijuegos 2D.
- **Backend:** Node.js con Express o Fastify.
- **Comunicación en Tiempo Real:** Socket.io para el chat y movimiento en el Lobby.
- **Base de Datos:**
    - **PostgreSQL:** Datos de usuario, inventario, clanes.
    - **Redis:** Leaderboards en tiempo real y sesiones.
- **Infraestructura:** Despliegue en Vercel (Frontend) y Railway/DigitalOcean (Backend).

## Componentes del Sistema
1.  **Identity Service:** Gestión de cuentas (Auth via Telegram o Email).
2.  **Economy Service:** API central que valida transacciones de Adena y ítems. Evita hacks sincronizando el estado en el servidor.
3.  **Minigame Bridge:** Un sistema que permite inyectar el estado del usuario desde el Lobby al minijuego de forma segura.

## Seguridad
- Validación del lado del servidor para cada intento de "Enchant" o "Spoil".
- Uso de Webhooks para transacciones de pago seguras.
