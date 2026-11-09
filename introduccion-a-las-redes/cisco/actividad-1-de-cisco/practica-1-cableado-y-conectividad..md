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



* ## Desarrollo Paso a Paso:

### **Paso 1: Exploramos  la barra de herramientas**

1. Acceder a la barra de herramientas inferior izquierda.
2. Identificar las categorías de componentes: Dispositivos de Red, Dispositivos Finales, Componentes, Conexiones, Miscelánea y Conexión Multiusuario.
3. Explorar las subcategorías de Dispositivos de Red: Routers, Switches, Hubs, Wireless Devices, Security y WAN Emulation.

### **Paso 2: Inspección del Armario de Cableado de la Sucursal**

1. Seleccionar la vista Physical (Físico) en la barra superior.
2. Navegar a Intercity Seward Sucursal Armario de Cableado de la Sucursal.
3. Inspeccionar los elementos físicos: Rack, Tablero de Cables, Mesa y Estante.
4. Identificar el router y switches montados en el Rack `ALS2.`
5. Cambiar a modo Logical, para verificar qué dispositivos se conectan inalámbricamente a `Access_Point` y volver a la vista física para ubicar su localización en el plano del edificio.

### **Paso 3: Conexión de Dispositivos Finales a la Red**

1. En el Tablero de Cables, seleccionar un cable directo de cobre `Copper Straight-Through.`
2. Hacer clic en el puerto `FastEthernet0` de la `PC_1` y conectar el otro extremo a un puerto `Fast Ethernet` disponible en el switch `ALS2.`
3. Seleccionar un cable de `Consola` del Tablero de Cables.
4. Conectar el extremo `RS232` de la `PC_1` al puerto `Console` del `Edge_Router.`

### **Paso 4: Instalación y Configuración del Router de Respaldo**

1. Desde el Estante, arrastrar `Backup_Router` a un espacio libre del `Rack.`
2. Hacer clic en `Backup_Router` Inspeccionar parte trasera y accionar el interruptor de encendido.
3. Tomar un cable `USB` del Tablero de Cables, conectarlo al puerto de consola `USB` del `Backup_Router` y el otro extremo al puerto `USB` de `Laptop_1.`
4. En `Laptop_1`, abrir Desktop Terminal, aceptar los parámetros por defecto e ingresar a la `CLI.`
5. Rechazar el diálogo de configuración inicial y asignar el nombre de host:<br>

`Router> enable`

`Router# configure terminal`

`Router(config)# hostname Edge_Router_Backup`

`Edge_Router_Backup(config)# end`



* ## Preguntas y Cuestionarios Resueltos

1. ¿Cuáles son las subcategorías de Dispositivos de Red? Routers, Switches, Hubs, Dispositivos inalámbricos, Dispositivos de seguridad y Emulación WAN.
2. ¿Qué dispositivos utilizan una conexión por cable para conectarse al switch ALS2?Dispositivos finales como los PCs de escritorio (ej. PC\_1) conectados mediante cables Ethernet directos de cobre a sus puertos Fast Ethernet.
3. ¿Qué dispositivo está conectado a Access\_Point? Dispositivos finales inalámbricos (como una laptop o tablet con interfaz inalámbrica activada).
4. ¿Dónde se encuentra físicamente el dispositivo conectado a Access\_Point? En la zona de trabajo / área de oficina de la Sucursal de Seward.
