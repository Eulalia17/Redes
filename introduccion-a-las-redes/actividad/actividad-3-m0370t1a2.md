---
icon: utility-pole
---

# Actividad 3 - M0370T1A2

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

## Objetivo

Lee detenidamente:

* Los dos primeros apartados se hacen en pareja.
* El apartado “Casa” lo realiza cada miembro del grupo de manera individual, pero se incorpora al documento común.    &#x20;

## Aula – cableado UTP

1. Analiza el cableado del aula:&#x20;
   1. ¿Qué tipo de cable de red se está utilizando?És un cable UTP.
   2. ¿Qué características tiene el cable?Tiene 4 pares, reduce interferencias electromagnéticas, par trenzado, cero protección, tiene flexibilidad.
   3. ¿Qué tipo de cable le acompaña?Le acompaña el cable de alimentación es un LAN 6, de tipo UTP, es un 23AWG que tiene de anchura de 0,57mm, es un cable LSOH que significa que está libre de halógenos y tiene 4 pares. Y también es el cable verde es el de electricidad.
   4.  Investiga las normativas para cableado de comunicación y de alimentación:\
       ¿Cumple con las normativas? Argumenta. El cable de alimentación especifica los componentes de cableado,de transmisión, los modelos de sistemas y los procedimientos de medición necesarios para la verificación del cableado de par trenzado y es un TIA/EIA 568-B.2-1.

       Y el cable de comunicación explica los requisitos generales para los sistemas de cableado de telecomunicaciones de uso general, este tipo de cableado se suele encontrar estructurado en edificios comerciales e industriales.

       El cable de alimentación (TIA/EIA 568-B.2-1) y el de comunicación cumplen normativas al definir componentes y requisitos para un cableado adecuado en sistemas eléctricos y de telecomunicaciones, garantizando su correcta instalación en edificios.


   5.  Investigar en qué casos se recomienda la instalación de cableado UTP, FTP o STP.

       1. UTP: Se recomienda para oficinas y aulas sin interferencias fuertes y aparte es el más económico y el que más se utiliza actualmente.
       2. FTP: También es recomendable para oficinas o comercios pero en este caso con interferencias moderadas.
       3. STP: Este cableado es más recomendado para entornos industriales o también para zonas con un gran ruido eléctrico y cada par cuenta con su propia protección para proteger el cableado.


   6. En qué casos utilizamos cable cruzado y en cuáles directo. ¿Actualmente podemos utilizar indistintamente un tipo de cable u otro? Argumenta.
      1. Cable directo: El cable directo se utiliza para conectar dos dispositivos de red que son de tipo diferente.
      2. Cable cruzado: Sirve para conectar directamente dos dispositivos idénticos o del mismo tipo.
      3.  Actualmente sí, hoy en día se pueden utilizar prácticamente de forma indistinta debido a que la gran mayoría de los dispositivos de red modernos integran una tecnología llamada Auto-MDI/MDIX (Medium Dependent Interface/Crossover).

          <br>
   7. Especifica la velocidad máxima de transmisión que soportan los diferentes tipos de cables de par trenzado.&#x20;
      1. Cat 3: Hasta 10 Mbps y con un ancho de banda de 16 MHz.
      2. Cat 5: Hasta 100 Mbps y con un ancho de banda de 100 MHz.
      3. Cat 5e: Hasta 1 Gbps / 1000 Mbps y con un ancho de banda de 100 MHz
      4. Cat 6: Hasta 1 Gbps y hasta 10 Gbps en distancias cortas de menos de 55 metros; ancho de banda de 250 MHz.
      5. Cat 6a: Hasta 10 Gbps en tramos completos de hasta 100 metros y con un ancho de banda de 500 MHz.&#x20;
      6.  Cat 7 / Cat 8: Desde 10 Gbps hasta 40 Gbps, orientados a centros de datos y redes de alto rendimiento y también con frecuencias de 600 MHz a 2000 MHz.

          <br>
   8. Especifica el uso de cada uno de los 8 pines que componen el cable trenzado. ¿Cuántos se utilizan para transmisión?
      1. Pin 1: Transmisión de datos positivos (TX+)
      2. Pin 2: Transmisión de datos negativos (TX-)
      3. Pin 3: Recepción de datos positivos (RX+)
      4. Pin 4: No utilizado / Reservado (se utiliza habitualmente para telefonía o voz)
      5. Pin 5: No utilizado / Reservado (se utiliza habitualmente para telefonía o voz)
      6. Pin 6: Recepción de datos negativos (RX-)
      7. Pin 7: No utilizado / Reservado (o alimentación PoE)
      8. Pin 8: No utilizado / Reservado (o alimentación PoE)
      9. Para transmisión se utiliza estos dos tipos:
         1. Fast Ethernet (10/100 Mbps): Se utilizan 4 pines en los cuales 2 son para transmitir y 2 para recibir.&#x20;
         2.  Gigabit Ethernet (1000 Mbps): Se utilizan los 8 pines simultáneamente de forma bidireccional.


   9. Realiza una comparativa entre las normas TIA 568A / B y C
      1. TIA/EIA-568-A: Es de código de colores clásico (en los cuales son Blanco-Verde/Verde en los pines 1-2) y es usado tradicionalmente en entornos residenciales de Norteamérica.&#x20;
      2. TIA/EIA-568-B: Es de código de colores alternativo (en los cuales son Blanco-Naranja/Naranja en los pines 1-2); es  el estándar más utilizado universalmente en redes actuales.&#x20;
      3.  TIA-568-C: Es la actualización global que estandariza los requisitos de todo el cableado estructurado (rendimiento de cables, fibra óptica, distancias y certificación).&#x20;



