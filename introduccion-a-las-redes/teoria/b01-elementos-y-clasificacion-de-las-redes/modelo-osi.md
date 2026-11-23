# Modelo OSI

> Transcripción del PDF «Modelo OSI» (43 páginas). Se mantiene el orden y el contenido textual del documento. Los elementos gráficos que no se pueden reproducir como texto están señalados con etiquetas para que puedas insertar la imagen o el diagrama correspondiente desde el PDF original.

## Página 1 — Portada

Ciclo Formativo de ASIX\
Septiembre 2026

**ETIQUETA — Foto de portada: alumnado trabajando con ordenadores y logotipo de PlanetaFP. Página 1.**

## Página 2 — Modelo OSI - TCP/IP – ATM – Microsoft

**ETIQUETA — Portada/título visual «Modelo OSI - TCP/IP – ATM – Microsoft», con logotipo de PlanetaFP. Página 2.**

## Página 3 — Pasos en la comunicación

En la red, si queremos establecer una comunicación entre dos equipos informáticos, debemos utilizar las normas de comunicación definidas en los protocolos de red que se utilizan.

**ETIQUETA — Diagrama del proceso de comunicación: «Mensaje a enviar → Codificación → Transmisión → Medio → Recepción → Decodificación → Mensaje recibido». Página 3.**

## Página 4 — Un protocolo de red debe definir

* **Codificación del mensaje:** cuando enviamos un texto o una imagen, el equipo solo puede utilizar ceros y unos para codificar la información.
* **Formateado y encapsulación del mensaje:** según el protocolo utilizado, los datos se estructurarán de modo que determinen la información necesaria para que el protocolo pueda procesarla.
* **Definición del tamaño del mensaje:** ha de tener un tamaño predefinido, tanto en tamaño máximo como en mínimo.
* **Tiempos de entrega de los mensajes:** la latencia que puede soportar la entrega de un mensaje es vital para que la comunicación sea viable.
* **Opciones de entrega de los mensajes:** un mensaje puede incluir información para el control de su entrega.

## Página 5 — Ejemplo

* Un acuse de recibo garantiza la entrega.
* Un control de validación del mensaje muestra que el mensaje no se ha corrompido en tránsito; y
* Un mensaje de apertura o de cierre puede permitir que una comunicación se establezca o se dé por cerrada entre ambas partes de la comunicación.

## Página 6 — OSI

1. En la década de 1990 la apuesta inicial por OSI demostró ser un error.
2. Los plazos de desarrollo se alargaron más de lo previsto;
3. Universidades y centros de investigación evolucionaron muy rápido, y migraron a protocolos como TCP/IP, que a finales de los 80 ya se consolidaba como un estándar de facto para la interconexión de sistemas abiertos.

Este hecho iba de la mano con la evolución de los sistemas informáticos: que pasaron de una arquitectura basada en grandes equipos centrales a los que se accedía mediante terminales (propio de los inicios de los 80), a la implantación de la informática distribuida conectada por medio de redes locales, a principios de los años 90.

## Página 7 — Algo de historia - Modelo OSI

* En la década de 1970 surgen redes de diferentes fabricantes, donde cada una tenía su propio conjunto de protocolos y estándares. Esto trajo incompatibilidades y dificultades para que los equipos de diferentes proveedores se comunicaran entre sí.
* La llamada organización Internacional de Normalización (ISO) creó el grupo de trabajo «Grupo de Estudio de Redes Abiertas» - Open Systems Interconnection Working Group - para abordar el problema de la falta de estándares de red. El objetivo: desarrollar un conjunto de estándares de red que permitiera la interoperabilidad entre sistemas de diferentes fabricantes.
* Década de los 80: La ISO lanzó el modelo OSI como un esfuerzo para estandarizar la arquitectura de redes.
* Cierto que el modelo OSI proporcionó un marco teórico para la comunicación en la red, pero no logró una adopción generalizada en la industria de la tecnología. En su lugar se utilizaron otras tecnologías y protocolos, como el conjunto de protocolos TCP/IP, que terminó siendo un estándar dominante en la práctica.
* Décadas posteriores: A pesar de no haberse convertido en el modelo dominante, el modelo OSI siguió siendo un marco teórico valioso en el campo de la informática y las redes. Se utilizó en la educación y en el diseño de sistemas de comunicación en algunas organizaciones.
* Hoy en día, el modelo OSI sigue siendo una referencia importante en la comprensión de las redes de computadoras y las comunicaciones, aunque en la práctica, la mayoría de las redes se basan en el conjunto de protocolos TCP/IP. Aunque no fue ampliamente adoptado en la implementación práctica, el modelo OSI desempeñó un papel crucial en el desarrollo de estándares de red y en la comprensión de las redes de computadoras a nivel teórico.

