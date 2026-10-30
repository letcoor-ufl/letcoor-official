# LETCOOR 1.0.0 — Documentación completa del usuario

> Documentación elaborada a partir del código fuente real de **LETCOOR 1.0.0** proporcionado el 30 de octubre de 2026.
> Esta documentación describe las funciones realmente expuestas por la aplicación Android/Windows y la interfaz actual.

---

## Índice

1. [Primeros pasos: conectar los dispositivos](#1-primeros-pasos-conectar-los-dispositivos)
2. [Permisos importantes, especialmente sin conexión](#2-permisos-importantes-especialmente-sin-conexión)
3. [Crear o unirse a un grupo](#3-crear-o-unirse-a-un-grupo)
4. [Comprender la pantalla principal](#4-comprender-la-pantalla-principal)
5. [El mapa táctico](#5-el-mapa-táctico)
6. [Crear un aviso](#6-crear-un-aviso)
7. [Crear un objetivo](#7-crear-un-objetivo)
8. [Crear una orden](#8-crear-una-orden)
9. [Crear un punto de reunión](#9-crear-un-punto-de-reunión)
10. [Enviar una alerta de seguridad](#10-enviar-una-alerta-de-seguridad)
11. [Interactuar con un objeto ya publicado](#11-interactuar-con-un-objeto-ya-publicado)
12. [El panel «Mando y actividad»](#12-el-panel-mando-y-actividad)
13. [El menú del grupo o del equipo](#13-el-menú-del-grupo-o-del-equipo)
14. [Equipos](#14-equipos)
15. [Participantes y roles](#15-participantes-y-roles)
16. [Invitar a un nuevo participante](#16-invitar-a-un-nuevo-participante)
17. [Operaciones](#17-operaciones)
18. [Campañas de roles](#18-campañas-de-roles)
19. [Sesiones](#19-sesiones)
20. [Intercambio de datos entre equipos](#20-intercambio-de-datos-entre-equipos)
21. [Gestión del grupo y de los equipos](#21-gestión-del-grupo-y-de-los-equipos)
22. [Límites de publicación](#22-límites-de-publicación)
23. [Ubicación](#23-ubicación)
24. [Notificaciones](#24-notificaciones)
25. [Mapas sin conexión](#25-mapas-sin-conexión)
26. [Conexión de red y funcionamiento sin conexión](#26-conexión-de-red-y-funcionamiento-sin-conexión)
27. [Privacidad, bloqueo y recuperación](#27-privacidad-bloqueo-y-recuperación)
28. [Roles disponibles](#28-roles-disponibles)
29. [Consejos de preparación antes de una actividad](#29-consejos-de-preparación-antes-de-una-actividad)
30. [Solución de problemas](#30-solución-de-problemas)
31. [Resumen rápido](#31-resumen-rápido)

---

# 1. Primeros pasos: conectar los dispositivos

LETCOOR utiliza un sistema de invitaciones entre dispositivos. Una invitación puede transmitirse mediante **código QR**, **enlace**, el sistema de compartir o un archivo, según la plataforma.

Para maximizar las posibilidades de conexión, especialmente **sin Internet**, prepare ambos dispositivos antes del intercambio.

## 1.1 Antes de escanear el código QR o abrir el enlace

En ambos dispositivos:

1. Abra LETCOOR y mantenga la aplicación en primer plano durante la primera conexión.
2. Active el **Wi‑Fi**.
3. Active el **Bluetooth**.
4. Acepte las solicitudes de Android/Windows relativas a **dispositivos cercanos**, Bluetooth, Wi‑Fi Direct o la red local.
5. Si Android propone hacer visible el teléfono por Bluetooth, acepte durante la fase de conexión.
6. Si Android solicita activar el servicio de ubicación para permitir la detección por radio, se recomienda activarlo para garantizar la compatibilidad con las API de proximidad del teléfono.
7. La **cámara** solo es necesaria para escanear un código QR. No es necesaria si utiliza un enlace.

> **Importante:** autorizar o activar el servicio de ubicación de Android para el descubrimiento de proximidad no activa automáticamente el uso compartido de su posición en LETCOOR. Compartir la ubicación es una función independiente y permanece desactivada hasta que usted mismo la active.

## 1.2 Conexión mediante código QR

### En el dispositivo que invita

1. Abra el menú del grupo o del equipo tocando su nombre en la parte superior izquierda.
2. Abra la pestaña **Invitar**.
3. Si hay varios destinos disponibles, elija el **grupo** o el **equipo** al que se va a unir.
4. Abra **Compartir invitación**.
5. Seleccione **Mostrar código QR**.
6. Mantenga el QR visible en la pantalla.

Un código QR puede estar compuesto por varias partes. LETCOOR las va mostrando automáticamente. Es posible pausar el avance o pasar manualmente a la parte anterior/siguiente.

### En el dispositivo invitado

1. En la pantalla de inicio, elija **Unirse con una invitación**.
2. Pulse el botón para escanear el QR.
3. Autorice la cámara si Android/Windows lo solicita.
4. Apunte al QR del otro dispositivo.
5. Si el QR contiene varias partes, mantenga la cámara orientada hacia la pantalla hasta que LETCOOR haya leído todas las partes.
6. LETCOOR importa la invitación y prepara una **respuesta**.
7. El dispositivo invitado muestra entonces un **enlace de respuesta** o un **QR de respuesta** que debe enviarse de vuelta al dispositivo que invita.

### Devolver la respuesta al dispositivo que invita

En el dispositivo que creó la invitación:

1. Permanezca en **Invitar**.
2. Abra **Recibir la respuesta**.
3. Escanee el QR de respuesta, pegue el enlace de respuesta o utilice el mecanismo de compartir disponible.
4. LETCOOR verifica la respuesta y, a continuación, inicia la conexión directa.

La aplicación muestra después el estado del intento: preparación de proximidad, conexión a Internet, búsqueda local, conexión establecida o tiempo de espera agotado.

## 1.3 Conexión mediante enlace

El procedimiento es idéntico, pero sin cámara.

### Dispositivo que invita

En **Invitar > Compartir invitación**:

1. Elija **Enlace de invitación**.
2. Pulse **Copiar enlace** o el botón de compartir.
3. Envíe el enlace al otro participante.

### Dispositivo invitado

1. Abra **Unirse con una invitación**.
2. Pegue el enlace en **Invitación que aceptar**, o utilice el botón del portapapeles.
3. LETCOOR procesa automáticamente un enlace válido.
4. A continuación, devuelva el **enlace de respuesta** al dispositivo que le invita.

### Dispositivo que invita

En **Recibir la respuesta**:

1. Pegue el enlace de respuesta o escanee el QR de respuesta.
2. LETCOOR verifica la respuesta.
3. La conexión se inicia automáticamente.

## 1.4 ¿Por qué hay que devolver una respuesta?

El flujo bidireccional permite que ambos dispositivos conozcan la información necesaria para intentar la conexión. LETCOOR puede entonces probar las rutas disponibles y autenticar al par antes de admitirlo en el grupo o el equipo.

## 1.5 Admisión al grupo y al equipo

Una invitación válida está firmada y apunta a un destino determinado en el momento de su creación.

- Una invitación de grupo permite unirse al grupo correspondiente.
- Una invitación procedente de un equipo puede incluir el acceso al **grupo principal y al equipo de quien invita**.
- Las claves privadas del grupo o el historial completo no se incluyen en el código QR.
- La admisión es validada por el protocolo LETCOOR después de la autenticación; no existe una validación manual adicional para una invitación válida, salvo que la política de admisión o los permisos del espacio lo impidan.

---

# 2. Permisos importantes, especialmente sin conexión

LETCOOR utiliza varias funciones del sistema. Para un uso sin Internet, los permisos de proximidad son especialmente importantes.

## 2.1 Bluetooth y Wi‑Fi Direct

En **Ajustes > Permisos**, LETCOOR ofrece:

- **Bluetooth y Wi‑Fi Direct — Permitir**
- **Cámara — Permitir**
- **Ubicación — Comprobar**

En versiones recientes de Android, LETCOOR puede solicitar, entre otros, permisos del sistema relacionados con:

- dispositivos cercanos;
- escaneo Bluetooth;
- conexión Bluetooth;
- anuncio Bluetooth;
- Wi‑Fi Direct / dispositivos Wi‑Fi cercanos;
- acceso a la red local en las versiones de Android que lo exigen.

En algunas versiones antiguas de Android, el descubrimiento Bluetooth/Wi‑Fi puede depender del permiso de ubicación de Android.

## 2.2 Ubicación: dos cosas diferentes

Hay que distinguir entre:

1. **La ubicación del sistema Android utilizada por algunas API de descubrimiento de proximidad.**
2. **El uso compartido voluntario de su posición en LETCOOR.**

Puede utilizar LETCOOR sin publicar su posición en el mapa. El uso compartido de la ubicación se configura por separado desde el icono **Ubicación**.

## 2.3 Cámara

La cámara solo se utiliza para escanear códigos QR. El escaneo no requiere el micrófono.

Si se deniega el acceso a la cámara:

- utilice el enlace de invitación;
- o vuelva a autorizar la cámara en los ajustes de Android/Windows.

## 2.4 Notificaciones del sistema

Las notificaciones del sistema pueden activarse desde el centro de notificaciones de LETCOOR. Permiten recibir alertas nativas para determinados eventos cuando la plataforma lo permite.

---

# 3. Crear o unirse a un grupo

En el primer inicio, si el dispositivo todavía no pertenece a ningún grupo, LETCOOR muestra la pantalla de bienvenida.

Dispone de dos opciones:

- **Crear un grupo**
- **Unirse con una invitación**

## 3.1 Crear un grupo

1. Pulse **Crear un grupo**.
2. Introduzca el **Nombre del grupo**.
3. El nombre debe contener al menos 2 caracteres.
4. Pulse **Crear**.

El creador obtiene el rol de administración del grupo y puede después crear equipos, invitar participantes y gestionar el espacio según las capacidades otorgadas por el Core.

## 3.2 Unirse a un grupo

1. Pulse **Unirse con una invitación**.
2. Importe el enlace o el QR.
3. Siga el intercambio invitación/respuesta descrito al principio de esta documentación.

## 3.3 N.º personal

Cada dispositivo dispone de un **N.º personal** que se muestra durante la incorporación inicial y en la pestaña **Contexto**.

Este número sirve como identificador legible por el usuario en la interfaz. La identidad criptográfica real se basa en la identidad del dispositivo LETCOOR, no en este código mostrado.

---

# 4. Comprender la pantalla principal

LETCOOR utiliza una interfaz **centrada en el mapa** en lugar de una sucesión de páginas clásicas.

## 4.1 Encabezado

En la parte superior de la pantalla:

- a la izquierda: el **nombre del grupo o del equipo actualmente seleccionado**;
- el subtítulo indica **Grupo** o **Equipo**;
- puede aparecer el estado **No sincronizado** si el contexto funciona sin sincronización;
- una campana abre las **Notificaciones**;
- el botón **Mando** abre el panel de mando y actividad;
- un indicador muestra el estado de la red: Internet directo, relé, Wi‑Fi Direct, Wi‑Fi local, Bluetooth, LAN, sincronización o búsqueda de conexión.

## 4.2 Mapa central

El mapa muestra los objetos autorizados en el contexto actual:

- órdenes;
- avisos;
- objetivos;
- citas / puntos de reunión;
- alertas de seguridad;
- presencia de equipo;
- presencia exacta cuando está autorizada;
- movimientos / trayectorias según los derechos y los intercambios activos.

## 4.3 Leyenda

El botón `?` muestra la leyenda, en particular:

- Peligro;
- Objetivo;
- Punto de reunión;
- Equipo.

## 4.4 Pie de página

La parte inferior de la pantalla indica:

- el número de miembros activos del contexto;
- el número de objetos activos;
- la posible presencia de una sesión en curso; en caso contrario, su N.º personal.

## 4.5 Abrir el menú del grupo o del equipo

Toque el nombre del contexto en la parte superior izquierda.

El panel contiene las pestañas:

- **Contexto**
- **Equipos**
- **Participantes**
- **Invitar**
- **Operaciones**
- **Gestión**
- **Ajustes**

Algunas funciones solo aparecen si su rol posee el permiso correspondiente.

---

# 5. El mapa táctico

## 5.1 Desplazarse

El mapa se maneja como un mapa táctil clásico: desplazamiento y zoom.

## 5.2 Añadir un objeto

Para publicar un objeto espacial:

1. Mantenga pulsado el lugar deseado.
2. LETCOOR abre **Añadir aquí**.
3. Se muestran las acciones autorizadas para su rol.

Las posibilidades son:

- **Aviso**
- **Objetivo**
- **Orden**
- **Punto de reunión**
- **Alerta de seguridad**

Las acciones no autorizadas en su contexto no se muestran.

## 5.3 Formas geográficas

Según el tipo de objeto, LETCOOR permite:

- **Punto**;
- **Zona circular**;
- **Polígono**;
- **Trazado**.

Para una zona circular, el radio se puede ajustar de **10 a 500 m**.

Para un polígono o un trazado:

1. elija la geometría;
2. pulse **Dibujar en el mapa**;
3. añada los vértices en el mapa;
4. utilice **Deshacer el último**, **Finalizar** o **Cancelar**.

El número de puntos está limitado por la interfaz.

## 5.4 Duración / vencimiento

Los objetos espaciales que no sean de seguridad pueden tener una duración de entre **5 y 360 minutos**, en intervalos de 5 minutos.

---

# 6. Crear un aviso

1. Mantenga pulsado el mapa.
2. Elija **Aviso**.
3. Seleccione el tipo.
4. Introduzca opcionalmente un nombre y una descripción.
5. Elija la geometría y la duración.
6. Pulse **Publicar**.

## Tipos de aviso disponibles

- Peligro
- Obstáculo
- Ruta bloqueada
- Paso impracticable
- Paso abierto
- Adversario observado
- Grupo observado
- Movimiento observado
- Problema de material
- Personalizado

Según su rol, un aviso puede publicarse dentro del equipo o a nivel del grupo.

Los exploradores y responsables que dispongan de los permisos necesarios pueden, entre otras cosas, confirmar, impugnar, resolver o promover determinados avisos.

---

# 7. Crear un objetivo

1. Mantenga pulsado el mapa.
2. Elija **Objetivo**.
3. Introduzca **Objetivo que realizar**.
4. Elija el tipo.
5. Elija la prioridad.
6. Seleccione la geometría.
7. Ajuste el vencimiento.
8. Pulse **Publicar**.

## Tipos de objetivo

- Alcanzar un punto
- Mantener una zona
- Capturar una zona
- Recuperar un objeto
- Llegar a una cita
- Observar una zona
- Personalizado

## Objetivo de equipo u objetivo final del grupo

Cuando el rol y el contexto lo permiten, el formulario permite elegir:

- **Todo el grupo — objetivo final**;
- **Este equipo — objetivo de equipo**.

El objetivo final es visible para los miembros del grupo y los equipos de acuerdo con las reglas de autorización del Core.

## Prioridades

La interfaz ofrece:

- P0 — Urgente
- P1 — Alta
- P2 — Normal
- P3 — Baja

---

# 8. Crear una orden

1. Mantenga pulsado el mapa.
2. Elija **Orden**.
3. Introduzca la instrucción personalizada si es necesario.
4. Elija el tipo de orden.
5. Elija la prioridad.
6. Puede vincular la orden a un **objetivo** existente.
7. Puede vincular la orden a una **cita** existente.
8. Si es necesario, LETCOOR permite crear directamente un objetivo o una cita en el mismo lugar y luego volver a la orden.
9. Elija la geometría y la duración.
10. Pulse **Publicar**.

## Tipos de orden

- Desplazarse
- Reagruparse
- Mantener la posición
- Avanzar
- Replegarse
- Defender
- Observar
- Asegurar un objetivo
- Personalizado

## Orden del jefe de grupo

Cuando la publicación es una orden de mando del grupo, el jefe de grupo elige los **equipos destinatarios**. El código operativo prevé que este tipo de orden esté dirigido a los jefes de los equipos seleccionados.

## Orden de equipo

Un jefe de equipo puede crear órdenes dentro de su equipo. Una orden de equipo también puede vincularse a una orden de mando principal cuando esta relación está disponible.

---

# 9. Crear un punto de reunión

1. Mantenga pulsado el mapa.
2. Elija **Punto de reunión**.
3. Asigne un nombre corto.
4. Elija un **Punto** o una **Zona circular**.
5. Ajuste la duración / vencimiento.
6. Publique.

El punto de reunión crea una cita que también puede utilizarse como referencia para una orden.

---

# 10. Enviar una alerta de seguridad

La alerta de seguridad es una publicación prioritaria.

1. Mantenga pulsado el mapa.
2. Elija **Alerta de seguridad**.
3. Introduzca un mensaje si es necesario.
4. Elija el tipo.
5. Pulse **Enviar alerta**.

## Tipos disponibles

- Lesión
- Detener la actividad
- Peligro
- Persona desaparecida
- Otra emergencia

Una alerta personalizada requiere un mensaje.

LETCOOR recuerda en la interfaz que la alerta P0 debe utilizarse en caso de peligro o necesidad de ayuda.

Según los permisos, un responsable puede después **Marcar como resuelta**.

---

# 11. Interactuar con un objeto ya publicado

Toque un objeto del mapa para abrir su ficha.

Las acciones propuestas dependen del tipo de objeto y de sus permisos.

## Aviso

Acciones posibles:

- Confirmar
- Impugnar
- Resolver
- Prolongar 15 min
- Cancelar el aviso
- Promover al grupo cuando el aviso procede de un equipo y el rol lo permite

Para determinados objetos operativos, LETCOOR también puede proponer:

- **Confirmar sobre el terreno**;
- **Votar para resolver**;
- **Informar de paso abierto**;
- **Retirar la información**.

## Objetivo

Un usuario que disponga del permiso correspondiente puede cambiar su estado:

- En curso
- Terminado
- Fallido
- Cancelado

## Orden

Pueden proponerse respuestas según el tipo de orden:

- Recibida
- Aceptada
- Terminada
- Imposible

El panel simplificado **Operaciones > Órdenes** utiliza como mínimo el acuse **Recibida** cuando la orden requiere una respuesta.

## Alerta de seguridad

El responsable autorizado puede elegir **Marcar como resuelta**.

---

# 12. El panel «Mando y actividad»

El botón **Mando** de la parte superior de la pantalla abre un panel separado destinado a operaciones que no están necesariamente vinculadas a un punto del mapa.

Incluye hasta tres pestañas:

- **Notificaciones**
- **Publicar**
- **Historial**

Las pestañas solo aparecen cuando tienen contenido o cuando una acción está autorizada.

## 12.1 Notificaciones

Muestra los objetos operativos accesibles:

- orden de mando;
- orden de equipo;
- objetivo;
- objetivo final del grupo;
- anuncio;
- informe que verificar;
- aviso verificado.

Cada tarjeta puede indicar:

- texto;
- tipo;
- estado;
- equipo/grupo;
- objetivo o cita vinculados;
- equipos destinatarios;
- acuses de recibo;
- votos;
- progreso por equipo.

Según su rol, los botones pueden proponer:

- Recibida;
- Verificar sobre el terreno;
- Retirar;
- Marcar como leída;
- Declarar terminada;
- Votar terminada;
- Votar imposible;
- Votar resuelta;
- Resolver.

## 12.2 Publicar

LETCOOR solo muestra las publicaciones autorizadas para su rol y su contexto.

Los tipos internos gestionados actualmente por la interfaz incluyen:

- Orden de mando
- Orden de equipo
- Objetivo de equipo
- Objetivo final del grupo
- Anuncio
- Informe que verificar
- Aviso verificado

Para una orden de mando, elija los equipos destinatarios.

Para una orden de equipo, puede seleccionar una orden de mando principal.

A continuación, introduzca la descripción y pulse **Publicar**.

Las publicaciones creadas desde este panel utilizan actualmente una duración operativa predeterminada de unos 30 minutos en el código de la interfaz.

## 12.3 Historial

Muestra los eventos registrados con su fecha, resumen e identificador del objeto.

---

# 13. El menú del grupo o del equipo

Toque el nombre del contexto en la parte superior izquierda.

## Pestaña Contexto

Muestra:

- el selector **Grupo o equipo**;
- el número de miembros;
- el número de dispositivos conectados;
- el estado de la sesión;
- sus roles;
- el tema Sistema / Claro / Oscuro;
- el idioma;
- su **N.º personal**, que se puede copiar.

Los idiomas expuestos actualmente por la interfaz son: **Sistema, Français, English, العربية, Deutsch y Русский**. La interfaz cambia automáticamente al sentido de derecha a izquierda para el árabe.

## Pestaña Equipos

Véase [Equipos](#14-equipos).

## Pestaña Participantes

Véase [Participantes y roles](#15-participantes-y-roles).

## Pestaña Invitar

Véase [Invitar a un nuevo participante](#16-invitar-a-un-nuevo-participante).

## Pestaña Operaciones

Véase [Operaciones](#17-operaciones).

## Pestaña Gestión

Véase [Gestión del grupo y de los equipos](#21-gestión-del-grupo-y-de-los-equipos).

## Pestaña Ajustes

Actualmente contiene:

- mapas sin conexión;
- gestión de permisos Bluetooth/Wi‑Fi Direct;
- permiso de cámara;
- comprobación de ubicación.

---

# 14. Equipos

La pestaña **Equipos** muestra los equipos del grupo.

Para cada equipo, LETCOOR muestra, entre otros:

- nombre;
- número de miembros;
- jefe de equipo;
- lista de participantes;
- su estado de acceso al equipo.

## Estados de acceso

- **Es miembro · acceso listo**
- **Adhesión registrada · recepción de claves en curso**
- **No forma parte de este equipo**

Si es miembro y el acceso está listo, pulse **Abrir mi equipo**.

## 14.1 Crear un equipo

Esta función aparece para el jefe de grupo que dispone del permiso correspondiente.

1. Introduzca el **Nombre del equipo**.
2. Elija el **Jefe de equipo** entre los miembros del grupo.
3. Seleccione opcionalmente los miembros iniciales.
4. Puede utilizar:
   - Seleccionar todo;
   - 10 personas;
   - 15 personas;
   - Deseleccionar todo.
5. Pulse **Crear el equipo y nombrar a su jefe**.

Un equipo admite como máximo 200 miembros iniciales en el formulario, incluido el jefe.

Los miembros seleccionados abandonan su posible equipo anterior dentro del mismo grupo para unirse al nuevo.

Cuando el grupo ya tiene diez equipos o más, el código impone reglas adicionales de tamaño mínimo: los equipos activos deben contar con al menos cuatro miembros para continuar la expansión.

## 14.2 Sustituir al jefe de equipo

Si la acción está autorizada:

1. abra el equipo;
2. utilice **Sustituir al jefe de equipo**;
3. elija un miembro del grupo.

## 14.3 Umbrales de validación

Los responsables autorizados pueden configurar:

- votos de exploradores necesarios para terminar;
- votos de exploradores necesarios para declarar imposible;
- votos necesarios para resolver un aviso.

---

# 15. Participantes y roles

La pestaña **Participantes** muestra los miembros del contexto seleccionado.

Puede buscar a un participante por su N.º personal o su identificador.

Toque un participante para abrir las acciones disponibles.

## 15.1 Roles permanentes y roles de sesión

Cuando hay una sesión disponible, el gestor puede elegir:

- **Permanente**;
- **Sesión**.

Un rol permanente permanece asociado al miembro según las reglas del grupo/equipo.

Un rol de sesión se aplica a la sesión seleccionada.

## 15.2 Asignar o retirar un rol

Los roles que puede asignar aparecen en forma de botones.

Un botón activo indica que el rol ya está presente. Pulsarlo permite retirarlo cuando tenga la autoridad necesaria.

También existe una sección **Administrar un rol en un equipo** que permite elegir:

1. el equipo de destino;
2. el rol;
3. **Asignar el rol de equipo** o **Retirar el rol de equipo**.

## 15.3 Asignación de sesión

Un administrador de sesión puede establecer al participante como:

- Activo;
- En pausa;
- Se ha ido;
- Retirado.

También puede elegir su equipo de sesión o **Sin equipo**.

Pulse **Aplicar la asignación**.

## 15.4 Retirar a un miembro

Cuando el permiso está disponible, aparece el botón **Retirar de este grupo o equipo**.

## 15.5 Transferir la administración del grupo

El responsable autorizado puede seleccionar a otro participante y utilizar **Transferir la administración**.

El destinatario deberá aceptar después la transferencia desde la sección **Gestión**.

## 15.6 Bloquear un dispositivo

La sección **Moderación** permite, cuando su rol lo autoriza:

- **Bloquear este dispositivo**;
- mostrar los dispositivos bloqueados;
- **Levantar el bloqueo**.

Un dispositivo bloqueado seguirá siendo rechazado en las nuevas invitaciones hasta que se levante el bloqueo.

---

# 16. Invitar a un nuevo participante

Abra **Invitar**.

## 16.1 Elegir el destino

Según su rol, el menú **Destino** permite elegir:

- el grupo;
- un equipo.

Un administrador del grupo puede disponer de varios destinos en el menú.

## 16.2 Admisiones abiertas / cerradas

La interfaz puede indicar:

- **Admisiones abiertas**;
- **Admisiones cerradas**.

Si su rol lo permite:

- **Abrir el acceso**;
- **Cerrar el acceso**.

Un equipo también puede heredar el cierre general del grupo.

## 16.3 Compartir la invitación

LETCOOR permite:

- enlace;
- QR;
- copia;
- compartir mediante el sistema;
- archivo `.letcoor` en las plataformas donde se ofrece el botón.

## 16.4 Recibir la respuesta

Después de que el otro dispositivo importe la invitación:

1. abra **Recibir la respuesta**;
2. escanee o pegue el enlace de respuesta;
3. LETCOOR inicia la conexión.

Si los intentos por Internet y proximidad agotan el tiempo de espera, el botón **Reintentar** permite volver a empezar.

## 16.5 Restablecer una invitación

El botón de restablecimiento permite invalidar/regenerar el intercambio actual cuando su rol lo permite.

---

# 17. Operaciones

La pestaña **Operaciones** permite elegir un grupo o un equipo y muestra después varias subpestañas según los permisos y el contenido:

- **Órdenes**
- **Anuncios**
- **Roles**
- **Intercambio entre equipos**
- **Sesiones**
- **Historial**

## 17.1 Órdenes

Muestra las órdenes activas con:

- tipo;
- prioridad;
- texto;
- estado de respuesta.

Cuando se requiere un acuse, el botón **Recibida** permite acusar recibo desde esta vista.

## 17.2 Anuncios

Muestra los anuncios activos.

Cada anuncio puede incluir:

- tipo;
- texto;
- estado fijado;
- botón **Acusar recibo**.

Un miembro autorizado puede crear un anuncio eligiendo:

### Tipos

- Información
- Importante
- Información del grupo
- Información de sesión
- Regla de la actividad
- Coordinación

### Expiración

- 15 min
- 1 h
- 4 h
- 24 h
- Sin expiración

Una casilla permite **Fijar el anuncio**.

---

# 18. Campañas de roles

Las campañas de roles permiten abrir temporalmente plazas para un rol determinado.

Se encuentran en:

**Menú del grupo/equipo > Operaciones > Roles**

## 18.1 Unirse a una campaña

Una campaña abierta muestra:

- el rol;
- su estado;
- el modo;
- el número de plazas ya asignadas / capacidad.

Pulse **Unirse** para solicitar el rol.

## 18.2 Modos de campaña

### Primeras solicitudes válidas — `FIRST_VALID`

Las primeras solicitudes elegibles se asignan automáticamente hasta agotar la capacidad disponible.

El código solo permite este modo para los roles considerados no privilegiados.

### Validación por un responsable — `ADMIN_APPROVAL`

Las solicitudes permanecen pendientes hasta que un responsable las apruebe.

El gestor ve **Solicitudes pendientes** y puede pulsar **Aprobar** para cada participante.

## 18.3 Crear una campaña

Si su rol permite gestionar campañas:

1. elija el **Rol**;
2. elija el **Modo** propuesto para ese rol;
3. elija el número de **Plazas** de 1 a 64;
4. elija la **Duración**:
   - 15 min;
   - 1 h;
   - 4 h;
   - 24 h;
5. pulse **Abrir una campaña**.

## 18.4 Cerrar una campaña

Un gestor autorizado puede pulsar **Cerrar**.

## 18.5 Retirar su solicitud

En **Historial**, una solicitud todavía pendiente puede mostrar **Retirar mi solicitud**.

## 18.6 Roles disponibles para las campañas

El código expone a las campañas, según el contexto y sus permisos:

- Explorador del grupo;
- Explorador de equipo;
- Relé;
- Cobertura;
- Asalto.

El rol de Jefe de grupo nunca se asigna mediante una campaña.

---

# 19. Sesiones

Una sesión representa un periodo operativo limitado dentro del grupo.

## 19.1 Crear una sesión

Desde **Gestión**, si dispone del permiso:

1. abra la sección **Sesión**;
2. introduzca la duración en minutos;
3. la duración máxima mostrada es de **56 días**;
4. pulse **Crear una sesión**.

## 19.2 Consultar las sesiones

En **Operaciones > Sesiones**, LETCOOR muestra:

- fecha de creación;
- estado: abierta/finalizada o estado de asignación;
- su posible equipo;
- final previsto.

## 19.3 Gestionar una sesión

El responsable autorizado puede:

- añadir **+ 1 h**;
- **Finalizar** la sesión.

## 19.4 Roles y asignaciones durante una sesión

En **Participantes**, puede elegir una sesión administrada, asignar roles limitados a esa sesión y asignar a los participantes a un equipo/estado.

---

# 20. Intercambio de datos entre equipos

Esta función está disponible desde un **equipo** en:

**Operaciones > Intercambio entre equipos**

No concede automáticamente acceso al contenido privado de otro equipo. Utiliza una oferta de intercambio creada y aceptada explícitamente.

## 20.1 Proponer un intercambio

1. Elija el **Equipo de destino**.
2. Elija los **Datos compartidos**.
3. Elija la precisión.
4. Ajuste la frecuencia.
5. Ajuste la expiración.
6. Pulse **Proponer el intercambio**.

## 20.2 Clases de datos disponibles

- Presencia general del equipo
- Señal
- Estado del equipo
- Posición precisa
- Historial de desplazamientos

## 20.3 Precisión

- Vista general / agregada
- Aproximada
- Precisa

Si se selecciona **Posición precisa**, la precisión pasa necesariamente a ser precisa en la interfaz.

## 20.4 Frecuencia

Ajustable entre **5 y 300 segundos**, en intervalos de 5 segundos.

## 20.5 Expiración

- 15 min
- 1 h
- 4 h
- 24 h

## 20.6 Aceptar o revocar

El equipo destinatario autorizado puede pulsar **Aceptar**.

Una oferta o un intercambio puede ser **Revocado** por la parte que disponga del permiso correspondiente.

---

# 21. Gestión del grupo y de los equipos

La pestaña **Gestión** centraliza las funciones administrativas.

## 21.1 Seleccionar un espacio

El selector **Grupo o equipo** permite elegir el espacio que administrar.

## 21.2 Unirse a un equipo existente

Cuando la acción está autorizada, un equipo puede proponer:

- **Unirse**;
- **Recuperar el acceso** cuando la adhesión existe pero las claves deben recuperarse.

## 21.3 Salir de un equipo

Pulse **Salir del equipo** y revise el resumen antes de confirmar.

## 21.4 Disolver un equipo

Un responsable autorizado ve **Disolver el equipo**.

La confirmación indica que:

- el equipo será disuelto para sus miembros;
- los miembros permanecen en el grupo;
- los demás dispositivos aplicarán la disolución cuando la reciban.

## 21.5 Salir de un grupo

Un miembro ordinario puede preparar un plan de salida y luego confirmarlo.

Si el participante dirige equipos, LETCOOR puede tener que disolver esos equipos antes de su salida según el plan calculado por el Core.

## 21.6 Disolver un grupo

El jefe de grupo autorizado puede utilizar **Disolver el grupo**.

La confirmación advierte de que el grupo y sus equipos serán disueltos. Los dispositivos sin conexión deberán volver a conectarse para recibir la disolución.

## 21.7 Unirse a un nuevo grupo o equipo

La página **Gestión** también contiene un bloque **Unirse a un grupo o equipo** con el mismo sistema de invitación que la incorporación inicial.

## 21.8 Invitaciones pendientes

Cuando el Core expone invitaciones que aceptar, estas aparecen con un botón **Aceptar** hasta su expiración.

## 21.9 Estado del equipo

El responsable autorizado puede publicar:

- Listo
- En movimiento
- En posición
- En reunión
- Necesita ayuda
- Desconectado

## 21.10 Política de posición exacta

En un equipo, un responsable autorizado puede elegir:

- **Permitir**;
- **Denegar**

para la política de posición exacta del equipo.

## 21.11 Transferencia de administración

Si hay una transferencia de administración pendiente para usted, la sección muestra **Aceptar la transferencia de administración**.

---

# 22. Límites de publicación

En **Gestión**, los responsables autorizados pueden configurar los límites de publicación del grupo o del equipo.

Los límites pueden definirse:

- de forma predeterminada;
- para un miembro concreto.

Parámetros expuestos actualmente:

- número de alertas de seguridad activas;
- avisos por minuto;
- avisos por 4 minutos.

Los valores del formulario van de 1 a 1000.

---

# 23. Ubicación

El icono **Ubicación** aparece en el mapa cuando la plataforma ofrece ubicación nativa.

## 23.1 Activar el uso compartido

1. Abra **Ubicación**.
2. Seleccione **Compartir mi ubicación**.
3. Ajuste la precisión.

LETCOOR vuelve a publicar la presencia periódicamente mientras el uso compartido está activo y la aplicación puede obtener la posición.

## 23.2 Precisión

El control deslizante va de **0 m a 1 km**.

- **0 m**: precisión disponible en el dispositivo, sin desplazamiento añadido por LETCOOR.
- valor superior: la posición compartida se desplaza aleatoriamente dentro del radio elegido.

## 23.3 Detener el uso compartido

Seleccione **No compartir mi ubicación**.

El uso compartido también se detiene cuando cambia el contexto o cuando la aplicación interrumpe la presencia según su ciclo de vida.

## 23.4 Estados mostrados

- Obteniendo ubicación…
- Uso compartido activo con su grupo
- Uso compartido pendiente de reanudación
- Ubicación no compartida

> Compartir la ubicación no es obligatorio para unirse a un grupo, utilizar el mapa, enviar órdenes o utilizar la malla.

---

# 24. Notificaciones

Toque la **campana** en la parte superior de la pantalla.

El centro de notificaciones reúne:

- eventos del grupo;
- cambios de conexión/transporte;
- avisos del sistema LETCOOR.

El indicador muestra el número de notificaciones no leídas.

## 24.1 Lectura

Las notificaciones se marcan como leídas cuando se vuelven suficientemente visibles en la lista o cuando se consulta la sección correspondiente.

## 24.2 Navegación

Tocar una notificación puede abrir:

- la sección Participantes;
- Equipos;
- Operaciones;
- un objeto del mapa;
- el panel Mando.

## 24.3 Notificaciones del sistema

Los ajustes de la campana permiten activar/desactivar las notificaciones nativas del sistema cuando la plataforma lo permite.

---

# 25. Mapas sin conexión

Abra:

**Menú del grupo/equipo > Ajustes > Mapas sin conexión**

## 25.1 Seleccionar una zona

1. Pulse **Seleccionar teselas en el mapa**.
2. LETCOOR cierra el panel y muestra una cuadrícula sobre el mapa.
3. Toque las celdas que desea conservar.
4. El contador indica el número de celdas seleccionadas sobre un máximo de 20.
5. Pulse **Validar** para volver a los ajustes o **Cancelar**.

## 25.2 Nivel de detalle

El menú **Detalle** permite seleccionar un zoom de 3 a 14.

Una zona demasiado grande con un nivel de detalle alto puede ser rechazada. La interfaz pide entonces reducir el detalle o elegir celdas más pequeñas.

## 25.3 Instalar

Una vez elegidas las celdas:

1. pulse **Instalar las celdas seleccionadas**;
2. siga el progreso;
3. puede **Cancelar la descarga**.

## 25.4 Eliminar un mapa

Los mapas instalados se muestran con su zoom y su tamaño. Pulse **Eliminar** para liberar espacio.

---

# 26. Conexión de red y funcionamiento sin conexión

LETCOOR puede utilizar varios transportes para una misma red lógica.

La interfaz reconoce, entre otros:

- **Internet directo**;
- **Internet mediante relé**;
- **Red local (LAN)**;
- **Wi‑Fi local**;
- **Wi‑Fi Direct**;
- **Bluetooth**.

## 26.1 Malla lógica

LETCOOR no exige que cada miembro esté conectado directamente con todos los demás.

Ejemplo:

```text
Teléfono A ↔ Teléfono B ↔ Teléfono C ↔ Teléfono D
```

Un evento autorizado puede ser retransmitido entre pares según la topología y las reglas de alcance del grupo/equipo.

El transporte físico y la identidad LETCOOR están separados: un par sigue identificado por su identidad LETCOOR aunque cambie la ruta de red.

## 26.2 Sin Internet

Para maximizar las posibilidades de funcionar sin Internet:

- active el Wi‑Fi;
- active el Bluetooth;
- autorice los dispositivos cercanos;
- autorice la red local si Android lo solicita;
- acepte la visibilidad/emparejamiento del sistema cuando LETCOOR lo solicite;
- mantenga LETCOOR en primer plano durante la primera conexión;
- acerque los dispositivos durante el arranque inicial;
- no rechace los diálogos del sistema necesarios para la radio de proximidad.

## 26.3 Estado de los transportes de proximidad

LETCOOR puede mostrar por separado:

- Wi‑Fi local;
- Wi‑Fi Direct;
- Bluetooth;

con estados como:

- permiso requerido;
- activación requerida;
- inicialización;
- listo;
- búsqueda;
- par encontrado;
- conexión;
- grupo formado;
- autenticación LETCOOR;
- conectado;
- recuperación;
- no disponible.

## 26.4 Wi‑Fi Direct ocupado

Si Android indica que Wi‑Fi Direct está ocupado, LETCOOR puede intentar recuperarlo. La pantalla de información de Wi‑Fi Direct recomienda, entre otras cosas, comprobar:

- que el Wi‑Fi esté activo;
- que el uso compartido de conexión/hotspot no entre en conflicto con Wi‑Fi Direct;
- que no haya ya otra búsqueda/conexión Wi‑Fi Direct en curso.

## 26.5 La red puede cambiar de transporte

El estado de la parte superior de la pantalla puede mostrar distintos transportes durante la sesión. LETCOOR puede disponer de rutas alternativas hacia un par y utilizar la ruta disponible según el estado de la red.

---

# 27. Privacidad, bloqueo y recuperación

LETCOOR aplica varios comportamientos de protección cuando los datos privados de un grupo ya no pueden verificarse con otros miembros.

## 27.1 Bloqueo tras una ausencia

El código de la interfaz prevé una pantalla:

**Sesión bloqueada después de un minuto de ausencia.**

Pulse **Volver a conectarse** para recuperar el acceso.

## 27.2 Verificación de la conexión con los miembros

Cuando se necesita una recuperación de privacidad, LETCOOR muestra:

**Verificando la conexión con los miembros…**

Intenta encontrar un miembro accesible y puede mostrar los detalles de los transportes de proximidad.

## 27.3 Eliminación automática local

Para determinados grupos configurados con recuperación automática, si no es posible volver a conectarse durante el periodo previsto, los datos locales del grupo pueden eliminarse **después de una verificación**.

La interfaz actual anuncia un plazo de veinte minutos para los grupos afectados.

Cuando se ofrece, puede:

- eliminar/restablecer los datos locales;
- o elegir **Conservar los datos bajo mi responsabilidad**, lo que desactiva la eliminación automática para este contexto.

LETCOOR advierte de que conservar estos datos puede aumentar el riesgo en caso de compromiso físico del dispositivo.

## 27.4 Protección de escritorio

En escritorio, la vista privada puede ocultarse/difuminarse cuando la ventana pierde el foco y luego actualizarse antes de volver a mostrarse.

---

# 28. Roles disponibles

El modelo de dominio de LETCOOR define nueve roles.

| Rol | Función general en el código actual |
|---|---|
| **Administrador del grupo** (`GROUP_ADMIN`) | Administración del grupo, creación de equipos y sesiones, gestión de miembros/roles, campañas, disolución, transferencia de administración, anuncios. |
| **Coordinador del grupo** (`GROUP_LEADER`) | Coordinación a nivel de grupo, órdenes/objetivos/avisos del grupo, campañas y anuncios según permisos. |
| **Jefe de equipo** (`TEAM_LEADER`) | Órdenes/objetivos/citas/estado de su equipo, intercambio entre equipos, anuncios, campañas de equipo. |
| **Explorador del grupo** (`GROUP_SCOUT`) | Avisos y confirmación/promoción a nivel del grupo según permisos. |
| **Explorador de equipo** (`TEAM_SCOUT`) | Informe/aviso de equipo, confirmación y promoción según permisos. |
| **Relé** (`TRANSMITTER`) | Capacidad de retransmisión prevista por el dominio y publicación de determinadas presencias resumidas según la política; este rol no concede acceso a los datos privados de otros equipos. |
| **Cobertura** (`COVER`) | Etiqueta operativa con las capacidades básicas del miembro. |
| **Asalto** (`ATTACKER`) | Etiqueta operativa con las capacidades básicas del miembro. |
| **Miembro** (`MEMBER`) | Capacidades básicas: aviso normal dentro de su equipo cuando está permitido, alerta de seguridad, respuesta a órdenes, presencia autorizada y participación en campañas. |

> Los permisos son calculados por el Core y son aditivos. La interfaz solo muestra las acciones realmente autorizadas. Pertenecer a un grupo no concede automáticamente acceso a los datos privados de todos sus equipos.

---

# 29. Consejos de preparación antes de una actividad

Para un uso real, especialmente en una zona donde Internet puede ser deficiente:

1. Instale la misma versión de LETCOOR en los dispositivos.
2. Cree el grupo antes de iniciar la actividad.
3. Haga que los participantes se unan mientras todavía estén físicamente cerca.
4. Acepte los permisos de proximidad en cada Android.
5. Active Bluetooth y Wi‑Fi.
6. Pruebe al menos una conexión sin datos móviles si el funcionamiento sin conexión es importante.
7. Cree los equipos y asigne los jefes antes de dispersarse.
8. Abra una sesión si desea roles/asignaciones de sesión y el historial correspondiente.
9. Descargue los mapas sin conexión necesarios antes de perder Internet.
10. Compruebe que los participantes sepan abrir:
    - Notificaciones;
    - Mando;
    - su equipo;
    - la función Alerta de seguridad.
11. Active el uso compartido de ubicación solo si realmente desea publicarla.

---

# 30. Solución de problemas

## Los dos dispositivos no se ven sin conexión

Compruebe en ambos dispositivos:

- Wi‑Fi activado;
- Bluetooth activado;
- permisos de **Dispositivos cercanos** concedidos;
- permiso de red local concedido si Android lo solicita;
- aplicación visible/detectable si el sistema solicita confirmación;
- LETCOOR en primer plano durante la búsqueda inicial.

Si Android abre los ajustes de ubicación, active el servicio de ubicación para maximizar la compatibilidad de descubrimiento. Esto no activa el uso compartido de posición de LETCOOR.

## «Wi‑Fi Direct no disponible» u «ocupado»

- desactive temporalmente cualquier uso compartido de conexión/hotspot manual;
- espere unos segundos;
- vuelva a iniciar el intento;
- compruebe que no haya otra aplicación o conexión Wi‑Fi Direct activa.

## El QR no funciona

- espere a que se hayan leído todas las partes del QR;
- acerque las pantallas;
- aumente el brillo de la pantalla que muestra el QR;
- utilice el control de zoom de la cámara;
- utilice el enlace en lugar del QR si es necesario.

## Se ha denegado la cámara

- utilice el enlace;
- o abra los ajustes de cámara de Windows/Android desde LETCOOR cuando se ofrezca el botón.

## El enlace se acepta, pero la conexión agota el tiempo de espera

- compruebe Internet o la proximidad;
- acerque los dispositivos;
- active Wi‑Fi y Bluetooth;
- acepte los diálogos del sistema;
- pulse **Reintentar** cuando aparezca el botón.

## Estoy en el grupo, pero no en un equipo

Abra:

**Contexto > Equipos** o **Gestión**.

Si el equipo permite la adhesión, utilice **Unirse**. Una invitación de equipo también puede admitir directamente al participante en el grupo principal y en el equipo de destino según el ticket recibido.

## «Adhesión registrada · recepción de claves en curso»

La adhesión se conoce, pero el acceso criptográfico al equipo todavía no está listo. Mantenga los dispositivos conectados para permitir la recuperación/sincronización de las claves. Si el botón **Recuperar el acceso** aparece en Gestión, utilícelo.

## Un objeto no es visible

Compruebe:

- el grupo/equipo seleccionado;
- sus permisos;
- la expiración del objeto;
- la sincronización de red;
- que un objeto privado de equipo no es automáticamente visible para los demás equipos.

## La ubicación no aparece

- compruebe el permiso de ubicación;
- compruebe que **Compartir mi ubicación** esté seleccionado;
- compruebe el grupo actual;
- espere a la siguiente publicación periódica;
- compruebe que la política del equipo permita la precisión necesaria.

---

# 31. Resumen rápido

## Para unirse a LETCOOR

```text
Dispositivo que invita
  ↓
Invitar
  ↓
QR o enlace
  ↓
El dispositivo invitado importa
  ↓
El dispositivo invitado genera una respuesta
  ↓
El dispositivo que invita escanea/pega la respuesta
  ↓
Conexión + autenticación + admisión
```

## Para crear algo en el mapa

```text
Mantener pulsado el mapa
  ↓
Aviso / Objetivo / Orden / Punto de reunión / Alerta de seguridad
  ↓
Rellenar el formulario
  ↓
Elegir zona / duración si está disponible
  ↓
Publicar
```

## Para gestionar un grupo

```text
Nombre del grupo arriba a la izquierda
  ↓
Contexto | Equipos | Participantes | Invitar | Operaciones | Gestión | Ajustes
```

## Para una campaña de roles

```text
Operaciones
  ↓
Roles
  ↓
Elegir rol + modo + plazas + duración
  ↓
Abrir una campaña
  ↓
Los miembros se unen
  ↓
Asignación automática o validación por un responsable según el modo
```

## Para funcionar sin Internet

```text
Wi‑Fi ACTIVADO
Bluetooth ACTIVADO
Permisos de proximidad autorizados
Red local autorizada si se solicita
Emparejamiento/visibilidad aceptados si se solicita
Dispositivos próximos en el primer contacto
LETCOOR abierto en primer plano
```

LETCOOR puede utilizar después los transportes disponibles y retransmitir la información autorizada entre pares según la topología de la malla.

---

**LETCOOR 1.0.0 — Documentación del usuario**
