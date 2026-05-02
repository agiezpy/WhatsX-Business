# Política de privacidad — **WhatsX Business**

**Última actualización:** 1 de mayo de 2026

**Responsable del tratamiento:** Datia Tech  
**Contacto (consultas de privacidad):** hola@datia.dev 

---

## 1. Qué es WhatsX Business

**WhatsX Business** es una extensión de navegador (Manifest V3) para [Google Chrome](https://www.google.com/chrome/) y navegadores compatibles. Añade un **panel lateral** con funciones de organización de clientes, notas, pedidos, compras y recordatorios mientras usas [WhatsApp Web](https://web.whatsapp.com/).

**WhatsX Business no está afiliada a Meta, WhatsApp ni a otras marcas de terceros.** El uso de WhatsApp Web queda sujeto a las condiciones y la privacidad de **Meta** y de dicho servicio, independientemente de esta extensión.

---

## 2. Datos que se tratan y finalidad

La extensión trata únicamente datos **necesarios para su funcionamiento** en tu dispositivo, con el fin de ofrecerte el CRM en el panel lateral y las funciones descritas en la tienda de extensiones.

Pueden incluirse, según el uso que hagas de la app:

| Tipo de información | Origen y uso |
|---------------------|--------------|
| **Identificadores de contacto** | Números de teléfono normalizados (y nombres asociados) que se detectan desde la pestaña de WhatsApp Web o que introduc/tú; sirven para vincular la ficha del cliente con el chat. |
| **Datos de perfil comercial** | Nombre del cliente, etiquetas (p. ej. lead, cliente, VIP), notas que escribas, registro de compras e importes, pedidos, fechas, formas de pago, estados, etc. |
| **Recordatorios** | Fecha, hora, mensaje y vínculo con un cliente, para mostrarte avisos y el listado de seguimientos. |
| **Métricas de uso (opcional)** | Si activás la analítica en la página de opciones de la extensión: eventos de uso del panel (p. ej. apertura del panel, interacción con secciones o funciones) y parámetros no sensibles; se envían a **Google Analytics 4** mediante el **Measurement Protocol** según la configuración que guardes. No forman parte del CRM “de negocio” (clientes, pedidos, etc.). |
| **Identificadores técnicos internos** | Id de alarmas, claves de almacenamiento local, etc., solo para el funcionamiento técnico de la extensión. |

No utilizamos los datos del CRM descritos en la tabla para publicidad dirigida ni para construir perfiles comerciales en **servidores propios** del desarrollador: **WhatsX Business no opera un backend** que reciba tus notas, fichas de clientes ni el contenido de tus conversaciones para almacenarlos o analizarlos en nuestros servidores.

De forma **opcional**, y **solo si vos lo activás** en los ajustes de la extensión (página de opciones / analítica), pueden enviarse a **Google LLC** métricas de **uso agregado** del panel mediante **Google Analytics 4** y el **Measurement Protocol**. El diseño actual de la extensión **no prevé** incluir en esos eventos el texto de los chats de WhatsApp, el contenido de las notas del CRM ni datos identificativos de clientes como parte del payload de analítica. Podés **desactivar** el envío en cualquier momento desde la misma página de opciones o borrando los datos de la extensión. El tratamiento por parte de Google se rige por la [Política de privacidad de Google](https://policies.google.com/privacy) y la documentación de [Google Analytics / Measurement Protocol](https://developers.google.com/analytics/devguides/collection/protocol/ga4).

---

## 3. Cómo y dónde se almacenan los datos

Los datos se guardan en las APIs del navegador, **en el equipo o perfil** donde tengas instalada la extensión:

- **IndexedDB (base de datos del navegador):** ficha de clientes (notas, etiquetas, compras, pedidos) y metadatos que la extensión asocia a recordatorios.  
- **Almacenamiento local de la extensión (`chrome.storage` local):** preferencias y criterios técnicos necesarios para el funcionamiento.  
- **Almacenamiento de sesión (cuando aplica):** datos temporales de la sesión (p. ej. caché de detección o de notificaciones) que no pretenden ser permanentes.  
- **Sincronización de Chrome (opcional):** si el volumen de datos lo permite, puede guardarse un **respaldo en cifrado** de la lista de clientes en el espacio de **sincronización de la cuenta de Google** del navegador, a través de la API `chrome.storage.sync`, según explica Google. Si no hay cupo, sincronización o red, el uso local sigue; el respaldo amplio no se aplica.  

El tratamiento vinculado a **cuenta de Google** (sync, inicio de sesión en Chrome) rige la [Política de privacidad de Google](https://policies.google.com/privacy) y la configuración de sync en tu navegador.

**No hay un servicio propio del desarrollador** al que la extensión envíe el contenido de tu CRM para almacenarlo o analizarlo en nuestros servidores. Aparte de la carga normal de **WhatsApp Web** y de los sitios que abras voluntariamente en el navegador, la extensión puede realizar solicitudes HTTPS a **`https://www.google-analytics.com/`** **únicamente** cuando **tengas activada** la analítica opcional y exista un envío de eventos configurado.

Si configurás GA4, los valores que introduzcas (p. ej. identificador de medición y secreto de API) se guardan en **`chrome.storage.local`** en tu dispositivo; solo se usan para contactar con los endpoints de Google Analytics según esa configuración.

Al abrir enlaces, el navegador puede cargar **web.whatsapp.com** según el uso (por ejemplo, al pulsar en una notificación o abrir un chat), sometido a las reglas de Meta/WhatsApp y del propio sitio.

---

## 4. Acceso a WhatsApp Web (página)

Para detectar el **chat activo** (p. ej. título o número, según la UI de WhatsApp), la extensión usa un **script de contenido** con permisos **solo** en el origen `https://web.whatsapp.com/`. Ese acceso es de **lectura** orientada a identificar el contexto de la conversación; **no** se envía el contenido de los mensajes a un servidor de **WhatsX Business** (no operamos un backend que recoja esas lecturas). Los cambios en el diseño de la web de WhatsApp pueden afectar a la detección, sin implicar transmisión de esos datos a terceros por la extensión bajo el diseño actual.

---

## 5. Permisos del navegador (resumen)

La extensión solicita permisos de Chrome para: **panel lateral** (`sidePanel`), **almacenamiento** (`storage`), **alarmas** (`alarms`), **notificaciones** (`notifications`), **pestañas** (`tabs`), **`scripting`** (inyectar o comprobar el content script en WhatsApp Web), **`windows`**, **`clipboardWrite`** (copiar al portapapeles texto que elijas —por ejemplo plantillas— para pegarlo de forma fiable en el cuadro de mensaje de WhatsApp Web) y **permisos de host** hacia **`https://web.whatsapp.com/*`** y, solo para la analítica opcional, hacia **`https://www.google-analytics.com/*`**.

Cada permiso se usa con **finalidades operativas** descritas en esta política. La lista exacta vigente aparece en el `manifest.json` publicado y en la ficha de la extensión en el momento de la instalación.

---

## 6. Conservación y supresión

- Los datos permanecen mientras **no** borres el perfil de extensión, desinstales la extensión o **limpiés el almacenamiento** de la extensión desde Ajustes de Chrome (`chrome://extensions` → detalles de la extensión).  
- Desinstalar la extensión o borrar sus datos en el navegador **elimina** la información almacenada en ese perfil, salvo copias en **sincronización de Google** si la tenías activa; en ese caso puedes gestionar sync desde tu cuenta o desactivarla, según Google.  

No conservamos en servidores nuestre una “copia” de tus datos, porque el modelo actual no preve ese backend.

---

## 7. Seguridad

Aplicamos las buenas prácticas habituales de desarrollo (datos en APIs del propio entorno de extensiones, sin exfiltración a servidores propios en el diseño descrito). **Ningún canal es 100% seguro**; protege además el acceso a tu equipo y a tu sesión de WhatsApp Web (contraseñas, bloqueo de sesión, etc.).

---

## 8. Menores

WhatsX Business no está pensada para menores. Si no tienes edad mínima para usar el navegador o WhatsApp de forma válida, no deberías usar la extensión. Los padres o tutores son quienes deben supervisar el uso.

---

## 9. Derechos y consultas

Según el lugar de residencia, podrás ejercer derechos de acceso, rectificación, oposición o supresión respecto de los datos bajo control del **responsable** (el desarrollador) cuando la ley lo permita, y respecto de datos que tengas **introducidos en la app**, principalmente accediendo o borrando datos desde el propio panel y la configuración de la extensión o del perfil. Para dudas sobre el tratamento descrito en **esta** política, contacta en: **hola@datia.dev**.

**Transferencias internacionales:** un eventual respaldo cifrado vía **Chrome Sync** puede implicar servidores de Google fuera de tu país; aplica la política de Google.

---

## 10. Cambios

Podemos actualizar esta política. La **“Última actualización”** en la cabecera indicará la versión reciente. Los cambios sustantivos conviene revisarlos en esta misma URL que publiques (por ejemplo, en el repositorio, sitio web o hosting estático vinculado a la ficha de la tienda de extensiones).

La versión de **1 de mayo de 2026** incorpora la descripción de la **analítica opcional (Google Analytics 4)**, del permiso **`clipboardWrite`** y del acceso de red a **Google Analytics**, alineada con el comportamiento publicado de la extensión.

---

## 11. Contacto

**Datia Tech**  
**Email:** hola@datia.dev 
