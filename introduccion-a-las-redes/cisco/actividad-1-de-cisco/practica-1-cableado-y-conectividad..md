---
icon: utility-pole-double
---

# Práctica 1 - Cableado y conectividad.

* ## Objetivo de la actividad:&#x20;

Investigamos la barra de herramientas inferior y dispositivos en un armario de Cableado. Conectamos dispositivos finales a dispositivos de red. Instalamos un router de respaldo. Configuramos un nombre de host. Exploramos el resto de la red.



* ## Qué se ha hecho:&#x20;

Recorrí la interfaz de navegación hasta la ubicación geográfica de la sucursal de Seward para visualizar su armario de telecomunicaciones. Examiné el contenido del rack y del tablero de cables, nos dirigimos al apartado lógico entonces podemos enlazar físicamente la <kbd>`PC_1`</kbd> al switch <kbd>`ALS2`</kbd> con un cable de cobre directo, instalé un router de respaldo (<kbd>`Backup_Router`</kbd>) en el rack, lo encendí y lo conecté a la <kbd>`Laptop_1`</kbd> mediante un cable USB para configurar su nombre con el comando <kbd>`hostname: Edge_Router`</kbd>.



* ## Qué has aprendido:&#x20;

A comprender la integración de los dispositivos dentro de la infraestructura de una sucursal corporativa y a manejar los distintos medios de transmisión.



* ## Conocer el entorno de Cisco Packet Tracer:&#x20;

A identificar visualmente la distribución de los equipos en los racks, reconociendo el propósito de cada componente y asociándolos con sus puertos lógicos correspondientes.



* ## Manipular el entorno físico de la red:&#x20;

A interactuar con elementos tangibles dentro del simulador, abriendo armarios de cableado, arrastrando dispositivos hacia los racks y accionando interruptores de encendido traseros.



* ## Investigar dispositivos en un armario de cableado:&#x20;

A auditar de forma práctica el hardware disponible y comprender su despliegue físico dentro del entorno de red.



* ## Instrucciones

### Parte 1: Investigar la Barra de Herramientas Inferior&#x20;

La barra de herramientas de iconos en la esquina inferior izquierda tiene varias categorías de componentes  de red. Debería ver categorías que corresponden a Dispositivos de Red, Dispositivos Finales, y  Componentes. La cuarta categoría (con el icono del rayo) es Conexiones y representa los medios de red  compatibles con Packet Tracer. Las dos últimas categorías son Miscelánea y Conexión multiusuario.&#x20;

¿Cuáles son las subcategorías de Dispositivos de Red?

Las subcategorias de los dispositivos de red en Cisco Packet Tracer:

1. Routers
2. Switches
3. Hubs
4. Wireless Devices
5. WAN Emulation
6. Security



### Parte 2: Investigar Dispositivos en un Armario de Cableado&#x20;

a. Si fuiste a explorar, vuelve a modo Físico e Intercity ahora. En la barra azul superior, haga clic en  Físico y, a continuación, utilice los botones Panel de Navegación o Nivel Atrás para desplazarse a  Intercity.&#x20;

b. Haga clic en Seward y, a continuación, haga clic en la Sucursal. &#x20;

c. Haga clic en el Armario de Cableado de la Sucursal. Observe que el armario de cableado tiene un  Rack, un Tablero de Cables, una Mesa y un Estante. El Rack contiene dispositivos que se pueden montar en rack. Si amplía el rack (herramienta de zoom o  Ctrl+rueda de desplazamiento), puede ver que los dispositivos están atornillados (montados) en el rack.  Debajo del dispositivo de distribución de energía, encontrará un router. Los routers conectan redes  diferentes. &#x20;

d. Debajo del router hay dos switches. Estos switches proporcionan conexiones por cable para conectarse  a otros dispositivos. Observe que los dispositivos tienen un nombre asignado por el administrador de red.  ¿Qué dispositivos utilizan una conexión por cable para conectarse al switch ALS2?&#x20;

<figure><img src="../../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

Los dispositivos que utilizan una conexión, podemos observar las conexiones:

* 🛜 Access\_Point (Punto de acceso inalámbrico): Un cable conecta uno de sus puertos directamente al switch ALS2.
* 🖥️ Web\_Server (Servidor web): Otro cable conecta la interfaz de red del servidor ubicado en la parte inferior del rack hacia el switch ALS2.

e. Debajo de los switches del Rack se encuentra un punto de acceso inalámbrico denominado  Access\_Point. Los puntos de acceso inalámbricos utilizan una conexión inalámbrica para conectarse a  otros dispositivos. Cambie al modo Lógico. ¿Qué dispositivo está conectado a Access\_Point?

<figure><img src="../../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

El ALS2 está conectado en el Access Point.

f. Cambie al modo Físico. Deberías estar de vuelta en el Armario de Cableado de la Sucursal. ¿Dónde  se encuentra físicamente el dispositivo conectado a Access\_Point?

![](<../../../.gitbook/assets/image (141).png>) &#x20;

El Acess Point se encuentra en el Rack.



### Parte 3: Conectar Dispositivos Finales a Dispositivos de Red&#x20;

Los dispositivos se pueden conectar de varias maneras. Para la conectividad de red, los dispositivos  normalmente se conectan mediante un cable directo de cobre o de forma inalámbrica. Para la conectividad  de administración, los dispositivos normalmente se conectan mediante un cable de consola o un cable USB.&#x20;

Nota: Packet Tracer calificará el resto de esta actividad. En cualquier momento, puede hacer clic en  Comprobar resultados en la parte inferior de la ventana Tareas. A continuación, haga clic en Elementos  de evaluación para ver qué elementos aún no ha completado.&#x20;

a. Investigue el Tablero de Cables. Incluye dos cables de Consola, diez cables directos de cobre, cuatro  cables de Fibra, dos cables Coaxiales y dos cables USB. Observe que las representaciones de cable en  modo Físico son más representativas de sus homólogos del mundo real. Cambie al modo Lógico. Observe que las representaciones de cable son diferentes en este modo.&#x20;

b. Cambie al modo Físico. Haga clic en un cable directo de cobre del Tablero de Cables. &#x20;

c. Mueva el ratón sobre los puertos de PC\_1 hasta que vea la ventana emergente FastEthernet0. El otro puerto RS232 es para conectar cables de Consola.&#x20;

d. Con el cable directo de cobre todavía seleccionado, haga clic en el puerto FastEthernet0 para conectar  el cable. Ahora el puerto debe estar resaltado en verde.&#x20;

e. Conecte el otro extremo del cable al switch ALS2 haciendo clic en un puerto Fast Ethernet vacío. El  cable ahora debería colgar entre la PC\_1 y el puerto de ALS2.&#x20;

f. Las PCs y los portátiles también se pueden conectar a dispositivos de red mediante un cable de consola  o un cable USB. Esta conexión proporciona acceso de administración. Haga clic en un cable de Consola del Tablero de Cables. &#x20;

g. Haga clic en el puerto RS232 en PC\_1. Ahora el puerto debe estar resaltado en verde. &#x20;

h. Pase el ratón sobre el Edge\_Router y busque el puerto de Consola. Puede hacer clic con el botón  derecho en > Inspeccionar Frente para ampliar y facilitar la búsqueda del puerto.&#x20;

i. Haga clic en el puerto de consola en Edge\_Router para conectar el cable de Consola. El cable ahora  debería colgar entre PC\_1 y el puerto de Consola en el Edge\_Router.

<br>
