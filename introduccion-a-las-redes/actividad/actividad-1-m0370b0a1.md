# 🤖 Actividad 1 - M0370B0A1

## ¿Qué? ¿Por Qué? ¿Impacto?

<br>

*   **¿Qué es una red?**&#x55;na red informática es un sistema de dispositivos informáticos interconectados (que van desde entornos tradicionales hasta entornos basados en la nube) que se comunican y comparten recursos entre sí.

    Los dispositivos en red se basan en protocolos de comunicación (reglas que describen cómo transmitir o intercambiar datos a través de una red), lo que les permite compartir información a través de conexiones físicas o inalámbricas.



* **¿Cuál es su importancia?**&#x4C;as redes informáticas son la columna vertebral de la conectividad moderna porque permiten conectar dispositivos para compartir información, recursos y comunicarse en tiempo real.&#x20;



* **Explícame por qué se considera que las redes de ordenadores son el sistema nervioso de la sociedad actual usando un ejemplo real de interrupción de servicio a gran escala.**&#x4C;as redes de ordenadores se consideran el sistema nervioso de la sociedad actual porque, de la misma forma que las neuronas transmiten los impulsos eléctricos que coordinan los músculos, los sentidos y los órganos de un cuerpo vivo, la infraestructura digital transporta el flujo de datos que mantiene operativos los servicios críticos de nuestro planeta (finanzas, transporte, salud y comunicación). Si el sistema nervioso falla, el cuerpo se paraliza; si las redes se interrumpen, la sociedad moderna se detiene por completo.El ejemplo real más nítido de este fenómeno ocurrió con el apagón informático mundial de CrowdStrike en julio de 2024.



* **¿Cuál es el ámbito de trabajo y salidas profesionales?**
  *   &#x20;**Ambito de trabajo:**

      * Departamentos de TI (Tecnologías de la Información): Soporte y mantenimiento de redes locales (LAN) y amplias (WAN) en empresas de cualquier sector (pymes o grandes multinacionales).
        * Proveedores de Servicios de Internet (ISP) y Telecomunicaciones: Gestión de conexiones, fibra óptica, redes inalámbricas y distribución de tráfico de datos.
        * Empresas de Ciberseguridad y Consultoría IT: Protección de redes frente a accesos no autorizados, ataques y brechas de seguridad.
        * Centros de Datos (Data Centers) y Cloud Computing: Operación de servidores e infraestructuras en la nube que requieren alta disponibilidad continua.&#x20;


  *   &#x20;**Salidad profesionales:**

      * Instalador-reparador / instaladora-reparadora de equipos informáticos.
        * Técnica / técnico de soporte informático.
        * Técnica / técnico de redes de datos.
        * Reparador / reparadora de periféricos de sistemas microinformáticos.
        * Comercial de microinformática.
        * Operador / operadora de tele-asistencia.
        * Operador / operadora de sistemas.


* **Compara el día a día de un Técnico en Sistemas y Redes (perfil ASIX) con el de un Analista de Ciberseguridad/SecOps (perfil universitario).  ¿Qué herramientas clave usa cada uno?** El día a día de un Técnico en Sistemas y Redes (perfil FP de Grado Superior en ASIX - Administración de Sistemas Informáticos en Red) y el de un Analista de Ciberseguridad / SecOps (perfil universitario o máster) difieren notablemente en sus objetivos principales. Mientras que el técnico de sistemas se enfoca en que todo funcione y esté disponible, el analista de seguridad se centra en proteger, detectar y mitigar riesgos.
  * **Técnico en Sistemas y Redes (perfil ASIX):**
    *   Su maleta de herramientas está orientada a la administración de sistemas operativos, la virtualización y la conectividad física y lógica.

        * Virtualización y Cloud: VMware vSphere/ESXi, Proxmox, Hyper-V, y paneles básicos de AWS o Azure.
        * Sistemas Operativos y Automatización: Consolas de Linux (Bash) y Windows Server (PowerShell, Active Directory, GPOs).
        * Monitoreo de Infraestructura: Zabbix, Nagios o Pandora FMS (para vigilar si un servidor o router se cae).
        * Redes y Diagnóstico: Wireshark (análisis de tráfico), Putty/SSH, consolas de Cisco/MikroTik y comandos de red nativos (`ping`, `traceroute`, `nslookup`).
        * Gestión: Sistemas de ticketing (Jira Service Desk, GLPI) y herramientas de copia de seguridad (Veeam Backup).


  * **Analista de Ciberseguridad/SecOps (perfil universitario):**
    * Su entorno de trabajo se basa en la correlación de datos masivos, la detección de intrusiones y la respuesta ante incidentes en tiempo real.
      * Plataformas SIEM y XDR: Splunk, Microsoft Sentinel, Elastic Security o QRadar (centralizan y correlacionan millones de logs para buscar ataques).
      * Seguridad de Endpoint (EDR): CrowdStrike Falcon, Microsoft Defender for Endpoint o SentinelOne (para aislar equipos infectados o ver procesos sospechosos).
      * Análisis y Triage de Red: Zeek, Suricata, Wireshark avanzado y firewalls de nueva generación (NGFW) como Palo Alto o Fortinet.
      * Gestión de Vulnerabilidades: Nessus, Qualys o OpenVAS (para escanear fallos en la infraestructura).
      * Automatización de Respuesta (SOAR): Cortex XSOAR o Splunk Phantom (para automatizar el bloqueo de IPs o cuentas comprometidas).