## Fibra óptica

1. ¿Cuáles son las ventajas y desventajas de la fibra óptica?
   * Las ventajas de la fibra óptica:
     * Alta velocidad y ancho de banda:Permite transferencias de datos más rápidas y eficientes.
     * Menos interferencias: Es inmune a interferencias electromagnéticas.
     * Mayor distancia de transmisión: Los datos se pueden transmitir a largas distancias sin pérdida significativa de señal.
     * Seguridad: No emite señales que puedan ser interceptadas fácilmente.
   * Las desventajas de la fibra óptica:
     * Coste elevado: Es más cara en términos de material e instalación en comparación con los cables de cobre.
     * Fragilidad: Es más delicada y requiere manejo cuidadoso.
     * Reparación compleja: La reparación y empalme requieren personal especializado y equipos específicos.
2.  ¿Cómo se realiza la transmisión de datos en la fibra óptica? ¿Cuáles son los principios físicos que lo permiten? Argumenta (reflexión de la luz...) La transmisión de datos en la fibra óptica se realiza convirtiendo las señales eléctricas en pulsos de luz que viajan a través de un filamento de vidrio o plástico a gran velocidad. Conversión de datos: Un emisor (con un LED o un láser) transforma los unos y ceros del código binario de una computadora en destellos o pulsos de luz encendidos y apagados. Viaje por el cable: La luz entra al cable y avanza por su interior. Recepción: Al final del recorrido, un sensor óptico detecta los destellos de luz y los convierte otra vez en señales eléctricas que el equipo de destino puede leer. El funcionamiento de la fibra se basa en la reflexión interna total y en las leyes de la óptica. Partes del cable: El cable tiene dos zonas principales. El centro se llama núcleo (hecho de vidrio muy puro y con un índice de refracción alto, lo que significa que la luz viaja un poco más lenta allí). La capa que lo envuelve se llama revestimiento (con un índice de refracción más bajo). El choque de la luz: Cuando el rayo de luz avanza por el núcleo e intenta salir hacia el revestimiento en un ángulo inclinado muy abierto, no logra cruzar al exterior. Ángulo crítico: Si el ángulo de incidencia (el choque contra la pared) es mayor que un límite llamado ángulo crítico, la luz se refleja por completo hacia adentro del núcleo, comportándose como si las paredes fueran espejos. Avance en zigzag: Gracias a este rebote continuo y sin pérdidas de energía, la luz queda atrapada y guiada a lo largo de todo el cable, incluso si este tiene curvas.

    <br>
