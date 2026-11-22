---
title: Política de privacidad de Ahorro
lang: es
---

# Política de privacidad de Savings Challenge & Budget

*Esta es una traducción. Si difiere de la [versión en inglés](../privacy), prevalece la versión en inglés.*

Fecha de entrada en vigor: 2026-11-22

Esta política explica cómo Savings Challenge & Budget (que aparece como «Ahorro» en su pantalla de inicio, la «App»), desarrollada por Stanislau Malchanau («nosotros»), trata su información. En resumen: **no recopilamos, vendemos ni compartimos sus datos personales. Su presupuesto se queda en su dispositivo y en su propia cuenta de iCloud. La App no guarda ni mueve dinero, no está conectada a ningún banco y no ofrece asesoramiento financiero.**

## 1. Datos que guarda la App

La App guarda en su dispositivo: sus gastos, ingresos y devoluciones (el importe, su moneda y el tipo de cambio usado, la categoría, una nota, la fecha, la hora y la zona horaria, y cómo se añadió el movimiento, por ejemplo con el teclado, desde un ticket o desde Apple Pay), sus categorías y sus límites, su presupuesto mensual y sus ajustes (el día en que empieza su mes, si lo que sobra pasa al mes siguiente), sus pagos recurrentes, sus objetivos de ahorro con lo que apartó y lo que sacó, sus retos de ahorro, los tipos de cambio que escribió usted mismo, el presupuesto compartido que lleva con una persona a la que invita (sección 3), sus respuestas a las preguntas del primer inicio y sus ajustes (la hora del recordatorio, el bloqueo con Face ID, el sonido y la vibración). Los movimientos eliminados se conservan 30 días en «Eliminados recientemente» para que pueda recuperarlos.

Estos registros describen cómo gasta y ahorra, y algunas leyes consideran esta información financiera o sensible. Nunca salen de su dispositivo ni de su cuenta de iCloud (secciones 2 y 3). No tenemos servidores que reciban sus registros, no tenemos acceso a ellos y la App nunca envía sus movimientos a un servicio de IA en línea ni a nadie más. El único servidor pequeño que sí tenemos (sección 6) responde con tipos de cambio y firma ofertas de descuento; nunca recibe sus registros.

## 2. Sincronización con iCloud

