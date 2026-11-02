# Interesante saber esto

## Codificar los mensajes

### Como codificar el mensaje en informática?

Codificar un mensaje en informática significa **transformar la información de un formato legible** (texto, audio o imagen) **a un formato que una computadora pueda procesar, almacenar o transmitir**, como señales eléctricas, impulsos de luz o números binarios (ceros y unos).

Dependiendo del objetivo, la codificación se divide en varios tipos principales:

1\. Codificación de caracteres (Texto a Binario)Convierte letras, números y símbolos en bytes y bits utilizando estándares universales:

* **ASCII:** Usa 7 u 8 bits para representar 128 o 255 caracteres básicos (letras sin tilde, números y símbolos).
* **Unicode / UTF-8:** El estándar actual que permite representar más de un millón de caracteres, incluyendo tildes, eñes, emojis y alfabetos de todo el mundo

2\. Codificación de datos multimedia. Los archivos complejos se comprimen y traducen a estructuras numéricas específicas:

* **Imágenes:** Formatos como JPEG o PNG que mapean los colores y píxeles en matrices de datos.
* **Audio y Video:** Formatos como MP3 o MP4 que transforman ondas sonoras y fotogramas en flujos de datos comprimidos.

3\. Cifrado y Encriptación (Seguridad)Si lo que buscas es **ocultar el contenido** del mensaje para que solo un receptor autorizado lo entienda, se aplican algoritmos criptográficos:

* **Cifrado Simétrico:** Se usa una sola clave secreta para codificar y decodificar el mensaje (ejemplo: AES).
* **Cifrado Asimétrico:** Se usan dos claves diferentes, una pública para cifrar y una privada para descifrar (ejemplo: RSA, usado en navegación web segura HTTPS).
* **Métodos clásicos de sustitución:** Como el _Cifrado César_ (desplazamiento de letras) o la conversión directa a código binario (0 y 1).&#x20;



## ISO

### Cuando surge el modelo OSI y porque?

