---
description: >-
  Se entrega el PKT y un documento con los apuntes de la configuración
  realizada. Reviso en el aula.
icon: signal-messenger
---

# M0370T1A5-allCisco

## Actividades

### M370T2A3 — Cisco Packet Tracer

**Módulo:** 0370 — Redes\
**Ciclo:** ASIX\
**Dedicación:** 4 horas\
**Modalidad:** Individual\
**Rúbrica:** Se hace en clase\
**Entrega:** Archivo PKT y enlace a GitBook.

### Objetivo

Introducción a Cisco Packet Tracer y a la configuración de:

1. **Router SOHO**
   * Apertura de puertos (_port forwarding_).
   * Redes de invitados.
   * DHCP y DNS.
2. **Servidores y servicios**
   * DHCP y DNS.
   * WEB.
   * FTP.

### Entrega

* Archivo PKT debidamente cumplimentado durante la práctica en clase.
* Documento con las preguntas planteadas y sus respuestas.

### Descripción de la práctica

La configuración representa una red de empresa conectada a un ISP y una red doméstica situada detrás de un router inalámbrico.

**Nota:** preparar en casa la topología de red con todos los dispositivos conectados.

### Dispositivos y redes

Se utilizan tres redes: LAN1-Empresa, LAN2-Casa e ISP.

#### 1. LAN1 — Empresa

* 1 PC inicial.
* 1 servidor.
* 3 PC adicionales.
* 1 impresora.
* 3 puntos de acceso (A17, A18 y A10).
* 1 switch.

#### 2. LAN2 — Casa

* 1 router inalámbrico.
* 2 portátiles.
* 1 impresora.

#### 3. ISP

* 2 routers.
* 2 servidores.

### Configuración general

1. Cada servidor tendrá una página web que se propone personalizar.
2. El servidor **Google**, situado en el ISP, será el servidor DNS para todos los dispositivos.
3. Configurar RIP en cada router.

### Configuración en la empresa

1. El servidor **Trantor** ofrecerá los servicios WEB, DHCP y DNS.
2. Añadir dos dispositivos (una impresora y un portátil) a la red de la empresa para que reciban los parámetros de red mediante DHCP.

### Configuración en el ISP

1. El servidor **Google** ofrecerá los servicios DHCP y DNS.
2. El servidor **Paco** ofrecerá el servicio FTP.

### Configuración en casa: Home Router

#### 1. Configuración básica

* Configurar la IP de Internet.
* Configurar el DNS apuntando al servidor Godo del ISP.
* Activar el servicio DHCP para los equipos de casa.

#### 2. Wi-Fi

* Habilitar exclusivamente la banda de 2,4 GHz.
* Habilitar la seguridad WPA2.

#### 3. Guest Network

* Habilitar el acceso de invitados sin posibilidad de acceder a la red doméstica.
* Deshabilitar mediante MAC el acceso a la red de 2,4 GHz del PC de Xenxito.

#### 4. Access Restriction

Configurar reglas de acceso a la red. En este caso, configurar una ACL estándar (1–99) para bloquear el protocolo HTTP a través del puerto 80 a los dispositivos indicados en la lista. En el ejemplo, únicamente se bloquea el PC con IP **192.168.0.102**.

**Comprobación:** probar qué ocurre si únicamente se bloquea el puerto 80 (HTTP) y no se bloquea el puerto 443 (HTTPS).

### Prueba de configuración extra

#### Empresa

1. Añadir dos portátiles y una impresora.
2. Añadir un punto de acceso y conectar un smartphone a él.

#### ISP

1. Habilitar el servicio FTP. La actividad indica que resulta más interesante hacerlo desde Linux.
2. Conectarse desde cualquier equipo al servidor donde se haya habilitado el servicio FTP.

#### Casa

1. Conectar un teléfono y una tablet a la Wi-Fi de invitados.
2. Probar a habilitar la MAC de un equipo externo para que pueda acceder al servidor de casa.
3. Comprobar qué le sucede al PC de Xenxita si se bloquea el acceso mediante **Website Blocking by URL** al servidor Godo.
4. Probar la opción **Blocked Applications**.

***

## Preguntas

### Preguntas sobre la práctica LAN–WAN–HOMELAN

#### Incidencias tenidas durante el proceso de configuración

Las incidencias que he tenido mientras hacía la actividad han sido las siguientes:

