# Fundamentos de Redes

## 1. Introducción

Una red informática es un conjunto de dispositivos conectados entre sí con el objetivo de intercambiar información y compartir recursos.

Estos dispositivos pueden ser ordenadores, servidores, teléfonos, impresoras, cámaras, routers, switches, puntos de acceso inalámbricos y muchos otros equipos capaces de comunicarse a través de una red.

Las redes permiten, entre otras cosas:

- Compartir información entre dispositivos.
- Acceder a servidores y servicios.
- Compartir recursos como impresoras.
- Comunicarse con otros dispositivos.
- Acceder a Internet.
- Administrar dispositivos de forma remota.
- Centralizar servicios y recursos.

En una empresa como NexaCorp, la red será la infraestructura que permitirá que cientos de dispositivos distribuidos entre diferentes departamentos y sedes puedan comunicarse de forma controlada.

---

## 2. Concepto básico de comunicación

Para entender una red podemos comenzar con el escenario más sencillo posible:

PC-A <----------> PC-B

El objetivo es que PC-A pueda enviar información a PC-B y que PC-B pueda responder.

Para conseguirlo necesitaremos responder progresivamente a varias preguntas:

- ¿Cómo se conectan físicamente los dispositivos?
- ¿Cómo se identifica cada dispositivo?
- ¿Cómo sabe un dispositivo dónde debe enviar la información?
- ¿Qué ocurre si existen cientos de dispositivos?
- ¿Qué ocurre si el destino se encuentra en otra red?
- ¿Cómo se determina el camino que debe seguir la información?

Estas preguntas introducirán progresivamente los principales conceptos y dispositivos utilizados en redes informáticas.

---

## 3. Dispositivos finales

Los dispositivos finales, también conocidos como *end devices* o *hosts*, son aquellos que actúan como origen o destino de la información que circula por una red.

Algunos ejemplos de dispositivos finales son:

- Ordenadores
- Portátiles
- Servidores
- Impresoras de red
- Teléfonos IP
- Smartphones
- Cámaras IP

Por ejemplo, cuando un ordenador solicita información a un servidor, ambos son dispositivos finales: el ordenador origina la solicitud y el servidor recibe dicha solicitud y genera una respuesta.

---

## 4. Switches

Un switch es un dispositivo de red utilizado principalmente para conectar dispositivos dentro de una red local o LAN.

Por ejemplo:

PC-A ──┐  
PC-B ──┼── SWITCH  
PC-C ──┤  
PC-D ──┘  

El switch recibe información a través de sus puertos y determina por qué puerto debe reenviarla para que llegue al dispositivo correspondiente.

Para realizar esta tarea, los switches Ethernet utilizan principalmente las direcciones MAC de los dispositivos y mantienen una tabla conocida como tabla MAC.

El funcionamiento de las direcciones MAC y de la tabla MAC se estudiará posteriormente con mayor profundidad.

---

## 5. Routers

Un router es un dispositivo de red cuya función principal es permitir la comunicación entre redes IP diferentes.

Por ejemplo:

Red A ─── Switch ─── Router ─── Switch ─── Red B

Cuando un dispositivo necesita comunicarse con un dispositivo situado en otra red, el tráfico puede ser enviado hacia un router.

El router analiza la dirección IP de destino y utiliza su tabla de routing para determinar hacia dónde debe enviar el paquete.

De forma simplificada:

- Un switch conecta dispositivos dentro de una red local.
- Un router permite comunicar redes diferentes.

Los switches trabajan principalmente con direcciones MAC para reenviar tramas dentro de una LAN, mientras que los routers utilizan direcciones IP para enrutar paquetes entre redes.

---

## 6. LAN y WAN

Las redes pueden clasificarse según diferentes características. Una de las más importantes es el área geográfica que abarcan.

### 6.1 LAN

Una LAN (*Local Area Network* o Red de Área Local) es una red que conecta dispositivos dentro de un área geográfica relativamente pequeña.

Algunos ejemplos son:

- La red de una vivienda.
- La red de una oficina.
- La red de un edificio empresarial.
- La red local de una sucursal.

En una LAN pueden encontrarse dispositivos como ordenadores, servidores, impresoras, teléfonos IP, puntos de acceso inalámbricos y switches.

En NexaCorp, cada una de las tres sedes contará con su propia infraestructura de red local:

- LAN de Málaga.
- LAN de Madrid.
- LAN de Sevilla.

---

### 6.2 WAN

Una WAN (*Wide Area Network* o Red de Área Amplia) permite interconectar redes que se encuentran geográficamente separadas.

Por ejemplo, NexaCorp necesita que los dispositivos de sus sedes de Málaga, Madrid y Sevilla puedan acceder a determinados recursos corporativos aunque se encuentren en ciudades diferentes.

De forma simplificada:

Málaga ─────┐  
            │  
Madrid ─────┼── WAN  
            │  
Sevilla ────┘  

La WAN permitirá establecer comunicación entre las diferentes sedes de la empresa.

Una WAN no es necesariamente Internet. Internet puede utilizarse como medio para establecer determinadas conexiones entre sedes, pero los conceptos de WAN e Internet no son equivalentes.

---

### 6.3 LAN y WAN en NexaCorp

De forma simplificada, la futura infraestructura de NexaCorp puede entenderse inicialmente de la siguiente manera:

LAN Málaga ──┐  
             │  
LAN Madrid ──┼── WAN  
             │  
LAN Sevilla ─┘  

Cada sede dispondrá de su propia infraestructura LAN y posteriormente se implementará la conectividad necesaria para permitir la comunicación entre las diferentes sedes.

---

## 7. NIC e Interfaces de Red

Para que un dispositivo pueda conectarse y comunicarse a través de una red necesita disponer de una interfaz de red.

### 7.1 NIC

Una NIC (*Network Interface Card* o Tarjeta de Interfaz de Red) es el componente que permite a un dispositivo conectarse a una red.

Un dispositivo puede disponer de diferentes interfaces de red. Por ejemplo, un ordenador portátil puede disponer de:

- Una interfaz Ethernet para conexiones mediante cable.
- Una interfaz WiFi para conexiones inalámbricas.

---

### 7.2 Interfaces de Red

Una interfaz de red representa un punto de conexión mediante el cual un dispositivo puede enviar y recibir información.

Los dispositivos de infraestructura, como routers y switches, pueden disponer de múltiples interfaces o puertos.

Por ejemplo, un router podría utilizar una interfaz para conectarse a una red y otra interfaz para conectarse a una red diferente.

En dispositivos Cisco pueden encontrarse interfaces con nombres como:

- FastEthernet
- GigabitEthernet

Cada interfaz puede identificarse mediante una nomenclatura específica, como `GigabitEthernet0/0` o `GigabitEthernet0/1`.

La configuración y nomenclatura de estas interfaces se estudiará posteriormente utilizando Cisco Packet Tracer.

---

## 8. Medios de Transmisión

Los dispositivos necesitan un medio a través del cual transmitir la información.

Los medios de transmisión pueden dividirse principalmente en:

### Medios cableados

Utilizan conexiones físicas para transmitir la información.

Algunos ejemplos son:

- Cableado de cobre Ethernet.
- Fibra óptica.

### Medios inalámbricos

Permiten transmitir información mediante señales inalámbricas sin utilizar un cable físico entre los dispositivos.

El ejemplo más habitual es una conexión WiFi.

La elección del medio de transmisión dependerá de factores como la distancia, velocidad necesaria, coste, entorno y tipo de dispositivo.

---

## 9. Ethernet

Ethernet es un conjunto de tecnologías y estándares utilizados principalmente para la comunicación de dispositivos dentro de redes LAN cableadas.

En una red Ethernet, la información se transmite mediante unidades denominadas tramas Ethernet o *Ethernet frames*.

Una trama Ethernet contiene diferentes campos necesarios para realizar la comunicación. Entre ellos se encuentran:

- Dirección MAC de origen.
- Dirección MAC de destino.
- Datos transportados.
- Información adicional de control.

Las tramas permiten transportar información entre dispositivos dentro de una red Ethernet.

---

## 10. Direcciones MAC

Una dirección MAC (*Media Access Control*) es un identificador utilizado por una interfaz de red para la comunicación a nivel de enlace.

Las direcciones MAC tienen normalmente una longitud de 48 bits y suelen representarse utilizando números hexadecimales.

Por ejemplo:

`00:1A:2B:3C:4D:5E`

Cuando un dispositivo genera una trama Ethernet, esta incluye una dirección MAC de origen y una dirección MAC de destino.

De forma simplificada:

- La MAC de origen identifica la interfaz que envía la trama.
- La MAC de destino identifica la interfaz a la que se dirige la trama.

---

## 11. Tabla MAC de un Switch

Los switches utilizan una tabla MAC para conocer a través de qué puerto pueden alcanzar determinadas direcciones MAC.

Cuando un switch recibe una trama, puede aprender la dirección MAC de origen y asociarla al puerto por el que ha recibido dicha trama.

Por ejemplo:

| Dirección MAC | Puerto |
|---|---|
| AAAA | Fa0/1 |
| BBBB | Fa0/2 |
| CCCC | Fa0/3 |

Si posteriormente el switch recibe una trama destinada a la dirección MAC `BBBB`, puede consultar su tabla y reenviar la trama a través del puerto `Fa0/2`.

