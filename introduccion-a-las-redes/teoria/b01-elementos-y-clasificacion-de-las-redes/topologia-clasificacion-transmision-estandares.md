---
icon: standard-definition
---

# Topología-clasificación-transmisión-estándares

<figure><img src="../../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>



## Arquitectura de la red

Especifica la forma en que los dispositivos se envían los datos de unos a otros sin tener en\
cuenta cómo están dispuestos los medios físicos por los que se transmite la información.

<figure><img src="../../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

Topología: Organización&#x20;del cableado

Método de&#x20;acceso: Medios guiados (cable de&#x20;par trenzado, coaxial o de&#x20;fibra óptica)\
Medios no guiados (red&#x20;inalámbrica por infrarrojos,&#x20;radio, microondas, etc.)

Protocolos de comunicación: Las reglas&#x20;utilizadas&#x20;para llevar a&#x20;cabo la&#x20;comunicación



## Topología de red

Mapa que representa el diseño de red que&#x20;queremos representar. Se utilizan dos tipos de&#x20;diagramas\
Diagrama de topología física&#x20;brinda información sobre cómo y dónde&#x20;están ubicados y conectados nuestros&#x20;equipos de red, tanto los dispositivos&#x20;finales, como los intermedios\
Diagrama de la topología lógica&#x20;muestra las direcciones de red de los&#x20;equipos, los servicios que proporciona,&#x20;etc.



## Topología física

Proporciona información que nos permita:\
Ubicar nuestro&#x20;equipo en las&#x20;instalaciones de&#x20;la empresa; por&#x20;ejemplo, en qué&#x20;planta y en qué&#x20;sala se encuentra&#x20;el dispositivo.\
A qué puntos de&#x20;conexión del&#x20;cableado de&#x20;nuestro edificio se&#x20;ha conectado.\
Qué puertos del&#x20;dispositivo está&#x20;utilizando para&#x20;cada conexión y&#x20;qué elemento hay&#x20;conectado en el&#x20;otro extremo de la&#x20;conexión.\
Qué tipo de&#x20;medio se está&#x20;utilizando.\
De utilidad a la&#x20;hora de realizar&#x20;cambios en la&#x20;topología de red.

<figure><img src="../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

Este tipo de mapa debe indicar:\
Qué direcciones&#x20;de red tiene&#x20;cada equipo.\
En qué&#x20;segmento de red&#x20;se conecta el&#x20;equipo.\
Con qué&#x20;equipos tiene&#x20;conexión directa&#x20;(tanto equipos&#x20;finales como&#x20;intermedios) y&#x20;mediante qué&#x20;tecnología (no&#x20;nos importará la&#x20;conexión física&#x20;que utilice).\
Qué servicios&#x20;proporciona ese&#x20;equipo.\
Cómo fluye la&#x20;información en&#x20;los equipos&#x20;intermedios; por&#x20;ejemplo, si&#x20;tenemos un&#x20;firewall, qué&#x20;tráficos autoriza&#x20;y qué tráficos&#x20;bloquea.\
Es importante&#x20;poder disponer&#x20;tanto del mapa&#x20;de la topología&#x20;física como del&#x20;de la topología&#x20;lógica.

<figure><img src="../../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

### Topología - BUS

Los dispositivos se conectan en cadena,&#x20;uno tras otro, formando una misma línea&#x20;de cable de interconexión entre todos&#x20;los dispositivos de esa red.\
En algunas ocasiones, son cables&#x20;cortos que conectan el equipo A con el&#x20;B, el B con el C, el C con el D, etc.,&#x20;formando así una misma conexión entre&#x20;todos los dispositivos como si de un&#x20;solo cable se tratase.\
Esta topología de red, aunque&#x20;desfasada al día de hoy para&#x20;interconectar equipos finales, se sigue&#x20;viendo en la interconexión de ciertos&#x20;dispositivos intermedios.

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>



### Topología - ANILLO

Es similar a una topología de&#x20;bus en la que interconectamos&#x20;los dos extremos formando un&#x20;anillo en el cableado.\
Este tipo de redes era muy&#x20;utilizado por algunas&#x20;tecnologías como las redes de&#x20;anillo de IBM que se utilizaban&#x20;en los años 70 y 80,\
Hoy día se ha relegado su uso&#x20;a otros propósitos, como la&#x20;interconexión de campus de&#x20;empresa en redes de anillo&#x20;de fibra óptica de alto&#x20;rendimiento.

<figure><img src="../../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>



### Topología - ESTRELLA

Las más utilizadas hoy día en redes medianas. En este tipo de topologías se&#x20;interconecta una serie de dispositivos (generalmente dispositivos finales) a algún&#x20;tipo de concentrador como puede ser un switch (conmutador) de red.\
Tienen la ventaja de la simplicidad en la instalación y la reducción de costes, y el&#x20;problema de que si cae el nodo central al que se conectan todos, toda la red de esa&#x20;estrella caerá.\
En entornos de empresa más grandes, podemos encontrar una variación de las&#x20;redes de estrella: las conocidas como estrellas extendidas. En una estrella&#x20;extendida, el nodo central será un equipo intermedio, generalmente un switch LAN&#x20;que se conectará en una estrella a otros switches LAN, a los que se conectarán los&#x20;equipos finales.

<figure><img src="../../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>



### Topología - MALLA

Es una variante de la topología de estrella que permite la interconexión creando conexiones redundadas. En ella, un nodo no tiene que conectarse únicamente a un concentrador, sino que puede hacerlo a más de uno. Esta topología puede ser:

* de malla completa si todos los nodos (los concentradores) se conectan con todos los nodos
* de malla parcial si los concentradores se conectan con otros concentradores, pero no con todos los concentradores de la topología. De esta manera, se simplifica el diseño, se abaratan los costes y se proporciona un nivel de tolerancia ante fallos de red que puede ser aceptable para la organización.

<figure><img src="../../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>



## Clasificación de las redes

Propiedad privada\
Conecta enlaces de una única oficina,&#x20;edificio o campus\
Tamaño limitado a varios Km\
Compartición de recursos (hardware,&#x20;software, datos)\
Topología: bus, anillo, estrella

<figure><img src="../../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

Propiedad pública o privada

Conecta enlaces dentro de una ciudad

Red única (TV cable) o formada por la interconexión de múltiples LAN

<figure><img src="../../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

Propiedad pública o privada\
Transmisión de datos a larga distancia (voz, vídeo,&#x20;imágenes, multimedia)\
Grandes áreas geográficas

<figure><img src="../../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

La difusión o broadcast\
Transmisión de información de un nodo&#x20;emisor a una multitud de nodos receptores&#x20;de manera simultánea.\
Útil en caso de:

*  Cuando el nodo emisor no conoce cual es el nodo destinatario como el  &#x20;descubrimiento automático de servicios en una red.
* Cuando el nodo emisor necesita enviar la misma información a múltiples  &#x20;receptores.
* Es el caso de la videoconferencia y el streaming.

<figure><img src="../../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

### REDES PUNTO A PUNTO & CONMUTACIÓN

Equipos que se conectan directamente a través de una&#x20;línea de transmisión.\
Muy sencillas, pero de coste elevado.\
Pueden utilizarse en:\
Pequeñas redes de telefonía&#x20;privadas\
Sistemas en los que es&#x20;imprescindible que no falle la&#x20;comunicación\
Poco prácticas

<figure><img src="../../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

### Clasificación de las redes REDES DE CONMUTACIÓN

<figure><img src="../../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

Conexión a través de nodos de conmutación.\
⚫ Todos los nodos desempeñan tareas relacionadas con el control de flujo, control&#x20;de la congestión y encaminamiento.\
⚫ No todos los nodos se conectan entre sí.\
⚫ No tiene por qué existir un enlace directo entre cada par de nodos, pero si algún&#x20;camino entre ellos.\
⚫ Los nodos no se preocupan del contenido de lo que han de encaminar, sólo se&#x20;preocupan de dar un servicio, de que la información se transmita correctamente, no&#x20;de su interpretación.

### Clasificación de las redes CONMUTACIÓN DE CIRCUITOS

Establecimiento del circuito\
⚫ Antes de transmitir una señal, se debe establecer un circuito extremo a extremo&#x20;desde el origen al destino, pasando por todos los nodos intermedios.\
⚫ Sirve para reservar todos los recursos necesarios para la comunicación,&#x20;durante la duración de la misma.\
⚫ Transferencia de información\
⚫ Una vez se ha establecido el circuito, la información se puede transmitir, sin sufrir&#x20;retardos entre los nodos.\
⚫ Desconexión\
⚫ Durante esta última fase se liberan todos los recursos reservados para la conexión.\
⚫ El camino debe estar disponible durante toda la comunicación y se desactiva una vez&#x20;finalizada ésta.

Poco eficiente: la capacidad del canal se reserva&#x20;permanentemente durante toda la duración de la\
conexión.\
• Sistema resulta poco flexible, ya que se debe&#x20;transmitir de forma continua y a una velocidad&#x20;constante.\
• La comunicación sufre un retardo mientras se&#x20;establece el circuito.\
• El retardo introducido por cada nodo del camino, en&#x20;la fase de transferencia se considera despreciable.\
• No existen mecanismos de control de flujo. Los&#x20;equipos origen y destino deben transmitir a la misma&#x20;velocidad.

Transparencia, ya que, una vez que&#x20;el circuito se ha establecido, la red se&#x20;comporta como si fuese una conexión&#x20;directa entre los dos extremos.

## Clasificación de las redes - resumen

REDES DE&#x20;DIFUSIÓN:&#x20;Un único canal de comunicaciones.&#x20;Necesario mecanismo de control de acceso al medio.&#x20;Decisión de si la información es de interés o no\
REDES DE&#x20;CONMUTACIÓN:&#x20;Conexión a través de nodos de conmutación. Nodos de conmutación (control de flujo, control de la&#x20;congestión y encaminamiento): tránsito o periféricos

## Internet

Internet es una red por la que podemos interconectar otras redes con un&#x20;ámbito global.\
• Entre los servicios que encontramos están:\
• las páginas web,\
• el correo electrónico,\
• la mensajería instantánea.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Cuando hablamos de las conexiones de red desde Internet en una empresa, podemos&#x20;diferenciar tres tipos de redes:\
intranet&#x20;o extranet&#x20;o Internet\
Y aunque los nombres son parecidos, deberemos diferenciarlospor su modo de acceso.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Red privada de una&#x20;empresa, a la que solo&#x20;pueden acceder los&#x20;usuarios de la propia&#x20;empresa.\
Muchas veces, el acceso&#x20;a esta red se hace a&#x20;través de Internet\
El usuario puede&#x20;encontrarse a miles&#x20;de kilómetros de la&#x20;empresa y aun así se&#x20;conectarse como si\
estuviese en la&#x20;oficina.

100% pública y&#x20;abierta para todo el&#x20;mundo.

En muchos casos, para&#x20;poder acceder a ese&#x20;servicio público, debemos&#x20;validar con un usuario y&#x20;contraseña para poder&#x20;acceder a la información&#x20;de interés.

Si algo se publica en&#x20;Internet, técnicamente&#x20;cualquier usuario o&#x20;equipo conectado a&#x20;Internet podría tener&#x20;acceso a este recurso.

No quiere decir que&#x20;podamos acceder a&#x20;toda la información&#x20;publicada en el&#x20;servidor aunque&#x20;hayamos accedido a&#x20;ese recurso.

## Extranet

Por ejemplo

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## Protocolos

un emisor que crea el mensaje – (equipo emisor)

un receptor que recibe e interpreta el mensaje tal como lo ha enviado el emisor - (equipo receptor)

un medio por el que se propaga el mensaje – cable de cobre, fibra óptica o radiofrecuencia.&#x20;

En la comunicación entre dos personas se necesitan tres componentes

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

¿Qué ocurre si no hablan el mismo idioma?

Se necesita además, que ambos hablen el mismo idioma.\
De no ser así, es necesario un intérprete que les sirva de intermediario.

En el mundo de las comunicaciones informáticas, el mecanismo es exactamente igual.\
También hará falta un idioma común. Es más, harán falta varios idiomas comunes para que\
los dos equipos puedan comunicarse.

<figure><img src="../../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

## Establecimiento de la comunicación

Entre dos personas, se hace necesario establecer unos ¿Qué necesitamos?

1. Identificar quién es el emisor y quién es el receptor. Si un emisor envía el mensaje, pero el receptor no sabe que está hablando con él, el mensaje no será interpretado.
2. Un lenguaje común en ambas partes. Si nos llega un mensaje, pero no entendemos qué nos están diciendo, la comunicación no será válida.
3. Velocidad de emisión y tiempos de entrega. Si alguien habla muy rápido, podemos no entender el mensaje, aunque hablemos el mismo idioma. Lo mismo pasa si el tiempo de entrega no es el adecuado.
4. Confirmación de la entrega del mensaje. Imaginemos una comunicación en la que el emisor está hablando durante un largo período de tiempo. El receptor solo tiene que escuchar, pero para mostrar que sigue escuchando y que está recibiendo correctamente la información, podría enviar algún tipo de acuse de recibo con respuestas tan simples como: “sí”, “claro”, “entiendo” …

En la red, si queremos establecer una comunicación entre dos equipos informáticos, debemos utilizar las&#x20;normas de comunicación definidas en los protocolos de red que se utilizan.

<figure><img src="../../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

## Un protocolo de red debe definir

Codificación del mensaje: cuando enviamos un texto o una imagen, el equipo solo puede utilizar&#x20;ceros y unos para codificar la información.\
Formateado y encapsulación del mensaje: según el protocolo utilizado, los datos se estructurarán de\
modo que determinen la información necesaria para que el protocolo pueda procesarla.\
Definición del tamaño del mensaje: ha de tener un tamaño predefinido, tanto en tamaño máximo\
como en mínimo.\
Tiempos de entrega de los mensajes: la latencia que puede soportar la entrega de un mensaje es\
vital para que la comunicación sea viable.\
Así como, Opciones de entrega de los mensajes: un mensaje puede incluir información para el control de su&#x20;entrega.\
Ejemplo\
un acuse de recibo garantiza la entrega.\
un control de validación del mensaje muestra que el mensaje no se ha corrompido en tránsito; y\
un mensaje de apertura o de cierre puede permitir que una comunicación se establezca o se dé&#x20;por cerrada entre ambas partes de la comunicación.

## Tipos de comunicación

Debemos diferenciar varios tipos de comunicaciones:

* Unicast: la comunicación es de uno a uno. Un equipo habla y otro equipo escucha.
* Multicast: la comunicación es de uno a muchos. Un equipo habla, y todos aquellos que se hayan asociado al grupo de multicast escucharán la comunicación. El resto de los equipos no lo escucharán o, si lo escuchan, ignorarán el mensaje.
* Broadcast: un equipo habla y todos los equipos de esa red escuchan. Este tipo de comunicación resulta muy útil cuando se quiere localizar cierta información que, de antemano, no se sabe quién tiene.

## Protocolo de red

<figure><img src="../../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

Debe tener una o varias funciones que permitan:

* Controlar el direccionamiento de quién envía y a quién va dirigido el mensaje.
* Proporcionar algún mecanismo que garantice la entrega del mensaje.
* Segmentar la información para simplificar el envío si es necesario y secuenciarla para poder reensamblarla al llegar al destino.
* Controlar el flujo de envío del mensaje.
* Detectar posibles errores durante el envío.
* Presentar algún tipo de interfaz para que el usuario o un servicio pueda interactuar con el protocolo.

Los protocolos de red se especializan&#x20;en determinadas funciones dentro de&#x20;la comunicación, pero no controlan&#x20;todo el proceso de envío

* Web: HTTP
* Correo: POP, STMP, IMAP
* Resolución de nombres: DNS, WINS
* Acceso remoto: TELNET, SSH, RDP
* Enrutamiento: RIP, OSPF, BGP
* Descargas de archivos: FTP, TFTP, SCP

Cuando hablamos del protocolo TCP y del protocolo IP,&#x20;estamos haciendo referencia a dos protocolos diferentes,&#x20;que tienen sus propias funciones.\
Cuando decimos protocolo TCP/IP, aunque no está del&#x20;todo bien, hacemos referencia a la familia de protocolos&#x20;que trabajan conjuntamente según unas reglas&#x20;comunes.

## NORMALIZACIÓN Y ORGANISMOS

### Una mirada atrás

1. 1969 – ARPANET – Las primeras redes, comerciales y militares, utilizaban sus   &#x20;propios protocolos. Por ejemplo, IBM utilizaban protocolos diferentes para sus   &#x20;productos
2. Las empresas mantenían redes de diferentes fabricantes y los problemas llegaron   &#x20;cuando necesitaron comunicar esas redes entre sí.
3. Incompatibilidades en los sistemas de transmisión
4. En ocasiones había que deshacerse de todo lo instalado y montar redes nuevas
5. En otras había que desarrollar adaptadores de red   . Alternativas muy costosas en cualquier caso. Se hizo necesario definir un conjunto común de normas que permitiera coordinar a   &#x20;todos los fabricantes.

### Estándares

¿Qué es un estándar? Descripción de normas que&#x20;deben seguirse para que todo&#x20;funcione adecuadamente

De facto: A este grupo pertenecen los estándares que aparecieron y se impusieron en el&#x20;mercado por su extensa utilización.\
Ejemplos:\
a) El ordenador personal PC de IBM y sus sucesores son normas de facto porque la&#x20;mayoría de fabricantes copiaron los equipos de IBM con mucha exactitud.\
a) UNIX es un sistema operativo convertido en un estándar al ser copiado por SCO,&#x20;Minix, Linux, etc

De jure:  Estándares formales y legales acordado por algún organismo de estandarización\
autorizado. Los hay de dos tipos:

1. Creados por tratados entre varios países
2. Organizaciones voluntarias

## Normas y estándares de red

Las encargadas de regular el desarrollo de las redes y conseguir la estandarización de los componentes y los protocolos son una serie de organizaciones internacionales. Algunas de las organizaciones de estándares abiertos que regulan los componentes de las redes son:

* International Organization for Standardization (ISO).
* Internet Engineering Task Force (IETF).
* Instituto de Ingenieros en Electricidad y Electrónica (IEEE).
* Internet Society (ISOC).
* Internet Architecture Board (IAB).

Otros organismos de estandarización que también veremos durante el uso de las redes son:

* Electronic Industries Alliance (EIA).
* Telecommunications Industry Association (TIA).
* Internet Corporation for Assigned Names and Numbers (ICANN).
* Internet Assigned Numbers Authority (IANA).
* Sector de Normalización de las Telecomunicaciones de la Unión Internacional de Telecomunicaciones (UIT-T).

### ITU International Telecom Union

Organización de las Naciones Unidas con sede en Ginebra.&#x20;

Constituida por las autoridades de Correos, Telégrafos y Teléfonos (PTT) de los países miembros. Realiza recomendaciones técnicas sobre teléfono, telégrafo e interfaces de comunicación de datos que se reconocen como estándares muy a menudo.&#x20;

Trabaja en colaboración con ISO (miembro de ITU actualmente) Sectores principales ITU-R radiocomunicaciones ITU-D desarrollo ITU-T telecomunicaciones

### ISO International Standards Organization

De carácter voluntario.&#x20;

Agrupa a 89 países.&#x20;

Sus miembros han desarrollado estándares para las naciones participantes.&#x20;

Uno de sus comités se ocupa de los sistemas de información desarrollando el modelo de referencia OSI así como protocolos para varios de sus niveles. Han desarrollado estándares en otros campos:

1. El estándar ISP 216 para medidas de papel como el A4
2. ISO 9000 sistemas de gestión de calidad
3. ISO 3166 – código de países

### ANSI – American National Standards Institute

Asociación con fines no lucrativos, formada por fabricantes, usuarios, compañías que ofrecen servicios públicos de comunicaciones. Es el representante americano de ISO, que adopta frecuentemente los estándares ANSI como normas internacionales.

### IEEE Institute of Electrical and Electronics Engineers

La mayor organización internacional sin ánimo de lucro formada por profesionales de las nuevas tecnologías.&#x20;

Publican revistas y realizan conferencias donde se publican investigaciones.&#x20;

Elaboran estándares en áreas de ingeniería eléctrica y computación.

Por ejemplo: a. IEEE 802 para redes de área local b. POSIX para sistemas operativos

### IETF Internet Engineering Task Force

Organización creada en EUA en 1986 para desarrollar los estándares que funcionan en Internet. Formada por técnicos y especialista que publican las recomendaciones de los protocolos de Internet, haciendo que los fabricantes se adapten a ellas para evitar problemas de compatibilidad y funcionamiento entre sistemas.

Los documentos que publican se denominan RFC (Request For Comments) y son la base para el desarrollo de todas las tecnologías que funcionan en Internet

Estos documentos publicados desde 1969, llegan a ser más de 5000 en la actualidad. Por ejemplo:

1. RFC 2616 (HTTP)
2. RFC 959 (FTP)
3. RFC 854 (TELNET)

### RFC - Request For Comments

Documentos publicados por la comunidad técnica que se utilizan para desarrollar estándares y protocolos relacionados con Internet y las redes de ordenadores.

Parte fundamental en la creación y evolución de las tecnologías de Internet.

Se utilizan para describir especificaciones técnicas, protocolos, procedimientos y pautas relacionadas con una amplia variedad de aspectos de la informática y las comunicaciones en línea. Actualizados y revisados a medida que las tecnologías evolucionan. Cuando se requieren cambios en un protocolo o especificación existente, se publica un nuevo RFC que describe los cambios propuestos.

Se utilizan para documentar aspectos técnicos, investigaciones y mejores prácticas relacionadas con Internet y la informática en general. Esto puede incluir descripciones detalladas de protocolos, algoritmos, consideraciones de seguridad y más.

RFC 2616 (HTTP)\
RFC 959 (FTP)\
RFC 854\
(TELNET)

### ISC Internet Systems Consortium

Sin ánimo de lucro fundada en 1994. Desarrolla y da soporte a determinadas herramientas que funcionan en Internet y que se utilizan como referencia. Por ejemplo:

1. BIND
2. DHCP
3. NTP

Todo el software que se desarrolla por el ISC se distribuye bajo licencia ISC, muy parecida a la usada por el MIT para distribuir la OpenSBD.

### ICANN Internet Corporation for Assigned Names and&#xD; Numbers

Organización sin ánimo de lucro. Creada en 1998. Asume las tareas de anterior IANA (Agencia de Asignación de Números de Internet). Mantiene un registro central de números asociados con los protocolos de Internet, además de los nombres de dominios y direcciones.

### W3C World Wide Web Consortium

Apareció en 1994. Presidido por Tim Berners-Lee. Produce estándares para todas las tecnologías que engloba a la WWW. Integrado por ás de 400 miembros y unos 69 investigadores. Dispone de oficinas regionales en varios países. Publica documentos oficiales denominados Recomendaciones del Consorcio que contienen los nuevos estándares y publicados de forma libre para que los fabricantes y desarrolladores puedan adaptarse a ellos Ejemplos:

1. HTML, CSS, DOM, XML

## Open Group

Ofrece estándares abiertos y neutrales para la industria informática. Sus miembros incluyen empresas, organismos e instituciones gubernamentales como HP, IBM, el departamento de Defensa de EUA, etc Ejemplo:

1. Estándar Single Unix Specification que certifica los productos de tipo Unix