* Conflicto de subredes y direcciones duplicadas en la empresa: Al iniciar la actividad me encontré con etiquetas mezcladas entre `192.168.1.0/24` y `192.168.3.0/24`, además de direcciones repetidas en notas y equipos, por lo que lo fui corrigiendo para unificar la LAN de la empresa en `192.168.3.0/24` con puerta de enlace `192.168.3.1` y revisar las etiquetas antiguas que aún quedaban visibles.
* Registro DNS apuntando a una subred anterior: El registro `A` de `[www.empresa.com](https://www.empresa.com)` apuntaba al principio a una IP de una subred anterior en vez de a la IP actual del servidor de la empresa (`192.168.3.66`), lo que impedía resolver bien el dominio hasta que lo actualicé.
* Servidor FTP (`Server0`) sin IP estática ni gateway al principio: Tenía `Server0` en DHCP con `Default Gateway: 0.0.0.0`, lo que no le permitía responder con fiabilidad fuera de su red; lo pasé a configuración estática con su IP (`70.0.0.2`) y su _Default Gateway_ (`70.0.0.1`).
* Conexión FTP con `Timed out`: Al probar la conexión FTP desde la empresa hacia el servidor, me salió `%Error opening ftp://... (Timed out)` y tuve que revisar las rutas RIP en los routers intermedios, el direccionamiento del servidor y el estado/usuario del servicio FTP.
* Ajustes en páginas web HTML: Corregí errores de texto en las páginas personalizadas (como `"Servervicio"` en la web de la empresa y faltas de ortografía en la web de casa).

#### ¿Por qué no podemos acceder a la web del servidor de casa desde el ISP o la empresa? ¿Qué tenemos que configurar para poder hacerlo?

* Por qué no puedo acceder directamente: El servidor de casa (`Portal_de_la_casa` en `192.168.0.101`) tiene una IP privada (`192.168.0.0/24`), que no es enrutable por Internet ni por el ISP, y está detrás de mi router de casa (`Hause`), que aplica NAT y bloquea por defecto las conexiones entrantes que no se hayan solicitado desde dentro.
* Qué tengo que configurar:
  * Port Forwarding: En el router de casa (`Hause`, en _Applications & Gaming / Port Forwarding_), debo redirigir el puerto `80` (HTTP) —y el `443` si uso HTTPS— hacia la IP privada interna del servidor de casa (`192.168.0.101`).
  * Dirección IP alcanzable: Tengo que asegurarme de que el router de casa tenga su IP WAN/Internet bien configurada (`13.0.0.2`) y alcanzable desde el ISP y desde la empresa.
  * Registro DNS: Debo hacer que el dominio (por ejemplo `[www.portaldelacasa.com](https://www.portaldelacasa.com)` o `[www.casa.com](https://www.casa.com)`) apunte a la IP WAN del router de casa (`13.0.0.2`) y no directamente a la IP privada `192.168.0.101` desde redes externas.

#### ¿Cómo o qué detalle nos indica la conexión del router del proveedor de servicios con el home router de casa?

En mi topología lo veo por el enlace físico que une el router del lado del proveedor/ISP (`Gemeni`, interfaz `Gig0/0/0`) con el router inalámbrico de casa (`Hause`, interfaz `Gig 0/1` / `0/0`), compartiendo el segmento de enlace `13.0.0.0/8` (con `13.0.0.1` en `Gemeni` y `13.0.0.2` en la interfaz WAN de `Hause`) y con los indicadores de enlace activos en verde en Packet Tracer.

#### ¿Cómo se lleva a cabo internamente la resolución del dominio y la descarga del HTML desde la perspectiva del cliente (navegador) y del DNS?

1. Comprobación de caché y petición DNS: Cuando abro el navegador en un cliente (como `Mikel_Oyarzabal`) y pido `[www.empresa.com](https://www.empresa.com)`, primero revisa si ya tiene esa IP en caché; si no la tiene, el sistema envía una consulta DNS (puerto UDP/TCP `53`) al servidor DNS configurado (`8.8.8.8`).
2. Respuesta del DNS: El servidor DNS busca el registro `A` correspondiente al dominio y me devuelve su IPv4 (`192.168.3.66`).
3. Conexión TCP y petición HTTP: Con esa IP, el navegador inicia la conexión hacia el servidor web (puerto `80` en HTTP o `443` en HTTPS) a través de su _Default Gateway_ (`192.168.3.1`) y los routers intermedios.
4. Descarga y renderizado del HTML: El servidor web responde (`HTTP/1.1 200 OK`) enviando el `index.html` y los recursos asociados (como imágenes o CSS), y el navegador lo interpreta y muestra en pantalla.

#### Cambia los DNS de los servidores y haz que todos apunten al servidor de Google 8.8.8.8

Configuro los DNS de los servidores y después hago que todos apunten al servidor de Google (`8.8.8.8`), tanto en la configuración estática como en los _pools_ DHCP y clientes (incluida la red de casa), comprobándolo después con `ipconfig /all` o en _IP Configuration_. _(En el enunciado se mencionan los nombres Trantor, Paco y Godo; en mi topología utilizo `Server LAN` en `192.168.3.66` para la empresa, `Google` en `8.8.8.8` y `Server0` para FTP y DHCP del ISP)._