Si ha iniciado sesión en iCloud, la App sincroniza su presupuesto mediante CloudKit de Apple, en la base de datos privada de su propia cuenta de iCloud, para que esté ahí en un iPhone nuevo y después de reinstalar. Apple almacena y protege estos datos conforme a su Política de privacidad (https://www.apple.com/legal/privacy/). No podemos verlos, leerlos ni exportarlos. Cuando algo cambia en iCloud, el servicio push de Apple puede activar la App para que descargue el cambio; esa notificación no lleva ninguno de sus registros. Puede desactivar la sincronización en Ajustes de iOS > [su nombre] > iCloud; entonces su presupuesto se queda solo en este iPhone.

## 3. El presupuesto compartido

Puede invitar a una persona a un presupuesto que llevan juntos. La invitación es un enlace de iCloud que usted mismo envía, y Apple guarda el presupuesto compartido en una zona compartida de CloudKit que solo ustedes dos pueden abrir. Lo que cualquiera de los dos añada a él lo ve la otra persona, y cada movimiento muestra quién lo añadió; su propio presupuesto nunca se comparte. Si escribe un nombre para el presupuesto compartido, la otra persona lo ve junto a sus movimientos; se guarda con su presupuesto en su cuenta de iCloud y en la zona compartida. La App le indica a la persona invitada si su suscripción está activa, para que pueda añadir movimientos gratis al presupuesto compartido (sección 2 de los Términos de uso). Cualquiera de los dos puede salir del presupuesto compartido o cerrarlo en la App en cualquier momento. Si deja de compartirlo, la otra persona puede conservar una copia de solo lectura de lo que había en el presupuesto compartido hasta entonces. Cuando Apple avisa a la App de que la otra persona añadió algo, la notificación pasa por el servicio push de Apple.

## 4. El escáner de tickets y la cámara

La App usa la cámara solo cuando abre el escáner de tickets, y iOS le pide permiso la primera vez. La foto del ticket se lee en su iPhone: el framework Vision de Apple encuentra su texto y cualquier código QR y, en los iPhone con Apple Intelligence, el modelo de lenguaje de Apple que funciona en el propio dispositivo ayuda a encontrar el total, la moneda y el nombre de la tienda. La foto y el texto reconocido permanecen solo en la memoria del teléfono mientras se leen y se eliminan justo después. Nunca se guardan, nunca se suben y nunca se envían a nosotros ni a ningún servicio en línea. Solo se almacena el gasto que usted guarda después (su importe, moneda, fecha y el nombre de la tienda en la nota), como cualquier otro movimiento.

## 5. Apple Pay mediante Atajos

La App no lee su Cartera (Wallet), sus tarjetas ni su banco. Si decide configurar una automatización personal en la app Atajos de Apple con su activador «Transacción», cada vez que pague con Apple Pay en una tienda, Atajos pasa el importe y el nombre del comercio a la acción de la App para añadir un gasto, en el mismo iPhone, y la App registra un gasto con ellos. Nada de esto se nos envía; el movimiento se guarda y se sincroniza como cualquier otro (secciones 1 y 2). No ocurre nada a menos que usted mismo configure la automatización, y puede cambiarla o eliminarla en Atajos en cualquier momento.

## 6. Tipos de cambio y ofertas de descuento (nuestro servidor)

Tenemos un servidor pequeño, en Cloudflare Workers, para dos tareas. Ninguna de ellas recibe sus registros.

- **Tipos de cambio.** Cuando un gasto está en una moneda distinta de su moneda principal, o cuando cambia su moneda principal, la App pide al servidor los tipos de cambio de ese día. La solicitud lleva solo la fecha: ningún importe, ninguna moneda y nada sobre usted. El servidor toma los tipos de referencia del día del Banco Central Europeo y, para las monedas que ese banco no publica, tipos de bancos centrales reunidos por el servicio abierto Frankfurter, y devuelve la tabla completa de ese día; su iPhone elige el tipo que necesita. Los gastos en su moneda principal nunca necesitan el servidor.
- **Ofertas de descuento.** Si desactiva la renovación, la App puede ofrecerle un precio más bajo para su siguiente periodo (sección 2 de los Términos de uso). Apple exige que firmemos esa oferta, así que justo antes de la compra la App envía al servidor solo el identificador de la propia App, los identificadores del plan y de la oferta y, cuando Apple lo pide, el número que el App Store asigna a la compra de su suscripción actual. El servidor añade un número aleatorio de un solo uso, los firma, responde y no guarda nada. No sabe nada de quién es usted: ni su nombre, ni su cuenta de Apple, ni ninguno de sus registros.

Como cualquier servidor, el nuestro ve la dirección IP de una solicitud para poder responderla. No guarda esa dirección en nada de lo que conserva y no vincula las solicitudes con ninguna persona. Cloudflare, que opera el servidor, puede conservar durante poco tiempo registros técnicos de las solicitudes por motivos de seguridad y fiabilidad, conforme a su propia política de privacidad (https://www.cloudflare.com/privacypolicy/).

## 7. Notificaciones y widgets

El recordatorio de la noche se programa en su iPhone, y solo si permite las notificaciones. No se nos envía ningún dato para entregarlo. Los widgets leen su presupuesto en su dispositivo.

## 8. Bloqueo con Face ID

Si activa el bloqueo, la App pide a iOS que compruebe su Face ID o su código. iOS gestiona Face ID por completo: la App nunca ve los datos de su cara y solo sabe si la comprobación se superó.

## 9. Compras

Apple vende y procesa las suscripciones a través del App Store. No recibimos sus datos de pago. Apple indica a la App si su suscripción está activa, qué plan eligió y con qué precio, si la renovación está activada y si hay una oferta disponible para su cuenta de Apple; la sección 10 explica qué parte de ello va a nuestras estadísticas de uso.

## 10. Estadísticas de uso e informes de fallos

Para saber qué funciones ayudan y dónde estorba la App, la App envía señales de uso anónimas a TelemetryDeck, un servicio de análisis de TelemetryDeck GmbH (Augsburgo, Alemania) con servidores en la UE. Su código es el único código de la App que no procede de Apple ni de nosotros. Una señal nombra una acción en la App: por ejemplo, que se completó un paso del primer inicio y cuál de sus respuestas de opción múltiple se eligió (qué le impidió antes llevar un presupuesto, si fijó un presupuesto mensual, el día en que empieza su mes, el tipo de su primer objetivo de la lista y en cuántos meses), cuánto tardó el primer gasto, que se añadió un gasto o un ingreso y cómo (con el teclado, desde un widget, un ticket, Apple Pay o un archivo) y si estaba en su moneda principal, que se creó un objetivo (su tipo de la lista y si tiene fecha), que se apartó dinero, se empezó un reto o se marcó una casilla, que se abrió un panel o se importó un archivo (con un recuento aproximado de sus líneas), que se mostró la pantalla de suscripción o una oferta, se eligió un plan, o que una suscripción comenzó, se renovó o se restauró, que la App pidió una valoración o, como un código de error breve, que algo no funcionó, por ejemplo que el App Store no respondió. Va acompañada de una marca de tiempo redondeada a la hora y de datos técnicos generales: las versiones de la App y de iOS, el modelo del dispositivo, el idioma, la región y la zona horaria, y ajustes de pantalla y accesibilidad como el modo oscuro o el tamaño del texto. Cuando una suscripción comienza o se renueva, su señal incluye además el plan, su precio convertido a dólares estadounidenses, la moneda y el país de su App Store, para que podamos ver qué planes eligen las personas.

Una señal nunca contiene sus importes, saldos ni cifras del presupuesto, sus categorías, notas ni nombres de objetivos, nombres de tiendas o comercios, fotos de tickets ni su texto, los tipos de cambio que escribió, su nombre, su correo electrónico, su cuenta de Apple ni su ubicación, ni nada sobre la persona con la que comparte un presupuesto. Su instalación solo se identifica mediante un identificador aleatorio que la App sala y convierte en hash antes de enviarlo, de modo que las señales no pueden vincularse a usted ni seguirle entre apps. TelemetryDeck no guarda direcciones IP ni usa cookies. Solo miramos estas señales como estadísticas para mejorar la App; no las vendemos, no las compartimos con anunciantes ni las usamos para rastrearle. La App no contiene código de publicidad ni de rastreo y no le rastrea en otras apps ni sitios web.

Por otra parte, si decide compartir análisis con los desarrolladores de apps en Ajustes de iOS > Privacidad y seguridad > Análisis y mejoras, Apple puede facilitarnos estadísticas de uso e informes de fallos agregados y anónimos. No le identifican.

## 11. Game Center

Si ha iniciado sesión en Game Center, los logros por sus hitos de ahorro se comunican a Game Center de Apple con su cuenta de Game Center y se tratan conforme a la Política de privacidad de Apple. Un logro solo dice que se alcanzó un hito; sus movimientos, notas y nombres de objetivos no se envían. No recibimos su identidad de Game Center.

## 12. Importación y exportación

La exportación de sus gastos e ingresos como archivo CSV y la importación de un archivo CSV de otra app de presupuesto se hacen en su dispositivo. La App lee solo el archivo que usted elige, y un archivo exportado va solo a donde usted lo envíe con el menú de compartir.

## 13. Lo que la App no hace

La App no guarda, mueve, invierte ni presta dinero. No está conectada a ningún banco, tarjeta ni cuenta de pago, y no ofrece asesoramiento financiero, fiscal ni de inversión. No accede a su Cartera, su ubicación, sus contactos, su fototeca ni su micrófono, y no tiene cuenta, inicio de sesión, publicidad, chat ni muro público.

## 14. Menores

La App es apta para todas las edades (clasificación 4+) y no recopila a sabiendas información personal de nadie, incluidos los menores de 13 años (o la edad equivalente en su país).

## 15. Conservación y eliminación de datos

Los datos se conservan mientras usted los guarde. Puede eliminar un movimiento en la App en cualquier momento; espera 30 días en «Eliminados recientemente» y después desaparece. Puede eliminarlo todo borrando la App y, para los datos sincronizados, en Ajustes de iOS > [su nombre] > iCloud > Gestionar almacenamiento de la cuenta > Ahorro. Lo que añadió a un presupuesto compartido se queda ahí para la otra persona hasta que uno de los dos lo elimine o se cierre el presupuesto compartido. Como no guardamos ninguna copia, no hay nada más que eliminar por nuestra parte. Las señales de uso son anónimas y no pueden asociarse a usted, y nuestro servidor no guarda nada sobre usted, así que en ninguno de los dos casos existe un registro personal que consultar o eliminar.

## 16. Sus derechos

Según dónde viva (por ejemplo, en virtud del RGPD en la UE, el UK GDPR, la CCPA/CPRA en California, la APPI en Japón, la PIPA en Corea o la LGPD en Brasil), puede tener derecho a acceder a sus datos personales, rectificarlos, eliminarlos o portarlos, y a oponerse a su tratamiento o limitarlo. Como no guardamos sus datos, puede ejercer estos derechos directamente en su dispositivo y en iCloud como se describe arriba; la exportación CSV en Ajustes le da todos sus gastos e ingresos en un solo archivo. También puede contactarnos con cualquier solicitud o pregunta, y puede presentar una reclamación ante su autoridad local de protección de datos.

No vendemos ni compartimos información personal según la definición de la CCPA/CPRA.

## 17. Cambios

Si esta política cambia, actualizaremos la fecha de arriba y, en caso de cambios importantes, se lo indicaremos en la App.

## 18. Contacto

Stanislau Malchanau, Bielorrusia
Correo electrónico: 7tam.official@gmail.com