Este mecanismo permite que los switches reenvíen las tramas hacia el puerto correspondiente en lugar de enviarlas innecesariamente por todos sus puertos.

---

## 12. MAC Desconocida y Flooding

Cuando un switch recibe una trama, consulta su tabla MAC para determinar por qué puerto debe reenviarla.

Si la dirección MAC de destino todavía no aparece en su tabla, el switch no sabe exactamente dónde se encuentra el dispositivo de destino.

En este caso, realiza un proceso conocido como *flooding*.

El switch reenvía la trama por los puertos correspondientes, excepto por el puerto a través del cual recibió originalmente la trama.

Los dispositivos que reciben la trama comprueban la dirección MAC de destino. El dispositivo correspondiente procesa la trama, mientras que los demás la descartan.

Cuando el dispositivo de destino responde, el switch puede aprender su dirección MAC y asociarla al puerto correspondiente.

De esta forma, la tabla MAC se construye dinámicamente a medida que circulan tramas por la red.

---

## 13. Unicast y Broadcast

Existen diferentes formas de enviar información dentro de una red.

### 13.1 Unicast

Una comunicación unicast se produce cuando la información se envía desde un dispositivo hacia un único dispositivo de destino.

Por ejemplo:

PC-A ─────────> PC-B

La trama contiene como dirección MAC de destino la dirección correspondiente a PC-B.

### 13.2 Broadcast

Una comunicación broadcast está dirigida a todos los dispositivos pertenecientes al mismo dominio de broadcast.

En Ethernet, la dirección MAC utilizada para broadcast es:

`FF:FF:FF:FF:FF:FF`

Cuando un switch recibe una trama de broadcast, la reenvía por los puertos correspondientes excepto por el puerto por el que recibió originalmente la trama.

Los broadcasts cumplen funciones importantes en determinadas operaciones de red.

Posteriormente se estudiará cómo tecnologías como ARP utilizan broadcasts y cómo los routers y las VLAN permiten limitar los dominios de broadcast.

---

## 14. ARP

ARP (*Address Resolution Protocol*) permite obtener la dirección MAC asociada a una dirección IPv4 dentro de una red local.

Cuando un dispositivo quiere comunicarse con otro dispositivo de su red local puede conocer su dirección IP, pero necesitar conocer también la dirección MAC correspondiente para poder enviar la trama Ethernet.

Por ejemplo:

PC-A:

- IP: `192.168.1.10`
- MAC: `AAAA`

PC-B:

- IP: `192.168.1.20`
- MAC: `BBBB`

Si PC-A quiere comunicarse con `192.168.1.20` pero no conoce su dirección MAC, puede utilizar ARP.

### 14.1 ARP Request

PC-A genera una solicitud ARP preguntando qué dispositivo posee la dirección IP `192.168.1.20`.

Como todavía desconoce la dirección MAC del dispositivo buscado, la solicitud se envía mediante broadcast utilizando como MAC de destino:

`FF:FF:FF:FF:FF:FF`

Los dispositivos de la red local reciben la solicitud ARP y comprueban la dirección IP solicitada.

### 14.2 ARP Reply

El dispositivo que posee la dirección IP solicitada responde indicando su dirección MAC.

En este ejemplo, PC-B informa de que:

`192.168.1.20 → BBBB`

PC-A puede almacenar temporalmente esta asociación en su tabla o caché ARP.

### 14.3 Comunicación posterior

Una vez conocida la dirección MAC de PC-B, PC-A puede construir una trama Ethernet utilizando:

- MAC de origen: `AAAA`
- MAC de destino: `BBBB`

El switch podrá entonces utilizar la dirección MAC de destino para reenviar la trama hacia el dispositivo correspondiente.

ARP permite, por tanto, relacionar el direccionamiento IPv4 utilizado para identificar dispositivos a nivel de red con las direcciones MAC utilizadas para la comunicación Ethernet dentro de la red local.

---

## 15. Tramas y Paquetes

Durante una comunicación de red, la información se organiza utilizando diferentes unidades de datos dependiendo del nivel de comunicación que se esté utilizando.

Dos conceptos fundamentales son las tramas y los paquetes.

### 15.1 Trama

Una trama o *frame* es una unidad de datos utilizada para la comunicación a nivel de enlace.

En una red Ethernet, las tramas contienen información como:

- Dirección MAC de origen.
- Dirección MAC de destino.
- Datos transportados.
- Información de control.

Los switches utilizan principalmente la información de las tramas, especialmente las direcciones MAC, para reenviar tráfico dentro de una red LAN.

### 15.2 Paquete

Un paquete es una unidad de datos utilizada a nivel de red.

En el caso de IPv4, un paquete IP contiene información como:

- Dirección IP de origen.
- Dirección IP de destino.
- Datos transportados.
- Información de control.

Los routers utilizan las direcciones IP para determinar cómo deben reenviar los paquetes entre diferentes redes.

### 15.3 Encapsulación básica

Un paquete IP puede ser transportado dentro de una trama Ethernet.

De forma simplificada:

Trama Ethernet  
└── Paquete IP  
    └── Datos

Esto permite utilizar diferentes tipos de información para distintas funciones durante una comunicación.

Por ejemplo:

- Las direcciones MAC permiten realizar la comunicación Ethernet en el enlace local.
- Las direcciones IP permiten identificar el origen y destino a nivel de red y posibilitan la comunicación entre redes diferentes.

Este proceso forma parte de un concepto denominado encapsulación, que se estudiará con mayor profundidad al analizar los modelos OSI y TCP/IP.

---

## 16. Modelo OSI

El modelo OSI (*Open Systems Interconnection*) es un modelo de referencia que divide el proceso de comunicación de red en siete capas.

Su objetivo es facilitar la comprensión de las diferentes funciones que intervienen cuando dos dispositivos se comunican a través de una red.

Las siete capas del modelo OSI son:

| Capa | Nombre | Función general |
|---:|---|---|
| 7 | Aplicación | Proporciona servicios de red a las aplicaciones |
| 6 | Presentación | Representación, transformación y protección de los datos |
| 5 | Sesión | Gestión de sesiones de comunicación |
| 4 | Transporte | Comunicación entre aplicaciones y control del transporte |
| 3 | Red | Direccionamiento lógico y comunicación entre redes |
| 2 | Enlace de datos | Comunicación mediante tramas dentro del enlace |
| 1 | Física | Transmisión física de bits |

---

### 16.1 Capa 1 - Física

La capa física se encarga de la transmisión de bits a través del medio físico.

Está relacionada con elementos como:

- Cableado de cobre.
- Fibra óptica.
- Señales eléctricas.
- Señales ópticas.
- Conectores.
- Características físicas de las interfaces.

---

### 16.2 Capa 2 - Enlace de Datos

La capa de enlace de datos permite la comunicación a través de un enlace de red.

En las redes Ethernet aparecen conceptos estudiados anteriormente como:

- Tramas Ethernet.
- Direcciones MAC.
- Switching.
- Tabla MAC.
- Broadcast.

Los switches Ethernet tradicionales operan principalmente en esta capa.

---

### 16.3 Capa 3 - Red

La capa de red permite el direccionamiento lógico y la comunicación entre redes diferentes.

En esta capa aparecen conceptos como:

- Direcciones IP.
- Paquetes IP.
- Routing.
- Routers.

Los routers utilizan información de Capa 3 para determinar cómo reenviar paquetes hacia otras redes.

---

### 16.4 Capa 4 - Transporte

La capa de transporte proporciona mecanismos para la comunicación entre aplicaciones de los dispositivos finales.

En esta capa aparecen protocolos fundamentales como:

- TCP
- UDP

También aparecen conceptos como los números de puerto, que permiten identificar diferentes servicios y aplicaciones.

Estos conceptos se estudiarán posteriormente con mayor profundidad.

---

### 16.5 Capas 5, 6 y 7

Las capas superiores están relacionadas principalmente con las sesiones de comunicación, la representación de la información y los servicios utilizados por las aplicaciones.

Entre los protocolos y servicios que encontraremos posteriormente se encuentran tecnologías como:

- HTTP / HTTPS
- DNS
- DHCP
- SSH

No todos estos protocolos pertenecen exclusivamente a una única capa del modelo de forma tan simple, pero el modelo OSI permite organizar conceptualmente las diferentes funciones que intervienen en una comunicación.

---

### 16.6 Relación entre conceptos estudiados

De forma simplificada:

| Concepto | Capa OSI |
|---|---:|
| Cableado y señales | 1 |
| Ethernet | 2 |
| Dirección MAC | 2 |
| Trama | 2 |
| Switch | Principalmente 2 |
| Dirección IP | 3 |
| Paquete IP | 3 |
| Router | Principalmente 3 |
| TCP / UDP | 4 |
| Aplicaciones y servicios de red | Capas superiores |

El modelo OSI no debe entenderse únicamente como una lista de siete capas que memorizar, sino como una herramienta para comprender y diagnosticar el funcionamiento de las comunicaciones de red.

---

## 17. Modelo TCP/IP

El modelo TCP/IP representa la arquitectura utilizada como base para la comunicación en Internet y en las redes IP modernas.

A diferencia del modelo OSI, que utiliza siete capas, el modelo TCP/IP suele representarse mediante cuatro capas:

