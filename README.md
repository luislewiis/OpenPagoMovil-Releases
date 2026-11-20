# ValidaPagoMovil — Beta cerrada

Beta de **ValidaPagoMovil** para probar captura de Pago Móvil, conciliación local y Modo Caja de Telegram.

## Descargar

Ve a **Releases** y descarga:

- `ValidaPagoMovil_v1.0.90-beta.apk`
- SHA-256: `5371F206DF3B172BED6F0B18DC46448F34EC2FD8A2BC5DDD92B2C6BBAA24AD26`

Instala con "Instalar de todas formas" si Android muestra el aviso de origen desconocido.

## Qué incluye esta beta

- Captura por SMS, notificación, accesibilidad, correo y modo local.
- Libro local cifrado y backup con contraseña.
- Telegram A (solo avisos), B (reclamar + /buscar) y C (experimental: /ref, /micierre, huérfanos).
- Tasas híbridas BCV USD/EUR, Binance P2P e Inteligente.
- Temas Azul, Negro total y Blanco.
- UI de Cobros expandible nativa.
- Sin anuncios.

## Límites de la beta

- Vence **30 días** después de la compilación.
- C está en periodo **experimental** y avisa del riesgo de batería.
- El feature-gate de 1 dispositivo / sin Suite / sin webhooks todavía no está aplicado en esta beta técnica.

## Requisitos de Telegram

1. Crea un bot en @BotFather y copia el token.
2. Agrega el bot al grupo/canal como administrador con "Publicar mensajes" y "Gestionar mensajes".
3. Publica `/pago` una vez.
4. En ValidaPagoMovil: Ajustes → Telegram → pega token → Detectar canal o grupo → Probar conexión → Guardar.
5. Para Modo Caja, cada cajero escribe `/id` y el operador pega los IDs autorizados.

## Feedback

Abre un issue en este repositorio con:

- modelo de teléfono y versión de Android,
- qué esperabas que pasara,
- qué pasó,
- captura o log de **Ajustes → Avanzado → Copiar último error**.

## Licencia y versiones

- **Beta:** gratis, sin anuncios, con vencimiento.
- **Gratis:** captura y libro local, 1 dispositivo, 1 destino, Modo A.
- **Pro:** $3.49/mes · $29.99/año — B/C, multidispositivo, Suite, webhooks y exportaciones.

Este repositorio es solo de distribución de la beta; no contiene el código fuente.
