---
description: >-
  Introducción a las Redes: Fundamentos de redes, Internet, direccionamiento y
  modelos de comunicación.
icon: alien
---

# IA-Introducción a las redes

## Resumen de Contenidos

* Modelos de Comunicación Humana vs Redes
* Concepto de Internet, Nube y Protocolos
* Direccionamiento Físico (MAC) e IP
* Cliente-Servidor vs Peer-to-Peer (P2P)
* Dispositivos Intermedios y Medios
* Arquitectura Backbone & Tier ISP



### 1. La Comunicación y la Necesidad de las Redes

Fundamentos teóricos de la transmisión de datos y elementos de la comunicación.

Modo Didáctico Estándar Activado: Explicaciones directas, ejemplos prácticos visuales y esquemas conceptuales estructurados.

#### Elementos de la Comunicación Informática

Al igual que la comunicación humana requiere un emisor, un receptor, un canal y un lenguaje común, las redes de computadores aplican exactamente la misma estructura técnica para mover bits entre dispositivos.

Emisor (Fuente)Dispositivo host que genera e inicia el envío del mensaje (Ej. PC de origen).Receptor (Destino)Dispositivo host final que recibe e interpreta el mensaje enviado.Código (Protocolo)Conjunto de reglas sintácticas y semánticas compartidas (TCP/IP).Canal (Medio)Soporte físico o inalámbrico por donde viaja la señal (UTP, Fibra, Aire).**Ejemplo en llamada de emergencia (112):** Carlos (Emisor) transmite voz codificada por telefonía (Canal) mediante protocolo de audio al operador (Receptor) en un contexto crítico.

#### Esquema: Red Local Doméstica (LAN)

192.168.0.0/24\[ Conexión WAN / Internet ]│Router Inalámbrico / Gateway (192.168.0.1)WiFi (Inalámbrico)Smartphone: 192.168.0.11Laptop: 192.168.0.12Ethernet (Cable UTP)PC-01: 192.168.0.14PC-02: 192.168.0.15

&#x20;**Punto clave:** Todos los dispositivos locales pertenecen a la misma subred interna, saliendo al exterior mediante la dirección IP Pública configurada en la interfaz WAN del router.

#### ¿Qué es Internet?

Es una **red descentralizada** mundial de redes interconectadas que utilizan la familia de protocolos **TCP/IP**.

**Característica clave:** Nadie es dueño de Internet de forma centralizada. Permite el intercambio libre de información sin barreras geográficas.

#### ¿Qué es la Nube?

Red global de **servidores remotos** interconectados que funcionan como un ecosistema único para almacenar, gestionar y ejecutar aplicaciones.

**Servicios habituales:** Streaming de vídeo, correo web, almacenamiento y software ofimático accesible desde cualquier dispositivo.

#### ¿Qué es un Protocolo?

Conjunto de **normas y estándares** que definen la sintaxis, semántica y sincronización para que los equipos entiendan la información.

**Anatomía:** Establece el formato de datos, la identificación de origen/destino y los métodos de recuperación de errores.



### 2. Dispositivos, Direccionamiento e Interacción

Diferenciación técnica entre dirección física (MAC) y lógica (IP), roles de servidor y topologías de servicio.

#### Identificación en Red: IP (Lógica) vs MAC (Física)

Comparativa directa fundamental para la administración de redes.

| Criterio          | Dirección MAC (Media Access Control)                                           | Dirección IP (Internet Protocol)                                                                 |
| ----------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| Capa de Red (OSI) | Capa 2 (Enlace de Datos)                                                       | Capa 3 (Red)                                                                                     |
| Naturaleza        | **Física y Permanente:** Grabada en la tarjeta de red (NIC) por el fabricante. | **Lógica y Variable:** Asignada manualmente o por servidor DHCP según la ubicación.              |
| Formato           | <p>48 bits (6 hexadecimales)<br>Ej: 00:1A:2B:3C:4D:5E</p>                      | <p>IPv4: 32 bits (4 octetos decimales)<br>Ej: 192.168.1.50</p>                                   |
| Función Principal | Identificar al dispositivo localmente dentro de un mismo segmento o red LAN.   | Identificar la conexión lógica del dispositivo y permitir el enrutamiento entre distintas redes. |