| Capa TCP/IP | Función general |
|---|---|
| Aplicación | Servicios y protocolos utilizados por las aplicaciones |
| Transporte | Comunicación entre aplicaciones |
| Internet | Direccionamiento IP y routing |
| Acceso a la red | Comunicación a través del enlace y medio físico |

Existe una relación aproximada entre los modelos OSI y TCP/IP:

| Modelo OSI | Modelo TCP/IP |
|---|---|
| Aplicación, Presentación y Sesión | Aplicación |
| Transporte | Transporte |
| Red | Internet |
| Enlace de datos y Física | Acceso a la red |

El modelo OSI se utiliza ampliamente como modelo de referencia para estudiar y comprender las funciones de una red, mientras que TCP/IP está directamente relacionado con la arquitectura utilizada en las redes IP actuales.

---

## 18. Encapsulación y Desencapsulación

Cuando un dispositivo envía información a través de una red, los datos atraviesan diferentes capas.

Cada capa puede añadir información necesaria para realizar su función. Este proceso se denomina encapsulación.

De forma simplificada:

Datos  
↓  
Segmento  
↓  
Paquete  
↓  
Trama  
↓  
Bits  

### 18.1 Datos

La aplicación genera los datos que necesitan ser enviados a través de la red.

### 18.2 Segmento

En la capa de transporte, protocolos como TCP pueden añadir información necesaria para la comunicación entre aplicaciones.

La unidad de datos asociada normalmente con TCP se denomina segmento.

UDP utiliza habitualmente el término datagrama.

### 18.3 Paquete

En la capa de red se añade información IP.

Entre esta información se encuentran:

- Dirección IP de origen.
- Dirección IP de destino.

El resultado puede ser un paquete IP.

### 18.4 Trama

En la capa de enlace, el paquete IP puede encapsularse dentro de una trama Ethernet.

Esta trama incluye información como:

- Dirección MAC de origen.
- Dirección MAC de destino.

### 18.5 Bits

Finalmente, la información se transmite a través del medio físico en forma de bits representados mediante las señales correspondientes al medio utilizado.

---

## 19. Desencapsulación

Cuando la información llega al dispositivo de destino se realiza el proceso inverso, denominado desencapsulación.

De forma simplificada:

Bits  
↓  
Trama  
↓  
Paquete  
↓  
Segmento  
↓  
Datos  

Cada capa procesa la información que le corresponde y entrega el contenido restante a la capa superior hasta que los datos llegan finalmente a la aplicación correspondiente.

La encapsulación y desencapsulación permiten que diferentes tecnologías y protocolos trabajen conjuntamente durante una comunicación de red.

---

## 20. Introducción a IPv4

IPv4 (*Internet Protocol version 4*) es un protocolo utilizado para proporcionar direccionamiento lógico a los dispositivos y permitir la comunicación a través de redes IP.

Una dirección IPv4 tiene una longitud de 32 bits.

Para facilitar su lectura, estos 32 bits se dividen en cuatro grupos de 8 bits denominados octetos.

Por ejemplo:

`192.168.1.10`

Esta dirección está formada por cuatro octetos:

- `192`
- `168`
- `1`
- `10`

Cada octeto está compuesto por 8 bits, por lo que una dirección IPv4 contiene:

`8 + 8 + 8 + 8 = 32 bits`

Cada octeto puede representar valores decimales comprendidos entre `0` y `255`.

---

### 20.1 Representación binaria

Aunque normalmente las direcciones IPv4 se escriben utilizando números decimales, internamente están formadas por bits.

Por ejemplo, el valor decimal:

`192`

puede representarse en binario como:

`11000000`

Una dirección IPv4 completa puede representarse tanto en decimal como en binario.

La conversión entre decimal y binario será importante posteriormente para comprender correctamente el funcionamiento de las máscaras de subred y el subnetting.

---

### 20.2 Parte de red y parte de host

Una dirección IPv4 puede dividirse conceptualmente en:

- Una parte que identifica la red.
- Una parte que identifica al host dentro de esa red.

Para determinar qué bits pertenecen a la parte de red y cuáles pertenecen a la parte de host es necesario utilizar una máscara de subred.

Por este motivo, una dirección IP debe interpretarse junto con su máscara o longitud de prefijo.

Por ejemplo:

`192.168.1.10/24`

La notación `/24` proporciona información sobre qué parte de la dirección identifica la red.

El funcionamiento de las máscaras y de la notación CIDR se estudiará posteriormente.

---

## 21. Sistema Binario Aplicado a IPv4

Los dispositivos digitales trabajan utilizando bits, cuyos posibles valores son `0` y `1`.

Una dirección IPv4 está formada por 32 bits divididos en cuatro octetos de 8 bits.

Dentro de un octeto, cada posición tiene un valor determinado:

| Bit | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Valor | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

Cuando un bit tiene el valor `1`, su valor correspondiente se suma. Cuando tiene el valor `0`, no se suma.

### 21.1 Conversión de binario a decimal

Por ejemplo:

`11000000`

Los bits activos corresponden a:

`128 + 64 = 192`

Por tanto:

`11000000 = 192`

Otro ejemplo:

`10101000`

Los bits activos corresponden a:

`128 + 32 + 8 = 168`

Por tanto:

`10101000 = 168`

Si todos los bits de un octeto tienen valor `1`:

`11111111`

El resultado es:

`128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = 255`

Por este motivo, el valor máximo que puede representar un octeto IPv4 es `255`.

### 21.2 IPv4 en binario

Una dirección IPv4 puede representarse completamente en binario.

Por ejemplo:

`192.168.1.10`

equivale a:

`11000000.10101000.00000001.00001010`

Ambas representaciones corresponden a la misma dirección IPv4.

Comprender la representación binaria es fundamental para entender posteriormente las máscaras de subred, CIDR y subnetting.

---

## 22. Máscara de Subred y CIDR

Una dirección IPv4 necesita información adicional para determinar qué parte de sus 32 bits identifica la red y qué parte puede utilizarse para identificar hosts.

Esta información puede representarse mediante una máscara de subred.

Por ejemplo:

IP: `192.168.1.10`

Máscara: `255.255.255.0`

La máscara puede representarse también en binario:

`11111111.11111111.11111111.00000000`

En una máscara de subred:

- Los bits con valor `1` representan el prefijo o parte de red.
- Los bits con valor `0` representan la parte disponible para hosts.

En este ejemplo existen 24 bits pertenecientes al prefijo de red y 8 bits correspondientes a la parte de host.

---

### 22.1 Notación CIDR

CIDR (*Classless Inter-Domain Routing*) permite representar la longitud del prefijo utilizando una notación más compacta.

Por ejemplo:

`192.168.1.10/24`

El `/24` indica que los primeros 24 bits corresponden al prefijo de red.

Por tanto:

`/24 = 255.255.255.0`

Otro ejemplo sería:

`/16 = 255.255.0.0`

ya que existen 16 bits con valor `1` en la máscara.

La longitud del prefijo es fundamental para determinar el tamaño de una red y calcular posteriormente su dirección de red, dirección de broadcast y rango de direcciones disponibles para hosts.

---

## 23. Dirección de Red, Broadcast y Hosts

Una subred IPv4 contiene diferentes tipos de direcciones. Entre ellas se encuentran la dirección de red, las direcciones asignables a hosts y la dirección de broadcast.

Para comprender estos conceptos podemos utilizar como ejemplo:

`192.168.1.10/24`

Un prefijo `/24` utiliza 24 bits para identificar la red y deja 8 bits para la parte de host.

### 23.1 Dirección de red

La dirección de red identifica a la propia subred.

Para obtenerla, todos los bits correspondientes a la parte de host tienen valor `0`.

En el ejemplo:

`192.168.1.10/24`

la dirección de red es:

`192.168.1.0/24`

Esta dirección no se utiliza normalmente como dirección de un dispositivo.

### 23.2 Dirección de broadcast

La dirección de broadcast permite enviar tráfico dirigido a todos los hosts de una determinada subred IPv4.

Para obtenerla, todos los bits correspondientes a la parte de host tienen valor `1`.

En el ejemplo:

`192.168.1.10/24`

la dirección de broadcast es:

`192.168.1.255`

Esta dirección no se asigna normalmente a un dispositivo.

### 23.3 Rango de hosts

Las direcciones comprendidas entre la dirección de red y la dirección de broadcast pueden utilizarse para identificar hosts.

Para la red `192.168.1.0/24`:

- Dirección de red: `192.168.1.0`
- Primer host: `192.168.1.1`
- Último host: `192.168.1.254`
- Dirección de broadcast: `192.168.1.255`

### 23.4 Número de hosts

El número de direcciones disponibles depende de la cantidad de bits utilizados para la parte de host.

En una red `/24` existen 8 bits de host.

Por tanto:

`2^8 = 256 direcciones`

En una subred IPv4 convencional se reservan la dirección de red y la dirección de broadcast.

Por tanto:

`2^8 - 2 = 254 hosts utilizables`

Esta fórmula será utilizada posteriormente para diseñar subredes con diferentes tamaños.

---

## 24. Introducción al Subnetting

El subnetting es el proceso de dividir una red IP en redes más pequeñas llamadas subredes.

Esta técnica permite utilizar el espacio de direccionamiento IP de forma más eficiente y separar diferentes grupos de dispositivos.

En una red empresarial, el subnetting puede utilizarse para crear redes independientes para diferentes departamentos, servicios o tipos de dispositivos.

