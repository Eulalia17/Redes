---
icon: circle-dashed
---

# EN QUE CASOS ESPECIFICAMENTE SE PUEDE HACER LA TOPOLOGÍA DE ANILLO

<figure><img src="../../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

La topología de anillo se puede utilizar específicamente en escenarios donde se requiere una transmisión de datos ordenada, sin colisiones y en redes de tamaño pequeño a mediano que no cambian de configuración constantemente. A continuación, se detallan los casos y entornos específicos donde su implementación es ideal o históricamente necesaria:

1\. Entornos industriales y de automatización (Redes de tiempo real)

* Sistemas de control de procesos: Se utiliza en fábricas y plantas de energía donde las máquinas y sensores deben comunicarse de forma síncrona.
* Casos con paso de testigo (Token Passing): Como los datos viajan en una sola dirección y un nodo necesita el "token" para transmitir, se garantiza que ningún dispositivo acapare la red y que no existan colisiones de datos.

2\. Redes que requieren alta disponibilidad (Anillo Doble)

* Redes FDDI (Fiber Distributed Data Interface): Se utiliza específicamente en infraestructuras de transporte de datos de larga distancia o campus universitarios.
* Sistemas de respaldo mecánico: Al implementar un anillo doble (dos anillos que viajan en direcciones opuestas), si un cable se rompe, el segundo anillo entra en acción de inmediato, evitando que la red se caiga.

3\. Conexiones de campus o redes troncales (Backbones)

* Interconexión de edificios: Cuando se quiere conectar una serie de edificios o servidores cercanos en un circuito cerrado utilizando fibra óptica.
* Optimización de cableado geométrico: En situaciones donde los nodos están físicamente distribuidos en forma de círculo o línea cerrada, lo que reduce el costo total de la tirada de cable en comparación con llevar un cable desde cada nodo hasta un switch central (estrella).

4\. Redes de telecomunicaciones de área amplia (WAN)

* Tecnología SONET/SDH: Las compañías de telecomunicaciones utilizan estructuras de anillo de fibra óptica para interconectar ciudades o centrales telefónicas, asegurando que si una ruta interurbana se corta, el tráfico se desvíe automáticamente por el otro lado del anillo.