El **modelo OSI** (Open Systems Interconnection) fue desarrollado por la [Organización Internacional de Normalización (ISO)](https://aws.amazon.com/es/what-is/osi-model/) a finales de la década de 1970 y se publicó oficialmente como estándar en **1984.**

¿Por qué surgió?

* **Incompatibilidad de redes:** En los años 70 y principios de los 80, cada fabricante de tecnología creaba sus propias arquitecturas, protocolos y sistemas de red cerrados (como SNA de IBM).
* **Falta de interoperabilidad:** Los equipos y el software de una marca no podían comunicarse con los de otra; las redes funcionaban como "islas" aisladas.
* **Necesidad de un estándar:** Se requería un marco de referencia universal y neutral que separara las funciones de comunicación en capas lógicas para que cualquier fabricante pudiera diseñar sistemas compatibles entre sí.

### Historia de ISO

La **Organización Internacional de Normalización** (ISO, por sus siglas en inglés) nació oficialmente el **23 de febrero de 1947** en Ginebra, Suiza, con el objetivo de unificar criterios industriales y facilitar el comercio global. Su nombre no es una sigla, sino que proviene del término griego _**isos**_, que significa «igual».

Antecedentes y origen:

* **1926 (ISA):** Se fundó en Praga y Nueva York la **Federación Internacional de Asociaciones de Estandarización Nacionales (ISA)**, centrada principalmente en la industria de Europa continental.
* **1939–1942:** Las actividades de la ISA quedaron suspendidas debido a la **Segunda Guerra Mundial**.
* **1944 (UNSCC):** Se creó el **Comité Coordinador de Estándares de las Naciones Unidas (UNSCC)** para coordinar normas entre los países aliados.
* **Octubre de 1946:** Delegados de la ISA y del UNSCC (65 representantes de **25 países**) se reunieron en Londres y acordaron unificar esfuerzos para crear una nueva organización global.

Principales hitos históricos:

* **1947:** Inicio oficial de operaciones el **23 de febrero**, con sede en Ginebra.
* **1951:** Se publica la primera norma oficial de la organización: la **ISO/R 1:1951** (referida a la temperatura de referencia para mediciones industriales).
* **1969:** Olle Sturen asume como secretario general e impulsa el fin del «nacionalismo técnico».
* **1987:** Se publica la primera edición de la famosa serie **ISO 9000** de gestión de la calidad, marcando el inicio masivo de las certificaciones empresariales.
* **Actualidad:** La organización agrupa a representantes de más de **160 países** y ha desarrollado decenas de miles de normas en áreas como calidad (**ISO 9001**), medio ambiente (**ISO 14001**) o seguridad de la información (**ISO 27001**).

### Las capas del modelo osi&#x20;

<figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

El **Modelo OSI** (Interconexión de Sistemas Abiertos) es un marco conceptual de 7 capas desarrollado por la ISO en 1984 para estandarizar las comunicaciones de red. Divide el proceso de transmisión de datos en niveles ordenados, desde el hardware físico hasta las aplicaciones del usuario.

Las 7 capas del Modelo OSI

**Capa 7: Aplicación**

* Es la más cercana al usuario final.
* Proporciona servicios de red y permite que las aplicaciones interactúen con el sistema.
* _Ejemplos de protocolos:_ HTTP, HTTPS, FTP, SMTP.

**Capa 6: Presentación**

* Traduce, codifica, comprime y cifra los datos para que la capa de aplicación pueda leerlos.
* Asegura que la información enviada sea compatible entre distintos sistemas.

**Capa 5: Sesión**

* Abre, mantiene, sincroniza y cierra las conexiones (sesiones) entre las aplicaciones de ambos extremos.
* Controla el intercambio de datos y los puntos de recuperación.

**Capa 4: Transporte**

* Gestiona la comunicación de extremo a extremo y divide los datos en **segmentos**.
* Controla la fiabilidad de la entrega.
* _Ejemplos de protocolos:_ TCP (confiable, orientado a conexión) y UDP (rápido, sin conexión).

**Capa 3: Red**

* Se encarga del enrutamiento de los **paquetes** y de determinar la mejor ruta a través de la red.
* Utiliza direcciones lógicas como las direcciones **IP**.
* _Dispositivos principales:_ Enrutadores (routers).

**Capa 2: Enlace de datos**

* Organiza los bits en **tramas** (frames) y gestiona el direccionamiento físico mediante direcciones **MAC**.
* Detecta y corrige errores ocurridos en el medio físico.
* _Subcapas:_ LLC y MAC.
* _Dispositivos principales:_ Conmutadores (switches) y puentes.

**Capa 1: Física**

* Es la base material del sistema. Transmite los **bits** crudos (ceros y unos) como señales eléctricas, pulsos de luz oradiofrecuencia.
* _Elementos:_ Cables de cobre, fibra óptica, tarjetas de red y antenas Wi-Fi.

### Dime ejemplos de appp en la capa osi herramientas

🗺️ Capa 7: Aplicación (Application)Es la capa con la que interactúas directamente. Las herramientas aquí son aplicaciones cliente o servidores que ejecutan los protocolos de red para transferir datos.

* **Navegadores Web (Chrome, Firefox, Edge):** Utilizan los protocolos **HTTP / HTTPS**.
* **Clientes de Correo (Outlook, Thunderbird):** Utilizan **SMTP, POP3, IMAP**.
* **Clientes de Transferencia de Archivos (FileZilla):** Utiliza **FTP / SFTP**.
* **Consolas de Administración Remota (PuTTY, OpenSSH):** Utilizan **SSH / Telnet**.
* **Herramientas de diagnóstico:** **Nslookup** o **Dig** (utilizan el protocolo **DNS**).

🎭 Capa 6: Presentación (Presentation)Se encarga de traducir, cifrar y comprimir los datos para que la capa de aplicación los entienda.

* **Herramientas de Cifrado y Seguridad:** **OpenSSL**, **GPG (GNU Privacy Guard)**. Manejan el cifrado de capas como **SSL / TLS**.
* **Formatos y Compresión:** Herramientas como **WinRAR** o **7-Zip** (compresión), o librerías que convierten formatos de imagen/video (como **FFmpeg**, JPEG, GIF, MP3).

🤝 Capa 5: Sesión (Session)Mantiene, abre y cierra la conversación (sesión) entre los dos extremos.

* **Herramientas de Escritorio Remoto y Bases de Datos:** **TeamViewer**, **AnyDesk** o clientes **SQL Server** (utilizan protocolos que gestionan y recuperan sesiones caídas).
* **Protocolos de autenticación y red:** Herramientas que gestionan **NetBIOS** (compartir archivos en Windows antiguo), **RPC** (Llamada a Procedimiento Remoto) o sesiones **SOCKS**.

🛄 Capa 4: Transporte (Transport)Se encarga de enviar los datos de manera confiable (TCP) o rápida (UDP).

* **Escáneres de Puertos:** **Nmap** (analiza si los puertos **TCP** o **UDP** de una máquina están abiertos o cerrados).
* **Herramientas de rendimiento de red:** **iPerf** (mide el ancho de banda máximo que soporta un enlace usando TCP o UDP).

🌐 Capa 3: Red (Network)Determina la mejor ruta física para enviar los datos (Direccionamiento IP y Enrutamiento).

* **Herramientas de Diagnóstico de Red (CLI):**
  * **Ping:** Prueba la conectividad básica usando el protocolo **ICMP**.
  * **Traceroute / Tracert:** Muestra la ruta exacta (los saltos de router) que toman los paquetes IP.
* **Sistemas Operativos de Routers:** **Cisco IOS**, **VyOS** o las interfaces de gestión de routers (revisan tablas de enrutamiento).

🔗 Capa 2: Enlace de Datos (Data Link)Se encarga del direccionamiento físico (Direcciones MAC) y de cómo los datos se colocan en el medio físico.

* **Analizadores de Paquetes / Sniffers:** **Wireshark** o **tcpdump**. Aunque capturan datos de todas las capas, son fundamentales aquí porque te permiten ver las tramas (Frames), las direcciones MAC y protocolos como **ARP** (que asocia IP con MAC) o **DHCP**.
* **Herramientas de gestión de Switches:** Consolas que gestionan protocolos como **STP** (Spanning Tree Protocol) o VLANs.

🔌 Capa 1: Física (Physical)Son los cables, conectores, tarjetas de red y las señales eléctricas u ópticas.

* **Herramientas de Hardware (Certificadores):** **Fluke Networks** (dispositivos físicos para probar si un cable Ethernet o de fibra óptica está dañado o tiene interferencia).
* **Herramientas de software Wi-Fi:** **InSSIDer** o **NetSpot** (analizan la potencia de las ondas de radio, canales y espectro electromagnético de las redes inalámbricas).
* Hab, bridge y 802.3



## Puertos

* 21 & 20 ⇒ FTP
  * Que es? El **Protocolo de Transferencia de Archivos** (_File Transfer Protocol_) es un estándar para subir y descargar archivos entre un cliente y un servidor a través de una red TCP. Utiliza el puerto **21** para el canal de control (comandos) y el puerto **20** para el canal de datos.
  * Como lo utilizamos? Se usa para administrar directorios y transferir grandes volúmenes de archivos (como subir el contenido de una página web a un hosting).
  * Ejemplos: Conectarse mediante un cliente gráfico como **FileZilla** a un servidor para subir una carpeta de imágenes. Usar comandos en la terminal (_ftp 192.168.1.10_) para descargar un archivo de configuración.
* 22 ⇒ SSH
  * Que es? El **Intérprete de Comandos Seguros** (_Secure Shell_) es un protocolo de administración remota que permite controlar equipos a distancia mediante una conexión completamente **cifrada**.
  * Como lo utilizamos? Se utiliza para iniciar sesión en servidores Linux, routers o dispositivos de red sin que las contraseñas viajen expuestas en la red.
  * Ejemplos: Escribir `ssh usuario@192.168.1.50` en la terminal para entrar a configurar un servidor VPS en la nube. Copiar un archivo de forma segura usando el comando `scp archivo.zip usuario@servidor:/ruta`.
* 23 ⇒ Telnet
  * Que es? Es un protocolo de comunicación que permite acceder a una máquina remota en modo texto. A diferencia de SSH, **no cifra los datos**, por lo que es considerado obsoleto e inseguro.
  * Como lo utilizamos? Antiguamente se usaba para gestionar equipos de red o servidores por línea de comandos; hoy en día desaconsejado por falta de seguridad.
  * Ejemplos: Ejecutar `telnet 192.168.1.1 23` para probar si un puerto o servicio responde en una IP local. Conectarse a un switch antiguo de red para modificar su configuración básica de fábrica.
* 25 ⇒ SMTP
  * Que es? El **Protocolo para la Transferencia Simple de Correo** (_Simple Mail Transfer Protocol_) es el estándar encargado de **enviar** correos electrónicos entre servidores de correo.
  * Como lo utilizamos? Los clientes de correo (como Outlook o Thunderbird) lo usan para entregar el mensaje al servidor de salida, y los servidores lo usan para reenviarlo al destinatario final.
  * Ejemplos: Configurar `://gmail.com` en el puerto 25 (o 587/465 con seguridad) para que una aplicación web pueda enviar correos de recuperación de contraseña. El envío de un mensaje desde el servidor de origen al servidor de correo del receptor.
* 80 ⇒ HTTP
  * Que es? El **Protocolo de Transferencia de Hipertexto** (_Hypertext Transfer Protocol_) es el protocolo base de la **World Wide Web** que permite la carga de páginas web sin cifrar.
  * Como lo utilizamos? El navegador web envía una petición al puerto 80 de un servidor web, el cual responde devolviendo el código HTML, imágenes y recursos de la página.
  * Ejemplos: Escribir `http://ejemplo.com` en el navegador para visualizar un sitio web que no utiliza certificado de seguridad (HTTPS). Una API básica que responde a solicitudes web (_GET_, _POST_) en texto plano.
* 53 ⇒ DNS
  * Que es? El **Sistema de Nombres de Dominio** (_Domain Name System_) es el directorio que **traduce los nombres de dominio** legibles (como `google.com`) a direcciones IP numéricas (como `142.250.x.x`). Funciona tanto en TCP como en UDP.
  * Como lo utilizamos? Trabaja en segundo plano cada vez que escribes una dirección web o usas un servicio de red para saber a qué máquina física hay que conectarse.
  * Ejemplos: Configurar `8.8.8.8` (el DNS público de Google) en los ajustes de red de tu ordenador. Ejecutar el comando `nslookup google.com` o `dig google.com` en la terminal para consultar la IP asociada a ese dominio.
*   67 & 68 ⇒ DHCP

    * Que es? El **Protocolo de Configuración Dinámica de Host** (_Dynamic Host Configuration Protocol_) asigna de forma automática los parámetros de red a los dispositivos que se conectan a ella. Utiliza el puerto **67** en el servidor y el puerto **68** en el cliente (UDP).
    * Como lo utilizamos? Permite que un aparato obtenga una dirección IP, máscara de subred y puerta de enlace sin que un administrador tenga que configurarlos de forma manual en cada equipo.
    * Ejemplos: Cuando enciendes tu móvil y te conectas al Wi-Fi de tu casa, el router (que actúa como servidor DHCP) le asigna por ejemplo la IP `192.168.1.15` de forma automática. Un ordenador portátil recién formateado que solicita una IP al conectar el cable de red (_Ethernet_).



## TCP/IP

<figure><img src="../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

1. Bien conocidos ⇒ 0-1023
2. Registringidos ⇒ 1024-49151
3. Dinámicas ⇒ 49152-65535
