---
description: >-
  Análisis comparativo de características físicas, protocolos de seguridad y
  direccionamiento en entornos de red.
icon: chromecast
---

# Arquitectura y Especificaciones de Dispositivos de Red.

## Introducción

Hoy en la hora de redes hemos visto y abierto unos switches por dentro. Tambien un poco de teoria.

## Descripción.

### Teoria del shiwtches:

*   Sección Cisco (Izquierda):&#x20;

    * Se completa la ficha técnica indicando el año `2013`, interfaces físicas de `24p G.E` (24 puertos Gigabit Ethernet) con soporte `PoE` (Power over Ethernet). En el apartado de características y direccionamiento se listan tecnologías clave como:
    * Redes virtuales (`VLAN`).
    * Protocolos de prevención de bucles (`STP / RSTP / MSTP`).
    * Medidas de seguridad y control: `Port Security`, `DHCP Snooping`, `Dynamic ARP Insp.` (Dynamic ARP Inspection) y calidad de servicio (`QoS`).
    * Configuración de subredes e IP mediante `VLSM`.


* Sección Juniper y Switch Extreme (Centro):&#x20;
  * Especificaciones detalladas del dispositivo Juniper (`Network NS-025-005`, v4.0) con sus protocolos de seguridad, cifrado (`AES / 3DES`), además de una sección para `Switch Extreme` y el protocolo de encaminamiento dinámico `OSPF`.
* Sección Router Cisco y Topología (Derecha):&#x20;
  * Se especifica el uso de `QoS`, una dirección IP pública/privada (`77.16.216...`), y un pequeño diagrama esquemático de red que ilustra enlaces y subredes con direcciones IP como `192.168.1.10`.

<figure><img src="../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>



* Enfoque en el switch Cisco (Izquierda):&#x20;
  * Detalle cercano de las características avanzadas de capa 2 y capa 3 del switch de `24 puertos Gigabit Ethernet con PoE`.
*   Esquema de conceptos: Se aprecia claramente la jerarquía de apuntes que relaciona las características del dispositivo con:

    * Diseño de subredes (`IP Subnet / VLSM`).
    * Segmentación lógica mediante `VLAN`.
    * Alta disponibilidad y convergencia de topología con `STP`, `RSTP` y `MSTP`.
    * Endurecimiento de puertos y mitigación de ataques con `Port Security`, `DHCP Snooping`, `Dynamic ARP Inspection` y gestión de tráfico con `QoS`.

    <figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>


* Enfoque central-derecho:&#x20;
  * Muestra con mayor detalle las especificaciones del dispositivo Juniper (año 2005, modelo _Network NS-025-005 / v.4.0_, 4 puertos Fast Ethernet de 10/100 Mbps).
* Parámetros de seguridad y red:&#x20;
  * Enrutamiento por zonas (_Trust_, _Untrust_, _DMZ_, _HA_), túneles VPN IPsec cifrados con algoritmos `AES / 3DES` en un recuadro destacado.
*   Protocolos y esquemas:&#x20;

    * Referencia al protocolo de enrutamiento estado-enlace `OSPF` y diagramas de topología de red con nodos interconectados y etiquetado de interfaces y direccionamiento IP (`X-IP: 192.168.1.10`).

    <figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>


* Sección Cisco:&#x20;
  * Se observa la estructura base para documentar las especificaciones de un dispositivo de esta marca, indicando campos vacíos para `Año / Fab:`, `Modelo / Versión:`, `Interfaces físicas:` y `Caract:`.
* Esquema central de red:&#x20;
  * Un diagrama topológico esquemático que muestra una nube (representando internet o una red externa), conectada a dos routers (`R`), los cuales descienden mediante líneas de enlace hacia un cortafuegos o Firewall (`FW`).
*   Sección Juniper:&#x20;

    * Se detallan especificaciones técnicas preliminares correspondientes al modelo `Network NS-025-005` (año 2005, fabricado en China), mostrando 4 puertos Fast Ethernet y características de enrutamiento como zonas de confianza (_Trust_, _Untrust_), zona desmilitarizada (_DMZ_), alta disponibilidad (_HA_), y soporte para VPN con IPsec.

    <figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>



### Siwtch:

