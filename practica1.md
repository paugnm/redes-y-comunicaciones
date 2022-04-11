#Práctica 1
---
####¿Qué es una red? ¿Cuál es el principal objetivo para construir una red?
Una red de computadoras es un conjunto de computadoras/dispositivos conectados con el objetivo de **compartir recursos** (dispositivos, información, servicios, etc).

####¿Qué es Internet? Describa los principales componentes que permiten su funcionamiento.
Hay dos formas de definir qué es internet: 
- Describiendo sus **componentes esenciales** 
- Describiéndola en términos de la **infraestructura de red que proporciona servicios a aplicaciones distribuídas.**

Los componentes básicos de Internet son:
- Fuente (Software)
- Emisor/Transmisor (Hardware)
- Medio de transmisión y dispositivos intermedios (Hardware)
- Procesos intermedios que tratan la información (Sw y Hw)
- Receptor (Hardware)
- Destino (Software)
- Otros: protocolos (Sw), información, mensaje transmitido (Sw)
- Señal de información, materialización del mensaje sobre el medio (Hw)

####¿Qué son las RFCs?
Son los documentos asociados a los **estándares de Internet** desarrollados por el IETF (Internet Engineering Task Force, Grupo de trabajo de ingeniería de Internet).

####¿Qué es un protocolo?
Un protocolo define el ***formato*** y el ***orden*** de los mensajes intercambiados entre dos o más entidades que se comunican, así como las ***acciones*** tomadas al producirse la transmisión y/o recepción de un mensaje u otro suceso.


####¿Por qué dos máquinas con distintos sistemas operativos pueden formar parte de una misma red?
Gracias a los modelos de organización en capas que reducen la complejidad y a que ambos extremos de la red siguen el mismo stack de protocolos en cada una de esas capas.

####¿Cuáles son las 2 categorías en las que pueden clasificarse a los sistemas finales o End Systems? Dé un ejemplo del rol de cada uno en alguna aplicación distribuida que corra sobre Internet.

Los hosts se clasifican en dos categorías: clientes y servidores. De un modo informal, podríamos decir que los clientes suelen ser las computadoras de escritorio y portátiles, los teléfonos inteligentes, etc., mientras que los servidores suelen ser equipos más potentes que almacenan y distribuyen páginas web, flujos de vídeo, correo electrónico, etc.

 ¿Cuál es la diferencia entre una red conmutada de paquetes de una red conmutada de circuitos?

####Existen dos métodos fundamentales que permiten transportar datos a través de la red de enlaces y conmutadores: la conmutación de paquetes y la conmutación de circuitos.
- **Conmutación de circuitos:** al establecer la comunicación entre los sistemas terminales, los recursos quedan reservados para el circuito, se transfieran datos o no. Ej: redes telefónicas.
- **Conmutación de paquetes:**  estos recursos no están reservados, los mensajes de una sesión utilizan los recursos bajo petición y, en consecuencia, pueden tener que esperar (es decir, ponerse en cola) para poder acceder a un enlace de comunicaciones.

####Analice qué tipo de red es una red de telefonía y qué tipo de red es Internet.

Internet es una red de conmutación por paquetes y la red de telefonía es una red de conmutación de circuitos.

####Describa brevemente las distintas alternativas que conoce para acceder a Internet en su hogar.

###### ADSL:
Acceso a Internet con la misma empresa telefónica local que proporciona el acceso telefónico local fijo. Por tanto, cuando se utiliza el acceso mediante DSL, la compañía telefónica del cliente también actúa como ISP. El módem ADSL de cada cliente utiliza la línea telefónica existente (hilo de cobre de par trenzado) para intercambiar datos con un multiplexor de acceso ADSL, ubicado en la central de la compañía telefónica localque “divide” el tráfico recibido para que las comunicaciones de voz vayan por un canal y el acceso a Internet por otro. 
###### Cablemodem:
Utiliza la infraestructura de televisión por cable existente. Las viviendas obtienen el acceso por cable a Internet de la misma compañía que les proporciona la televisión por cable. Se usa fibra óptica para conectar el terminal de cabecera del cable a una serie de nodos de área situados en el vecindario, a partir de los cuales se utiliza cable coaxial tradicional para llegar a todos los domicilios. Puesto que en este sistema se emplea tanto cable coaxial como fibra, a menudo se denomina sistema HFC (Hybrid Fiber Coax, Híbrido de fibra y coaxial).

