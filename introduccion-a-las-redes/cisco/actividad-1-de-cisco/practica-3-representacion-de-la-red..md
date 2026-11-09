---
icon: user-headset
---

# Práctica 3 - Representación de la red.

* ## Objetivo de la actividad:&#x20;

Explorar una versión simplificada de una red corporativa para asimilar la función y organización de cada uno de sus elementos.



* ## Qué se ha hecho:&#x20;

Localicé y clasifiqué las categorías de dispositivos en la barra de herramientas inferior (intermediarios, terminales, medios y conexiones). Analicé las diferencias funcionales entre las redes de área local (LAN) y las redes de área amplia (WAN). Desarrollé ejercicios de desafío añadiendo dispositivos finales y enlazándolos mediante medios físicos y lógicos.



* ## Qué has aprendido:&#x20;

A comprender qué aparatos componen una infraestructura global, cómo opera el modelo cliente-servidor y qué criterios se siguen al seleccionar los medios de transmisión.



* ## Conocer el entorno de Cisco Packet Tracer:&#x20;

A navegar con soltura por una topología compleja, entendiendo el propósito formativo de la herramienta en entornos académicos.



* ## Manipular el entorno físico de la red:&#x20;

A unir terminales y nodos mediante el uso de cables de cobre, fibra óptica y conexiones inalámbricas.



* ## Investigar dispositivos en un armario de cableado:&#x20;

A inspeccionar los distintos distribuidores de una sucursal reconociendo el equipamiento montado en racks y mesas de trabajo.



* ## Desarrollo paso a paso:

### **Paso 1: Verificación de Parámetros de Fábrica**

Hacer clic en el switch `S1` pestaña CLI y presionar Enter.

Acceder al modo `EXEC` privilegiado y revisar la configuración activa:\
`Switch> enable`

`Switch# show running-config`\
Verificar la cantidad de interfaces `FastEthernet (24)` y `GigabitEthernet (2),` así como el rango de líneas `VTY (0 15).`

Comprobar que startup-config no está presente en la `NVRAM` al ejecutar `show startup-config.`

### **Paso 2: Configuración de Seguridad Basada en Texto Plano y Cifrado**

Asignar nombre de host al switch `S1:`\
`Switch# configure terminal`

`Switch(config)# hostname S1`\
Asegurar el acceso por consola:\
`S1(config)# line console 0`

`S1(config-line)# password letmein`

`S1(config-line)# login`

`S1(config-line)# exit`\
Configurar la contraseña de acceso al modo privilegiado `(c1$c0)` y la contraseña secreta cifrada `(itsasecret):`\
`S1(config)# enable password c1$c0`

`S1(config)# enable secret itsasecret`\
Cifrar todas las contraseñas almacenadas en texto plano:\
`S1(config)# service password-encryption`

### **Paso 3: Configuración del Banner de Advertencia (MOTD)**

Definir un aviso de inicio de sesión de seguridad:\
`S1(config)# banner motd "This is a secure system. Authorized Access Only!"`

`S1(config)# exit`

### **Paso 4: Guardado de la Configuración en la NVRAM**

Copiar la configuración en ejecución de la RAM a la memoria no volátil `(NVRAM):`\
`S1# copy running-config startup-config`\
Repetir la secuencia de pasos en el switch `S2.`



* ## Preguntas y Cuestionarios Resueltos

1. Enumere las categorías de los dispositivos intermediarios: Routers, switches, hubs, firewalls y puntos de acceso inalámbricos.
2. Explique el modelo cliente-servidor: Estructura donde los dispositivos cliente solicitan datos o servicios a un servidor dedicado, el cual procesa las peticiones e imparte la información solicitada.
3. Enumere al menos dos funciones de los dispositivos intermediarios: Regenerar y retransmitir señales de datos. Mantener información sobre las rutas existentes en la red para determinar el mejor camino de envío.
4. Enumere al menos dos criterios para elegir un tipo de medio de red: La distancia máxima permitida antes de sufrir atenuación de la señal. El entorno de instalación y las exigencias de ancho de banda o inmunidad al ruido.
5. Diferencia entre LAN y WAN: Una LAN proporciona acceso a usuarios locales en un área geográfica reducida; una WAN interconecta redes LAN distantes a través de grandes áreas geográficas mediante proveedores de telecomunicaciones.