Por ejemplo, NexaCorp podría necesitar redes diferentes para:

- Dirección
- Administración
- Finanzas
- Recursos Humanos
- Ventas
- Desarrollo
- IT / Sistemas
- Servidores
- Telefonía IP
- WiFi corporativo
- WiFi de invitados
- Administración de dispositivos de red

Cada una de estas redes puede necesitar una cantidad diferente de direcciones IP.

Por este motivo, es importante aprender a calcular correctamente el tamaño de las subredes.

---

## 25. Subredes /25

Una red `/24` dispone de 8 bits para hosts:

`11111111.11111111.11111111.00000000`

Su máscara es:

`255.255.255.0`

Si utilizamos un bit adicional para la parte de red, obtenemos un prefijo `/25`:

`11111111.11111111.11111111.10000000`

Su máscara decimal es:

`255.255.255.128`

Por tanto:

`/25 = 255.255.255.128`

En una red `/25` quedan 7 bits disponibles para hosts.

El número total de direcciones es:

`2^7 = 128`

En una subred IPv4 convencional:

`128 - 2 = 126 hosts utilizables`

---

### 25.1 División de una /24 en subredes /25

Si tenemos:

`192.168.1.0/24`

podemos dividirla en dos subredes `/25`.

Primera subred:

- Dirección de red: `192.168.1.0`
- Primer host: `192.168.1.1`
- Último host: `192.168.1.126`
- Broadcast: `192.168.1.127`

Segunda subred:

- Dirección de red: `192.168.1.128`
- Primer host: `192.168.1.129`
- Último host: `192.168.1.254`
- Broadcast: `192.168.1.255`

Por tanto:

| Subred | Primer host | Último host | Broadcast |
|---|---|---|---|
| `192.168.1.0/25` | `192.168.1.1` | `192.168.1.126` | `192.168.1.127` |
| `192.168.1.128/25` | `192.168.1.129` | `192.168.1.254` | `192.168.1.255` |

---

### 25.2 Tamaño de bloque

Una forma práctica de calcular dónde comienza cada subred consiste en utilizar el tamaño de bloque.

Para una máscara `/25`:

`255.255.255.128`

El octeto donde cambia la máscara tiene el valor `128`.

El tamaño de bloque puede calcularse mediante:

`256 - 128 = 128`

Por tanto, las redes comienzan cada 128 direcciones:

`0`

`128`

Esto genera:

`192.168.1.0/25`

y:

`192.168.1.128/25`

La siguiente dirección de red permite determinar también el broadcast de la subred anterior.

Por ejemplo:

Segunda red:

`192.168.1.128`

Por tanto, el broadcast de la primera será la dirección inmediatamente anterior:

`192.168.1.127`

---

## 26. Relación entre Prefijo, Direcciones y Hosts

A medida que aumenta la longitud del prefijo, se utilizan más bits para identificar la red y quedan menos bits disponibles para hosts.

Por ejemplo:

| Prefijo | Máscara | Bits de host | Direcciones totales | Hosts utilizables* |
|---|---|---:|---:|---:|
| `/24` | `255.255.255.0` | 8 | 256 | 254 |
| `/25` | `255.255.255.128` | 7 | 128 | 126 |
| `/26` | `255.255.255.192` | 6 | 64 | 62 |
| `/27` | `255.255.255.224` | 5 | 32 | 30 |
| `/28` | `255.255.255.240` | 4 | 16 | 14 |
| `/29` | `255.255.255.248` | 3 | 8 | 6 |
| `/30` | `255.255.255.252` | 2 | 4 | 2 |

\*La columna de hosts utilizables representa el cálculo tradicional para subredes IPv4 con dirección de red y broadcast.

Esto muestra una relación fundamental:

- Un prefijo más pequeño proporciona más espacio para hosts.
- Un prefijo más grande proporciona menos espacio para hosts.
- Aumentar el prefijo permite crear redes más pequeñas.

Esta relación será fundamental posteriormente para diseñar el direccionamiento IP de NexaCorp de forma eficiente.

---

## 27. Cálculo de Subredes mediante el Tamaño de Bloque

El tamaño de bloque permite identificar de forma rápida dónde comienza y termina cada subred.

Puede calcularse utilizando:

`256 - valor del octeto relevante de la máscara`

El octeto relevante es aquel en el que la máscara deja de tener un valor de `255` y comienza la división de las subredes.

---

### 27.1 Ejemplo con /26

Una máscara `/26` es:

`255.255.255.192`

En binario:

`11111111.11111111.11111111.11000000`

Existen:

- 26 bits de red.
- 6 bits de host.

El número total de direcciones por subred es:

`2^6 = 64`

Los hosts utilizables son:

`64 - 2 = 62`

También podemos calcular el tamaño de bloque mediante:

`256 - 192 = 64`

Por tanto, las subredes avanzan de 64 en 64:

- `0`
- `64`
- `128`
- `192`

Si dividimos `192.168.1.0/24` utilizando `/26`, obtenemos:

| Subred | Primer host | Último host | Broadcast |
|---|---|---|---|
| `192.168.1.0/26` | `192.168.1.1` | `192.168.1.62` | `192.168.1.63` |
| `192.168.1.64/26` | `192.168.1.65` | `192.168.1.126` | `192.168.1.127` |
| `192.168.1.128/26` | `192.168.1.129` | `192.168.1.190` | `192.168.1.191` |
| `192.168.1.192/26` | `192.168.1.193` | `192.168.1.254` | `192.168.1.255` |

---

## 28. Subredes /27

Una máscara `/27` es:

`255.255.255.224`

En binario:

`11111111.11111111.11111111.11100000`

Quedan 5 bits disponibles para hosts.

Por tanto:

`2^5 = 32 direcciones`

Hosts utilizables:

`32 - 2 = 30`

El tamaño de bloque también puede calcularse mediante:

`256 - 224 = 32`

Las subredes avanzan de 32 en 32:

- `0`
- `32`
- `64`
- `96`
- `128`
- `160`
- `192`
- `224`

Por ejemplo, utilizando `192.168.1.0/24`:

| Subred | Primer host | Último host | Broadcast |
|---|---|---|---|
| `192.168.1.0/27` | `192.168.1.1` | `192.168.1.30` | `192.168.1.31` |
| `192.168.1.32/27` | `192.168.1.33` | `192.168.1.62` | `192.168.1.63` |
| `192.168.1.64/27` | `192.168.1.65` | `192.168.1.94` | `192.168.1.95` |
| `192.168.1.96/27` | `192.168.1.97` | `192.168.1.126` | `192.168.1.127` |
| `192.168.1.128/27` | `192.168.1.129` | `192.168.1.158` | `192.168.1.159` |
| `192.168.1.160/27` | `192.168.1.161` | `192.168.1.190` | `192.168.1.191` |
| `192.168.1.192/27` | `192.168.1.193` | `192.168.1.222` | `192.168.1.223` |
| `192.168.1.224/27` | `192.168.1.225` | `192.168.1.254` | `192.168.1.255` |

---

## 29. Método para Calcular una Subred

Para calcular una subred IPv4 se puede seguir el siguiente procedimiento:

### Paso 1 - Identificar el prefijo

Por ejemplo:

`192.168.1.70/26`

El prefijo es `/26`.

### Paso 2 - Obtener la máscara

`/26 = 255.255.255.192`

### Paso 3 - Calcular el tamaño de bloque

`256 - 192 = 64`

Las posibles redes son:

`0, 64, 128, 192`

### Paso 4 - Localizar la IP

La IP del ejemplo termina en:

`70`

El valor `70` se encuentra entre:

`64 - 127`

Por tanto, pertenece a la subred:

`192.168.1.64/26`

### Paso 5 - Obtener el broadcast

La siguiente subred comienza en:

`192.168.1.128`

La dirección inmediatamente anterior es:

`192.168.1.127`

Por tanto, este es el broadcast.

### Paso 6 - Obtener los hosts

El primer host es la dirección inmediatamente posterior a la dirección de red:

`192.168.1.65`

El último host es la dirección inmediatamente anterior al broadcast:

`192.168.1.126`

El resultado completo es:

- IP analizada: `192.168.1.70/26`
- Red: `192.168.1.64/26`
- Primer host: `192.168.1.65`
- Último host: `192.168.1.126`
- Broadcast: `192.168.1.127`
- Hosts utilizables: `62`

---

## 30. VLSM

VLSM (*Variable Length Subnet Mask*) es una técnica que permite utilizar máscaras de subred de diferentes tamaños dentro de un mismo esquema de direccionamiento.

Su objetivo es adaptar el tamaño de cada subred a la cantidad de dispositivos que realmente necesita.

Sin VLSM, podríamos terminar asignando subredes demasiado grandes a departamentos pequeños, desperdiciando muchas direcciones IP.

---

### 30.1 ¿Por qué utilizar VLSM?

Supongamos que una empresa tiene los siguientes departamentos:

- Desarrollo: 60 dispositivos.
- Ventas: 50 dispositivos.
- Administración: 20 dispositivos.
- IT: 10 dispositivos.

No todos necesitan una subred del mismo tamaño.

Por ejemplo, una `/26` proporciona:

`62 hosts utilizables`

Esto podría ser apropiado para Desarrollo.

Sin embargo, utilizar también una `/26` para IT supondría reservar 62 direcciones utilizables cuando solamente se necesitan aproximadamente 10.

