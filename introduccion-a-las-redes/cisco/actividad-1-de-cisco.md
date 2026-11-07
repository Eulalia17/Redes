# Actividad 1 de Cisco

## **Rúbrica:**

* te veo trabajar en clase y verifico cada actividad - 1pto
* informe revisado en el aula - 1pto
* si no te veo trabajar en el aula, no califico

## **¿Qué se entrega?**

Para cada actividad se entrega:

* el pkt completado correspondiente
* informe que contiene:
  * objetivo de la actividad
  * qué se ha hecho
  * qué has aprendido
  * conocer el entorno de cisco packet tracer.
  * manipular el entorno fisico de la red.
  * investigar dispositivos en un armario de cableado

## Practica

### Práctica 1 - Cableado y conectividad

* Objetivo de la actividad: Comprender y familiarizarme con el funcionamiento de la herramienta Cisco Packet Tracer, explorando las diferencias entre el modo lógico y el físico, además de realizar conexiones de red, gestión de equipos y configuraciones iniciales.
* Qué se ha hecho: Recorrí la interfaz de navegación hasta la ubicación geográfica de la sucursal de Seward para visualizar su armario de telecomunicaciones. Examiné el contenido del rack y del tablero de cables, enlacé físicamente la `PC_1` al switch `ALS2` con un cable de cobre directo, instalé un router de respaldo (`Backup_Router`) en el rack, lo encendí y lo conecté a la `Laptop_1` mediante un cable USB para configurar su nombre con el comando `hostname Edge_Router`.
* Qué has aprendido: A comprender la integración de los dispositivos dentro de la infraestructura de una sucursal corporativa y a manejar los distintos medios de transmisión.
* Conocer el entorno de Cisco Packet Tracer: A identificar visualmente la distribución de los equipos en los racks, reconociendo el propósito de cada componente y asociándolos con sus puertos lógicos correspondientes.
* Manipular el entorno físico de la red: A interactuar con elementos tangibles dentro del simulador, abriendo armarios de cableado, arrastrando dispositivos hacia los racks y accionando interruptores de encendido traseros.
* Investigar dispositivos en un armario de cableado: A auditar de forma práctica el hardware disponible y comprender su despliegue físico dentro del entorno de red.



### Práctica 2 - Configuraciones básicas

* Objetivo de la actividad: Demostrar y aplicar mi capacidad para configurar los parámetros iniciales en una red local pequeña utilizando la interfaz de línea de comandos (CLI) de dispositivos Cisco IOS.
* Qué se ha hecho: Conecté los equipos terminales a los switches mediante cables de consola. Configuré los nombres de host (`Room-145` y `Room-146`), las claves de acceso seguro para la consola y las líneas VTY, la contraseña secreta de habilitación, el cifrado general y un mensaje MOTD. Asigné IPs a las interfaces virtuales (`VLAN 1`) y a las tarjetas de red, guardando los cambios con el comando `copy running-config startup-config`.
* Qué has aprendido: A establecer parámetros esenciales de capa 2 y capa 3, blindar el acceso a los dispositivos mediante credenciales encriptadas y comprobar la conectividad de extremo a extremo.
* Conocer el entorno de Cisco Packet Tracer: A familiarizarme con la simulación de redes, la interpretación de tablas de direccionamiento y las herramientas interactivas de evaluación automática (_Check Results_).
* Manipular el entorno físico de la red: A gestionar los enlaces físicos y de consola, comprobando además el estado operativo de los puertos a través de sus indicadores visuales.
* Investigar dispositivos en un armario de cableado: A examinar la ubicación y conectividad física de los switches y ordenadores dentro de una topología estructurada.



### Práctica 3 - Representación de la red

* Objetivo de la actividad: Explorar una versión simplificada de una red corporativa para asimilar la función y organización de cada uno de sus elementos.
* Qué se ha hecho: Localicé y clasifiqué las categorías de dispositivos en la barra de herramientas inferior (intermediarios, terminales, medios y conexiones). Analicé las diferencias funcionales entre las redes de área local (LAN) y las redes de área amplia (WAN). Desarrollé ejercicios de desafío añadiendo dispositivos finales y enlazándolos mediante medios físicos y lógicos.
* Qué has aprendido: A comprender qué aparatos componen una infraestructura global, cómo opera el modelo cliente-servidor y qué criterios se siguen al seleccionar los medios de transmisión.
* Conocer el entorno de Cisco Packet Tracer: A navegar con soltura por una topología compleja, entendiendo el propósito formativo de la herramienta en entornos académicos.
* Manipular el entorno físico de la red: A unir terminales y nodos mediante el uso de cables de cobre, fibra óptica y conexiones inalámbricas.
* Investigar dispositivos en un armario de cableado: A inspeccionar los distintos distribuidores de una sucursal reconociendo el equipamiento montado en racks y mesas de trabajo.



### Práctica 4 - Configuraciones iniciales en switch

* Objetivo de la actividad: Llevar a cabo tareas avanzadas de configuración y seguridad inicial en switches Cisco Catalyst utilizando la interfaz de línea de comandos.
* Qué se ha hecho: Accedí al switch `S1` por consola e inspeccioné su configuración predeterminada ejecutando `show running-config`. Establecí la contraseña de consola con `password letmein`, la de habilitación con `enable password c1$c0` y la clave secreta con `enable secret itsasecret`. Activé el cifrado global con `service password-encryption` y configuré un banner MOTD. Reupliqué los ajustes en el switch `S2`, asegurando el almacenamiento en la NVRAM mediante `copy running-config startup-config`.
* Qué has aprendido: A aplicar políticas estrictas de seguridad física y lógica en nodos de red, protegiendo tanto los accesos por consola como la administración privilegiada.
* Conocer el entorno de Cisco Packet Tracer: A interpretar los diferentes niveles jerárquicos de comandos en Cisco IOS (_User EXEC_, _Privileged EXEC_ y _Global Configuration_).
* Manipular el entorno físico de la red: A comprobar las conexiones de los puertos _Fast Ethernet_ y _Gigabit Ethernet_ en switches Catalyst 2960.
* Investigar dispositivos en un armario de cableado: A analizar las especificaciones de hardware de los switches (número de interfaces y tipos de memoria) a través de comandos diagnósticos en la CLI.





### Práctica 5 - ARP

* Objetivo de la actividad: Examinar y comprender en profundidad la operativa del protocolo de resolución de direcciones (ARP) y el uso de las tablas de direcciones MAC tanto en entornos locales como remotos.
* Qué se ha hecho: Generé solicitudes ARP vaciando la caché local con el comando `arp -d` y lanzando pings en el modo simulación de Packet Tracer. Inspeccioné las tramas de difusión (_broadcast_) y los procesos de inundación (_flooding_) en los switches. Consulté las tablas de direcciones MAC mediante `show mac-address-table` y los registros ARP mediante `show arp` o `arp -a` en terminales y routers.
* Qué has aprendido: A descubrir cómo los dispositivos relacionan las direcciones físicas de Capa 2 a partir de las direcciones IP de Capa 3, gestionando las comunicaciones locales o a través de pasarelas remotas.
* Conocer el entorno de Cisco Packet Tracer: A utilizar con eficacia el modo simulación y el inspector de PDU (_Protocol Data Unit_) para auditar el tráfico de red paso a paso.
* Manipular el entorno físico de la red: A verificar la correcta interconexión entre pasarelas, puntos de acceso inalámbricos y segmentos de cableado estructurado.
* Investigar dispositivos en un armario de cableado: A validar el direccionamiento y la distribución de puertos en equipos intermediarios empleando comandos de diagnóstico en la CLI.
