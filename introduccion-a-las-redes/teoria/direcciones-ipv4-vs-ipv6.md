---
description: >-
  fundamentos de Redes: IPv4 e IPv6 Módulos: SMX (0225) y ASIX (0370) - Material
  Didáctico
icon: sidebar-flip
---

# Direcciones IPv4 vs IPv6

## El Protocolo IPv4

El protocolo IPv4 utiliza direcciones de **32 bits**, divididas en 4 octetos (8 bits cada uno) escritos en formato decimal separados por puntos (ej. `192.168.1.10`). Toda dirección consta de dos partes definidas por la **máscara de subred**: la parte de red y la parte de host.

### Direccionamiento con Clases

| Clase | Binario Inicial | Rango (1er Octeto)          | Máscara por Defecto    |
| ----- | --------------- | --------------------------- | ---------------------- |
| A     | 0xxx xxxx       | 0.0.0.0 a 127.255.255.255   | 255.0.0.0 (/8)         |
| B     | 10xx xxxx       | 128.0.0.0 a 191.255.255.255 | 255.255.0.0 (/16)      |
| C     | 110x xxxx       | 192.0.0.0 a 223.255.255.255 | 255.255.255.0 (/24)    |
| D     | 1110 xxxx       | 224.0.0.0 a 239.255.255.255 | Multicast              |
| E     | 1111 xxxx       | 240.0.0.0 a 255.255.255.255 | Reservada/experimental |

### Direcciones Privadas vs Públicas

Las IP privadas no son enrutables en Internet. Normalmente, el router utiliza **NAT** (Network Address Translation) para que varios equipos con direcciones privadas puedan acceder al exterior usando una o varias direcciones públicas. Los rangos privados son:

* **10.0.0.0/8:** de 10.0.0.0 a 10.255.255.255.
* **172.16.0.0/12:** de 172.16.0.0 a 172.31.255.255.
* **192.168.0.0/16:** de 192.168.0.0 a 192.168.255.255.

Una dirección pública puede ser enrutable en Internet; una privada se utiliza dentro de redes locales. No basta con mirar la clase para decidir si una IP es privada: hay que comprobar si pertenece a uno de los rangos privados definidos.

**Concepto avanzado (ASIX): VLSM y sumarización.** CIDR permite representar redes con un prefijo de longitud variable. VLSM permite dividir una red en subredes de tamaños diferentes para aprovechar mejor las direcciones. La sumarización agrupa varios prefijos contiguos en una ruta más amplia y reduce el tamaño de las tablas de enrutamiento.

### El protocolo IPv6

IPv6 se diseñó, entre otros motivos, para resolver la escasez de direcciones IPv4. Utiliza direcciones de **128 bits**, escritas como ocho bloques hexadecimales de 16 bits separados por dos puntos. Un ejemplo completo es `2001:0db8:0000:0000:0000:ff00:0042:8329`.

### Reglas de simplificación IPv6

* **Omitir ceros iniciales:** en cada bloque se pueden quitar los ceros situados a la izquierda. Por ejemplo, `0db8` se escribe `db8`.
* **Comprimir bloques de ceros:** una secuencia consecutiva de bloques `0000` se puede sustituir por `::`, pero solo una vez en una dirección. Por ejemplo, `2001:0db8:0000:0000:0000:ff00:0042:8329` se puede escribir `2001:db8::ff00:42:8329`.
* No se deben usar dos compresiones `::` en una misma dirección, porque no se podría saber cuántos bloques se han omitido.

### Tipos importantes de direcciones IPv6

* **Unicast global:** normalmente dentro de `2000::/3`; se puede enrutar globalmente cuando está asignada y configurada correctamente.
* **Link-local:** dentro de `FE80::/10`; se utiliza en el enlace local y no se enruta a otras redes. Las interfaces IPv6 suelen disponer de una dirección de este tipo.
* **Unique Local Address (ULA):** dentro de `FC00::/7`, habitualmente con prefijos `FD`; se usa para comunicaciones privadas internas.
* **Multicast:** dentro de `FF00::/8`; envía tráfico a un grupo de interfaces. IPv6 no utiliza broadcast como IPv4.
* **Anycast:** una misma dirección se asigna a varias interfaces y el enrutamiento entrega el tráfico a una de ellas, normalmente la más cercana según las rutas.

## Resolución de direcciones: ARP y NDP