Con VLSM podemos utilizar diferentes prefijos:

| Departamento | Hosts necesarios | Prefijo posible | Hosts utilizables |
|---|---:|---:|---:|
| Desarrollo | 60 | `/26` | 62 |
| Ventas | 50 | `/26` | 62 |
| Administración | 20 | `/27` | 30 |
| IT | 10 | `/28` | 14 |

De esta forma se aprovecha mejor el espacio de direccionamiento disponible.

---

## 31. Selección del Tamaño de una Subred

Para seleccionar una subred debemos determinar cuántos bits de host necesitamos.

En una subred IPv4 convencional podemos utilizar:

`2^h - 2`

donde `h` representa el número de bits disponibles para hosts.

Por ejemplo, si necesitamos una red para 20 dispositivos:

Con 4 bits:

`2^4 - 2 = 14`

No es suficiente.

Con 5 bits:

`2^5 - 2 = 30`

Sí es suficiente.

Por tanto, necesitamos 5 bits para hosts.

IPv4 dispone de 32 bits:

`32 - 5 = 27`

La subred apropiada sería:

`/27`

que proporciona 30 direcciones utilizables para hosts.

---

## 32. Diseño VLSM

Cuando se diseña un esquema VLSM, una práctica habitual consiste en ordenar las redes desde la que necesita más direcciones hasta la que necesita menos.

Por ejemplo:

| Red | Hosts necesarios |
|---|---:|
| Desarrollo | 60 |
| Ventas | 50 |
| Administración | 20 |
| IT | 10 |

Ordenamos de mayor a menor y seleccionamos el prefijo correspondiente:

| Red | Hosts necesarios | Prefijo |
|---|---:|---:|
| Desarrollo | 60 | `/26` |
| Ventas | 50 | `/26` |
| Administración | 20 | `/27` |
| IT | 10 | `/28` |

Posteriormente se asignan las subredes consecutivamente evitando que sus rangos se solapen.

---

## 33. Ejemplo Básico de VLSM

Supongamos que disponemos de un espacio de direccionamiento suficientemente grande y queremos asignar las siguientes subredes:

- Desarrollo: 60 hosts.
- Ventas: 50 hosts.
- Administración: 20 hosts.
- IT: 10 hosts.

Una posible distribución sería:

### Desarrollo

`192.168.1.0/26`

- Red: `192.168.1.0`
- Hosts: `192.168.1.1 - 192.168.1.62`
- Broadcast: `192.168.1.63`

### Ventas

`192.168.1.64/26`

- Red: `192.168.1.64`
- Hosts: `192.168.1.65 - 192.168.1.126`
- Broadcast: `192.168.1.127`

### Administración

`192.168.1.128/27`

- Red: `192.168.1.128`
- Hosts: `192.168.1.129 - 192.168.1.158`
- Broadcast: `192.168.1.159`

### IT

`192.168.1.160/28`

- Red: `192.168.1.160`
- Hosts: `192.168.1.161 - 192.168.1.174`
- Broadcast: `192.168.1.175`

Las direcciones restantes podrían reservarse para futuras redes o ampliaciones.

---

## 34. VLSM en NexaCorp

VLSM será utilizado posteriormente para diseñar el direccionamiento IP de NexaCorp.

Los diferentes departamentos y servicios tienen necesidades distintas.

Por ejemplo, en la sede de Málaga existen departamentos de tamaños muy diferentes:

- Desarrollo: 60 empleados.
- Ventas: 50 empleados.
- IT / Sistemas: 25 empleados.
- Administración: 20 empleados.
- Finanzas: 20 empleados.
- Recursos Humanos: 15 empleados.
- Dirección: 10 empleados.

Además, será necesario reservar direccionamiento para otros segmentos como:

- Servidores.
- Telefonía IP.
- WiFi corporativo.
- WiFi de invitados.
- Administración de dispositivos de red.
- DMZ.

Por tanto, utilizar diferentes tamaños de subred permitirá diseñar un esquema de direccionamiento más eficiente y preparado para el crecimiento futuro.

El direccionamiento definitivo de NexaCorp se diseñará posteriormente durante la fase de implementación.

---

## 35. Direcciones IPv4 Privadas y Públicas

No todas las direcciones IPv4 tienen el mismo propósito.

Una distinción fundamental es la existente entre direcciones IP públicas y privadas.

### 35.1 Direcciones IPv4 privadas

Las direcciones IPv4 privadas están destinadas al uso dentro de redes internas y no se enrutan directamente a través de Internet.

Los rangos privados definidos para IPv4 son:

| Rango | Prefijo |
|---|---|
| `10.0.0.0 - 10.255.255.255` | `10.0.0.0/8` |
| `172.16.0.0 - 172.31.255.255` | `172.16.0.0/12` |
| `192.168.0.0 - 192.168.255.255` | `192.168.0.0/16` |

Estas direcciones pueden reutilizarse en diferentes organizaciones.

Por ejemplo, dos empresas diferentes pueden utilizar internamente la dirección:

`192.168.1.10`

sin que exista ningún conflicto entre ellas, siempre que sus redes privadas sean independientes.

NexaCorp utilizará direccionamiento privado para sus redes internas.

### 35.2 Direcciones IPv4 públicas

Las direcciones IPv4 públicas permiten identificar dispositivos o servicios dentro del espacio de direccionamiento utilizado en Internet.

A diferencia de las direcciones privadas, las direcciones públicas utilizadas en Internet deben ser globalmente únicas dentro de ese contexto.

Para permitir que dispositivos con direcciones privadas accedan a Internet se utilizan normalmente mecanismos como NAT, que se estudiarán posteriormente.

---

## 36. Direcciones IPv4 Especiales

Además de las direcciones públicas y privadas existen direcciones reservadas para funciones específicas.

### 36.1 Loopback

El bloque:

`127.0.0.0/8`

está reservado para funciones de loopback.

La dirección más conocida es:

`127.0.0.1`

Esta dirección permite a un dispositivo comunicarse consigo mismo a través de su propia pila TCP/IP.

Por ejemplo:

`ping 127.0.0.1`

puede utilizarse como una comprobación básica del funcionamiento de TCP/IP en el propio dispositivo.

### 36.2 APIPA

El rango:

`169.254.0.0/16`

corresponde al direccionamiento link-local de IPv4.

En determinados sistemas, cuando un dispositivo está configurado para obtener una dirección automáticamente mediante DHCP y no consigue contactar con un servidor DHCP, puede autoconfigurarse con una dirección de este rango.

Encontrar una dirección similar a:

`169.254.x.x`

en un equipo que debería recibir configuración mediante DHCP puede ser una señal de que existe un problema con DHCP o con la conectividad hacia dicho servicio.

---

## 37. Gateway Predeterminado

Un dispositivo puede comunicarse directamente con otros dispositivos pertenecientes a su misma subred.

Sin embargo, cuando necesita comunicarse con una dirección situada en otra red, necesita enviar el tráfico hacia un dispositivo capaz de enrutarlo.

Ese dispositivo suele ser un router o un dispositivo de Capa 3.

La dirección utilizada por un host para alcanzar otras redes se conoce como gateway predeterminado o puerta de enlace predeterminada.

Por ejemplo:

- PC: `192.168.1.10/24`
- Gateway: `192.168.1.1`

Si el PC quiere comunicarse con:

`192.168.1.20`

el destino pertenece a su misma subred.

Sin embargo, si quiere comunicarse con:

`192.168.2.20`

el destino pertenece a otra subred y el tráfico deberá enviarse hacia el gateway correspondiente.

---

## 38. Comunicación dentro de la Misma Red

Supongamos:

PC-A:

- IP: `192.168.1.10/24`
- MAC: `AAAA`

PC-B:

- IP: `192.168.1.20/24`
- MAC: `BBBB`

Ambos pertenecen a:

`192.168.1.0/24`

PC-A determina, utilizando su propia dirección IP y máscara, que PC-B se encuentra dentro de su misma subred.

Si todavía no conoce la dirección MAC de PC-B, puede utilizar ARP para obtenerla.

Una vez conocida, puede crear una trama Ethernet dirigida directamente a la MAC de PC-B.

De forma simplificada:

`PC-A → Switch → PC-B`

En este caso no es necesario utilizar el gateway predeterminado para la comunicación entre ambos hosts.

---

## 39. Comunicación entre Redes Diferentes

Supongamos ahora:

PC-A:

`192.168.1.10/24`

PC-B:

`192.168.2.20/24`

Las redes son:

`192.168.1.0/24`

y:

`192.168.2.0/24`

Por tanto, PC-A determina que PC-B no pertenece a su misma subred.

PC-A no intenta enviar directamente la trama Ethernet a la MAC de PC-B.

En su lugar, envía el tráfico hacia su gateway predeterminado.

Por ejemplo:

`192.168.1.1`

Para hacerlo, PC-A necesita conocer la dirección MAC correspondiente a la interfaz del gateway situada en su red local.

Si no la conoce, puede utilizar ARP.

La comunicación podría representarse de forma simplificada como:

`PC-A → Switch → Router → Switch → PC-B`

El paquete IP mantiene como destino la dirección IP de PC-B, mientras que las tramas utilizadas en cada enlace emplean las direcciones MAC necesarias para realizar la comunicación local correspondiente.

