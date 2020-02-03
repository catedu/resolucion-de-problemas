#Protocolos
Digamos que son las reglas del lenguaje de los paquetes de información, hay muchos protocolos, los comunes son:

* **HTTP** es el protocolo de las páginas Web, [se inventó en el CERN](https://es.wikipedia.org/wiki/Historia_de_la_World_Wide_Web) para publicar información entre científicos.
* **HTTPS** es el mismo que en anterior pero añadiendo una seguridad de su origen. **Nunca tenemos que navegar en una página web importante por ejemplo un banco o tienda virtual que no sea en su inicio HTTPS** (o el símbolo del candado en el navegador) de lo contrario es una página web falsa o fishing que nos quiere robar las contraseñas.
* **FTP** es el protocolo para la transferencia de ficheros.
* **SMTP POP3** el de los correos electrónicos.

##TCP/IP

Todos estos protocolos utilizan paquetes de información, pero estos a su vez utilizan el protocolo **TCP/IP** digamos que es *el protocolo de Internet*.

* **TCP**  (transmision control protocol) se encarga de asegurar que el paquete tenga su contenido correcto.
* **IP** (Internet protocol) es la dirección del equipo destino. **Todos** los equipos conectados a Internet tienen un número.

>**info**
>Cuando se inventó este protocolo fue cuando realmente se inventó Internet pues posibilitaba la interconexión entre ordenadores de forma masiva y con libertad ¿sabías que tiene su origen [en la guerra fría](https://es.wikipedia.org/wiki/ARPANET)?.
 
#DHCP

DHCP, Dynamic Host ConfigurationProtocol se inventó para simplificar las asignaciones de IPs a los equipos para hacerlo automático, básicamente es una conversación entre el ordenador que quiere conectarse a Internet y el servidor, esta figura sería el esquema dentro de tu LAN:

![Elaboración propia con imágenes CC de Wikipedia](/assets/2019-12-26 08_39_47-Window.png)

La pregunta del ordenador cliente *"No tengo IP ¿alguien me da una?"* la lanza a una IP especial llamada **Broadcast** que son todo unos al final y que lo leen todos los de su LAN.

#La IP pública

También ocurre esto entre tu router y el servidor de tu proveedor de telefónia de Internet, luego tenemos:

* La IP que muestra nuestro router a nuestra LAN que la podemos definir nosotros, es fija, llamada **puerta de enlace**
* Una IP del router al servidor de Internet que la define el servidor de Internet por su propio protocolo DHCP, al ser una IP temporal, entonces se llama **IP dinámica**..
* La que navega el servidor de Internet y la que ve el mundo. Es la **IP Pública** y esta geolocalizada. ¿Cual es? Pues por ejemplo lo puedes averiguar en [https://ipleak.net](https://ipleak.net/)
* Esta información **es pública** aunque navegues de incógnito esta información se utiliza por ejemplo cuando visitas una página web, los anuncios te personalizan su contenido.
* Como puedes ver **todo lo que hacemos en Internet deja un rastro  **. 

>**info**
>Investiga: Entra en [https://ipleak.net](https://ipleak.net/) cuando estés por el ámbito rural (aunque sea con tu móvil) verás que no coincide con tu situación real. Yo por ejemplo estoy ahora en Calamocha y me dice que navego con 188.244.80.254 de Zaragoza. Esto es debido a que mi servidor de Internet está en los servidores de AST de Pignatelli y tienen esa IP.

![Elaboración propia con imágenes CC de Wikipedia](/assets/2020-01-14 19_47_52.jpg)

>**info**
>INVESTIGA UN POCO: Entra en dos equipos diferentes de tu centro (o de tu casa, por ejemplo un ordenador y el móvil pero ojo, el móvil conectado a la misma LAN que el ordenador (o sea por Wifi no con datos móviles)) y a la vez a la página [ipleak.net](https://ipleak.net/) en los dos equipos ¿cómo es posible que están navegando con la misma IP?
>Respuesta: Esto es debido a que las IPs de tu LAN son reservadas y navegan con la misma IP pública que es el mismo servidor de Internet

##La IP del router, puerta de enlace, acceso o Gateway

Esta IP privada del router hacia nuestra LAN es la IP que todos los equipos de nuestro centro tienen que saber para poder navegar, pues necesitan saber quién es el que les va a proveer el servicio de Internet. Esta IP especial se llama **IP DE LA PUERTA DE ENLACE** o también **GATEWAY**, suele ser en tu centro la 172.168.1.1.

##¿Cómo se configura el DHCP ?
Vamos a poner el ejemplo de configurar el DHCP de un AP Ubiquiti.

>**info**
>También podría ser el del [router](/redes/router.md), los conceptos son los mismos pero las pantallas y lugar del menú cambian y depende de las marcas, esto **NO es un tutorial** sino un curso para que entiendas los conceptos.

>Esta configuración, igual que lo explicado en el [router](/redes/router.md)  está reservada al [servicio técnico](/problemas-que-hago.md), se muestra aquí para comprender los conceptos.

Entramos en su aplicación web, supongamos que en  el AP Ubiquiti es la http://192.168.1.102 y después de loguearnos, en Network la dirección IP del AP, su máscara de red, la dirección Gateway. Si quisieramos que el router le asigne dinámicamente una IP marcaríamos DHCP, pero es mejor que sea estática para poder localizar este AP Ubiquiti.

![Capbura de pantalla](/assets/2019-12-26 09_20_51-Window.png)

¿Pero no íbamos a configurar la DHCP y ahora dices que es mejor dejarla estática? Ojo no te confundas esa es la IP del AP Ubiquiti, lo que queremos es que ese AP Ubiquiti asigne automáticamente IP a nuestros equipos de la LAN:

![Elaboración propia con imágenes CC de Wikipedia](/assets/2019-12-26 09_39_37-Window.png)

En configuración de la LAN es donde activaremos el DHCP

![Captura de pantalla](/assets/2019-12-26 09_43_28-Window.png)

Como vemos en la figura se ha activado el DHCP y proporcionará a los equipos IPs desde la 169.254.190.2 hasta la 169.254.190.254 durante 172.800 segundos. También vemos que hay una excepción para la impresora que le dará una IP fija y así la tenemos localizada para poderla instalar en los equipos.

>**info**
>OJO para que el DHCP funcione, en cada equipo tiene que estar configurado la opción DHCP, esto lo veremos en el [siguiente capítulo.](/redes/ips.md)

Gráficamente la configuración quedaría así:

![Elaboración propia con imágenes CC de Wikipedia](/assets/2019-12-26 10_09_15-Window.png)
