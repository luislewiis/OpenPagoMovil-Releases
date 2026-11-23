successfully downloaded text file (SHA: 2709997666631a4b487fab6abf0a8d0bba219ab3)
# ValidaPagoMovil — Descargas

Repositorio **público de distribución**. Aquí solo viven las APK, la guía de
instalación y el feedback. El código fuente, la Suite y la versión Pro están en
un repositorio privado.

## Canales

| Canal | Tag | Qué es |
|---|---|---|
| **Beta** | `v1.0.91-beta` | Beta pública con licencia firmada, A/B/C y límites. |
| **Gratis** | `free-v1.0.91` | Versión gratuita con anuncios internos y Modo A. |
| **Pro** | privado | B/C, Suite, webhooks, multi-dispositivo y exportaciones. |

Cada edición tiene su propio nombre en el lanzador: **ValidaPagoMovil Free**,
**ValidaPagoMovil Beta** y **ValidaPagoMovil Pro**. Free y Beta no se convierten
en Pro con un archivo `.opmlic`; Pro se instala aparte y se activa con licencia.

## Descarga directa

- **Beta 1.0.91:** https://github.com/luislewiis/OpenPagoMovil-Releases/releases/download/v1.0.91-beta/ValidaPagoMovil_v1.0.91-beta.apk
- **Gratis 1.0.91:** https://github.com/luislewiis/OpenPagoMovil-Releases/releases/download/free-v1.0.91/ValidaPagoMovil_v1.0.91-free.apk
- **Pro:** se entrega por release privado/licencia (ver PRO.md).

## Beta 1.0.91

Descarga desde **Releases**:

- `ValidaPagoMovil_v1.0.91-beta.apk`
- versionCode **84**
- SHA-256: `3FE8D8451D669BF5F0A23EBD8A9D776DC19E70CEE53FD684DDB3F83F526CAC3F`
- Tamaño: 5.967.391 bytes

### Qué incluye

- Captura por SMS, notificación, accesibilidad, correo y modo local.
- Libro local cifrado y backup con contraseña.
- Telegram **A** (solo avisos), **B** (Reclamar + `/buscar`) y **C**
  (experimental: `/ref`, `/micierre`, huérfanos).
- Tasas híbridas BCV USD/EUR, Binance P2P e Inteligente.
- Temas Azul, Negro total y Blanco.
- UI de Cobros nativa con scroll unico para ver todas las transacciones.
- **Sin anuncios.**
- **Licencia beta incluida y firmada** (ECDSA P-256). No tienes que importar
  nada para probarla.

### Límites de la beta

- Vence el **31/01/2027 23:59 UTC**.
- **1 dispositivo** y **1 destino de Telegram**.
- **Sin Suite**, sin multi-dispositivo, sin webhooks y sin exportaciones
  avanzadas.
- C sigue siendo **experimental**: avisa del riesgo de batería y pide
  biometría/PIN.
- El límite de 1 dispositivo es local a la instalación. Para una licencia Pro
  atada a tu teléfono se usa el ID de dispositivo (ver `PRO.md`).

## Versión gratis 1.0.91

Disponible en **Releases** con el tag `free-v1.0.91`:

- `ValidaPagoMovil_v1.0.91-free.apk`
- versionCode **84**
- SHA-256: `2E224B43683BE3BB4770ADF8028E2E9B55DE017FF5EE8F333E057C4B5692E7B4`

Incluye captura, libro local, Modo A, 1 dispositivo y 1 destino. Muestra
**anuncios internos** de ValidaPagoMovil (no hay rastreadores de terceros).

La versión Free es un producto independiente y **no se activa con `.opmlic`**.
Para quitar los anuncios y usar B/C, Suite, webhooks y multi-dispositivo,
instala **ValidaPagoMovil Pro**.

## Pro

La versión Pro no se publica en este repositorio. Incluye:

- Modo Caja **B/C** en producción.
- **Suite Desktop** y modo servidor.
- **Webhooks**, multi-dispositivo y exportaciones avanzadas.
- Sin anuncios.
- Licencia `.opmlic` firmada, atada a tu dispositivo.

Precios de referencia: **$3.49/mes** o **$29.99/año**.

Cómo comprar y activar: [PRO.md](PRO.md).

## Instalar

1. Descarga la APK desde **Releases**.
2. Si Android muestra el aviso de origen desconocido, elige
   **Instalar de todas formas**.
3. Abre la app y acepta los términos.
4. En el primer uso elige **Usar sin servidor** (Free/Beta) o conecta tu Suite
   si tienes Pro.
5. Concede SMS/notificaciones/accesibilidad según la guía de la app.

### Telegram

1. Crea un bot en [@BotFather](https://t.me/BotFather) y copia el token.
2. Agrega el bot al grupo/canal como administrador con **Publicar mensajes** y
   **Gestionar mensajes**.
3. Publica `/pago` una vez.
4. En la app: **Ajustes → Telegram → pegar token → Detectar canal o grupo →
   Probar conexión → Guardar**.
5. Para Modo Caja, cada cajero escribe `/id` y el operador pega los IDs
   autorizados.

## Privacidad

- El libro local vive cifrado con Android Keystore.
- `allowBackup=false`: Android no sube el libro a la nube.
- El token del bot se guarda cifrado.
- Los logs se sanean (teléfonos, cédulas, OTP, tokens).
- Telegram/WhatsApp reciben el teléfono enmascarado, monto y referencia; no
  reciben el libro completo.
- La versión gratis usa anuncios internos, sin SDK de terceros.

Más detalle: [PRIVACY.md](PRIVACY.md).

## Feedback

Abre un issue en este repositorio con:

- modelo de teléfono y versión de Android,
- qué esperabas que pasara,
- qué pasó,
- captura o log de **Ajustes → Avanzado → Copiar último error**.

No publiques tokens, cédulas, teléfonos completos ni referencias reales.