Este comportamiento explica una diferencia fundamental:

- Las direcciones IP permiten identificar origen y destino a nivel de red.
- Las direcciones MAC se utilizan para entregar las tramas en los enlaces Ethernet correspondientes.

---

## 40. Protocolos de Red

Un protocolo es un conjunto de reglas y procedimientos que permiten que diferentes dispositivos puedan comunicarse.

Los dispositivos necesitan utilizar protocolos compatibles para interpretar correctamente la información intercambiada.

Algunos protocolos y tecnologías importantes que se estudiarán durante el proyecto son:

| Protocolo / Tecnología | Función general |
|---|---|
| Ethernet | Comunicación en redes LAN |
| ARP | Relación entre IPv4 y MAC dentro del enlace local |
| IPv4 | Direccionamiento y entrega de paquetes |
| ICMP | Mensajes de control y diagnóstico |
| TCP | Transporte orientado a conexión |
| UDP | Transporte no orientado a conexión |
| DHCP | Configuración automática de parámetros de red |
| DNS | Resolución de nombres |
| HTTP / HTTPS | Comunicación web |
| SSH | Administración remota segura |
| OSPF | Intercambio de información de routing |

Cada uno será estudiado con mayor profundidad cuando sea necesario durante el desarrollo de NexaCorp.

---

## 41. TCP y UDP

TCP y UDP son dos protocolos fundamentales de la capa de transporte.

Permiten que las aplicaciones de los dispositivos puedan intercambiar información a través de una red.

### 41.1 TCP

TCP (*Transmission Control Protocol*) proporciona un servicio orientado a conexión.

Entre sus características se encuentran mecanismos relacionados con:

- Establecimiento de conexiones.
- Entrega fiable.
- Control del orden de los datos.
- Detección y recuperación ante determinados datos perdidos.
- Control de flujo.

Estas características hacen que TCP sea apropiado para aplicaciones donde la entrega correcta y ordenada de la información es importante.

### 41.2 UDP

UDP (*User Datagram Protocol*) proporciona un mecanismo de transporte más simple y no establece una conexión del mismo modo que TCP.

UDP no proporciona por sí mismo las mismas garantías de entrega y orden que TCP.

Esto reduce la sobrecarga del protocolo y puede resultar útil para determinadas aplicaciones donde se priorizan características como la baja latencia o donde la propia aplicación gestiona los mecanismos necesarios.

La elección entre TCP y UDP depende de las necesidades del protocolo o aplicación.

---

## 42. Puertos TCP y UDP

Una dirección IP permite identificar un dispositivo o interfaz dentro de una red IP, pero un mismo dispositivo puede ejecutar múltiples servicios simultáneamente.

Los números de puerto permiten identificar los diferentes servicios o procesos de comunicación.

Por ejemplo, un servidor podría ofrecer simultáneamente:

- Una página web.
- Un servicio DNS.
- Acceso mediante SSH.

Todos pueden utilizar la misma dirección IP, pero utilizar diferentes números de puerto.

Los números de puerto tienen 16 bits, por lo que sus valores se encuentran entre:

`0 - 65535`

Algunos ejemplos habituales son:

| Servicio | Puerto habitual | Transporte |
|---|---:|---|
| FTP | 20/21 | TCP |
| SSH | 22 | TCP |
| DNS | 53 | UDP/TCP |
| DHCP | 67/68 | UDP |
| HTTP | 80 | TCP |
| HTTPS | 443 | TCP |

Estos valores permiten que el sistema operativo entregue la información recibida al servicio correspondiente.

---

## 43. ICMP y Ping

ICMP (*Internet Control Message Protocol*) se utiliza para transmitir determinados mensajes de control y diagnóstico relacionados con IP.

Una de las herramientas más conocidas que utiliza ICMP es:

`ping`

Ping permite comprobar si existe conectividad IP con otro dispositivo y obtener información básica sobre la comunicación.

Por ejemplo:

`ping 192.168.1.20`

De forma simplificada, pueden intercambiarse:

- ICMP Echo Request.
- ICMP Echo Reply.

Si existe respuesta, sabemos que se ha conseguido establecer determinada conectividad IP entre los dispositivos.

Sin embargo, que un ping falle no significa necesariamente que el dispositivo esté apagado.

El tráfico ICMP puede estar bloqueado por firewalls, ACL u otros mecanismos de seguridad.

Ping será una de las herramientas principales utilizadas durante este proyecto para verificar y diagnosticar conectividad.

---

## 44. Traceroute

Traceroute es una herramienta de diagnóstico utilizada para observar los diferentes saltos de Capa 3 que sigue el tráfico hacia un destino.

En Windows puede utilizarse:

`tracert`

Por ejemplo:

`tracert 8.8.8.8`

Mientras que ping permite comprobar conectividad básica, traceroute puede ayudar a identificar por qué routers o saltos está pasando el tráfico y en qué punto podría existir un problema.

Esta herramienta será especialmente útil cuando NexaCorp disponga de múltiples routers y conexiones entre sedes.

---

## 45. DHCP

DHCP (*Dynamic Host Configuration Protocol*) permite proporcionar automáticamente parámetros de configuración de red a los clientes.

Sin DHCP, podría ser necesario configurar manualmente en cada dispositivo información como:

- Dirección IP.
- Máscara de subred.
- Gateway predeterminado.
- Servidores DNS.

En una empresa con cientos de dispositivos, realizar este proceso manualmente sería poco práctico y aumentaría la posibilidad de cometer errores.

Mediante DHCP, los dispositivos pueden obtener automáticamente la configuración correspondiente.

De forma simplificada, el proceso inicial de DHCP en IPv4 suele explicarse mediante cuatro mensajes:

1. DHCP Discover.
2. DHCP Offer.
3. DHCP Request.
4. DHCP ACK.

Este proceso suele recordarse mediante las siglas:

`DORA`

DHCP se implementará posteriormente en NexaCorp para automatizar la configuración de diferentes dispositivos.

---

## 46. DNS

DNS (*Domain Name System*) permite relacionar nombres con información necesaria para localizar recursos, entre otras funciones.

Una de sus funciones más conocidas consiste en resolver nombres de dominio a direcciones IP.

Por ejemplo, para los usuarios es mucho más sencillo utilizar un nombre como:

`www.ejemplo.com`

que memorizar una dirección IP.

De forma simplificada:

`Nombre → DNS → Dirección IP`

DNS será un servicio fundamental dentro de la infraestructura empresarial y de la comunicación con servicios de Internet.

---

## 47. Switching

El switching es el proceso mediante el cual los switches reciben y reenvían tramas dentro de una red.

Como se ha estudiado anteriormente, un switch Ethernet puede aprender direcciones MAC observando la dirección MAC de origen de las tramas que recibe.

Estas asociaciones se almacenan en su tabla MAC.

Posteriormente puede consultar la dirección MAC de destino para determinar por qué puerto debe reenviar una trama.

El switching será uno de los elementos fundamentales de las redes LAN de NexaCorp.

Posteriormente se estudiarán conceptos más avanzados como:

- VLAN.
- Trunking.
- Spanning Tree Protocol.
- EtherChannel.
- Port Security.
- DHCP Snooping.
- Dynamic ARP Inspection.

---

## 48. Routing

El routing es el proceso utilizado para determinar cómo deben enviarse paquetes entre redes diferentes.

Los routers mantienen información sobre las redes que conocen mediante una tabla de routing.

Esta tabla puede contener rutas obtenidas de diferentes formas, por ejemplo:

- Redes directamente conectadas.
- Rutas estáticas.
- Rutas aprendidas mediante protocolos dinámicos de routing.

Cuando un router recibe un paquete destinado a otra red, consulta su tabla de routing para determinar cómo debe reenviarlo.

Durante el proyecto se estudiarán inicialmente las rutas estáticas y posteriormente protocolos dinámicos como OSPF.

---

## 49. Tabla de Routing

Una tabla de routing contiene información que permite a un dispositivo de Capa 3 conocer diferentes redes y determinar cómo alcanzarlas.

De forma conceptual, una entrada podría indicar:

`Para llegar a la red X → utiliza el siguiente salto o interfaz Y`

Los routers comparan la dirección IP de destino de los paquetes con las rutas disponibles para tomar decisiones de forwarding.

Si no existe una ruta adecuada hacia el destino, el router no podrá reenviar correctamente el paquete hacia dicha red.

Posteriormente se estudiará el funcionamiento de las tablas de routing utilizando dispositivos Cisco reales dentro de Packet Tracer.

---

## 50. Ruta Predeterminada

Una ruta predeterminada puede utilizarse cuando un router no dispone de una ruta más específica hacia el destino.

En IPv4 suele representarse como:

`0.0.0.0/0`

Conceptualmente significa:

`Si no conozco una ruta más específica, utiliza este camino.`

Las rutas predeterminadas son habituales, por ejemplo, para dirigir tráfico hacia Internet desde determinadas partes de una red.

No debe confundirse:

- Gateway predeterminado de un host.
- Ruta predeterminada de un router.

Ambos conceptos están relacionados con alcanzar destinos externos, pero se aplican en contextos diferentes.

---

## 51. NAT y PAT

Las redes empresariales utilizan normalmente direcciones IPv4 privadas para sus dispositivos internos.

Estas direcciones privadas no se enrutan directamente a través de Internet.

