# Política de Privacidad de Pohua

**Última actualización:** 7 de julio de 2026

Pohua (“nosotros” o “la app”) es una aplicación de Android para llevar el control de gastos e ingresos personales, leyendo las notificaciones que las apps de bancos envían a tu celular. Esta política explica qué información procesa la app, cómo se procesa y qué control tienes sobre ella.

**Responsable del tratamiento:** Emiliano Ocampo Cervantes **Contacto:** hola@pohua.app **País de residencia:** México

---

## 1. Resumen rápido

- Para usar Pohua **inicias sesión con tu cuenta de Google**. Guardamos tu nombre, correo y foto de perfil **en tu dispositivo** para identificar tu cuenta (ver la sección "Cuenta e inicio de sesión").
- Pohua funciona **en tu dispositivo**. De forma predeterminada, no enviamos tu información financiera fuera de tu celular.
- Puedes activar un **respaldo opcional** de tus datos en **tu propio Google Drive**. Esa copia es **tuya y queda bajo tu control**: nosotros **nunca la vemos ni la recibimos** y **no pasa por ningún servidor de Pohua** (ver sección 3).
- Incluye una telemetría **opcional y anónima**, **apagada por defecto**, que solo se activa si tú la enciendes y que nunca envía datos personales ni financieros (ver sección 7).
- **No usamos publicidad ni rastreo**, ni analíticas o reportes de errores de terceros (Firebase, Sentry, etc.).
- **No compartimos tu información con terceros.**
- Si desinstalas la app, **todos tus datos del dispositivo desaparecen con ella** (si activaste el respaldo, la copia en tu Google Drive se conserva hasta que tú la borres; ver sección 8).

---

## 2. Información que Pohua procesa

Pohua usa el permiso del sistema **"Acceso a notificaciones"** (`BIND_NOTIFICATION_LISTENER_SERVICE`) para detectar automáticamente tus transacciones a partir de las notificaciones que llegan a tu celular.

Para reconocer transacciones de cualquier banco o aplicación financiera —incluso de formatos que aún no conoce— Pohua analiza el contenido de las notificaciones directamente en tu dispositivo. Las notificaciones que claramente no son financieras (mensajería, redes sociales, noticias, navegación, etc.) se descartan de inmediato, sin guardarse. Solo se conservan en el dispositivo las que parecen una transacción, para mostrártelas y que tú las confirmes o edites.

Todo este análisis ocurre dentro de tu celular y el contenido de tus notificaciones no se envía a ningún servidor nuestro. Solo sale de tu dispositivo en dos casos que tú controlas: la telemetría opcional de la Sección 7 (si la activas), que envía plantillas anónimas sin datos reales; y el respaldo opcional de la Sección 3 (si lo activas), que guarda una copia en **tu propio** Google Drive, sin pasar por nosotros.

De las notificaciones que son transacciones, Pohua extrae automáticamente:

- Fecha y hora
- Monto y moneda
- Tipo de movimiento (gasto, ingreso, transferencia)
- Cuenta de origen
- Contraparte (comercio o persona, cuando aparece)
- Texto original de la notificación (para auditoría dentro de la app)

Pohua también procesa notificaciones de Gmail cuando contienen correos de tarjetas de crédito (por ejemplo, Naranja X Crédito). Pohua no accede a tus correos directamente, ni a la API de Gmail, ni a tu cuenta del banco. Solo lee notificaciones que ya están en tu dispositivo.

---

## 3. Dónde se almacena la información

Toda la información procesada por Pohua se guarda **localmente en tu dispositivo**, en una base de datos privada de la aplicación (Room/SQLite dentro del almacenamiento interno protegido por Android, accesible solo por Pohua).

- **No** enviamos tus datos a servidores de Pohua. Por defecto, nada de tu información sale del dispositivo.
- La única información que enviamos a un servidor nuestro es la telemetría **opcional** descrita en la sección 7, que está **apagada por defecto** y que nunca incluye tus datos financieros ni el contenido de tus notificaciones.

### Respaldo opcional en tu propio Google Drive

Puedes activar un **respaldo opcional** de tus datos. Cuando lo activas, Pohua guarda una copia de tu base de datos en **tu propia cuenta de Google Drive**, en una carpeta privada de datos de la aplicación (*appDataFolder*). Puntos clave:

- **Es tu Drive, bajo tu control.** La copia se sube directamente desde tu dispositivo a tu cuenta de Google. **Nosotros nunca vemos, recibimos ni almacenamos esa copia**, y **no pasa por ningún servidor de Pohua**. A diferencia de la telemetría, aquí no hay intermediario: es una transferencia entre tú y tu propio Google Drive.
- **Es opcional y la activas tú.** Está apagado mientras no lo enciendas en Ajustes → Copia de seguridad. Una vez activado, la copia puede actualizarse automáticamente (por ejemplo, una vez al día por WiFi); puedes desactivarlo en cualquier momento.
- **Va a una carpeta de datos de la app.** Esa carpeta (*appDataFolder*) no aparece como archivos normales en Google Drive: no es navegable junto a tus documentos; es un espacio privado que solo gestiona la app.
- **Puedes borrar esa copia cuando quieras** (ver sección 8).

---

## 3 bis. Cuenta e inicio de sesión

Para usar Pohua inicias sesión con **tu cuenta de Google** (Sign in with Google). Al hacerlo, la app recibe de Google y **guarda en tu dispositivo**:

- Tu **nombre** y **foto de perfil** (para mostrarte con qué cuenta estás usando la app).
- Tu **correo electrónico**.
- El **identificador de tu cuenta de Google** (un ID técnico que distingue tu cuenta).

