---
icon: star-sharp-half-stroke
---

# Práctica 5 - ARP.

* Objetivo de la actividad: Examinar y comprender en profundidad la operativa del protocolo de resolución de direcciones (ARP) y el uso de las tablas de direcciones MAC tanto en entornos locales como remotos.
* Qué se ha hecho: Generé solicitudes ARP vaciando la caché local con el comando `arp -d` y lanzando pings en el modo simulación de Packet Tracer. Inspeccioné las tramas de difusión (_broadcast_) y los procesos de inundación (_flooding_) en los switches. Consulté las tablas de direcciones MAC mediante `show mac-address-table` y los registros ARP mediante `show arp` o `arp -a` en terminales y routers.
* Qué has aprendido: A descubrir cómo los dispositivos relacionan las direcciones físicas de Capa 2 a partir de las direcciones IP de Capa 3, gestionando las comunicaciones locales o a través de pasarelas remotas.
* Conocer el entorno de Cisco Packet Tracer: A utilizar con eficacia el modo simulación y el inspector de PDU (_Protocol Data Unit_) para auditar el tráfico de red paso a paso.
* Manipular el entorno físico de la red: A verificar la correcta interconexión entre pasarelas, puntos de acceso inalámbricos y segmentos de cableado estructurado.
* Investigar dispositivos en un armario de cableado: A validar el direccionamiento y la distribución de puertos en equipos intermediarios empleando comandos de diagnóstico en la CLI.