#### Modelo Cliente - Servidor

Los clientes solicitan servicios (páginas web, correo, archivos) a servidores dedicados que procesan y responden a múltiples peticiones simultáneas.

Servidor WebApache, Nginx, IIS

Servidor de CorreoPostFix, Exchange, IMAP/SMTP

Servidor de ArchivosSamba, NFS, FTP

#### Redes Peer-to-Peer (P2P)

Todos los equipos (pares) pueden actuar simultáneamente como clientes y servidores. Ideal para hogares o pequeñas oficinas sin servidores dedicados.

Ventajas

* • Fácil configuración
* • Menor coste inicial
* • Sin punto único de fallo

Desventajas

* • Sin administración central
* • Baja seguridad
* • No es escalable



### 3. Componentes de Infraestructura y Transmisión

Dispositivos intermedios y medios físicos e inalámbricos para la interconexión.

#### Dispositivos Intermedios

Garantizan la conectividad y dirigen el flujo de datos entre redes individuales.

* **Switch (Conmutador):**&#x43;onecta equipos dentro de la misma LAN en Capa 2 usando la tabla MAC.
* **Router (Enrutador):**&#x49;nterconecta redes distintas en Capa 3 tomando decisiones de ruta mediante IP.
* **Firewall (Cortafuegos):**&#x46;iltra el tráfico permitiendo o denegando paquetes por seguridad.

#### Medios de Transmisión (Canal)

Hilos de Cobre

Los datos se codifican en **impulsos eléctricos**.

UTP / STP / FTP / CoaxialFibra Óptica

Los datos se codifican como **pulsos de luz**.

Monomodo / Multimodo (LC, SC, ST)Inalámbrico (Ondas)

Los datos viajan por el **espectro electromagnético**.

Wi-Fi (802.11) / Bluetooth / Zigbee

**Factores para elegir un medio:** Distancia máxima sin atenuación, entorno de instalación (interferencias electromagnéticas EMI), ancho de banda/velocidad requerida y presupuesto económico.

Arquitectura Global

#### Columna Vertebral de Internet (Backbone) & Tiers

[Explorar Submarine Cable Map](https://www.submarinecablemap.com/)

Tier 1 (Top Level): ISP principales con infraestructura global. No pagan peaje por tránsito (Ej: AT\&T, Lumen, Verizon).

Tier 2 (Nacional/Regional): Proveedores regionales que compran tránsito a Tier 1 y realizan acuerdos de peering entre sí.

Tier 3 (Acceso Final): ISP locales que venden conectividad directa al cliente final residencial y empresarial.

IXP / NAP (Puntos Neutros): Puntos físicos de intercambio directo de tráfico entre redes (Ej: DE-CIX, LINX, CATNIX).



### 4. Evolución Histórica de las Redes de Computadores.

Principales hitos tecnológicos desde la conmutación de paquetes hasta la era moderna.

* 61  : 1961-69  . Kleinrock & ARPANET
* 74  : 1974  . Nace TCP / IP
* 84  : 1984-85  . Cisco & Sistema DNS
* 91  : 1991  . WWW & HTML (Berners-Lee)
* 03  : 2003+  . Estándar IPv6 & Nube



### 5. Objetivos de Aprendizaje, Autoevaluación y Reto Práctico

Alineación con el módulo técnico de administración de redes y evaluación formativa.

#### Objetivos del Módulo MP0370

ASIX MP0370: Planificació i Administració de Xarxes

* Analizar la arquitectura de redes identificando la jerarquía de protocolos (TCP/IP y OSI).
* Integrar equipos en redes gestionando direccionamiento lógico (IPv4/IPv6) y servicios de red esenciales.



### Cuestionario de Autoevaluación Rápida

{% embed url="https://tally.so/r/pblbp1" %}

### Reto de Laboratorio Adicional (Para profundizar en Packet Tracer / CLI)

Abre la consola de comandos de tu sistema operativo (CMD o Terminal Linux) y ejecuta la orden `ipconfig /all` (Windows) o `ip a` (Linux). Identifica cuál es tu **Dirección Física (MAC)** y cuál tu **IPv4 por defecto**.

"No te quedes inmóvil al borde del camino…" — Mario Benedetti. ¡La mejor forma de aprender es hacer!
