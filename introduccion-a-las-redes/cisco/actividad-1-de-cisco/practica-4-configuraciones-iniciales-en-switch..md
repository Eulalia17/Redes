---
icon: router
---

# Práctica 4 - Configuraciones iniciales en switch.

* Objetivo de la actividad: Llevar a cabo tareas avanzadas de configuración y seguridad inicial en switches Cisco Catalyst utilizando la interfaz de línea de comandos.
* Qué se ha hecho: Accedí al switch `S1` por consola e inspeccioné su configuración predeterminada ejecutando `show running-config`. Establecí la contraseña de consola con `password letmein`, la de habilitación con `enable password c1$c0` y la clave secreta con `enable secret itsasecret`. Activé el cifrado global con `service password-encryption` y configuré un banner MOTD. Reupliqué los ajustes en el switch `S2`, asegurando el almacenamiento en la NVRAM mediante `copy running-config startup-config`.
* Qué has aprendido: A aplicar políticas estrictas de seguridad física y lógica en nodos de red, protegiendo tanto los accesos por consola como la administración privilegiada.
* Conocer el entorno de Cisco Packet Tracer: A interpretar los diferentes niveles jerárquicos de comandos en Cisco IOS (_User EXEC_, _Privileged EXEC_ y _Global Configuration_).
* Manipular el entorno físico de la red: A comprobar las conexiones de los puertos _Fast Ethernet_ y _Gigabit Ethernet_ en switches Catalyst 2960.
* Investigar dispositivos en un armario de cableado: A analizar las especificaciones de hardware de los switches (número de interfaces y tipos de memoria) a través de comandos diagnósticos en la CLI.