## Página 8 — OSI

Este modelo de referencia de interconexión de sistema abierto (OSI) por sus siglas en inglés Open System Interconnection) está basado en una división de siete capas, y en cada una se define una parte de las funciones que permiten el envío de datos por la red.

## Página 9 — OSI

Se le llama **CAPA** a cada uno de los diferentes niveles independientes en que está estructurado el modelo.

* La capa n ofrece una serie de servicios a la capa n + 1.
* La capa n sólo ve los servicios que le ofrece la capa n – 1.
* La capa n en un determinado sistema sólo se comunica con su homóloga en el sistema remoto (comunicación de igual a igual o peer-to-peer).

Esta conversación se efectúa de acuerdo a una serie de reglas conocidas como protocolo de la capa n.

## Página 10 — Modelo OSI - ventajas

* Divide la comunicación en partes más pequeñas y sencillas.
* Facilita la normalización de los componentes de la red, con lo que permite el desarrollo y el apoyo de diferentes fabricantes.
* Permite que diferentes tipos de hardware (hardware) y programas (software) se comuniquen entre ellos.
* Impide que los cambios en una capa afecten las otras, lo que permite un desarrollo más acelerado.
* Divide la comunicación de la red en partes más pequeñas y hace más fácil su comprensión.

## Página 11 — Pila de protocolos: OSI y TCP/IP

El conjunto de protocolos que utiliza una determinada arquitectura en todas sus capas se denomina pila de protocolos, con lo que es frecuente escuchar hablar de la pila de protocolos OSI y TCP/IP.

En función de cómo se establezca la comunicación entre capas se distinguen dos tipos de servicios:

1. Orientados a conexión.
2. No orientados a conexión.

## Página 12 — OSI

* **Capa 1:** capa física.
* **Capa 2:** capa de enlace de datos.
* **Capa 3:** capa de red.
* **Capa 4:** capa de transporte.
* **Capa 5:** capa de sesión.
* **Capa 6:** capa de presentación.
* **Capa 7:** capa de aplicación.

**ETIQUETA — Diagrama «Las 7 capas del modelo OSI»: representación de transmisión y recepción, con las capas de aplicación, presentación, sesión, transporte, red, enlace y físico. Página 12.**

## Página 13 — OSI

**ETIQUETA — Ilustración en perspectiva de las siete capas OSI apiladas, con ejemplos de funciones y protocolos en cada nivel. Página 13.**

## Página 14 — Capa 1 - física

* Se ocupa de la **transmisión de bits** usando un canal de comunicación, y también de definir las características del canal.
* Regula aspectos de la comunicación como el tipo de señal (analógica, digital), el esquema de codificación, sincronización de los bits, tipo de modulación, tipo de enlace (punto a punto, punto a multipunto).
* Regula el modo de comunicación (duplex, half-duplex o simplex), tasa de bits (número de bits por segundo), topología usada, y, en general, todas las cuestiones eléctricas, mecánicas, señalización y procedimiento en la interfaz física (cables, conectores, enchufes ...) entre los dispositivos que se comunican.
* Especifica características como los niveles de tensión eléctrica, las frecuencias, la velocidad de datos físicas, las distancias de transmisión, los conectores empleados, tipos de cables o de fibras ópticas o radioenlaces, y otros atributos similares son especificaciones de la capa física.

**Estándares de cables y dispositivos, Hubs o tarjetas de red.**

## Página 15 — Capa 2 - enlace de datos

* Divide un enlace de datos en varias conexiones físicas.
* **Control de flujo:** regula la velocidad a la cual la capa de enlace trabaja dinámicamente.
* Proporciona parámetros de **Calidad de Servicio (QoS):**
  * Tiempo medio entre fallas, BER (Bit Error Rate).
  * Disponibilidad de servicio.
  * Retardo en el tránsito.
* **Detección de errores:**
  * CRC - Control de Redundancia Cíclica.