######Fibra óptica:
Proporciona velocidades aún más altas que el ADSL y el cable que puede brindar una red pura de fibra óptica al hogar FTTH (Fiber-To-The-Home, Fibra hasta el hogar). El concepto en que se basa FTTH es muy simple: proporcionar una ruta de fibra óptica directa hasta la vivienda desde la central telefónica. Sobrepasan en gran medida a cualquier otra tecnología salvo en lo que refiere a las dificultades que presenta el manejo del cable de fibra en tanto nos encontramos frente a un hilo de vidrio frágil y de poca maleabilidad pero con una fuerte resistencia a ruidos externos. Entonces, las bondades tecnológicas que ofrece la transmisión de información a través de la fibra, sumado a sus bajos costos de fabricación (el silicio es considerablemente más económico que el cobre), entre otras cualidades, colocan a este sistema dentro de los primeros puestos en tecnologías de transporte de datos. 

######Acceso a Internet en Redes de Telefonía Móvil

####¿Qué ventajas tiene una implementación basada en capas o niveles?

- Reduce la complejidad 
- Las capas de abajo ocultan la complejidad a las de arriba, abstracción
- Las capas de arriba utilizan servicios de las de abajo: interfaces, similar a APIs
- Los cambios en una capa no deberían afectar a las demás si la interfaz se mantiene
- Facilita el desarrollo y la evolución de las componentes de red asegurando interoperabilidad
- Facilita el aprendizaje, diseño y administración de las redes

####¿Cómo se llama la PDU de cada una de las siguientes capas: Aplicación, Transporte, Red y Enlace
**PDU:** Protocol Data Unit, Unidad de protocolo de datos.
| Capa       | PDU    |
|:----------:|:------:|
| Aplicación |Datos   | 
| Transporte |Segmento|
| Red        |Paquete |
| Enlace     |Trama   | 

####¿Qué es la encapsulación? Si una capa realiza la encapsulación de datos, ¿qué capa del nodo receptor realizará el proceso inverso?
Mientras los datos de la aplicación bajan al stack del protocolo y se transmiten por los medios de la red, varios protocolos le agregan información en cada nivel. Esto comúnmente se conoce como **proceso de encapsulación**. 

El proceso inverso es realizado por la misma capa que realizó el encapsulamiento pero del lado del receptor.

####Describa cuáles son las funciones de cada una de las capas del stack TCP/IP o protocolo de Internet.

#####Capa de aplicación
Es donde residen las aplicaciones de red y sus protocolos de nivel de aplicación. La capa de aplicación de Internet incluye muchos protocolos, tales como el protocolo HTTP (que permite la solicitud y transferencia de documentos web), SMTP (que permite la transferencia de
mensajes de correo electrónico) y FTP (que permite la transferencia de archivos entre dos sistemas terminales).

#####Capa de transporte
La capa de transporte de Internet transporta los mensajes de la capa de aplicación entre los puntos terminales de la aplicación. En Internet, existen dos protocolos de transporte, TCP y UDP, pudiendo cada uno de ellos transportar los mensajes de la capa de aplicación. 

#####Capa de Red
La capa de red de Internet es responsable de trasladar los paquetes de la capa de red, conocidos
como datagramas, de un host a otro. El protocolo de la capa de transporte Internet (TCP o UDP) de un host de origen pasa un segmento de la capa de transporte y una dirección de destino a la capa de red. Luego, la capa de red proporciona el servicio de suministrar el segmento a la capa de transporte del host de destino.
La capa de red de Internet incluye el conocido protocolo IP. Existe un único protocolo IP y todos los componentes de Internet que tienen una capa de red deben ejecutar el protocolo IP.

#####Capa de acceso a la red
La capa de acceso a la red es la primera capa de la pila TCP/IP. Ofrece la capacidad de acceder a cualquier red física, es decir, brinda los recursos que se deben implementar para transmitir datos a través de la red.

####Compare el modelo OSI con la implementación TCP/IP
![Capas del modelo TCP/IP y OSI](img\osi-tcp.jpg)
#####Similitudes:
- Ambos se dividen en capas.
- Ambos tienen capas de aplicación, aunque incluyen servicios distintos
- Ambos tienen capas de transporte similares.
- Ambos tienen capa de red similar pero con distinto nombre.
- Se supone que la tecnología es de conmutación de paquetes (no de conmutación de circuitos).

#####Diferencias:
- TCP/IP combina las funciones de la capa de presentación y de sesión en la capa de aplicación. 
- TCP/IP combina la capas de enlace de datos y la capa física del modelo OSI en una sola capa. 
- TCP/IP más simple porque tiene menos capas. 
- Los protocolos TCP/IP son los estándares en torno a los cuales se desarrolló Internet, de modo que la credibilidad del modelo TCP/IP se debe en gran parte a sus protocolos. 
- El modelo OSI es un modelo “más” de referencia, teórico, aunque hay implementaciones.

