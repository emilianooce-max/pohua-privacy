# Política de Privacidad de Pohua

**Última actualización:** 27 de mayo de 2026

Pohua ("nosotros" o "la app") es una aplicación de Android para llevar el control de gastos e ingresos personales, leyendo las notificaciones que las apps de bancos envían a tu celular. Esta política explica qué información procesa la app, cómo se procesa y qué control tienes sobre ella.

**Responsable del tratamiento:** Emiliano Ocampo Cervantes
**Contacto:** hola@pohua.app
**País de residencia:** México

---

## 1. Resumen rápido

- Pohua funciona **100% en tu dispositivo**. No enviamos tus datos a ningún servidor.
- **No compartimos información con terceros**. No tenemos acceso remoto a tus datos.
- **No usamos publicidad, rastreo, analíticas ni reportes de errores externos.**
- Si desinstalas la app, **todos tus datos desaparecen con ella**.

---

## 2. Información que Pohua procesa

Pohua usa el permiso del sistema **"Acceso a notificaciones"** (`BIND_NOTIFICATION_LISTENER_SERVICE`) para leer el contenido de las notificaciones que llegan a tu celular, únicamente de las aplicaciones bancarias o de fintech que tú decides activar dentro de Pohua. Por ejemplo: Nu México, Revolut, Global66, Naranja X y similares. También procesa notificaciones de Gmail cuando estas contienen correos de tarjetas de crédito (por ejemplo, Naranja X Crédito).

A partir del texto de esas notificaciones, Pohua extrae automáticamente:

- Fecha y hora de la transacción
- Monto y moneda
- Tipo de movimiento (gasto, ingreso, transferencia)
- Cuenta de origen
- Contraparte (nombre del comercio o persona, cuando aparece en la notificación)
- Texto original de la notificación (para auditoría dentro de la app)

**Pohua no accede a tus correos directamente, ni a la API de Gmail, ni a tu cuenta del banco.** Solo lee notificaciones que ya están presentes en tu dispositivo.

---

## 3. Dónde se almacena la información

Toda la información procesada por Pohua se guarda **localmente en tu dispositivo**, en una base de datos privada de la aplicación (Room/SQLite dentro del almacenamiento interno protegido por Android, accesible solo por Pohua).

- **No** subimos tus datos a la nube.
- **No** los enviamos a ningún servidor propio ni de terceros.
- **No** los respaldamos automáticamente en servicios externos.

Si en una versión futura agregamos respaldo opcional en tu propio Google Drive, actualizaremos esta política y te avisaremos dentro de la app antes de habilitarlo.

---

## 4. Información que Pohua **no** procesa

Para que quede claro, Pohua **no** recolecta, procesa ni accede a:

- Tu nombre, correo electrónico ni datos de identificación personal
- Tus contactos
- Tu ubicación geográfica
- Tu cámara, micrófono o galería
- Tu historial de navegación
- Identificadores publicitarios (Advertising ID)
- Tus credenciales bancarias o contraseñas
- El contenido completo de tus correos electrónicos

---

## 5. Servicios de terceros

**Pohua no integra ningún servicio de terceros que recolecte datos.** En particular, no utilizamos:

- Firebase Analytics ni Google Analytics
- Firebase Crashlytics ni otros servicios de reporte de fallos
- Mixpanel, Amplitude, Sentry o herramientas similares
- SDK publicitarios (AdMob, Facebook Audience Network, etc.)
- SDK de redes sociales (Facebook, Twitter, etc.)

---

## 6. Pagos dentro de la app

Cuando se habiliten las versiones de pago (Base, Plus y Pro), los pagos se procesarán **exclusivamente a través de Google Play Billing**. Google maneja toda la información de pago (tarjetas, comprobantes, datos fiscales). Pohua **no ve, no almacena ni tiene acceso a los datos de tu tarjeta** ni a ningún otro método de pago.

Para más información sobre cómo Google maneja esos datos, consulta la [Política de Privacidad de Google](https://policies.google.com/privacy).

---

## 7. Telemetría

La versión actual de Pohua **no envía telemetría de ningún tipo**.

En el futuro podríamos agregar telemetría **opcional y anónima** (por ejemplo: errores de parsing o fallos del sistema), que estará apagada por defecto y solo se activará si tú decides hacerlo desde la pantalla de Configuración. Si esta función se implementa, esta política se actualizará con todos los detalles antes de habilitarla.

---

## 8. Tus derechos sobre los datos

Como toda la información vive en tu dispositivo, tienes control total:

- **Acceso:** abre Pohua y verás todos tus datos.
- **Modificación:** puedes editar transacciones desde la app.
- **Eliminación parcial:** puedes borrar transacciones individuales desde la app.
- **Eliminación total:** desinstalar Pohua elimina por completo la base de datos del dispositivo.

Si tienes dudas sobre cómo ejercer estos derechos, escríbenos a **hola@pohua.app**.

---

## 9. Edad mínima de uso

Pohua está diseñado para personas **mayores de 18 años**. La aplicación procesa información financiera personal y está pensada para usuarios con cuentas bancarias o de fintech propias. **No está dirigida a menores de edad** y no recolectamos información de menores de manera intencional.

Si eres menor de 18 años, por favor no uses Pohua.

---

## 10. Seguridad

Pohua aprovecha las medidas de seguridad nativas de Android:

- La base de datos se encuentra dentro del almacenamiento interno privado de la aplicación, inaccesible para otras apps.
- El acceso al sistema de notificaciones requiere tu autorización explícita.
- Los datos no salen de tu dispositivo, por lo que el principal riesgo es el acceso físico al celular. Te recomendamos usar bloqueo de pantalla (PIN, huella o reconocimiento facial).

---

## 11. Cambios a esta política

Podemos actualizar esta política con el tiempo, especialmente cuando agreguemos nuevas funcionalidades (por ejemplo, respaldo en Drive o telemetría opcional). Cuando haya cambios significativos:

- Actualizaremos la fecha de "Última actualización" al inicio de este documento.
- Para cambios que afecten cómo manejamos tus datos, te avisaremos también dentro de la app.

Te recomendamos revisar esta política de vez en cuando.

---

## 12. Contacto

Si tienes dudas, comentarios o quieres ejercer algún derecho sobre tus datos, contáctanos:

**Email:** hola@pohua.app
**Repositorio del proyecto:** [github.com/emilianooce-max/Pohua](https://github.com/emilianooce-max/Pohua)

---

*Esta política aplica a la aplicación Pohua publicada en Google Play. Para otras versiones o distribuciones, podría aplicar una política diferente.*
