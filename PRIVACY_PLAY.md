# Política de privacidad — ValidaPagoMovil (versión Play)

**Última actualización:** 2026-11-24
**Aplicación:** ValidaPagoMovil (`com.validapagomovil.app.play`)
**Versión:** 1.0.94 (build 87)

Esta política aplica **solo a la versión limitada publicada en Google Play**.
La versión completa distribuida fuera de Play tiene su propia política.

## 1. Qué hace esta versión

ValidaPagoMovil Play es un cuaderno local de pagos Pago Móvil. Lee
**notificaciones bancarias** que el usuario autoriza mediante el acceso a
notificaciones de Android, extrae banco, monto y referencia, y guarda el pago en
el teléfono. No es un banco, no mueve dinero, no pide claves bancarias, OTP ni
saldo.

Esta versión **no incluye** SMS, accesibilidad, Suite, servidor local, broker,
Telegram, WhatsApp automático, webhooks, multi-dispositivo, anuncios de terceros
ni actualizaciones fuera de Play.

## 2. Datos que procesa

- **Pagos:** banco, monto, referencia, fecha/hora, canal y el teléfono del
  pagador **solo si la notificación bancaria lo incluye**.
- **Configuración:** nombre del comercio, tasas, tema, idioma, voz, impresora,
  seguridad y preferencias.
- **Diagnóstico:** logs locales saneados y último error.

No se recibe ni se almacena la clave de la banca en línea, OTP, saldo ni
credenciales de pago.

## 3. Dónde se guarda

- El libro local y la cola usan **EncryptedSharedPreferences** con una clave del
  **Android Keystore** (AES-256-GCM).
- `allowBackup=false`: Android no sube el libro a Google Drive ni a otro backup
  en la nube.
- Los backups manuales se cifran con contraseña (AES-256-GCM + PBKDF2).
- Los datos se quedan en el teléfono. Esta versión **no envía pagos a ningún
  servidor de ValidaPagoMovil**.

## 4. Qué sale del teléfono

- **Tasas:** consultas HTTPS a BCV/Binance/proveedor configurado. No incluyen
  datos de pagos.
- **Backups:** solo si el usuario exporta manualmente a un archivo que él elige.
- **Google Play:** la app se instala y actualiza desde Play; Google aplica su
  propia política.

No hay analítica, telemetría, publicidad de terceros ni rastreadores.

## 5. Permisos

- **Notificaciones (NotificationListenerService):** leer notificaciones
  bancarias para detectar pagos. Es el único canal de captura de esta versión.
- **POST_NOTIFICATIONS:** mostrar la notificación del servicio en Android 13+.
- **Servicio en primer plano (specialUse):** mantener la captura de
  notificaciones activa en segundo plano.
- **Cámara:** escanear QR C2P y QR de configuración.
- **Bluetooth:** impresora térmica opcional.
- **Biometría/huella:** bloqueo local de la app (opcional).
- **RECEIVE_BOOT_COMPLETED:** reanudar el servicio tras reiniciar el teléfono.
- **Internet:** consultar tasas.

Esta versión **no pide** READ_SMS, RECEIVE_SMS, accesibilidad,
SYSTEM_ALERT_WINDOW, REQUEST_INSTALL_PACKAGES ni alarmas exactas.

## 6. Retención y borrado

- Puedes borrar pagos individuales desde Cobros.
- Puedes exportar/restaurar el libro desde Ajustes.
- Al desinstalar la app se borran los datos locales (salvo backups que hayas
  exportado).
- Para revocar el acceso a notificaciones: Ajustes de Android → Acceso a
  notificaciones → desactiva ValidaPagoMovil.

## 7. Menores

La app es una herramienta de negocio para mayores de 18 años. No está dirigida
a niños ni recopila datos de menores.

## 8. Contacto

Para preguntas de privacidad, abre un issue en el repositorio público de
descargas:

https://github.com/luislewiis/OpenPagoMovil-Releases/issues

No incluyas datos reales de pagos ni credenciales.