3. ¿Cuáles son las principales ventajas de la fibra óptica en relación con los cables de cobre? Argumenta.
   1. Mayor velocidad y ancho de banda: La fibra transmite pulsos de luz (fotones), lo que permite manejar volúmenes masivos de datos superiores a 10 Gbps, superando ampliamente la capacidad de los hilos de electricidad (electrones) del cobre.&#x20;
   2. Mayor alcance sin pérdida de señal: Los cables de cobre sufren una fuerte caída de rendimiento y se limitan por lo general a unos 100 metros de distancia por segmento. La fibra óptica monomodo puede cubrir trayectos de hasta 40 kilómetros sin necesidad de repetidores o amplificadores.&#x20;
   3. Inmunidad a las interferencias electromagnéticas: Al ser un material dieléctrico (de vidrio o silicio), la fibra no conduce electricidad. No le afectan los campos electromagnéticos de motores, electrodomésticos o tendidos eléctricos cercanos, a diferencia del cobre que actúa como una antena.&#x20;
   4. Seguridad superior: La fibra óptica no emite radiación electromagnética ni señales eléctricas susceptibles de ser interceptadas externamente, ofreciendo una transmisión de datos mucho más privada y segura.&#x20;
   5.  Durabilidad y ligereza: Los cables de fibra son más delgados, pesan mucho menos y resisten mejor la tensión mecánica y los cambios climáticos extremos que el cableado de cobre tradicional.

       <br>
4.  ¿Qué tipos de fibra óptica existen? Dependiendo del número de modos de propagación, hay dos grandes tipos de fibra óptica: monomodo y multimodo.

    Monomodo: Es una fibra óptica diseñada para transportar luz solo directamente a través de la fibra, el modo transversal.

    Multimodo: Es un tipo de fibra óptica mayormente utilizada en el ámbito de la comunicación en distancias cortas


5.  ¿Cuál es la estructura de la fibra óptica? Está constituida por un núcleo y un revestimiento, ambos cilindros concéntricos y con diferente índice de refracción, siendo el del exterior inferior al del interior. Según el uso y las condiciones a las que será sometida, la fibra óptica además se cubre externamente con una capa llamada recubrimiento.


6. ¿En qué casos se recomienda el uso de cada tipo?&#x20;

* Se recomienda usar cada tipo de fibra óptica según la distancia del enlace y el ancho de banda necesario para la instalación: Fibra Monomodo (SMF): Tiene un núcleo muy estrecho que permite que la luz viaje en línea recta sin rebotar.
* Casos recomendados: Largas distancias: Enlaces de decenas o miles de kilómetros, como conexiones submarinas, internacionales y redes de operadores de telecomunicaciones. Conexiones de alta velocidad y hogar (FTTH): Llevar internet de alta velocidad con baja latencia directamente a los hogares y edificios. Grandes redes metropolitanas (MAN): Comunicar diferentes zonas de una ciudad o regiones extensas. Fibra Multimodo (MMF): Tiene un núcleo más ancho por el que viajan múltiples rayos de luz, lo que limita la distancia debido a la dispersión de la señal.
* Casos recomendados: Cortas distancias: Enlaces usualmente inferiores a 500 metros o máximo 2 kilómetros. Redes locales (LAN): Conexiones dentro de una misma oficina, campus universitario o edificios corporativos. Centros de datos (Data Centers): Interconexión de servidores y equipos de red en espacios reducidos por su bajo costo en los equipos de transmisión.



