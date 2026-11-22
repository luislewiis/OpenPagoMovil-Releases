# Planes y activación Pro

## Planes

| | **Gratis** | **Beta 1.0.91** | **Pro** |
|---|---|---|---|
| Captura SMS/notificación/accesibilidad | Sí | Sí | Sí |
| Libro local + backup | Sí | Sí | Sí |
| Telegram A (solo avisos) | Sí | Sí | Sí |
| Telegram B (Reclamar + /buscar) | No | Sí | Sí |
| Telegram C (/ref, /micierre, huérfanos) | No | Sí (experimental) | Sí |
| Suite Desktop / modo servidor | No | No | Sí |
| Multi-dispositivo | No | No | Sí |
| Webhooks | No | No | Sí |
| Exportaciones avanzadas | No | No | Sí |
| Marca blanca | No | No | Sí |
| Anuncios | Sí (internos) | No | No |
| Dispositivos | 1 | 1 | Según licencia |
| Destinos Telegram | 1 | 1 | Según licencia |

Precios de referencia:

- **Pro mensual:** $3.49/mes
- **Pro anual:** $29.99/año

## Cómo comprar

Abre un issue en este repositorio o escribe por el mismo canal donde recibiste
la beta. Indica:

- nombre o comercio,
- plan (mensual/anual),
- cantidad de teléfonos,
- ID de dispositivo de cada teléfono (ver abajo).

No envíes cédulas, tokens de Telegram ni datos de pagos.

## Activar una licencia `.opmlic`

1. Instala la APK **ValidaPagoMovil Pro** (se entrega por release privado). La APK Free no acepta `.opmlic`.
2. Abre **Ajustes → Licencia**.
3. Copia tu **ID de dispositivo** (formato `ABCD-EFGH-IJKL-MNOP`).
4. Envía ese ID al vendedor.
5. Recibe el archivo `.opmlic` y pulsa **Importar .opmlic**.
6. La app verifica la firma ECDSA P-256, la fecha y el dispositivo. Si es
   válida, la edición cambia a **PRO** al instante.
7. Si la APK Pro no tiene licencia, muestra una pantalla de activación con el
   mismo botón de importar y el ID del dispositivo.

## Qué pasa si la licencia vence

- La app vuelve a la edición gratuita (o bloquea la APK Pro si no hay licencia).
- El libro local, los backups y la configuración **no se borran**.
- Puedes importar una licencia nueva sin reinstalar.

## Seguridad

- La clave privada que firma las licencias **no está en la APK**.
- La APK solo contiene la clave pública.
- Una licencia alterada o de otro dispositivo se rechaza.
- El archivo no contiene datos de pagos ni credenciales.

## Soporte

Incluye en el issue:

- edición y versión (`Ajustes → Licencia` y pie de Ajustes),
- ID de dispositivo,
- modelo de teléfono y Android,
- pasos para reproducir.