#### ¿Cómo se lleva a cabo la resolución del dominio a nivel del DNS?

A nivel del DNS, el cliente manda una consulta con el nombre de dominio (FQDN) y el tipo de registro (habitualmente `A` para IPv4 o `AAAA` para IPv6). El servidor DNS consultado busca en su zona o registros locales o reenvía/resuelve jerárquicamente la consulta (servidores raíz, TLD, autoritativos o reenviadores) hasta conseguir la IP exacta, devolverla al cliente y guardarla en caché durante el tiempo que marque el TTL (_Time To Live_).

#### ¿Podemos utilizar la misma dirección IP de red en la nueva sucursal (`192.168.1.0/24`) y en la red de la empresa que ya tenemos configurada?

* En la realidad y en enrutamiento IP estándar (como RIP en Cisco Packet Tracer): No es recomendable ni funciona de forma transparente si dos redes interconectadas mediante routers con tablas de rutas comparten el mismo prefijo.
* Motivo: Si dos redes LAN conectadas a un mismo entorno enrutado usan exactamente el mismo prefijo (por ejemplo `192.168.1.0/24`), los routers no pueden saber con claridad hacia qué sucursal mandar un paquete dirigido a `192.168.1.x`, generando ambigüedad de rutas y conflictos de encaminamiento.
* Qué hago en la práctica: En mi red actual la empresa ya usa `192.168.3.0/24`, y en general lo correcto es asignar subredes distintas a cada sede (por ejemplo `192.168.1.0/24` para una sucursal y `192.168.2.0/24` o `192.168.3.0/24` para otra). Si en un caso real existieran redes solapadas que no se pudieran cambiar, tendría que recurrir a soluciones más complejas como NAT/PAT o túneles/VPN con traducción de direcciones, algo que prefiero evitar diseñando bien las subredes desde el inicio.



### Preguntas sobre puertos lógicos

#### ¿Cómo se clasifican dichos puertos y por qué (según su uso)?

Según la IANA (_Internet Assigned Numbers Authority_), los puertos TCP/UDP (del `0` al `65535`) se clasifican en tres rangos según su uso habitual:

* Puertos bien conocidos (_Well-Known Ports_, `0–1023`): Reservados para servicios y protocolos estándar del sistema y de red muy extendidos (como HTTP, FTP, SSH, DNS, SMTP, POP3, IMAP, NTP).
* Puertos registrados (_Registered Ports_, `1024–49151`): Asignados a aplicaciones, software o servicios específicos de fabricantes u organizaciones (como MySQL o VNC).
* Puertos dinámicos o efímeros (_Dynamic / Private Ports_, `49152–65535`): Utilizados temporalmente por los sistemas operativos y clientes para abrir conexiones salientes hacia los puertos de destino.

#### Puertos y función de cada servicio pedido

* FTP:
  * Puerto: `20 / 21`
  * Función: Transferencia de ficheros (`20` para datos y `21` para control), sin cifrar.
  * Protocolo: TCP
* SSH:
  * Puerto: `22`
  * Función: _Shell_ remota segura y transferencia cifrada de ficheros.
  * Protocolo: TCP
* DNS:
  * Puerto: `53`
  * Función: Resolución de nombres de dominio; UDP para consultas habituales y TCP para transferencias de zona o respuestas grandes.
  * Protocolo: UDP y TCP
* HTML / HTTP:
  * Puerto: `80 / 443`
  * Función: `80` para tráfico web HTTP sin cifrar y `443` para tráfico web HTTPS cifrado con TLS/SSL (sobre los que se sirve contenido HTML).
  * Protocolo: TCP
* MySQL:
  * Puerto: `3306 / 3307`
  * Función: Conexiones de clientes y aplicaciones a bases de datos MySQL.
  * Protocolo: TCP
* Portainer:
  * Puerto: `9443 / 9000`
  * Función: Gestión de contenedores (como Docker) mediante interfaz web/HTTPS.
  * Protocolo: TCP
* SMTP:
  * Puerto: `25 / 465 / 587`
  * Función: Envío y retransmisión de correo electrónico (`25` entre servidores / relevo tradicional, `465` SMTPS con SSL/TLS y `587` _submission_ desde cliente a servidor).
  * Protocolo: TCP
* POP3:
  * Puerto: `110 / 995`
  * Función: Recepción y descarga de correo (`110` sin cifrar y `995` POP3S con SSL/TLS; por defecto suele descargar y eliminar del servidor).
  * Protocolo: TCP
