---
icon: screwdriver-wrench
---

# Práctica 2 - Configuraciones básicas.

* ## Objetivo de la actividad:&#x20;

Demostrar y aplicar mi capacidad para configurar los parámetros iniciales en una red local pequeña utilizando la interfaz de línea de comandos (CLI) de dispositivos Cisco IOS.



* ## Qué se ha hecho:&#x20;

Conecté los equipos terminales a los switches mediante cables de consola. Configuré los nombres de host (`Room-145` y `Room-146`), las claves de acceso seguro para la consola y las líneas VTY, la contraseña secreta de habilitación, el cifrado general y un mensaje MOTD. Asigné IPs a las interfaces virtuales (`VLAN 1`) y a las tarjetas de red, guardando los cambios con el comando `copy running-config startup-config`.



* ## Qué has aprendido:&#x20;

A establecer parámetros esenciales de capa 2 y capa 3, blindar el acceso a los dispositivos mediante credenciales encriptadas y comprobar la conectividad de extremo a extremo.



* ## Conocer el entorno de Cisco Packet Tracer:&#x20;

A familiarizarme con la simulación de redes, la interpretación de tablas de direccionamiento y las herramientas interactivas de evaluación automática (_Check Results_).



* ## Manipular el entorno físico de la red:&#x20;

A gestionar los enlaces físicos y de consola, comprobando además el estado operativo de los puertos a través de sus indicadores visuales.



* ## Investigar dispositivos en un armario de cableado:&#x20;

A examinar la ubicación y conectividad física de los switches y ordenadores dentro de una topología estructurada.



* ## Desarrollo paso a paso:

### **Paso 1: Clasificación de Componentes de Topología**

1. Abrir la topología de red asignada.
2. Contabilizar y clasificar los componentes:
3. Dispositivos terminales (End Devices): PCs, Laptops, Servidores, Impresoras.
4. Dispositivos intermediarios: Switches, Routers, Puntos de acceso.
5. Medios de conexión: Cable directo de cobre, fibra óptica, enlaces coaxiales e inalámbricos.

### **Paso 2: Análisis Conceptual y Comparativo**

1. Modelo `Cliente-Servidor`: Los clientes envían peticiones de servicios (`HTTP, DNS, FTP`) a través de la red, y los servidores procesan y responden a dichas solicitudes de forma centralizada.
2. Criterios de Selección de Medios: Distancia máxima sin degradación de señal, costo de implementación, ancho de banda requerido y susceptibilidad a interferencias electromagnéticas `(EMI).`
3. LAN vs. WAN:
   1. LAN (Local Area Network): Red de alta velocidad que abarca un área geográfica limitada (oficina o edificio).
   2. WAN (Wide Area Network): Red que interconecta múltiples LANs separadas por amplias distancias geográficas, a menudo administrada por proveedores de servicios (ISP).
