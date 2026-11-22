---
description: >-
  Se entrega el PKT y un documento con los apuntes de la configuración
  realizada. Reviso en el aula.
icon: signal-messenger
---

# M0370T1A5-allCisco

## Actividades

### M370T2A3 — Cisco Packet Tracer

**Módulo:** 0370 — Redes\
**Ciclo:** ASIX\
**Dedicación:** 4 horas\
**Modalidad:** Individual\
**Rúbrica:** Se hace en clase\
**Entrega:** Archivo PKT y enlace a GitBook.

### Objetivo

Introducción a Cisco Packet Tracer y a la configuración de:

1. **Router SOHO**
   * Apertura de puertos (_port forwarding_).
   * Redes de invitados.
   * DHCP y DNS.
2. **Servidores y servicios**
   * DHCP y DNS.
   * WEB.
   * FTP.

### Entrega

* Archivo PKT debidamente cumplimentado durante la práctica en clase.
* Documento con las preguntas planteadas y sus respuestas.

### Descripción de la práctica

La configuración representa una red de empresa conectada a un ISP y una red doméstica situada detrás de un router inalámbrico.

**Nota:** preparar en casa la topología de red con todos los dispositivos conectados.

### Dispositivos y redes

Se utilizan tres redes: LAN1-Empresa, LAN2-Casa e ISP.

#### 1. LAN1 — Empresa

* 1 PC inicial.
* 1 servidor.
* 3 PC adicionales.
* 1 impresora.
* 3 puntos de acceso (A17, A18 y A10).
* 1 switch.

#### 2. LAN2 — Casa

* 1 router inalámbrico.
* 2 portátiles.
* 1 impresora.

#### 3. ISP

* 2 routers.
* 2 servidores.

### Configuración general

1. Cada servidor tendrá una página web que se propone personalizar.
2. El servidor **Google**, situado en el ISP, será el servidor DNS para todos los dispositivos.
3. Configurar RIP en cada router.

### Configuración en la empresa

1. El servidor **Trantor** ofrecerá los servicios WEB, DHCP y DNS.
2. Añadir dos dispositivos (una impresora y un portátil) a la red de la empresa para que reciban los parámetros de red mediante DHCP.

### Configuración en el ISP

1. El servidor **Google** ofrecerá los servicios DHCP y DNS.
2. El servidor **Paco** ofrecerá el servicio FTP.

### Configuración en casa: Home Router

#### 1. Configuración básica

* Configurar la IP de Internet.
* Configurar el DNS apuntando al servidor Godo del ISP.
* Activar el servicio DHCP para los equipos de casa.

#### 2. Wi-Fi

* Habilitar exclusivamente la banda de 2,4 GHz.
* Habilitar la seguridad WPA2.

#### 3. Guest Network

* Habilitar el acceso de invitados sin posibilidad de acceder a la red doméstica.
* Deshabilitar mediante MAC el acceso a la red de 2,4 GHz del PC de Xenxito.

#### 4. Access Restriction

Configurar reglas de acceso a la red. En este caso, configurar una ACL estándar (1–99) para bloquear el protocolo HTTP a través del puerto 80 a los dispositivos indicados en la lista. En el ejemplo, únicamente se bloquea el PC con IP **192.168.0.102**.

**Comprobación:** probar qué ocurre si únicamente se bloquea el puerto 80 (HTTP) y no se bloquea el puerto 443 (HTTPS).

### Prueba de configuración extra

#### Empresa

1. Añadir dos portátiles y una impresora.
2. Añadir un punto de acceso y conectar un smartphone a él.

#### ISP

1. Habilitar el servicio FTP. La actividad indica que resulta más interesante hacerlo desde Linux.
2. Conectarse desde cualquier equipo al servidor donde se haya habilitado el servicio FTP.

#### Casa

1. Conectar un teléfono y una tablet a la Wi-Fi de invitados.
2. Probar a habilitar la MAC de un equipo externo para que pueda acceder al servidor de casa.
3. Comprobar qué le sucede al PC de Xenxita si se bloquea el acceso mediante **Website Blocking by URL** al servidor Godo.
4. Probar la opción **Blocked Applications**.

***

## Preguntas

### Preguntas sobre la práctica LAN–WAN–HOMELAN

1. Incidencias tenidas durante el proceso de configuración.
2. ¿Por qué no podemos acceder a la web del servidor de casa desde el ISP o la empresa? ¿Qué tenemos que configurar para poder hacerlo?
3. ¿Cómo o qué detalle nos indica la conexión del router del proveedor de servicios con el _home router_ de casa?
4. ¿Cómo se lleva a cabo internamente la resolución del dominio y la descarga del HTML desde la perspectiva del cliente (navegador) y del DNS?
5. Cambia los DNS de los servidores y haz que todos apunten al servidor de Google **8.8.8.8**.
6. ¿Cómo se lleva a cabo la resolución del dominio a nivel del DNS?
7. Analiza la siguiente situación: imaginemos que al escenario configurado (LAN-WAN-HOMELAN) añadimos una sucursal de la empresa (LAN) y queremos que utilice la misma dirección IP de red: **192.168.1.0/24**. La sucursal también está conectada al ISP.
8. ¿Podemos utilizar la misma dirección IP de red en la nueva sucursal y en la red de la empresa que ya tenemos configurada? Ten en cuenta lo que sucede en la realidad y lo que tenemos configurado en Cisco.

### Preguntas sobre puertos lógicos

9. En relación con los puertos lógicos:
10. ¿Cómo se clasifican dichos puertos y por qué (según su uso)?
11. Indica qué puertos se utilizan para los siguientes servicios y qué hace cada uno de ellos:
12. **FTP**
13. **SSH**
14. **DNS**
15. **HTML / HTTP**
16. **MySQL**
17. **Portainer**
18. **SMTP**
19. **POP3**
20. **IMAP**
21. **DHCP**
22. **VNC**
23. **LDAP**
24. **OpenVPN**
25. **WireGuard**
26. **NTP**



## Investigación

* Configuracion del ISP: **Investigación:** investigar el uso del servicio FTP y cómo conectarse desde el equipo PC0 de la empresa al servicio FTP del servidor Paco en el ISP. Explicar el procedimiento e incluir una captura de pantalla.
*   Configuracion extra:

    * ISP ⇒  Investigar qué cambios hay que realizar para que el servidor Paco proporcione parámetros de red (direcciones IP) a dos PC que se conectarán a la red **30.0.0.0/8**.



## Bibliografia