Siwtch 1.jpg

* Vista trasera del equipo:&#x20;
  * Muestra la parte posterior de un switch gestionable (con chasis violeta, característico de modelos como los switches Extreme Networks de la serie Summit).
* Componentes visibles:&#x20;
  * Módulos de fuentes de alimentación redundantes extraíbles (PSU) con indicadores LED de estado (`AC OK`, `DC OK`), rejillas de ventilación con ventiladores integrados para refrigeración activa, y una ranura de expansión lateral protegida con una tapa metálica rotulada (`Slot B`).
* Verificación:&#x20;
  * Los ventiladores giran y los indicadores LED de alimentación muestran un estado verde operativo (_OK_).

foto



#### `Siwtch 2.jpg`

* Vista superior con chasis abierto:&#x20;
  * Muestra el interior completo del switch con la cubierta metálica superior retirada.
* Componentes visibles:&#x20;
  * Placa base principal (_motherboard_) de color verde con disipadores de calor pasivos en los chipsets principales, las fuentes de alimentación redundantes instaladas en el lateral derecho, y los módulos de puertos y ranuras de expansión accesibles en la parte frontal y posterior.
* Verificación:&#x20;
  * El interior está libre de acumulación de polvo y los componentes modulares se encuentran firmemente acoplados a sus zócalos.

foto



#### 3. `Siwtch 3.jpg`

* Detalle de la placa base (Mainboard):&#x20;
  * Vista en primer plano de los circuitos integrados, procesadores y bancos de memoria de la placa principal.
* Componentes visibles:&#x20;
  * Circuitos integrados con disipadores, chips de procesamiento (etiquetados con marcas como PMC y circuitos de control), zócalos de expansión, condensadores electrolíticos y conectores internos de cableado plano y de alimentación.
*   Verificación:&#x20;

    * No se aprecian componentes abombados, fugas en los condensadores ni pistas de circuito impreso dañadas o quemadas.

    foto



#### 4. `Siwtch 4.jpg`

* Detalle del módulo de puertos y circuitería de capa física:&#x20;
  * Vista de cerca de una tarjeta de interfaz o placa hija (_daughterboard_) conectada mediante buses internos.
* Componentes visibles:&#x20;
  * Microchips controladores de puertos, matriz de resistencias y condensadores de montaje superficial (_SMD_), y etiquetas de número de parte y control de calidad (_S/N_).
* Verificación:&#x20;
  * Los conectores de interfaz y los buses de datos están correctamente alineados y sin holguras.

foto



#### 5. `siwtch 5.jpg`

* Detalle de la circuitería de control y reloj en placa:&#x20;
  * Vista cercana de la placa base de un dispositivo Cisco.
* Componentes visibles:&#x20;
  * Zócalo para pila de tipo botón (para la memoria CMOS/reloj de tiempo real), chips controladores de puertos de red con marcado superficial, y el logotipo oficial de CISCO serigrafiado sobre la placa de circuito impreso.
* Verificación:&#x20;
  * La batería de respaldo CMOS se encuentra correctamente alojada en su soporte y los componentes circundantes están intactos.

foto



#### 6. `Siwtch 6.jpg`

* Vista interior de un dispositivo de seguridad/routing (NetScreen):&#x20;
  * Chasis abierto de un dispositivo con la circuitería característica de equipos Juniper/NetScreen.
* Componentes visibles:&#x20;
  * Placa base con procesadores integrados (como chips de la familia PowerPC), múltiples chips de memoria y control, fuente de alimentación interna en el lateral derecho con cableado de corriente alterna protegido, y conectores de puertos en el panel posterior.
* Verificación:&#x20;
  * El cableado interno de alimentación está ordenado y alejado de los componentes de alta frecuencia para evitar interferencias electromagnéticas.

foto



7\. `Siwtch 7.jpeg`

* Etiqueta de especificaciones y panel de alimentación (NetScreen / Juniper):&#x20;
  * Vista exterior posterior.
* Datos técnicos:&#x20;
  * Corresponde al modelo NS-025 (Juniper Networks, fabricado en China en el año 2005), con especificaciones de marcado CE, UL y VCCI. Al lado se observa el interruptor físico de encendido (`O / I`) y el conector de alimentación IEC con compartimento para fusible.