NAT (*Network Address Translation*) permite modificar información de direccionamiento IP al atravesar determinados dispositivos de red.

Una utilización habitual consiste en permitir que dispositivos con direccionamiento privado puedan comunicarse con Internet utilizando direccionamiento público.

PAT (*Port Address Translation*) permite que múltiples dispositivos internos compartan una misma dirección IPv4 pública diferenciando las comunicaciones mediante información adicional, como los números de puerto.

De forma simplificada:

`Muchos dispositivos privados → NAT/PAT → IP pública → Internet`

NAT y PAT se configurarán posteriormente cuando NexaCorp necesite conectividad hacia Internet.

---

## 52. VLAN

Una VLAN (*Virtual Local Area Network*) permite crear redes lógicas independientes utilizando infraestructura de switching.

Sin VLAN, conectar muchos dispositivos al mismo entorno de Capa 2 podría hacer que todos formasen parte del mismo dominio de broadcast.

Mediante VLAN podemos separar lógicamente diferentes grupos.

Por ejemplo:

- VLAN Dirección.
- VLAN Ventas.
- VLAN Desarrollo.
- VLAN IT.
- VLAN Voz.
- VLAN Invitados.
- VLAN Servidores.
- VLAN Administración.

Dos dispositivos conectados físicamente al mismo switch pueden pertenecer a VLAN diferentes y estar lógicamente separados.

Cada VLAN suele asociarse a una subred IP diferente.

Las VLAN serán fundamentales para implementar la segmentación de NexaCorp.

---

## 53. Puertos Access

Un puerto configurado como access pertenece normalmente a una única VLAN y suele utilizarse para conectar dispositivos finales.

Por ejemplo:

`PC → Puerto Access → Switch`

Un PC del departamento de Ventas podría conectarse a un puerto perteneciente a la VLAN de Ventas.

Otro PC conectado al mismo switch podría utilizar otro puerto perteneciente a la VLAN de Desarrollo.

De esta forma, un único switch físico puede proporcionar conectividad a diferentes redes lógicas.

---

## 54. Trunking y 802.1Q

Cuando dos switches necesitan transportar tráfico perteneciente a múltiples VLAN a través del mismo enlace puede utilizarse un enlace trunk.

Por ejemplo:

`Switch 1 ═════ TRUNK ═════ Switch 2`

Un trunk puede transportar tráfico perteneciente a diferentes VLAN.

IEEE 802.1Q permite identificar a qué VLAN pertenece una trama mediante etiquetado.

Esto permitirá extender las VLAN necesarias entre diferentes switches de la infraestructura.

Posteriormente se estudiarán conceptos relacionados como:

- Etiquetado 802.1Q.
- VLAN nativa.
- VLAN permitidas en un trunk.

---

## 55. Routing Inter-VLAN

Las VLAN permiten separar redes lógicamente.

Sin embargo, en determinadas situaciones será necesario que dispositivos pertenecientes a VLAN diferentes puedan comunicarse.

Como cada VLAN puede representar una red IP diferente, se necesita routing para permitir esta comunicación.

A este proceso se le conoce como routing inter-VLAN.

La comunicación puede realizarse mediante diferentes diseños, como:

- Router-on-a-Stick.
- Switches multicapa.

En NexaCorp, las comunicaciones entre departamentos estarán controladas y no se permitirá necesariamente que todas las VLAN puedan comunicarse libremente entre sí.

---

## 56. Dominio de Broadcast

Un dominio de broadcast representa el conjunto de dispositivos que pueden recibir determinado tráfico broadcast de Capa 2.

Los switches pueden reenviar broadcasts dentro de la VLAN correspondiente.

Los routers no reenvían normalmente broadcasts Ethernet entre diferentes redes.

Las VLAN permiten dividir una infraestructura de switching en diferentes dominios de broadcast.

Por ejemplo:

`VLAN 10 → Dominio de broadcast 1`

`VLAN 20 → Dominio de broadcast 2`

Esta separación mejora la organización, escalabilidad y control de la red.

---

## 57. Spanning Tree Protocol

Cuando se añaden enlaces redundantes entre switches pueden producirse bucles de Capa 2.

Los bucles Ethernet pueden provocar problemas graves, como:

- Tormentas de broadcast.
- Inestabilidad de las tablas MAC.
- Duplicación de tramas.

STP (*Spanning Tree Protocol*) permite mantener redundancia física evitando que todos los caminos redundantes permanezcan activos simultáneamente cuando esto produciría un bucle.

STP crea una topología lógica libre de bucles y puede permitir utilizar caminos alternativos cuando cambia la topología.

Posteriormente se estudiarán conceptos como:

- Root Bridge.
- Root Port.
- Designated Port.
- Puertos bloqueados o alternativos.
- RSTP.
- BPDU.

---

## 58. EtherChannel

EtherChannel permite agrupar varios enlaces físicos Ethernet y tratarlos lógicamente como un único enlace.

Por ejemplo:

`Switch A ==== varios enlaces ==== Switch B`

puede convertirse lógicamente en:

`Switch A ===== EtherChannel ===== Switch B`

Esto puede proporcionar:

- Mayor capacidad agregada.
- Redundancia de enlaces.
- Simplificación lógica de varios enlaces físicos.

Entre los mecanismos relacionados con EtherChannel se encuentran:

- LACP.
- PAgP.

Esta tecnología será utilizada posteriormente en la infraestructura redundante de NexaCorp.

---

## 59. ACL

Una ACL (*Access Control List*) permite crear reglas para permitir o denegar determinado tráfico de red.

Las ACL pueden evaluar información como:

- Dirección IP de origen.
- Dirección IP de destino.
- Protocolos.
- Puertos, dependiendo del tipo de ACL.

Por ejemplo, NexaCorp podría necesitar permitir que determinados usuarios accedan a un servidor mientras se impide ese acceso desde la red de invitados.

Las ACL serán una de las herramientas utilizadas para implementar políticas de comunicación entre segmentos.

---

## 60. Seguridad de Capa 2

La seguridad de una red empresarial no depende únicamente de firewalls.

También existen mecanismos destinados a proteger la infraestructura de switching.

Durante el proyecto se estudiarán tecnologías como:

### Port Security

Permite aplicar restricciones relacionadas con las direcciones MAC que pueden utilizar determinados puertos de acceso.

### DHCP Snooping

Permite establecer controles relacionados con mensajes DHCP y diferenciar puertos confiables y no confiables.

### Dynamic ARP Inspection

Puede utilizar información confiable para validar determinados mensajes ARP y ayudar a mitigar ataques relacionados con falsificación ARP.

### BPDU Guard

Puede proteger determinados puertos frente a la recepción inesperada de BPDUs de Spanning Tree.

Estas tecnologías se implementarán cuando la infraestructura básica de switching ya esté funcionando.

---

## 61. Redes Inalámbricas

Las redes inalámbricas permiten conectar dispositivos mediante tecnologías como WiFi.

Un punto de acceso inalámbrico o Access Point permite proporcionar conectividad inalámbrica a los clientes.

En NexaCorp existirán al menos dos tipos conceptuales de acceso inalámbrico:

- WiFi corporativo.
- WiFi para invitados.

Ambas redes deberán permanecer separadas.

Los usuarios corporativos podrán acceder a determinados recursos internos según las políticas definidas.

Los invitados deberán disponer de acceso a Internet sin obtener acceso a la infraestructura corporativa interna.

---

## 62. Telefonía IP y Voice VLAN

La telefonía IP permite transportar comunicaciones de voz utilizando redes IP.

Los teléfonos IP pueden compartir parte de la infraestructura física utilizada por otros dispositivos, pero es habitual separar lógicamente el tráfico de voz.

Para ello pueden utilizarse Voice VLAN.

Esto facilita la organización y aplicación de políticas específicas para los dispositivos de telefonía.

NexaCorp dispondrá de telefonía IP como parte de su infraestructura empresarial.

---

## 63. DMZ

Una DMZ (*Demilitarized Zone*) es un segmento de red utilizado para aislar determinados servicios que necesitan estar más expuestos o ser accesibles desde redes externas.

Por ejemplo, una organización podría disponer de determinados servidores públicos dentro de una DMZ.

El objetivo es evitar colocar estos servicios directamente dentro de la red interna de usuarios.

De forma conceptual:

`Internet → Firewall → DMZ`

y, de forma separada:

`Firewall → Red interna`

La comunicación entre Internet, DMZ y red interna deberá estar controlada mediante políticas de seguridad.

NexaCorp utilizará una DMZ para determinados servicios públicos.

---

## 64. Redundancia y Alta Disponibilidad

Una red empresarial debe intentar reducir los puntos únicos de fallo en aquellos elementos considerados críticos.

La redundancia consiste en disponer de recursos o caminos alternativos capaces de mantener determinados servicios cuando se produce un fallo.

Puede aplicarse a elementos como:

- Enlaces.
- Switches.
- Routers.
- Gateways.
- Conexiones WAN.

Sin embargo, añadir redundancia también aumenta la complejidad y puede generar problemas si no se utilizan los protocolos adecuados.

Durante el proyecto se utilizarán tecnologías como STP, EtherChannel y mecanismos de redundancia de gateway.

---

## 65. HSRP

HSRP (*Hot Standby Router Protocol*) es un protocolo de redundancia de primer salto utilizado en dispositivos Cisco.