En una red Ethernet, el equipo necesita la dirección MAC del destino local o de la puerta de enlace para construir la trama. IPv4 e IPv6 resuelven esta relación de formas diferentes.

### IPv4: ARP

ARP (Address Resolution Protocol) permite averiguar qué dirección MAC corresponde a una IPv4 de la red local.

1. El equipo envía una solicitud ARP mediante broadcast preguntando quién utiliza la IPv4 buscada.
2. El dispositivo propietario responde con su dirección MAC, normalmente mediante un mensaje unicast.
3. El emisor guarda temporalmente la asociación en su caché ARP.

En Windows, `arp -a` muestra la tabla ARP. El comando `arp -d *` intenta eliminar las entradas de la caché y puede requerir permisos elevados.

### IPv6: NDP

NDP (Neighbor Discovery Protocol) funciona mediante mensajes ICMPv6 y multicast, sin broadcast. Incluye Neighbor Solicitation (NS) y Neighbor Advertisement (NA), que ayudan a descubrir vecinos y sus direcciones de enlace. En Windows se puede consultar la tabla de vecinos con `netsh interface ipv6 show neighbors`.

## Asignación automática: DHCPv4, SLAAC y DHCPv6

### DHCPv4: proceso DORA

1. **Discover:** el cliente busca un servidor DHCP.
2. **Offer:** el servidor ofrece una dirección y parámetros de configuración.
3. **Request:** el cliente solicita la oferta elegida.
4. **Acknowledge:** el servidor confirma la concesión.

Los parámetros pueden incluir máscara, puerta de enlace, DNS y duración de la concesión. Si el servidor DHCP está en otra subred, normalmente se configura un agente relay en el router.

### IPv6: SLAAC y DHCPv6

Los routers anuncian información de red mediante Router Advertisement (RA). Las banderas del RA ayudan a indicar cómo debe obtener el equipo la dirección y otros parámetros:

* **SLAAC:** el host forma su dirección usando el prefijo anunciado y un identificador de interfaz generado por el sistema. No necesita que DHCPv6 le asigne la dirección.
* **SLAAC + DHCPv6 sin estado:** SLAAC configura la dirección y DHCPv6 puede proporcionar otros parámetros, como DNS.
* **DHCPv6 con estado:** el servidor DHCPv6 asigna y registra direcciones y parámetros; el router sigue anunciando la información necesaria para alcanzar otras redes.

La interpretación exacta de las banderas debe comprobarse en el RA recibido y en la configuración de la red; no debe suponerse que todos los equipos usan el mismo método.

## Herramienta de Diagnóstico IPv4

Introduce una dirección IPv4 para analizar su clase, máscara por defecto, y determinar si es pública, privada, loopback o reservada. Excelente para comprobaciones en el módulo de **Xarxes Locals (0225)**.

## Material desarrollado del PDF: interpretación del diagnóstico IPv4

La segunda página del PDF muestra un ejemplo de la herramienta con la dirección **191.16.45.51**. El resultado indicado es **Clase B**, máscara por defecto **255.255.0.0 (/16)** y tipo de red **pública**. También muestra el primer octeto en binario: `10111111`.

### 1. Cómo se analiza una IPv4

Una dirección IPv4 contiene cuatro octetos separados por puntos. Cada octeto debe ser un número entre 0 y 255. Para analizarla:

1. Comprueba que hay exactamente cuatro octetos y que cada uno está dentro del rango válido.
2. Identifica el primer octeto para clasificar la dirección según el esquema tradicional por clases.
3. Consulta la máscara o el prefijo para distinguir la parte de red de la parte de host. La clase por sí sola no determina la subred real cuando se utiliza CIDR.
4. Comprueba si la dirección pertenece a un rango especial, como privado, loopback o reservado.
5. Interpreta el resultado teniendo en cuenta la configuración real de la interfaz, la máscara y la puerta de enlace.

### 2. Ejemplo del PDF: 191.16.45.51

| Campo                          | Resultado del ejemplo | Interpretación                                                            |
| ------------------------------ | --------------------- | ------------------------------------------------------------------------- |
| Dirección introducida          | `191.16.45.51`        | IPv4 válida: cuatro octetos.                                              |
| Clase principal                | Clase B               | El primer octeto, 191, está en el rango tradicional de Clase B (128–191). |
| Máscara por defecto (classful) | `255.255.0.0` (`/16`) | En el esquema por clases, los dos primeros octetos corresponden a la red. |
| Tipo de red                    | Pública               | No pertenece a los rangos privados IPv4 habituales.                       |
| Primer octeto en binario       | `10111111`            | Es la representación binaria de 191.                                      |