* IMAP:
  * Puerto: `143 / 993`
  * Función: Recepción de correo con sincronización manteniendo los mensajes en el servidor (`143` sin cifrar y `993` IMAPS con SSL/TLS).
  * Protocolo: TCP
* DHCP:
  * Puerto: `67 / 68`
  * Función: Asignación automática de parámetros de red (`67` para el servidor y `68` para los clientes).
  * Protocolo: UDP
* VNC:
  * Puerto: `5900 / 5901 / ...`
  * Función: Control remoto de la interfaz gráfica (escritorio) transmitiendo eventos de teclado, ratón y pantalla.
  * Protocolo: TCP
* LDAP:
  * Puerto: `389 / 636`
  * Función: Consulta y gestión de servicios de directorio (`389` LDAP y `636` LDAPS cifrado con TLS/SSL).
  * Protocolo: TCP
* OpenVPN:
  * Puerto: `1194`
  * Función: Creación de túneles VPN cifrados punto a punto o de sitio a sitio para conectar redes o usuarios remotos de forma segura.
  * Protocolo: UDP / TCP
* WireGuard:
  * Puerto: `51820`
  * Función: Establecimiento de túneles VPN cifrados modernos de alto rendimiento y baja latencia.
  * Protocolo: UDP
* NTP:
  * Puerto: `123`
  * Función: Sincronización horaria entre equipos y servidores de la red.
  * Protocolo: UDP



### Investigación

#### Configuración del ISP: uso del servicio FTP y conexión desde un equipo de la empresa al servidor del ISP

* Uso del servicio FTP: Utilizo el protocolo FTP (_File Transfer Protocol_) para subir, descargar, listar, renombrar o borrar archivos entre un cliente y un servidor a través de la red.
*   Procedimiento desde un equipo de la empresa hacia `Server0` (Paco):

    1. Compruebo que `Server0` tiene su IP configurada (`70.0.0.2` con _Default Gateway_ `70.0.0.1` en `ChatGPT`), es alcanzable desde el PC de la empresa (`192.168.3.0/24`) y tiene el servicio FTP activado (`On`) con usuario y contraseña creados.
    2. Abro en el PC la pestaña Desktop > Command Prompt.
    3. Ejecuto `ftp 70.0.0.2`.
    4. Escribo el Username y el Password cuando me los pide.
    5. Pruebo comandos como `dir` o `ls` para listar archivos, `get <archivo>` para descargar, `put <archivo>` para subir y `quit` para salir de la sesión.



#### Configuración extra (ISP): cambios para que el servidor dé IP por DHCP a dos PCs en `30.0.0.0/8`

1. IP estática y puerta de enlace en el servidor: Configuro en `Server0` (conectado a través del switch `Raul_Asencio` y el router `ChatGPT` cuya interfaz `Gig 0/1` tiene `30.0.0.1`) una IP estática `30.0.0.2` en su interfaz hacia esa red, máscara `255.0.0.0` y puerta de enlace `30.0.0.1` (manteniendo `70.0.0.2` en su interfaz hacia `70.0.0.0/8` y anunciando `30.0.0.0` en RIP en `ChatGPT`).
2. Activar y configurar el servicio DHCP en el servidor: Entro en Services > DHCP, pongo el servicio en On y configuro el _pool_ para `30.0.0.0/8` con:
   * Default Gateway: `30.0.0.1`.
   * DNS Server: `8.8.8.8`.
   * Start IP Address: `30.0.0.10` (una IP libre fuera de la del router y la del servidor).
   * Subnet Mask: `255.0.0.0`.
   * Maximum Number of Users: al menos `2` (por ejemplo `20`) y pulso Add / Save.
3. Configurar los dos PCs como clientes DHCP: En `Alejandro_Grimaldo` y `Fermin_Lopez` (conectados al switch `Raul_Asencio`), entro en Desktop > IP Configuration y marco DHCP para comprobar que reciben IP dentro de `30.0.0.0/8` (`30.0.0.10` y `30.0.0.20` o las asignadas), máscara `255.0.0.0`, gateway `30.0.0.1` y DNS `8.8.8.8`.

### Bibliografía

Enunciado de la práctica `M370T2A3 — Cisco Packet Tracer` (Módulo `0370 — Redes`, ciclo ASIX)&#x20;

{% embed url="https://punkymo.gitbook.io/miwiki/redes/cisco/acceso-y-password" %}



IANA — Service Name and Transport Protocol Port Number:

{% embed url="https://www.iana.org/assignments/service-names-port-numbers" %}



{% embed url="https://es.scribd.com/document/69979614/Listado-de-Puertos" %}



{% embed url="https://oposergas.com/info/puertos-tcp-udp-mas-preguntados" %}



{% embed url="https://ideaweb.es/puertos-servidores/" %}