Permite que varios dispositivos participen en la provisión de un gateway virtual para los hosts.

En lugar de depender exclusivamente de la dirección física de un único router o dispositivo de Capa 3, los clientes pueden utilizar una dirección IP virtual como gateway.

Si el dispositivo que está proporcionando activamente el servicio deja de estar disponible, otro dispositivo puede asumir el papel correspondiente.

HSRP se estudiará posteriormente cuando NexaCorp disponga de una infraestructura donde tenga sentido implementar redundancia de gateway.

---

## 66. WAN

Una WAN permite conectar redes geográficamente separadas.

En NexaCorp será necesario establecer comunicación entre:

- Málaga.
- Madrid.
- Sevilla.

Cada sede dispondrá de su propia infraestructura LAN.

Posteriormente se implementará una arquitectura WAN que permita intercambiar tráfico entre las sedes.

El diseño exacto dependerá de las tecnologías que puedan representarse adecuadamente dentro de Cisco Packet Tracer y de los objetivos educativos del proyecto.

---

## 67. OSPF

OSPF (*Open Shortest Path First*) es un protocolo de routing dinámico.

Permite que routers intercambien información sobre las redes disponibles y calculen rutas para alcanzar diferentes destinos.

Una ventaja de utilizar routing dinámico es que la infraestructura puede adaptarse automáticamente a determinados cambios de topología sin depender exclusivamente de rutas configuradas manualmente.

Durante el proyecto se estudiará progresivamente:

- Routing estático.
- Ruta predeterminada.
- OSPF.
- Vecindades OSPF.
- Intercambio de rutas.
- Selección de caminos.
- Posibles diseños multiárea cuando resulte apropiado.

---

## 68. Servicios Centralizados

Una infraestructura empresarial puede utilizar diferentes servicios centralizados para facilitar su administración.

NexaCorp incorporará progresivamente servicios como:

### DHCP

Asignación automática de parámetros de red.

### DNS

Resolución de nombres.

### NTP

Sincronización horaria de dispositivos.

### Syslog

Centralización de determinados mensajes y eventos generados por dispositivos.

### AAA

Mecanismos relacionados con autenticación, autorización y contabilización.

### TFTP

Protocolo sencillo de transferencia de archivos que puede utilizarse en determinados escenarios de administración y laboratorio.

Estos servicios serán implementados y verificados individualmente durante el proyecto.

---

## 69. Administración Segura mediante SSH

Los dispositivos de red necesitan ser administrados.

Aunque es posible realizar determinadas configuraciones utilizando acceso local, en una infraestructura empresarial resulta necesario disponer de mecanismos de administración remota.

SSH (*Secure Shell*) permite establecer sesiones remotas cifradas.

Se utilizará SSH para administrar de forma segura dispositivos compatibles.

La administración de routers y switches estará restringida a las redes y usuarios autorizados.

---

## 70. Monitorización de Red

Administrar una red no consiste únicamente en configurarla.

También es necesario conocer su estado y detectar problemas.

Durante el proyecto se introducirán mecanismos y protocolos relacionados con la monitorización y administración, como:

- SNMP.
- Syslog.
- NTP.
- CDP.
- LLDP.

Estas herramientas permitirán obtener información sobre dispositivos, eventos, vecinos y funcionamiento de la infraestructura.

---

## 71. Troubleshooting

El troubleshooting es el proceso sistemático utilizado para identificar, localizar y solucionar problemas.

Una metodología básica puede incluir:

1. Identificar el problema.
2. Recopilar información.
3. Determinar qué partes funcionan correctamente.
4. Localizar dónde comienza el fallo.
5. Formular una posible causa.
6. Comprobar la hipótesis.
7. Aplicar una solución.
8. Verificar que el servicio funciona correctamente.
9. Documentar el problema y la solución.

El modelo OSI puede utilizarse como referencia durante este proceso.

Por ejemplo, ante un problema de conectividad podrían comprobarse progresivamente:

- Estado físico del enlace.
- Configuración de interfaces.
- VLAN.
- Dirección MAC.
- Dirección IP.
- Máscara.
- Gateway.
- Tabla de routing.
- ACL.
- DNS.
- Servicio de aplicación.

El proyecto incluirá escenarios creados intencionadamente para practicar troubleshooting.

---

## 72. Herramientas Básicas de Diagnóstico

Durante el proyecto se utilizarán diferentes comandos y herramientas para verificar el funcionamiento de la red.

Algunos ejemplos son:

### `ping`

Permite realizar pruebas básicas de conectividad IP.

### `tracert` / `traceroute`

Permite observar los saltos de Capa 3 hacia un destino.

### `ipconfig`

En sistemas Windows permite consultar información sobre la configuración IP de las interfaces.

### `arp`

Permite consultar información relacionada con la caché ARP del sistema.

### Comandos `show` de Cisco IOS

Permiten consultar el estado y configuración de diferentes elementos de los dispositivos Cisco.

Algunos ejemplos que aparecerán posteriormente son:

`show ip interface brief`

`show interfaces`

`show mac address-table`

`show vlan brief`

`show interfaces trunk`

`show ip route`

Estos comandos se estudiarán cuando se utilicen realmente durante las diferentes fases del proyecto.

---

## 73. Flujo Básico de una Comunicación

A partir de todos los conceptos estudiados podemos representar de forma simplificada una comunicación entre dos dispositivos.

Supongamos que PC-A quiere comunicarse con un servidor situado en otra red.

### Paso 1 - La aplicación genera información

Una aplicación del PC genera los datos que necesita enviar.

### Paso 2 - Capa de transporte

TCP o UDP puede proporcionar la información necesaria para identificar la comunicación entre aplicaciones.

### Paso 3 - Capa de red

IPv4 añade información como:

- IP de origen.
- IP de destino.

### Paso 4 - Decisión local o remota

El dispositivo utiliza su dirección IP y máscara para determinar si el destino pertenece a su propia subred.

Si el destino está en otra red, deberá utilizar el gateway predeterminado.

### Paso 5 - Resolución de la MAC necesaria

Si el dispositivo no conoce la MAC necesaria para realizar la entrega en el enlace local, puede utilizar ARP.

Si el destino está en otra red, la MAC que necesita inicialmente será la correspondiente al siguiente salto local, normalmente el gateway, y no la MAC del dispositivo remoto.

### Paso 6 - Creación de la trama

El paquete IP se encapsula dentro de una trama Ethernet con las direcciones MAC correspondientes al enlace.

### Paso 7 - Switching

Los switches utilizan información de Capa 2 para reenviar la trama dentro de la LAN.

### Paso 8 - Routing

Cuando la trama llega al router, este procesa el paquete IP y consulta su información de routing para decidir cómo continuar hacia la red de destino.

Para el siguiente enlace se utilizará una nueva encapsulación de Capa 2 apropiada para dicho enlace.

### Paso 9 - Llegada al destino

El proceso continúa hasta alcanzar la red donde se encuentra el dispositivo de destino.

Finalmente, el dispositivo recibe la información y realiza el proceso de desencapsulación hasta entregar los datos a la aplicación correspondiente.

---

## 74. Aplicación de los Fundamentos a NexaCorp

Los conceptos estudiados en este documento constituyen la base sobre la que se construirá la infraestructura de NexaCorp.

Durante las siguientes fases será necesario aplicar estos conocimientos para:

- Diseñar el direccionamiento IPv4.
- Crear subredes mediante VLSM.
- Segmentar departamentos mediante VLAN.
- Configurar switches.
- Configurar trunks.
- Implementar routing entre VLAN.
- Configurar routers.
- Comunicar las diferentes sedes.
- Proporcionar DHCP y DNS.
- Proporcionar acceso a Internet mediante NAT/PAT.
- Aplicar ACL.
- Implementar seguridad de Capa 2.
- Crear redes WiFi corporativas y de invitados.
- Implementar telefonía IP.
- Crear una DMZ.
- Añadir redundancia.
- Implementar routing dinámico.
- Centralizar servicios de administración y monitorización.
- Crear y resolver fallos de red.

Cada tecnología será estudiada con mayor profundidad antes de ser implementada.

---

## 75. Resumen

Una red informática permite que diferentes dispositivos puedan intercambiar información y compartir recursos.

Los dispositivos finales generan y reciben información, mientras que dispositivos intermediarios como switches y routers permiten transportar el tráfico a través de la infraestructura.

Los switches trabajan principalmente con tramas Ethernet y direcciones MAC dentro de redes LAN.

Los routers permiten comunicar diferentes redes utilizando direccionamiento IP y tablas de routing.

IPv4 utiliza direcciones de 32 bits divididas en cuatro octetos.

Las máscaras de subred y los prefijos CIDR permiten determinar qué parte de una dirección identifica la red y qué parte corresponde a los hosts.

El subnetting permite dividir redes en subredes más pequeñas y VLSM permite utilizar diferentes tamaños según las necesidades reales.

Protocolos como ARP, ICMP, TCP, UDP, DHCP y DNS cumplen diferentes funciones necesarias para que las comunicaciones puedan producirse correctamente.

Tecnologías como VLAN, STP, EtherChannel, ACL, NAT, OSPF y HSRP permitirán construir progresivamente una infraestructura empresarial segmentada, escalable, segura y redundante.

Todos estos conceptos se aplicarán de forma práctica durante la construcción de la red de NexaCorp en Cisco Packet Tracer.