* **Corrección de errores:**
  * ARQ - Allowed to ReQuest.
  * FEC - Forward Error Control.
* La IEEE lo subdivide en dos capas:
  * MAC - Medium Access Control.
  * LLC - Logical Link Control.

## Página 16 — Capa 2 - Enlace de datos

La capa de enlace de datos se ocupa del direccionamiento físico, de la topología de red, del acceso a la red, de la notificación de errores, de la distribución ordenada de tramas y del control de flujo de datos.

La capa de enlace de datos proporciona un tránsito de datos fiable a través de un enlace físico.

**Switches**

**Resumiendo**

**ETIQUETA — En la diapositiva aparece el rótulo «Switches» y una flecha hacia «Resumiendo». Página 16.**

## Página 17 — Capa 3 - red

* La tarea fundamental de este nivel es:
  * El enrutado.
  * La conmutación de paquetes.
* El trabajo de esta capa va acorde al tipo de conexión y es muy variable.
* Se ocupa del direccionamiento lógico y puede utilizar diferentes protocolos, dependiendo del modelo de comunicación (IP, IPX ...).
* Se controla el encaminamiento de los paquetes de comunicación, es decir, la selección de la ruta que seguirán los paquetes desde el terminal origen hasta el terminal destino.
* Sus funciones y servicios son:
  * Encaminamiento y retransmisión (define las rutas a seguir).
  * Conmutación de paquetes.
  * Multiplexación de conexiones de red.
  * Establecimiento de circuitos virtuales.
  * Direccionamiento de red.

**Routers y protocolos como el ARP, ICMP o IP.**

## Página 18 — Capa 3 - red

Por tanto, determina por dónde se tiene que enviar la información para que pueda llegar al destinatario, diferenciando si se trata de tráfico interno de nuestra propia red o si se tiene que reenviar a un router para que la encamine fuera de ella.

**Resumiendo**

**ETIQUETA — Flecha roja que señala el apartado «Resumiendo». Página 18.**

## Página 19 — Capa 4 - Transporte

Su misión fundamental es la **conexión de extremo a extremo**.

Incluye las funciones de establecer, mantener y finalizar los circuitos virtuales de comunicación, utiliza la detección y corrección de errores en el transporte, y la información del control del flujo de los datos.

La capa de transporte **segmenta los datos** del sistema emisor para que sean más fácilmente transportables, y las une y reorganiza en el sistema receptor.

También tiene las funciones de multiplexar y demultiplexar, que permite dirigir la información recibida de la capa de red hacia la aplicación que lo necesita.

En la capa aplicación pueden haber diferentes procesos ejecutándose, como FTP, HTTP o SSH y la capa transporte debe dirigir el proceso correspondiente.

## Página 20 — Capa 4 - Transporte

**TCP, UDP, PUERTOS**

* La tarea fundamental de este nivel es:
  * Conexión de extremo a extremo (end to end).
* Permite al usuario elegir entre distintas calidades de servicio.
* Optimiza la relación costo beneficio.
* Se definen cinco clases que van desde la cero (sin recuperación y eliminando paquetes dañados) hasta la cuatro (Detección y corrección de errores extendida).
* Funciones y servicios:
  * Correspondencia entre direcciones de transporte y de red.
  * Supervisión de red.
  * Facturación de extremo a extremo.

## Página 21 — Capa 5 - Sesión

La capa de sesión establece, administra y finaliza las sesiones de comunicación entre dos equipos terminales.

Las capas de aplicación, presentación y sesión son capas específicas para cada modelo de aplicación.

Las capas de transporte, red, enlace y física son capas específicas de transmisión de datos.

## Página 22 — Capa 5 - Sesión

Sus funciones y servicios fundamentales:

* Establecimiento del diálogo Half Dúplex o Full Dúplex.
* Reseteado de sesión a un punto preestablecido.
* Establecimiento de puntos de control en el flujo de datos para comprobaciones intermedias y recuperación durante la transferencia de archivos.
* Abortos y rearranques.

**NetBIOS – NetBEUI**

## Página 23 — Capa 6 - Presentación

Asegura que la información transmitida por la capa de aplicación podrá ser utilizada por la capa de aplicación del receptor.

Traduce los diferentes formatos de datos, para lo que utiliza un formato común. Una de las tareas más importantes de la capa de presentación es el cifrado y descifrado.

