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

pag: 20