* Verificación:&#x20;
  * El interruptor responde al accionamiento mecánico y el fusible de protección está debidamente alojado en su cavidad.

foto



#### 8. `Siwtch 9.jpeg`

* Panel posterior de Switch Cisco Catalyst:&#x20;
  * Vista trasera de un switch Cisco Catalyst 2960-X (Modelo: `WS-C2960X-24PS-L`).
* Componentes visibles:&#x20;
  * Rejilla de ventilación central, advertencia de seguridad eléctrica (_Warning: To reduce the risk of electric shock..._), ranura para fuente de alimentación modular redundante opcional (con cubierta ciega instalada), puerto de expansión FlexStack, y etiquetas con la dirección MAC (`7C:21:0D:62:82:00`) y número de serie.
* Verificación:&#x20;
  * Las etiquetas identificativas y de MAC son legibles y el chasis no presenta abolladuras que obstruyan los módulos posteriores.

foto



#### 9. `Siwtch8.jpeg`

* Panel inferior / Base de chasis (Cisco Catalyst 2960-X):&#x20;
  * Vista de la chapa inferior del switch.
* Datos y certificaciones:&#x20;
  * Placa de características técnicas que indica el modelo `Catalyst 2960 (COMMUTATEUR / 交换机 / 交换機)`, fecha de fabricación (`20190925`), especificaciones eléctricas de entrada (`100-240V ~ 8-4A, 50-60Hz`), y sellos regulatorios internacionales (CE, FCC, KCC, ICES).
* Verificación:&#x20;
  * Los pies de goma de apoyo están completos y la estructura metálica inferior mantiene su rigidez estructural.

foto



#### 10. `Switch 10.jpeg`

* Vista superior exterior (Cisco Catalyst):&#x20;
  * Tapa superior metálica del switch con el logotipo clásico de CISCO troquelado en relieve junto a las ranuras de ventilación longitudinales.
* Verificación:&#x20;
  * La superficie se encuentra limpia, sin arañazos profundos y con los tornillos de sujeción laterales correctamente fijados al chasis.

foto



### Inspección de Materiales de Red y Kit de Herramientas de Campo

* Tipo de componente:&#x20;
  * Cable de consola plano (Rollover / Rolled Cable).
* Conectores y características:&#x20;
  * Presenta un conector hembra DB9 (RS-232) de color azul claro en un extremo y un conector RJ-45 en el otro.
* Función técnica:&#x20;
  * Se utiliza para la gestión fuera de banda (_Out-of-Band management_) y la configuración inicial por puerto de consola de switches, routers y firewalls (Cisco, Juniper, etc.) conectándose al puerto serie COM de un equipo host.

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>



* Equipos e interconexiones presentes:
  * Punto de acceso Wi-Fi: Dispositivo de red inalámbrico empresarial Fortinet FortiAP 231G (chasis blanco con tres LED de estado).
  * Adaptador USB a Serie: Cable convertidor transparente/plateado con conector USB Tipo-A en un extremo y conector macho DB9 en el otro.
  * Cable de consola: Cable plano de consola DB9 a RJ-45 conectado al adaptador USB a Serie, formando un conjunto completo para la administración del puerto de consola desde ordenadores portátiles modernos sin puerto serie nativo.
* Verificación:&#x20;
  * La combinación del adaptador USB a Serie con el cable de consola permite abrir sesiones de terminal (mediante PuTTY, Tera Term o Minicom) en entornos de red donde los equipos carecen de interfaz serie DB9.

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>



* Maletín de herramientas manuales aisladas:&#x20;
  * Estuche de plástico azul rígido con un juego de herramientas orientadas a trabajos eléctricos y de mantenimiento informático.
* Herramientas contenidas:
  * Alicates: Alicate de puntas finas/semirredondas, alicate de corte diagonal y alicate universal de presión, todos provistos de mangos ergónomicos aislantes bicolor (rojo y negro).
  * Destornilladores: Juego de destornilladores aislados de punta plana y de estrella (Phillips) con mango rojo dieléctrico para protección contra descargas eléctricas.
  * Comprobador: Buscapolos o destornillador comprobador de tensión con cuerpo transparente y clip metálico.

foto
