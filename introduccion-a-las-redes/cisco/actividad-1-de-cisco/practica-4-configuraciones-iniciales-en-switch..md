---
icon: router
---

# Práctica 4 - Configuraciones iniciales en switch.

* ## Objetivo de la actividad:&#x20;

Llevar a cabo tareas avanzadas de configuración y seguridad inicial en switches Cisco Catalyst utilizando la interfaz de línea de comandos.



* ## Qué se ha hecho:&#x20;

Accedí al switch `S1` por consola e inspeccioné su configuración predeterminada ejecutando `show running-config`. Establecí la contraseña de consola con `password letmein`, la de habilitación con `enable password c1$c0` y la clave secreta con `enable secret itsasecret`. Activé el cifrado global con `service password-encryption` y configuré un banner MOTD. Reupliqué los ajustes en el switch `S2`, asegurando el almacenamiento en la NVRAM mediante `copy running-config startup-config`.



* ## Qué has aprendido:&#x20;

A aplicar políticas estrictas de seguridad física y lógica en nodos de red, protegiendo tanto los accesos por consola como la administración privilegiada.



* ## Conocer el entorno de Cisco Packet Tracer:&#x20;

A interpretar los diferentes niveles jerárquicos de comandos en Cisco IOS (_User EXEC_, _Privileged EXEC_ y _Global Configuration_).



* ## Manipular el entorno físico de la red:&#x20;

A comprobar las conexiones de los puertos _Fast Ethernet_ y _Gigabit Ethernet_ en switches Catalyst 2960.



* ## Investigar dispositivos en un armario de cableado:&#x20;

A analizar las especificaciones de hardware de los switches (número de interfaces y tipos de memoria) a través de comandos diagnósticos en la CLI.



* ## Desarrolo paso a paso:

### **Paso 1: Configuración de Interfaz VLAN 1 en Switches**

En `S1`, configurar la dirección IP de gestión de la `SVI` (Switch Virtual Interface):\
`S1# configure terminal`

`S1(config)# interface vlan 1`

`S1(config-if)# ip address 192.168.1.253 255.255.255.0`

`S1(config-if)# no shutdown`\
Aplicar la configuración equivalente para la `VLAN 1` en `S2.`

### **Paso 2: Configuración de Direccionamiento IP en Hosts Finales**

En `PC1,` acceder a Desktop IP Configuration.

Establecer la dirección IP y la máscara de subred (ejemplo: `IP 192.168.1.1, Máscara 255.255.255.0).`

Repetir el procedimiento en `PC2` asignando su dirección correspondiente en la misma subred.

### **Paso 3: Verificación de Conectividad Extremo a Extremo**

1. Abrir la consola de comandos (Command Prompt) en `PC1.`
2. Probar la conectividad mediante el comando ping hacia la IP de `S1, S2 y PC2:`\
   `ping 192.168.1.2`



* ## Preguntas y Cuestionarios Resueltos

1. ¿Cuántas interfaces Fast Ethernet y Gigabit Ethernet tiene el switch Catalyst 2960? 24 interfaces Fast Ethernet y 2 interfaces Gigabit Ethernet.
2. ¿Cuál es el rango de valores para las líneas VTY? 0 15 (permite 16 sesiones virtuales simultáneas de administración remota).
3. ¿Qué comando muestra el contenido de la NVRAM? show startup-config
4. ¿Por qué el switch responde con "startup-config no está presente"? Porque el dispositivo aún no ha guardado la configuración en ejecución (running-config) en la memoria no volátil (NVRAM).
5. ¿Por qué se requiere el comando login al configurar la consola? Para habilitar el aviso del indicador de contraseña al intentar conectarse al puerto serie de consola; sin este comando, el switch ignora la clave definida.
6. ¿Qué se muestra como contraseña de enable secret en el archivo de configuración? Una secuencia de texto encriptada mediante un algoritmo de hash de vía única (MD5/SHA).
7. ¿Por qué se ve diferente a la contraseña configurada originalmente? Porque el comando enable secret la almacena en formato cifrado e irreversible para evitar su lectura a simple vista.
8. Si se configuran más contraseñas, ¿se cifran automáticamente tras activar service password-encryption?Sí, el comando cifrará retroactivamente y a futuro todas las contraseñas en texto plano dentro del archivo de configuración.
9. ¿Cuándo se muestra el mensaje de MOTD? Inmediatamente antes del inicio de sesión, al establecer contacto con la CLI del equipo.
10. ¿Por qué todos los switches deben tener un aviso de MOTD? Por motivos legales de auditoría y seguridad corporativa, advirtiendo explicitamente que el acceso no autorizado está prohibido.
11. Abreviatura más corta de copy running-config startup-config: copy run start