7.  ¿Cuáles serían las limitaciones a la hora de implementar y mantener redes de fibra óptica?  La implementación y el mantenimiento de las redes de fibra óptica ofrecen un rendimiento excepcional en ancho de banda y velocidad, pero se enfrentan a importantes limitaciones técnicas, económicas y logísticas.

    🛠️ Limitaciones en la Implementación (Instalación)

    * Altos costos iniciales: El despliegue de infraestructura requiere una inversión económica muy elevada. Los componentes (cables de fibra, transceptores láser, amplificadores) y la obra civil especializada encarecen enormemente el proyecto en comparación con tecnologías inalámbricas o de cobre. Fragilidad física del material: El núcleo del cable está hecho de vidrio de alta pureza. Esto significa que los cables no se pueden doblar en ángulos muy pronunciados (tienen un radio de curvatura limitado) ya que se quiebran con facilidad o provocan pérdidas por atenuación del haz de luz. Complejidad y obra civil: La instalación suele requerir permisos gubernamentales para realizar zanjas, perforaciones o despliegues aéreos en postes. Esto ralentiza los tiempos de ejecución y genera fricciones en zonas urbanas densamente pobladas. Mano de obra altamente calificada: No cualquier técnico puede instalar fibra óptica. Se necesitan profesionales capacitados en el uso de herramientas de precisión, como las cortadoras de fibra y las fusionadoras de arco eléctrico.

    🔧 Limitaciones en el Mantenimiento y Operación

    * Dificultad de reparación (Empalmes complejos): Cuando un cable de cobre se rompe, se puede unir de forma relativamente sencilla. Si un hilo de fibra óptica se corta, repararlo exige un proceso de fusión milimétrico mediante equipos costosos. Cualquier desalineación de micrómetros arruinará la transmisión de datos. Vulnerabilidad a daños físicos: Los cables enterrados sufren frecuentemente cortes accidentales por excavaciones de otras obras públicas (el conocido "efecto excavadora"). Además, en tendidos aéreos, están expuestos a tormentas, caída de árboles e incluso al vandalismo o mordeduras de roedores. Equipos de diagnóstico costosos: Para localizar una falla o ruptura en una línea de kilómetros de longitud, se necesitan herramientas de alta tecnología muy caras, como el OTDR (Reflectómetro del Dominio de Tiempo Óptico). Incompatibilidad eléctrica directa: La fibra óptica transmite luz, no electricidad. Esto significa que los dispositivos finales (computadoras, routers) no pueden procesar la señal directamente; se requieren conversores óptico-eléctricos en los nodos, los cuales consumen energía y añaden puntos potenciales de falla en la red.

## Cableado estructurado

1.  ¿Qué es el cableado troncal y cuál es la función principal en una infraestructura de red? El cableado troncal es la columna vertebral de la red de un edificio. Consiste en los cables, distribuidores y elementos de conexión que unen entre si las distintas salas de equipos, armarios de telecomunicaciones y la entrenada de servicios del edificio.

    Su función principal consiste en interconectar y transportar el tráfico masivo de datos entre las diferentes zonas y plantas del edificio. Concentra todo el caudal que proviene de las distintas áreas  de trabajo para canalizarlo hacia los servidores principales , los switches principales y los routers de salida a internet.


2. ¿Cuáles son las diferencias entre cableado troncal de cobre y cableado troncal de fibra?¿En qué casos se debe elegir una u o otra? Diferencias principales

| Características             | Troncal de cobre                                               | Troncal de fibra óptica                                          |
| --------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------- |
| Ancho de banda              | Limitado en distancias largas                                  | Prácticamente limitado (gigabytes/terabytes por segundo)         |
| Distancia máxima            | Registrada normalmente a 100 metros por segmento               | Puede alcanzar kilómetros sin perder señal                       |
| Inmunidad a interferencias  | Vulnerable a ruido electromagnético (motores, luces, etc.).    | Totalmente inmune a interferencias electromagnéticas (EMI/RFI).  |
| Tamaño y peso               | Mangueras de cables gruesas y pesadas.                         | Cables muy delgados, ligeros y fáciles de canalizar.             |
| Coste                       | Electrónica de red más barata, cable de mayor coste por peso.  | Electrónica (transceptores) más cara, pero idónea a largo plazo  |

Elegir Cobre:

* En trayectos muy cortos (menos de 50–90 metros) dentro del mismo edificio o entre armarios muy cercanos.
* Cuando el presupuesto inicial para la electrónica de red es reducido.
* Para conexiones auxiliares de baja velocidad o telefonía tradicional (cables multipar).

Elegir Fibra Óptica:

