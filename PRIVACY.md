# Privacidad — ValidaPagoMovil

## Qué datos procesa

- **Pagos Pago Móvil:** banco, monto, referencia, fecha/hora, canal y teléfono
  del pagador cuando el banco lo incluye.
- **Configuración:** nombre del comercio, tasas, destinos de Telegram/WhatsApp,
  preferencias de la app.
- **Telegram:** token del bot, chat/canal destino y message_id de cada aviso.
- **Diagnóstico:** logs locales saneados y último error.

No se recibe ni se almacena la clave de tu banca en línea, OTP ni saldo.

## Dónde se guarda

- El libro local y la cola usan **EncryptedSharedPreferences** con una clave del
  **Android Keystore** (AES-256-GCM).
- El token del bot también se guarda cifrado.
- `allowBackup=false`: Android no sube el libro a Google Drive ni a otro backup
  en la nube.
- Los backups manuales se cifran con contraseña (AES-256-GCM + PBKDF2).

## Qué sale del teléfono

- **Telegram/WhatsApp:** solo si tú configuras ese canal. Se envía banco, monto,
  referencia y teléfono **enmascarado**; no se envía el libro completo.
- **Tasas:** consultas HTTPS a BCV/Binance/proveedor configurado.
- **Suite (solo Pro):** si conectas la Suite, los pagos se envían a **tu**
  servidor; no a un servidor de ValidaPagoMovil.
- **Actualizaciones:** consulta HTTPS a GitHub Releases.
- **Anuncios gratis:** son anuncios internos de ValidaPagoMovil. No hay SDK de
  anuncios ni rastreadores de terceros en esta versión.

No hay analítica, telemetría ni publicidad de terceros en la beta ni en Pro.

## Permisos

- **SMS:** leer/recibir SMS para detectar Pago Móvil.
- **Notificaciones:** leer notificaciones bancarias (incluidas las local-only).
- **Accesibilidad:** fallback para notificaciones que Android no entrega; solo
  procesa apps de la allowlist.
- **Cámara:** escanear QR de la Suite y QR C2P.
- **Contactos:** **no se pide READ_CONTACTS**. El selector usa el diálogo nativo
  y solo recibe el contacto que eliges.
- **Bluetooth:** impresora térmica opcional.
- **Burbuja/overlay:** función opcional de mostrador.
- **Instalar APK:** actualizador guiado; el usuario confirma cada instalación.

## Retención y borrado

- Puedes borrar pagos individuales desde Cobros.
- Puedes exportar/restaurar el libro desde Ajustes.
- Al desinstalar la app se borran los datos locales (salvo backups que hayas
  exportado).
- Para revocar el acceso de un bot, usa `/revoke` en @BotFather y borra el
  token en la app.

## Contacto

Abre un issue en el repositorio de descargas para preguntas de privacidad. No
incluyas datos reales de pagos ni credenciales.