**Importante:** `/16` es la máscara por defecto histórica de la Clase B, no necesariamente la máscara configurada en un equipo real. En redes modernas se utiliza CIDR, por lo que hay que conocer el prefijo configurado para calcular correctamente la red, el broadcast y los hosts disponibles.

### 3. Rangos especiales que conviene reconocer

| Uso             | Rango o dirección                                   | Para qué sirve                                                                     |
| --------------- | --------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Privada         | `10.0.0.0/8`                                        | Direccionamiento interno de redes.                                                 |
| Privada         | `172.16.0.0/12`                                     | Direccionamiento interno de redes.                                                 |
| Privada         | `192.168.0.0/16`                                    | Direccionamiento interno de redes.                                                 |
| Loopback        | `127.0.0.0/8` (por ejemplo, `127.0.0.1`)            | Pruebas del propio equipo; el tráfico no se envía a la LAN.                        |
| Link-local IPv4 | `169.254.0.0/16`                                    | Puede aparecer cuando un equipo no consigue una concesión DHCP y se autoconfigura. |
| Multicast       | `224.0.0.0/4`                                       | Comunicación dirigida a grupos.                                                    |
| Documentación   | `192.0.2.0/24`, `198.51.100.0/24`, `203.0.113.0/24` | Direcciones reservadas para ejemplos y documentación.                              |

### 4. Comprobaciones prácticas en Windows

Abre la terminal o CMD y utiliza estos comandos:

* `ipconfig`: muestra la configuración IP básica.
* `ipconfig /all`: muestra detalles de la interfaz, DHCP, DNS y dirección física.
* `ping 192.168.1.1`: comprueba si hay respuesta desde una dirección indicada; sustituye la IP por la que quieras probar.
* `arp -a`: muestra las asociaciones IPv4–MAC aprendidas.
* `tracert 8.8.8.8`: muestra los saltos de la ruta hacia un destino, si la red permite esas respuestas.

Una respuesta correcta al ping no garantiza que todos los servicios funcionen; y la ausencia de respuesta no demuestra por sí sola que el equipo esté apagado, ya que un cortafuegos puede bloquear ICMP.

### 5. Actividad de comprobación

Analiza cada dirección con la herramienta y explica el resultado. La clasificación por clases es histórica; cuando se proporciona una máscara o un prefijo, utiliza ese dato para determinar la red real.

| Dirección de ejemplo | Qué debes comprobar                                                                            |
| -------------------- | ---------------------------------------------------------------------------------------------- |
| `192.168.10.5`       | Si pertenece al rango privado y qué información adicional necesitas para determinar la subred. |
| `10.20.30.40`        | Qué rango privado contiene la dirección.                                                       |
| `172.20.5.10`        | Si está dentro del bloque privado `172.16.0.0/12`.                                             |
| `127.0.0.1`          | Por qué es una dirección loopback.                                                             |
| `169.254.10.20`      | Qué puede indicar una dirección link-local IPv4 en un equipo cliente.                          |
| `191.16.45.51`       | Reproduce el ejemplo del PDF: clase tradicional, máscara por defecto y tipo de dirección.      |

### 6. Diferencias clave entre IPv4 e IPv6

| Característica           | IPv4                          | IPv6                                 |
| ------------------------ | ----------------------------- | ------------------------------------ |
| Longitud                 | 32 bits                       | 128 bits                             |
| Representación           | Decimal, cuatro octetos       | Hexadecimal, ocho bloques            |
| Separador                | Punto (`.`)                   | Dos puntos (`:`)                     |
| Resolución de vecinos    | ARP                           | NDP mediante ICMPv6                  |
| Broadcast                | Sí                            | No; utiliza multicast                |
| Configuración automática | DHCPv4 o configuración manual | SLAAC, DHCPv6 o configuración manual |
| Espacio de direcciones   | Más limitado                  | Muchísimo mayor                      |

**Conclusión:** la herramienta del PDF sirve como ayuda didáctica para reconocer la notación, la clase tradicional y algunos rangos especiales IPv4. Para diagnosticar una red real, contrasta siempre el resultado con la máscara/prefijo configurado, la puerta de enlace, las rutas y la conectividad.