* Interconexión entre plantas o entre edificios distintos (troncal de campus).
* En trayectos que superen los 90–100 metros.
* En entornos industriales o zonas con fuerte ruido electromagnético (junto a motores, ascensores o líneas de alta tensión).
* Cuando se busca preparar la red para el futuro (10G, 40G, 100G Speed) sin tener que sustituir el cableado



3.  Revisa la webgrafía que te adjunto y explica la estructura del cableado estructurado atendiendo a:

    1. cableado vertical
    2. sala central de equipamiento
    3. armario de telecomunicaciones
    4. áreas de trabajo
    5. toma del edificio

    Sala central de equipamiento: Es el espacio centralizado donde se ubican los servidores principales, los switches troncales y los equipos de red principales que gestionan todo el tráfico del edificio.

    Armario de telecomunicaciones: Son los espacios repartidos por las diferentes plantas o zonas que albergan los paneles de parcheo (patch panels) y los switches secundarios para distribuir la red localmente.

    Cableado vertical: Es la columna vertebral de la red. Consiste en el cableado de alta capacidad (generalmente fibra óptica) que interconecta la sala central de equipamiento con los distintos armarios de telecomunicaciones de las plantas.

    Áreas de trabajo: Son las zonas físicas donde se sitúan los usuarios con sus dispositivos finales (ordenadores, teléfonos, impresoras) conectados a las rosetas de pared mediante latiguillos.

    Toma del edificio: Es el punto físico de entrada por donde los servicios de telecomunicaciones externos (proveedores de internet, líneas de operadores) penetran al edificio para conectarse con la red interna.

    <br>

## Investiga herramientas de diseño de redes

Investiga las diferentes herramientas existentes en el mercado para diseñar una red.&#x20;

Rellena la siguiente tabla con tres opciones:

| Herramienta                            | Características                                                                                                                      | Gratis / Pago                                                                             |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| <p><br></p><p>Cisco Packet Tracer </p> | <p><br></p><p>Es el simulador oficial </p><p>de Cisco para diseñar </p><p>y configurar redes </p><p>con dispositivos virtuales. </p> | <p><br></p><p>Es Gratis (Requiere </p><p>cuenta de Cisco </p><p>Networking Academy). </p> |
| GNS3                                   | Es un simulador de código abierto que emula sistemas operativos de red reales .                                                      | Gratis                                                                                    |
| Lucidchart                             | Es una herramienta de diagramación en la nube para crear topologías y esquemas de red de forma colaborativa.                         | Freemium (Versión gratuita limitada y planes de pago)                                     |

## Tu casa&#x20;

1. Analiza e investiga la instalación de la red de tu casa.¿Qué tipo de fibra llega a tu casa: monomodo o multimodo? Argumenta
   1.  En casa de Eulalia:

       La fibra que llega es monomodo, porque tiene la instalación de Movistar. Movistar opera sobre redes FTTH (Fiber to the Home) con tecnología GPON, la cual trabaja exclusivamente con fibra monomodo para cubrir grandes distancias desde la central hasta el domicilio sin degradación de la señal.

       En la instalación de interior utilizan la normativa ITU-T G.657A2. Es un tipo de fibra monomodo ultra-flexible especialmente diseñada para interiores, ya que permite doblarse en esquinas y rincones muy cerrados sin que se atenúe o se pierda la señal de internet. Los latiguillos y rosetas que instala Movistar utilizan conectores SC/APC. Son fácilmente reconocibles porque el plástico exterior del conector es de color verde (indicativo de su pulido en ángulo de 8° para evitar reflexiones) y el latiguillo óptico de conexión suele ser de color amarillo.


   2.  En casa de David:&#x20;

       La fibra que llega es monomodo (SMF). Al igual que en la instalación de    Movistar FTTH (Fiber to the Home), se utiliza esta tecnología porque permite transmitir los datos mediante pulsos de luz a lo largo de grandes distancias desde la central de la compañía hasta el hogar sin que la señal sufra pérdidas ni degradación.<br>