## ¿Qué contenidos tenemos que dominar?

<br>

* **¿Cuáles son los fundamentos físicos y lógicos a considerar?**&#x4C;os fundamentos físicos y lógicos de una red informática abarcan tanto la infraestructura tangible de hardware como las reglas de software y arquitectura que permiten el flujo ordenado de los datos.
  *   Los elementos físicos son los componentes palpables y los medios materiales que hacen posible la conexión eléctrica o inalámbrica entre los dispositivos.&#x20;

      * Medios de transmisión: Los canales por los que viajan los datos, que pueden ser guiados (como el cable de par trenzado Ethernet o la fibra óptica) o no guiados (ondas de radio, Wi-Fi o infrarrojos).
      * Dispositivos de red (Hardware activo): Equipos que conectan, amplifican o dirigen la señal, tales como los switches o conmutadores (que centralizan una red local en estrella) y los routers o enrutadores (que interconectan distintas redes, como una red doméstica con Internet).
      * Adaptadores de red (NIC): Tarjetas físicas (alámbricas o inalámbricas) integradas o de expansión que otorgan a cada equipo una identidad de hardware única llamada dirección MAC.
      * Topología física: La disposición real y tangible de los cables y dispositivos en el espacio (por ejemplo, en estrella, bus o anillo).


  *   Los elementos lógicos definen cómo se estructuran, interpretan y transportan los paquetes de datos a través de la infraestructura física.

      * Modelos de referencia (OSI y TCP/IP): Estructuras conceptuales divididas en capas que estandarizan los procesos de comunicación. Van desde la señal eléctrica pura hasta la interfaz de usuario final.
      * Protocolos de comunicación: Las reglas y lenguajes comunes que permiten a los equipos entenderse, destacando la suite TCP/IP (con protocolos fiables como TCP o rápidos como UDP).&#x20;
      * Direccionamiento lógico: El sistema de identificación numérica de los dispositivos en la red, como las direcciones IP (IPv4 o IPv6), además del uso de máscaras de subred para segmentar lógicamente el tráfico.
      * Topología lógica: La forma en que los datos viajan realmente de un nodo a otro dentro de la red, la cual puede diferir de la distribución física del cableado.


* **¿Qué dispositivos de red tenemos que aprender a configurar? ¿Qué son los protocolos? ¿Cuál es su uso?**
  * **Dispositivos de red:**&#x50;ara construir y administrar una red, se deben configurar principalmente routers (enrutadores), switches (conmutadores) y puntos de acceso inalámbricos.
  * **Los protocolos:**&#x4C;os protocolos de red son un conjunto de reglas y estándares que permiten que diferentes dispositivos se comuniquen entre sí de forma ordenada. Funcionan como un idioma común para que equipos de distintas marcas compartan información sin problemas.
  * **Uso:**&#x53;irven para organizar, enviar y recibir datos de manera segura y eficiente a través de la red. Sus funciones principales incluyen:
    * Direccionamiento: Identificar el origen y el destino de cada mensaje (por ejemplo, usando direcciones IP).
      * Formato de datos: Empaquetar la información en bloques estructurados que cualquier aparato pueda entender.
      * Control de errores: Detectar si faltan datos o si hubo fallas durante el envío para solicitar que se repitan.



## **Links**

### **Links de la actividad:**

{% embed url="https://www.ibm.com/es-es/think/topics/networking" %}

{% embed url="https://redesietsb.school.blog/la-importancia-de-las-redes/" %}

{% embed url="https://www.todofp.es/que-estudiar/familias-profesionales/informatica-comunicaciones/sistemas-microniformaticos-redes.html" %}

{% embed url="https://fpaspasia.com/salidas-laborales-fp-sistemas-microinformaticos-redes/" %}

{% embed url="https://openwebinars.net/blog/topologia-de-redes-informaticas/" %}

{% embed url="https://www.godaddy.com/resources/es/tecnologia/que-son-los-protocolos-de-red-y-cuales-son-los-mas-importantes-hoy-en-dia" %}

{% embed url="https://azure.microsoft.com/es-es/resources/cloud-computing-dictionary/what-is-virtualization" %}



{% embed url="https://submarine-cable-map-2025.telegeography.com/" %}

{% embed url="https://www.meteovigo.es/observacion/radar-de-aviones-en-tiempo-real.html" %}

{% embed url="https://www.vesselfinder.com/es" %}

{% embed url="https://satellitemap.space/" %}
