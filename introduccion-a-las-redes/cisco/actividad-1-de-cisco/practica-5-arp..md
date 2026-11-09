---
icon: star-sharp-half-stroke
---

# Práctica 5 - ARP.

* ## Objetivo de la actividad:&#x20;

Examinar y comprender en profundidad la operativa del protocolo de resolución de direcciones (ARP) y el uso de las tablas de direcciones MAC tanto en entornos locales como remotos.



* ## Qué se ha hecho:&#x20;

Generé solicitudes ARP vaciando la caché local con el comando `arp -d` y lanzando pings en el modo simulación de Packet Tracer. Inspeccioné las tramas de difusión (_broadcast_) y los procesos de inundación (_flooding_) en los switches. Consulté las tablas de direcciones MAC mediante `show mac-address-table` y los registros ARP mediante `show arp` o `arp -a` en terminales y routers.



* ## Qué has aprendido:&#x20;

A descubrir cómo los dispositivos relacionan las direcciones físicas de Capa 2 a partir de las direcciones IP de Capa 3, gestionando las comunicaciones locales o a través de pasarelas remotas.



* ## Conocer el entorno de Cisco Packet Tracer:&#x20;

A utilizar con eficacia el modo simulación y el inspector de PDU (_Protocol Data Unit_) para auditar el tráfico de red paso a paso.



* ## Manipular el entorno físico de la red:&#x20;

A verificar la correcta interconexión entre pasarelas, puntos de acceso inalámbricos y segmentos de cableado estructurado.



* ## Investigar dispositivos en un armario de cableado:&#x20;

A validar el direccionamiento y la distribución de puertos en equipos intermediarios empleando comandos de diagnóstico en la CLI.



* ## Desarrollo paso a paso:

### **Paso 1: Examen de Solicitud ARP en Comunicación Local**

Abrir la terminal en PC `(172.16.31.2)` y limpiar la tabla ARP: `arp -d`\
Cambiar al modo `Simulation.`

Ejecutar ping `172.16.31.3.` Se generarán dos unidades de datos de protocolo `(PDU)`: una `ICMP` y una `ARP.`

Avanzar el tiempo mediante `Capture/Forward`. Observar que la `PDU ARP` realiza un flooding (difusión masiva) por todos los puertos del switch activo salvo el de origen, mientras que el paquete `ICMP` aguarda la resolución física.

Inspeccionar la trama `ARP:` su dirección `MAC` de destino es `FFFF.FFFF.FFFF (broadcast).`

Al responder el equipo de destino, la trama regresa de forma unidireccional (unicast) y la dirección MAC de origen y destino se invierten.

### **Paso 2: Inspección de Tablas de Direcciones MAC y ARP**

En `172.16.31.2,` ingresar al modo de tiempo real (Realtime) y consultar la tabla ARP: `arp -a`\
Respuesta: Muestra el mapeo entre la dirección `IP 172.16.31.3` y su dirección `MAC` asociada.

Hacer clic en `Switch1` pestaña `CLI` y consultar la tabla de direcciones MAC aprendidas dinámicamente: `Switch1# show mac-address-table`

### **Paso 3: Proceso ARP en Comunicaciones Remotas**

Limpiar nuevamente la tabla `ARP (arp -d)` en `172.16.31.2.`

Entrar a modo simulación y ejecutar un ping a un host remoto `(ping 10.10.10.1).`

Analizar la `PDU ARP` generada: la dirección IP solicitada en el paquete `ARP` no es la IP del host de destino remoto `(10.10.10.1),` sino la dirección IP de la puerta de enlace predeterminada `(Default Gateway / Router).`

Causa: Los dispositivos no pueden enviar tramas de Capa 2 directamente fuera de su subred local; por lo tanto, la resolución ARP debe obtener la dirección MAC del router local para que este encamine el tráfico hacia la red remota.



* ## Preguntas y Cuestionarios Resueltos

1. ¿La dirección MAC de destino de la solicitud ARP original se indica en la tabla? No, porque al ser una trama de difusión (broadcast) de descubrimiento, la dirección física de destino es FFFF.FFFF.FFFF.
2. ¿Cuántas copias de la PDU realizó el Switch1 en la solicitud ARP? Hizo copias para todos los puertos pertenecientes a esa VLAN, excepto por el puerto por el que ingresó la trama.
3. ¿Qué sucedió con las direcciones MAC de origen y destino en la respuesta ARP? Se invirtieron: la dirección MAC del dispositivo que responde pasó a ser el origen (source) y la del solicitante pasó a ser el destino (destination).
4. ¿Cuántas copias realizó el switch durante la respuesta de ARP? Una sola copia (unicast), dirigida al puerto específico del solicitante según la tabla de direcciones MAC del switch.
5. ¿Cuándo emite una terminal una solicitud de ARP? Cuando requiere transmitir datos hacia una IP de su misma subred local pero desconoce la dirección física (MAC) de destino.
6. ¿Por qué hay dos direcciones MAC asociadas a un mismo puerto en un switch? Ocurre cuando ese puerto conecta con otro dispositivo intermediario (como otro switch, hub o access point) a través del cual transitan múltiples dispositivos finales.
7. ¿Cuál es la IP de destino de una solicitud ARP para tráfico destinado a una red remota? La dirección IP de la puerta de enlace predeterminada (Default Gateway / Interfaz del router).
8. ¿Por qué la solicitud ARP no busca la MAC de la IP remota directamente? Porque las direcciones MAC se utilizan exclusivamente para la entrega en el segmento de red local (Capa 2). Las comunicaciones hacia redes externas deben ser entregadas al router para que este las encamine.
9. ¿Qué ocurre con el primer ping enviado cuando se debe resolver ARP hacia el router? El primer paquete suele expirar (Time Out) debido al tiempo de procesamiento y retardo consumido en generar y resolver la trama de solicitud y respuesta ARP preliminar.