2. Especifica los tipos de cables que intervienen en la configuración
   1.  En casa de Eulalia:

       El dispositivo receptor de la señal de red en la habitación es un Descodificador UHD Movistar+ fabricado por ARRIS (Modelo A 00412518 / VIP5242A), el cual recibe los datos de red por el cable Ethernet amarillo conectado a su puerto posterior.

       Este decodificador está conectado directamente al equipo principal de la vivienda, que es el Router Smart WiFi (HGU / Home Gateway Unit) de Movistar.

       Especificaciones del Router Smart WiFi de Movistar (HGU):

       * Tipo de equipo: Dispositivo "3 en 1" que integra ONT GPON + Router + Punto de Acceso Wi-Fi.
       * Entrada de red (WAN): 1 puerto óptico SC/APC (GPON) de fibra monomodo.
       * Puertos de red local (LAN): 4 puertos Gigabit Ethernet (RJ45) a 10/100/1000 Mbps (donde se conecta el cable Ethernet amarillo hacia el descodificador ARRIS).
       * Puerto de telefonía: 1 puerto RJ11 (FXS) para la línea fija mediante VoIP.
       * Conectividad Wi-Fi (Doble Banda simultánea):
       * Banda 2.4 GHz: Wi-Fi 4 (802.11n), hasta 300 Mbps (mayor alcance).
       * Banda 5 GHz: Wi-Fi 5 (802.11ac), con 4 antenas internas en configuración 4x4 MIMO (máxima velocidad de la fibra).
       * Indicadores LED: Panel frontal con luces indicadoras de estado para Red, Internet, Wi-Fi, Wi-Fi + y Teléfono.

       b. En casa de David:

       Tengo un router Smart WiFi (HGU) de Movistar.&#x20;

       Tipo de equipo: Un dispositivo "3 en 1" que integra ONT GPON, router y punto de acceso Wi-Fi.

       Puertos: 1 entrada óptica SC/APC (GPON), 4 puertos gigabit ethernet (RJ45) a 10/100/1000 Mbps y 1 puerto RJ11 para telefonía fija.

       Conectividad Inalámbrica: Tiene doble banda simultánea (2.4 GHz con Wi-Fi 4 y 5 GHz con Wi-Fi 5 de alta velocidad).


3. ¿Qué tipo de router tienes? Las especificaciones del mismo.
   1.

       En casa de Eulalia:

       El dispositivo receptor de la señal de red en la habitación es un Descodificador UHD Movistar+ fabricado por ARRIS (Modelo A 00412518 / VIP5242A), el cual recibe los datos de red por el cable Ethernet amarillo conectado a su puerto posterior.

       Este decodificador está conectado directamente al equipo principal de la vivienda, que es el Router Smart WiFi (HGU / Home Gateway Unit) de Movistar.

       Especificaciones del Router Smart WiFi de Movistar (HGU):

       * Tipo de equipo: Dispositivo "3 en 1" que integra ONT GPON + Router + Punto de Acceso Wi-Fi.
       * Entrada de red (WAN): 1 puerto óptico SC/APC (GPON) de fibra monomodo.
       * Puertos de red local (LAN): 4 puertos Gigabit Ethernet (RJ45) a 10/100/1000 Mbps (donde se conecta el cable Ethernet amarillo hacia el descodificador ARRIS).
       * Puerto de telefonía: 1 puerto RJ11 (FXS) para la línea fija mediante VoIP.
       * Conectividad Wi-Fi (Doble Banda simultánea):
       * Banda 2.4 GHz: Wi-Fi 4 (802.11n), hasta 300 Mbps (mayor alcance).
       * Banda 5 GHz: Wi-Fi 5 (802.11ac), con 4 antenas internas en configuración 4x4 MIMO (máxima velocidad de la fibra).
       * Indicadores LED: Panel frontal con luces indicadoras de estado para Red, Internet, Wi-Fi, Wi-Fi + y Teléfono.

       b. En casa de David:

       Tengo un router Smart WiFi (HGU) de Movistar.&#x20;

       Tipo de equipo: Un dispositivo "3 en 1" que integra ONT GPON, router y punto de acceso Wi-Fi.

       Puertos: 1 entrada óptica SC/APC (GPON), 4 puertos gigabit ethernet (RJ45) a 10/100/1000 Mbps y 1 puerto RJ11 para telefonía fija.

       Conectividad Inalámbrica: Tiene doble banda simultánea (2.4 GHz con Wi-Fi 4 y 5 GHz con Wi-Fi 5 de alta velocidad).<br>

