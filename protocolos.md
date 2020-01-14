#Protocolos
Digamos que son las reglas del lenguaje de los paquetes de información, hay muchos protocolos, los comunes son:

* **HTTP** es el protocolo de las páginas Web, [se inventó en el CERN](https://es.wikipedia.org/wiki/Historia_de_la_World_Wide_Web) para publicar información.
* **HTTPS** es el mismo que en anterior pero añadiendo una seguridad de su origen. **Nunca tenemos que navegar en una página web importante por ejemplo un banco o tienda virtual que no sea en su inicio HTTPS** (o el símbolo del candado en el navegador) de lo contrario es una página web falsa o fishing que nos quiere robar las contraseñas.
* **FTP** es el protocolo para la transferencia de ficheros.
* **SMTP POP3** el de los correos electrónicos.

##TCP/IP

Todos estos protocolos utilizan paquetes de información, pero estos a su vez utilizan el protocolo **TCP/IP** digamos que es *el protocolo de Internet*.

* **TCP**  (transmision control protocol) se encarga de asegurar que el paquete tenga su contenido correcto.
* **IP** (Internet protocol) es la dirección del equipo destino. **Todos** los equipos conectados a Internet tienen un número.

>Cuando se inventó este protocolo fue cuando realmente se inventó Internet pues posibilitaba la interconexión entre ordenadores de forma masiva y con libertad ¿sabías que tiene su origen [en la guerra fría](https://es.wikipedia.org/wiki/ARPANET)?.
 
#DHCP

DHCP, Dynamic Host ConfigurationProtocol se inventó para simplificar las asignaciones de IPs a los equipos para hacerlo automático, básicamente es una conversación entre el ordenador que quiere conectarse a Internet y el servidor, esta figura sería el esquema dentro de tu LAN:

![](/assets/2019-12-26 08_39_47-Window.png)

*Fuente elaboración propia con imágenes CC de Wikipedia*

También ocurre esto entre tu router y el servidor de tu proveedor de telefónia de Internet, luego en el router tenemos dos IPs la que muestra a nuestra LAN que la podemos definir nosotros, es fija y es una de las IPs reservadas y la que navega el router por el mundo. Al ser una IP temporal se dice que es una **IP dinámica**

![](/assets/2019-12-26 08_54_36-Window.png)

*Fuente elaboración propia con imágenes CC de Wikipedia*

Todos los ordenadores de tu LAN navegan con esa **IP pública** que está asignada temporalmente a tu router, y esta geolocalizada. ¿Cual es? Pues por ejemplo lo puedes averiguar en [https://ipleak.net](https://ipleak.net/), prueba dentro de unas horas y verás que ha cambiado. Toda esa información es pública de tu navegación en Internet, y es lo que permite localizar a los cyberdelincuentes. También puedes ver que no coincide exáctamente donde estás especialmente en el mundo rural pues está geolocalizada en el servidor de Internet. 

##La IP del router
Esta IP privada del router hacia nuestra LAN es la IP que todos los equipos de nuestro centro tienen que saber para poder navegar, pues necesitan saber quién es el que les va a proveer el servicio de Internet. Esta IP especial se llama **IP DE LA PUERTA DE ACCESO** o también **GATEWAY**.

##¿Cómo se configura el DHCP ?
Vamos a poner el ejemplo de configurar el DHCP de un AP Ubiquiti.

>También podría ser el del [router](/redes/router.md), los conceptos son los mismos pero las pantallas y lugar del menú cambian y depende de las marcas, esto **NO es un tutorial** sino un curso para que entiendas los conceptos.

>Esta configuración, igual que lo explicado en el [router](/redes/router.md)  está reservada al [servicio técnico](/problemas-que-hago.md), se muestra aquí para comprender los conceptos.

Entramos en su aplicación web, supongamos que en  el AP Ubiquiti es la http://192.168.1.102 y después de loguearnos, en Network la dirección IP del AP, su máscara de red, la dirección Gateway. Si quisieramos que el router le asigne dinámicamente una IP marcaríamos DHCP, pero es mejor que sea estática para poder localizar este AP Ubiquiti.

![](/assets/2019-12-26 09_20_51-Window.png)

¿Pero no íbamos a configurar la DHCP y ahora dices que es mejor dejarla estática? Ojo no te confundas esa es la IP del AP Ubiquiti, lo que queremos es que ese AP Ubiquiti asigne automáticamente IP a nuestros equipos de la LAN:

![](/assets/2019-12-26 09_39_37-Window.png)
*Fuente elaboración propia con imágenes CC de Wikipedia*

En configuración de la LAN es donde activaremos el DHCP

![](/assets/2019-12-26 09_43_28-Window.png)

Como vemos en la figura se ha activado el DHCP y proporcionará a los equipos IPs desde la 169.254.190.2 hasta la 169.254.190.254 durante 172.800 segundos. También vemos que hay una excepción para la impresora que le dará una IP fija y así la tenemos localizada para poderla instalar en los equipos.

>OJO para que el DHCP funcione, en cada equipo tiene que estar configurado la opción DHCP, esto lo veremos en el [siguiente capítulo.](/redes/ips.md)

Gráficamente la configuración quedaría así:

![](/assets/2019-12-26 10_09_15-Window.png)

*Fuente elaboración propia con imágenes CC de Wikipedia*