Ejemplo: los protocolos NetBios (Novell) y XDR (External Data Representation, representación de datos externa) es un protocolo de presentación de datos. Permite la transferencia de datos entre máquinas de diferentes arquitecturas y sistemas operativos.

## Página 24 — Capa 7 - Aplicación

Permite al usuario acceder a la red. Provee de las interfaces de usuario y soporte para servicios como el correo electrónico, transferencia de archivos, administración de bases de datos compartidas y otros tipos de servicios distribuidos.

La capa de aplicación es la más cercana al usuario. Proporciona servicios de red a las aplicaciones del usuario, por ejemplo acceso a ficheros, acceso a impresoras ...

Es la única capa que no proporciona ningún servicio a ninguna otra capa. Esta capa sincroniza y da servicio a la recuperación y el control de errores y la integridad de los datos.

Como protocolos de ejemplo de esta capa encontramos el HTTP (Hipertexto Transfer Protocol, protocolo de transferencia de hipertexto) que es el protocolo usado por el World Wide Web, que permite solicitar y recibir páginas webs y FTP (File Transfer protocolo, protocolo para la transferencia de archivos).

**SMTP, Telnet, FTP**

**ETIQUETA — Rótulo verde con ejemplos de protocolos de aplicación y pequeños elementos gráficos de la diapositiva. Página 24.**

## Página 25 — Direccionamiento – una analogía para comprender

El direccionamiento abarca más de un nivel del modelo. Hagamos una analogía con una carta postal.

* Al usuario final, la única dirección que le interesa es la del domicilio postal al que desea enviar su carta.
* Detrás del mismo, existe todo un sistema diseñado que permite que la carta llegue a su destino:
  * La carta es depositada en un buzón que, a su vez, es colocada en una determinada bolsa.
  * La bolsa tiene un código de identificación sólo conocido por los empleados de las sucursales de correo.
  * Esta bolsa se dirigirá hacia un avión, ferrocarril, camión, etc. con una identificación de vuelo, andén, etc. conocido por los empleados del ferrocarril, aeropuerto o transporte correspondientes.
  * Este proceso se puede desglosar hasta el mínimo detalle formando parte de un conjunto de direccionamiento absolutamente desconocido para un usuario final.

**ETIQUETA — Esquema/ilustración de la analogía del direccionamiento mediante una carta postal. Página 25.**

## Página 26 — TCP/IP (Transmission Control Protocol/Internet Protocol)

Nació de los trabajos de la ARPA (Advanced Research Project Agency, agencia de proyectos avanzados de investigación) del Departamento de Defensa de EE.UU. (1960 – 1970).

Este modelo consta de 4 capas:

1. Capa de aplicación.
2. Capa de transporte.
3. Capa de Internet.
4. Capa de acceso a la red.

**ETIQUETA — Diagrama de las cuatro capas del modelo TCP/IP. Página 26.**

## Página 27 — TCP/IP

El conjunto de protocolos TCP/IP fue el elegido para el uso de Internet por los desarrolladores de ésta, y el tiempo quiso que se convirtiera en el protocolo de facto para el uso de las comunicaciones de red de la mayoría de los proveedores de servicios de red.

TCP/IP tiene su propio modelo de capas similar al del modelo OSI.

En lugar de siete capas, tenemos únicamente cuatro.

## Página 28 — Capa de aplicación

Aspectos de representación, codificación y control del diálogo, es decir, los protocolos de las aplicaciones que generan los datos que se transmiten por la red.

Realiza las funciones de las capas de:

* Aplicación.
* Presentación.
* Sesión.

del modelo OSI.

## Página 29 — Capa de transporte

* Establecer la transmisión de información sin ningún tipo de error.
* Es la encargada de tratar los aspectos relacionados con la calidad del servicio desde el punto de vista del control del flujo y la corrección de los errores.

**TCP (transport control protocol)**\
**UDP (user datagram protocol)**

## Página 30 — Capa de Internet

* Realiza las funciones de la capa de red del modelo OSI.
* Permite que se puedan enviar paquetes de datos desde cualquier punto independientemente del tipo de red y de la ruta utilizada.
* Provee de la funcionalidad para las comunicaciones entre redes a través de enrutadores.

Se puede interpretar esta red como un sistema postal, dado que cuando se envía una carta no se sabe qué ruta ha tomado el cartero para llevarla a su destino. Sencillamente, interesa que la carta llegue.