## Diseña

Selecciona una de las herramientas gratuitas anteriores y utilízala para diseñar las redes de casa y del aula. La red del aula no necesita tener los 36 equipos que tenemos. Argumenta tu decisión en el uso de esa herramienta en detrimento de las demás.

1. Escribe la IP de un dispositivo de tu casa, por ejemplo, el móvil.
   1.  En casa de Eulalia:

       Dirección IPv4 del equipo (PC/Portátil): 192.168.1.56 (obtenida a través del "Adaptador de LAN inalámbrica Wi-Fi").

       Puerta de enlace predeterminada (Router Movistar): 192.168.1.
   2.  En casa de David:

       Dirección IPv4 de mi PC: Es la IP 192.168.1.46.

       Puerta de enlace predeterminada (Router): 192.168.1.1<br>
2. ¿Qué topología se implementa en la red: bus, árbol, estrella...?&#x20;
   1.  En casa de Eulalia: La topología que se implementa en la red doméstica es en Estrella.

       Justificación: Todos los dispositivos de la casa (tu ordenador con IP 192.168.1.56, teléfonos móviles, descodificador de televisión, Smart TV, etc.) Se conectan de forma centralizada al Router Smart WiFi de Movistar (que actúa con la IP 192.168.1.1 como punto de acceso y conmutador central).
   2.  En la casa de David:

       La tipología que se implementa es una topología estrella.


3.  ¿Qué características tiene ese tipo de topología?

    1.  En casa de Eulalia:

        Las características claves de la tipología estrella

        * Nodo central concentrador: Todos los equipos envían y reciben la información a través del equipo central (el router doméstico 192.168.1.1), el cual gestiona el tráfico entre los dispositivos de la red local e Internet.
        * Aislamiento de fallos: Si un dispositivo pierde la conexión (por ejemplo, si se apaga el Wi-Fi del móvil o se desconecta el ordenador), el resto de la red sigue funcionando sin verse afectado.
        * Fácil instalación y gestión: Añadir un nuevo equipo a la red (por cable Ethernet o mediante Wi-Fi) es inmediato y no interrumpe el servicio de los demás.
        * Dependencia del punto central (Punto único de fallo): Si el router central se apaga, se avería o se reinicia, toda la red local de la vivienda se queda sin conexión entre los dispositivos y sin acceso a Internet.





        <img src="../../.gitbook/assets/unknown (1).png" alt="" height="243" width="624">


    2. En casa de David:  Todos los equipos de la casa se conectan de forma centralizada al Router Smart WiFi. En caso de que si un dispositivo se desconecta o falla, el resto de la red sigue funcionando con total normalidad; sin embargo, si el router central se apaga, toda la red local e Internet dejan de estar accesibles.&#x20;



<img src="../../.gitbook/assets/unknown (2).png" alt="" height="243" width="624">



## Enlaces

{% embed url="https://unitel-tc.com/normas-sobre-cableado-estructurado/" %}

{% embed url="https://cablematic.com/" %}

{% embed url="http://www.cabletec.es/noticia/utp-frente-a-stp-ftp-cual-es-la-mejor-opcion-para-una-instalacion-17" %}

{% embed url="https://www.syscomblog.com/2017/12/cuanto-hay-que-separar-los-cables.html" %}

{% embed url="http://www.ing.ula.ve/~javierj/eslared/cableado/dia3/referencias/TIA-EIA-568-C_resumen.pdf" %}

{% embed url="https://www.youtube.com/watch?v=LYicldCPKrc" %}

{% embed url="https://www.adrformacion.com/knowledge/administracion-de-sistemas/el_cableado_estructurado_de_una_red_de_area_local.html" %}

{% embed url="https://www.redestelecom.es/infraestructuras/cableado-estructurado-que-es-tipos-y-utilidades/" %}
