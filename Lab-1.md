## [Preguntas reflexivas de ambientación](#) ✔

¿Cual es la dirección de red y de broadcast de un host que tiene una ip 192.168.10.10/30?.

    La dirección de red y de broadcast de un host con la IP 192.168.10.10/30 son las siguientes:
    
    - Dirección de red: Para calcular la dirección de red, se realiza una operación AND entre la dirección IP y la máscara
    de subred. En este caso, la máscara de subred /30 tiene un valor de 255.255.255.252 en formato decimal. Realizando la 
    operación AND, se obtiene la dirección de red: 192.168.10.8[6].

    - Dirección de broadcast: La dirección de broadcast es la última dirección de la subred y se utiliza para enviar datos 
    a todos los hosts dentro de la red. En este caso, la dirección de broadcast sería la siguiente dirección después de la 
    dirección de red. Para una máscara /30, que tiene un tamaño de subred de 4 direcciones, la dirección de broadcast sería
    192.168.10.11[6].

    Por lo tanto, la dirección de red es 192.168.10.8 y la dirección de broadcast es 192.168.10.11.

¿Que información se puede inferir de un host con la dirección 169.254.255.200/26?.

    La dirección IP 169.254.255.200/26 pertenece a la clase de direcciones IP reservadas para el uso de enlaces locales o 
    APIPA (Automatic Private IP Addressing). Estas direcciones se asignan automáticamente a dispositivos cuando no pueden
    obtener una dirección IP válida de un servidor DHCP.

    Al analizar la dirección IP 169.254.255.200/26, podemos inferir lo siguiente:

    1. **Dirección IP**: La dirección IP es 169.254.255.200. Esta dirección se encuentra en el rango reservado para enlaces
    locales.

    2. **Máscara de subred**: La máscara de subred /26 indica que los primeros 26 bits de la dirección IP representan la 
    parte de red y los últimos 6 bits representan la parte de host.

    3. **Rango de direcciones**: Con una máscara de subred /26, el rango de direcciones válido para hosts sería desde 
    169.254.255.192 hasta 169.254.255.255. Sin embargo, la dirección específica 169.254.255.200 se encuentra dentro de este 
    rango.

    4. **Número de hosts**: Con una máscara de subred /26, hay un total de 64 direcciones posibles para hosts. Sin embargo,
    algunas de estas direcciones pueden estar reservadas para otros fines, como la dirección de broadcast y la dirección 
    de red.

    En resumen, la información que se puede inferir de un host con la dirección 169.254.255.200/26 es que pertenece a la 
    clase de direcciones IP reservadas para enlaces locales y que se encuentra dentro de un rango de direcciones válido para
    hosts con una máscara de subred /26.

¿Cuantas sub-redes puede lograr con la mascara 172.16.0.0/22?.

    Para calcular cuántas subredes se pueden lograr con la máscara 172.16.0.0/22, podemos utilizar la fórmula 2^n, donde
    "n" es el número de bits que se han tomado prestados de la porción de host. En este caso, la máscara /22 utiliza 22 
    bits para la porción de red y 10 bits para la porción de host. Por lo tanto, se han tomado prestados 10 bits de la 
    porción de host. La fórmula 2^n nos dice que podemos crear 2^10 subredes, lo que equivale a 1024 subredes[1]. Por lo
    tanto, con la máscara 172.16.0.0/22, se pueden lograr 1024 subredes.

¿Cuantos clientes puede tener la sub red 172.16.0.0/22?.

    Para determinar cuántos clientes puede tener la subred 172.16.0.0/22, es necesario conocer la cantidad de direcciones
    IP disponibles en la subred. La máscara de subred /22 indica que los primeros 22 bits de la dirección IP son parte de
    la porción de red, mientras que los últimos 10 bits son parte de la porción de host. Esto significa que hay 
    2^10 - 2 = 1022 direcciones IP disponibles para los clientes en la subred. La resta de 2 se debe a que la dirección
    de red (172.16.0.0) y la dirección de broadcast (172.16.3.255) no se pueden asignar a dispositivos[1]. Por lo tanto,
    la subred 172.16.0.0/22 puede tener hasta 1022 clientes.

¿Que clase y tipo de dirección es 10.10.10.0/24?.

    La dirección 10.10.10.0/24 es una dirección de red de Clase A[2]. Esto significa que los primeros 8 bits de la 
    dirección IP están reservados para identificar la red, mientras que los últimos 24 bits se utilizan para identificar
    los dispositivos en la red[5]. En este caso, la máscara de subred es 255.255.255.0, lo que indica que los primeros 
    24 bits de la dirección IP son fijos y los últimos 8 bits pueden variar para identificar los dispositivos en la red[5].

    En resumen, la dirección 10.10.10.0/24 pertenece a una red de Clase A y tiene una máscara de subred de 255.255.255.0,
    lo que permite hasta 256 direcciones IP en la red[4].

## [Caracterización de los adaptadores](#) ✔
|Parámetro||Valor|
|--|:--:|--:|
|Número de adaptadores Físicos|-->|3|
|Número de adaptadores Virtuales|-->|2|
|Tipo de Adaptador principal|-->|Ethernet|
|Fabricante del Adaptador principal|-->|Realtek PCIe FE Family Controller|
|Código MAC del fabricante|-->|C8-5B-76|
|MAC|-->|C8-5B-76-0C-16-08|

## [Caracterización de la red](#) ✔
|Parámetro|Valor|
|--|--:|
|__Subnet__|192.168.0.1/24|
|IPv4|192.168.254.109|
|Subnet Mask decimal|24|
|Subnet Mask octetos|255.255.255.0|
|Número de direcciones de Host|254|
|Rango de direcciones de Host|192.168.0.1-254|
|IP Broadcast||
|Server DHCP||
|Server DNS|192.168.0.1|

## [Caracterización de la puerta de enlace](#) ✔
|Parámetro|Valor|
|--|--:|
|Número de Entradas en la tabla ARP |11|
|IPv4 Gateway|192.168.0.1|
|MAC Gateway|C8-5B-76-0C-16-08|
|ISP|TV AZTECA SUCURSAL COLOMBIA|
|[IP Publica][5]|190.2.210.158|
|[Sistema Autónomo][6]|AS262186|

## [Retardo de la red](#) ✔
|Servidor|IP|Tiempo promedio/ms|
|--|--|--|
|DNS Google|8.8.8.8|25ms|
|DNS Cloudflare|1.1.1.1|39ms|
|OpenDNS|208.67.222.222|93ms|
|Alternate DNS|76.76.19.19|38ms|
|DNS Quad9|9.9.9.9|25ms|
|AdGuard DNS|94.140.14.14|175ms|

## [Capacidad del canal](#) ✔
|Servidor|Ping/ms|Down/MB|Up/MB|
|--|:--:|--:|--:|
|[speed test][1]|36|34|34|
|[Netflix][2]|33|21|23|
|[Claro][3]|33|39.8|39.4|
|[nperf][4]|47|40.70|37.29|

## [Distancia desde el host](#) ✔
|Servidor|Ping/ms|Numero de Saltos|
|--|:--:|--:|
|google.com|38|11|
|GMail.com|25|11|
|YouTube.com|22|11|
|dns.google|25|11|
|aws.amazon.com|39|11|
|portal.azure.com|21|10|
|login.live.com|97|14|
|Facebook.com|27|11|
|c.ns.WhatsApp.net|110|18|
|claro.com.co|172|17|
|platzi.com|64|12|
|rappi.com.co|161|28|