**Para qué se usa:** identificar tu cuenta dentro de la app y ligar tus datos locales a ella (por ejemplo, para avisarte si abres la app con una cuenta distinta a la que usaste antes). Esta información se guarda en el almacenamiento privado de la app en tu dispositivo; **no la publicamos, no la compartimos con terceros y no la vendemos**. **No guardamos tu contraseña de Google** (el inicio de sesión lo maneja Google). Al iniciar sesión también autorizas el acceso a la carpeta privada de la app en **tu propio** Google Drive, pero solo si activas el respaldo (sección 3).

Si más adelante habilitamos las versiones de pago, tu cuenta servirá para reconocer tu licencia; los pagos los seguirá manejando Google Play (sección 6).

---

## 4. Información que Pohua **no** procesa

Para que quede claro, Pohua **no** recolecta, procesa ni accede a:

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

La telemetría opcional (sección 7) se envía a un **servidor propio del responsable** de la app, no a un servicio de analítica de terceros.

---

## 6. Pagos dentro de la app

Cuando se habiliten las versiones de pago (Base, Plus y Pro), los pagos se procesarán **exclusivamente a través de Google Play Billing**. Google maneja toda la información de pago (tarjetas, comprobantes, datos fiscales). Pohua **no ve, no almacena ni tiene acceso a los datos de tu tarjeta** ni a ningún otro método de pago.

Para más información sobre cómo Google maneja esos datos, consulta la [Política de Privacidad de Google](https://policies.google.com/privacy).

---

## 7. Telemetría (opcional, apagada por defecto)

Pohua incluye una función de telemetría **opcional** para ayudarnos a mejorar el reconocimiento automático de notificaciones de más bancos. Está **apagada por defecto** y solo se activa si tú la enciendes manualmente desde **Configuración**.

**Mientras la telemetría esté apagada (estado por defecto), Pohua no envía nada fuera de tu dispositivo.**

Si decides activarla, Pohua envía a un servidor propio (controlado por el responsable de la app y alojado en infraestructura de Cloudflare) únicamente lo siguiente:

- **Estructuras anónimas de notificaciones:** plantillas del formato de una notificación —ya sea una que la app no logró interpretar, o una que tú confirmas como transacción— donde los valores reales (montos, nombres, números de cuenta, saldos) se reemplazan por marcadores **antes** de salir del dispositivo. Sirven para enseñarle a la app a reconocer bancos o formatos nuevos.
- **Versión de la app.**
- **Un identificador aleatorio y rotativo** (cambia aproximadamente cada 30 días) que **no está ligado a tu identidad** ni a tu cuenta; solo agrupa eventos del mismo dispositivo de forma temporal.
- **Reportes de fallos (crashes):** información técnica del error, depurada de datos personales.

**La telemetría nunca incluye:**

- El texto original ni el contenido real de tus notificaciones.
- Montos, saldos, nombres de comercios o personas, ni números de cuenta.
- Tu nombre, correo, ubicación ni ningún dato que te identifique.

Los datos viajan **cifrados** (HTTPS) y se usan exclusivamente para mejorar Pohua. **No se comparten con terceros, no se usan para publicidad y no se venden.** Para esta función la app utiliza el permiso de **Internet**, que no se usa para ningún otro fin.

Como la información es anónima y no está ligada a tu identidad, no podemos vincular los datos de telemetría a una persona para borrarlos individualmente. Puedes **detener todo envío en cualquier momento** desactivando la telemetría en Configuración.

---

## 8. Tus derechos sobre los datos

Como tu información vive en tu dispositivo (y, si activaste el respaldo, también en una copia en tu propio Google Drive), tienes control total:

- **Acceso:** abre Pohua y verás todos tus datos.
- **Eliminación parcial:** puedes borrar transacciones individuales desde la app.
- **Eliminación total en el dispositivo:** desinstalar Pohua elimina por completo la base de datos de tu teléfono.
- **Eliminación de la copia de respaldo:** si activaste el respaldo en Google Drive, esa copia **no** se borra al desinstalar la app. Para eliminarla tienes dos vías:
  - **Desde la app:** Ajustes → Copia de seguridad → **"Borrar respaldos de Drive"** elimina todas las copias guardadas.
  - **Quitando el acceso desde tu cuenta de Google:** en [myaccount.google.com](https://myaccount.google.com) → "Conexiones con terceros" (o "Apps con acceso a tu cuenta") puedes retirarle a Pohua el acceso a tu Drive y eliminar sus datos. Este permiso se retira desde Google, no desde la app.

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
- De forma predeterminada los datos no salen de tu dispositivo. Si activas la telemetría (sección 7) o el respaldo en tu Google Drive (sección 3), esa información viaja **cifrada** (HTTPS): la telemetría hacia nuestro servidor (anónima) y el respaldo hacia tu propia cuenta de Google. El principal riesgo sigue siendo el acceso físico al celular; te recomendamos usar bloqueo de pantalla (PIN, huella o reconocimiento facial).

---

## 11. Cambios a esta política

Podemos actualizar esta política con el tiempo, especialmente cuando agreguemos nuevas funcionalidades. Cuando haya cambios significativos:

- Actualizaremos la fecha de “Última actualización” al inicio de este documento.
- Para cambios que afecten cómo manejamos tus datos, te avisaremos también dentro de la app.

Te recomendamos revisar esta política de vez en cuando.

---

## 12. Contacto

Si tienes dudas, comentarios o quieres ejercer algún derecho sobre tus datos, contáctanos:

**Email:** hola@pohua.app **Repositorio del proyecto:** [github.com/emilianooce-max/Pohua](https://github.com/emilianooce-max/Pohua)

---

*Esta política aplica a la aplicación Pohua publicada en Google Play. Para otras versiones o distribuciones, podría aplicar una política diferente.*
