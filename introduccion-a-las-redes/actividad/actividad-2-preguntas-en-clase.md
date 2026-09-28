# 🤔 Actividad 2 - Preguntas en clase

## Los tipos de redes, ¿Que es ?

### Organismos y Estándares (IEEE)

* `IEEE: Siglas de Institute of Electrical and Electronics Engineers. Es la organización profesional internacional que define las normas y estándares de hardware, redes y telecomunicaciones.`
* `IEEE 802.11: Estándar para redes inalámbricas WLAN (Wi-Fi).`
* `IEEE 802.3: Estándar para redes locales cableadas (Ethernet).`
*   `IEEE 802.15: Estándar para redes inalámbricas de área personal WPAN (Bluetooth, Zigbee).`

    &#x20;

### Tipos de Cable de Cobre y su Blindaje

El blindaje sirve para proteger la transmisión de las interferencias electromagnéticas (EMI) externas.

| **Tipo de cable**                      | **Significado**                        | **Tipo de blindaje**                                                                                                 |
| -------------------------------------- | -------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| UTP (_Unshielded Twisted Pair_)        | Par trenzado sin blindaje              | No tiene ninguna lámina ni malla protectora. Es el más económico y común en interiores.                              |
| FTP / F/UTP (_Foiled Twisted Pair_)    | Par trenzado con lámina global         | Lleva una lámina de aluminio que envuelve a todos los pares juntos.                                                  |
| STP (_Shielded Twisted Pair_)          | Par trenzado blindado individualmente  | Cada par individual lleva su propia lámina o malla protectora.                                                       |
| S/FTP (_Screened Foiled Twisted Pair_) | Par trenzado blindado global y por par | Lleva blindaje individual en cada par y además una malla global alrededor del conjunto. Ofrece la máxima protección. |

### Normas de Cableado EIA/TIA-568A y TIA-568B

Son las dos normas estándar que definen el orden de los hilos de colores al ponchar un conector RJ45.

* Norma T568A: Blanco/Verde, Verde, Blanco/Naranja, Azul, Blanco/Azul, Naranja, Blanco/Marrón, Marrón.
* Norma T568B: Blanco/Naranja, Naranja, Blanco/Verde, Azul, Blanco/Azul, Verde, Blanco/Marrón, Marrón.
* Cable Directo (Straight-through): Mismo estándar en ambos extremos (A-A o B-B). Se usa para conectar dispositivos de distinto tipo (PC a Switch).
* Cable Cruzado (Crossover): Un extremo con norma A y el otro con norma B. Se usa para conectar dispositivos del mismo tipo (PC a PC, Switch a Switch). Nota: Hoy en día la función Auto-MDIX en los switches hace esta conmutación automáticamente.

### ¿Qué son los pares de cables?

Son conjuntos de dos hilos de cobre aislados y trenzados entre sí a lo largo del cable. Un cable Ethernet estándar contiene 4 pares (8 hilos).

El trenzado se utiliza para reducir la diafonía (crosstalk) o interferencia entre los propios pares vecinos y atenuar el ruido electromagnético externo.

### Tipos de Conectores

* RJ45: Conector de 8 pines (8P8C) usado universalmente en redes Ethernet sobre cable UTP/STP.
* RJ49: Variante del RJ45 diseñada específicamente para cables blindados (STP/FTP); incorpora una pestaña metálica exterior para conectar el blindaje del cable a la toma de tierra del equipo.
* RJ11: Conector de 4 o 6 pines (más pequeño) usado tradicionalmente para telefonía analógica y líneas ADSL.
* RS-232: Estándar de comunicación serie antiguo (habitualmente con conector DB9 o mediante adaptadores RJ45 a DB9/USB) utilizado para conectarse al puerto de consola de switches, routers y firewalls para su configuración inicial.

### ¿Qué tipo de cable se debe utilizar en industrias o cerca de equipamiento eléctrico?

En entornos industriales o cerca de motores, transformadores y maquinaria pesada hay alto ruido electromagnético. Las mejores opciones son:

1. Cable STP o S/FTP (Categoría 6A, 7 o 7A): Si se usa cobre, debe tener un apantallamiento de alta densidad (S/FTP) y estar correctamente conectado a toma de tierra para absorber las interferencias.
2. Fibra Óptica (Recomendado): Es la mejor opción para la industria. Dado que transmite luz en lugar de señales eléctricas, es 100% inmune a las interferencias electromagnéticas (EMI) y no sufre problemas de masa o tierra.
