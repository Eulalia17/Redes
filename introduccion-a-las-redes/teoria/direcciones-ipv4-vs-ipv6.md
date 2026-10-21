---
description: >-
  fundamentos de Redes: IPv4 e IPv6 Módulos: SMX (0225) y ASIX (0370) - Material
  Didáctico
---

# Direcciones IPv4 vs IPv6

## El Protocolo IPv4

El protocolo IPv4 utiliza direcciones de **32 bits**, divididas en 4 octetos (8 bits cada uno) escritos en formato decimal separados por puntos (ej. `192.168.1.10`). Toda dirección consta de dos partes definidas por la **máscara de subred**: la parte de red y la parte de host.

### Direccionamiento con Clases

| Clase | Binario Inicial | Rango (1er Octeto)          | Máscara por Defecto |
| ----- | --------------- | --------------------------- | ------------------- |
| A     | 0xxx xxxx       | 0.0.0.0 a 127.255.255.255   | 255.0.0.0 (/8)      |
| B     | 10xx xxxx       | 128.0.0.0 a 191.255.255.255 | 255.255.0.0 (/16)   |
| C     | 110x xxxx       | 192.0.0.0 a 223.255.255.255 | 255.255.255.0 (/24) |
| D     | 1110 xxxx       | 224.0.0.0 a 239.255.255.255 | Multicast           |

### Direcciones Privadas vs Públicas

Las IP privadas no son enrutables en Internet. Requieren de **NAT** (Network Address Translation) en el router para salir al exterior. Los rangos privados son:

* **Clase A:** 10.0.0.0 /8
* **Clase B:** 172.16.0.0 /12 (hasta 172.31.255.255)
* **Clase C:** 192.168.0.0 /16 (hasta 192.168.255.255)

**Concepto Avanzado (ASIX): VLSM y Sumarización**

El direccionamiento sin clase (CIDR) abandona las máscaras por defecto. \*\*VLSM\*\* (Máscaras de longitud variable) permite subdividir redes optimizando el espacio de direcciones, evitando el desperdicio del 50% o más que suele darse con subredes clásicas. La \*\*sumarización\*\* agrupa rutas contiguas reduciendo el tamaño de las tablas de enrutamiento.

### El Protocolo IPv6

Debido al agotamiento de direcciones IPv4, IPv6 proporciona direcciones de **128 bits** (340 sextillones de IPs). Se escriben en 8 bloques de 16 bits en formato hexadecimal, separados por dos puntos (`:`).

### Reglas de Simplificación

* **Ceros iniciales:** Se pueden omitir los ceros a la izquierda en un bloque.\
  `0138` -> `138`
* **Compresión de ceros (::):** Un grupo consecutivo de bloques compuestos solo por ceros puede sustituirse por `::`. **Solo se puede usar una vez por dirección.**\
  Ejemplo: `2001:0db8:0000:0000:0000:0000:1428:57ab` -> `2001:db8::1428:57ab`

### Tipos de Direcciones IPv6

**Unicast Global (GUA)**

Equivalentes a las IP públicas de IPv4. Son enrutables en Internet. Actualmente comienzan en el rango **2000::/3** (el primer dígito hexadecimal es 2 o 3).

**Link-Local (LLA)**

Usadas para comunicación dentro de la misma red LAN. No son enrutables. Obligatorias en toda interfaz IPv6. Comienzan por **FE80::/10**.

**Unicast Local Única (ULA)**

Equivalentes a las IP privadas. Enrutables internamente en la empresa, pero no en Internet. Comienzan por **FC00::/7** (prácticamente FD).

**Multicast y Anycast**

IPv6 elimina el Broadcast. El **Multicast** comienza por **FF00::/8** (ej. FF02::1 a todos los nodos). **Anycast** asigna la misma IP a múltiples equipos, enrutando al más cercano

## Resolución de Direcciones (Capa 2 a Capa 3)

Para enviar una trama Ethernet en una red LAN, el equipo emisor necesita conocer la dirección MAC (Capa 2) del equipo de destino o de la puerta de enlace. El mecanismo difiere totalmente entre IPv4 e IPv6.

### IPv4: Protocolo ARP

Address Resolution Protocol utiliza mensajes **Broadcast** para descubrir direcciones MAC.

* **ARP Request (Broadcast):** "¿Quién tiene la IP 192.168.1.10? Dime tu MAC." Destino MAC: `FF:FF:FF:FF:FF:FF`
* **ARP Reply (Unicast):** "Yo tengo la 192.168.1.10 y mi MAC es AA:BB:CC:..."
* Comandos: `arp -a` (ver tabla en Windows). `arp -d *` (borrar tabla).

### IPv6: Protocolo NDP (ICMPv6)

Neighbor Discovery Protocol elimina el Broadcast y usa mensajes **Multicast de ICMPv6**.

* **Neighbor Solicitation (NS):** Solicitud multicast pidiendo la MAC de un vecino. Usa dirección Multicast de nodo solicitado.
* **Neighbor Advertisement (NA):** Respuesta Unicast con la MAC.
* Comandos: `netsh interface ipv6 show neighbors` (Windows).

## Asignación de Direcciones IP

### DHCPv4 (IPv4)

El proceso de concesión DORA (Discover, Offer, Request, Acknowledge):

1. **DHCPDISCOVER (Broadcast):** El cliente busca un servidor.
2. **DHCPOFFER (Unicast):** El servidor ofrece una IP del Pool.
3. **DHCPREQUEST (Broadcast):** El cliente acepta la IP (informa a los demás servidores para que liberen ofertas).
4. **DHCPACK (Unicast):** El servidor confirma la concesión.

\* Nota: Si el DHCP está en otra red, el router debe configurarse como **Relay Agent** (`ip helper-address` en Cisco).

### Asignación Dinámica en IPv6

En IPv6 los hosts localizan el router enviando un **Router Solicitation (RS)**. El router responde con un **Router Advertisement (RA)** usando banderas (Flags A, O, M) para indicar cómo autoconfigurarse:

**1. SLAAC**

Stateless Address Autoconfiguration. No usa servidor DHCP.

`A=1, O=0, M=0`

El host usa el prefijo de red del Router (RA) y genera su host ID (aleatorio o **EUI-64** a partir de su MAC).

**2. SLAAC + DHCPv6**

DHCPv6 "Sin Estado".

`A=1, O=1, M=0`

SLAAC da IP y Gateway. El DHCPv6 entrega otros parámetros (DNS, Dominio).

**3. DHCPv6 (Stateful)**

Similar a DHCPv4.

`A=0, O=0, M=1`

El router solo da el Gateway. Todo el resto de la IP e info la da el DHCPv6 central.

## Herramienta de Diagnóstico IPv4

Introduce una dirección IPv4 para analizar su clase, máscara por defecto, y determinar si es pública, privada, loopback o reservada. Excelente para comprobaciones en el módulo de **Xarxes Locals (0225)**.