## Página 31 — Capa de acceso a la red

Realiza las funciones de la capa de enlace de datos física.

Es independiente de la tecnología física que se utiliza; por eso, no siempre se asocia esta capa con la capa física del modelo OSI, pero nosotros sí la asociaremos por claridad en la representación.

## Página 32 — TCP/IP y OSI

Existe mucha correlación que hay entre los modelos TCP/IP y OSI.

Cuando hablamos de las capas del modelo TCP/IP utilizamos la numeración de capa correspondiente en el modelo OSI.

Por tanto: el protocolo Internet es de capa 3 tal como sería su equivalente en OSI y la capa de aplicación de TCP/IP sería de capa 7.

**ETIQUETA — Esquema comparativo de correspondencia entre las capas TCP/IP y OSI, con flechas entre ambos modelos. Página 32.**

## Página 33 — TCP/IP

**ETIQUETA — Diagrama de la pila TCP/IP con sus capas y ejemplos de protocolos organizados por nivel. Página 33.**

## Página 34 — TCP/IP

**ETIQUETA — Diagrama de flujo/arquitectura del modelo TCP/IP: representación de las capas y de la comunicación entre ellas. Página 34.**

## Página 35 — OSI vs TCP/IP

**ETIQUETA — Cuadro gráfico comparativo de las capas del modelo OSI y del modelo TCP/IP. Página 35.**

## Página 36 — OSI vs TCP/IP

| Característica                                                                     | Modelo OSI                                                                                                   | TCP / IP                                                                              |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| Modelo                                                                             | Teórico                                                                                                      | Implementación                                                                        |
| Tecnología utilizada                                                               | Ex. IEEE 802.3                                                                                               | Conmutación por paquetes                                                              |
| Número de capas                                                                    | 7                                                                                                            | 4                                                                                     |
| Servicios orientados a la conexión (CONS) y los no orientados a la conexión (CLNS) | Soporta CONS y CLNS en la capa de red. Únicamente CONS en la capa de transporte (la que percibe el usuario). | Soporta CLNS en la capa de red. Soporta las dos modalidades en la capa de transporte. |

**ETIQUETA — Tabla original comparativa «OSI vs TCP/IP». Página 36. Insertar la captura si se desea conservar exactamente el diseño de la tabla.**

## Página 37 — ATM - modo de transferencia asíncrona (Asynchronous Transfer Mode)

## Página 38 — ATM — Asynchronous Transfer Mode

Definido por las normas de las organizaciones ANSI y ITU (International Telecommunications Union).

Definido para el transporte de señales de voz, datos y video entre otros.

Desarrollado para satisfacer las necesidades de la red digital de servicios integrados de banda ancha a finales de los años 1980.

Utilizan su propio modelo de referencia, muy diferente de OSI y TCP/IP.

Es un modelo en 3 capas (algunas divididas en subcapas):

* Capa física.
* Capa ATM.
* Capa de adaptación de ATM.

Ninguna coincide exactamente con las capas de OSI.

**ETIQUETA — Esquema gráfico de las tres capas ATM y sus subcapas. Página 38.**

## Página 39 — ATM

Es una arquitectura en tres dimensiones.

**ETIQUETA — Diagrama tridimensional de la arquitectura ATM y sus planos/capas. Página 39.**

## Página 40 — ATM

**ETIQUETA — Diagrama de la arquitectura ATM: relación entre los nodos/usuarios, el modo ATM y los planos de control, usuario y gestión. Página 40.**

## Página 41 — ATM

**Capa física:** relacionada directamente con la red y el medio de transmisión. La información puede transmitirse utilizando protocolos de comunicación de la red sobre la que funcione.

**Capa ATM:** responsable del transporte de las celdas por la red y del establecimiento y liberación de las conexiones. Decide la ruta que van a seguir las celdas de información y de control de la congestión.

**Capa de adaptación ATM:** divide toda la información que se quiere transmitir en celdas y las reensambla en el otro extremo. Es aconsejable que las aplicaciones trabajen directamente con celda (y ocultar los detalles de diseño de la red).

## Página 42 — Links

* https://aprendiendoarduino.wordpress.com/2017/09/10/protocolo-tcpip/
* Material de Cisco en el campus.

## Página 43 — ¡Continuará!

**ETIQUETA — Imagen de cierre con la fotografía del alumnado y el texto «¡Continuará!». Página 43.**
