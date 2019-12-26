#Protocolos
Digamos que son las reglas del lenguaje de los paquetes de información, hay muchos protocolos, los comunes son:

* **HTTP** es el protocolo de las páginas Web
* **HTTPS** es el mismo que en anterior pero añadiendo una seguridad de su origen. **Nunca tenemos que navegar en una página web importante por ejemplo un banco o tienda virtual que no sea en su inicio HTTPS** (o el símbolo del candado en el navegador) de lo contrario es una página web falsa o fishing que nos quiere robar las contraseñas.
* **FTP** es el protocolo para la transferencia de ficheros.
* **SMTP POP3** el de los correos electrónicos.

##TCP/IP

Todos estos protocolos utilizan paquetes de información, pero estos a su vez utilizan el protocolo **TCP/IP** digamos que es *el protocolo de Internet*.

* **TCP**  (transmision control protocol) se encarga de asegurar que el paquete tenga su contenido correcto.
* **IP** (Internet protocol) es la dirección del equipo destino. **Todos** los equipos conectados a Internet tienen un número.

>Cuando se inventó este protocolo fué cuando realmente se inventó Internet ¿sabías que tiene su origen en la guerra fría?.
 
#DHCP

DHCP, Dynamic Host ConfigurationProtocol se inventó para simplificar las asignaciones de IPs a los equipos para hacerlo automático, básicamente es una conversación entre el ordenador que quiere conectarse a Internet y el servidor, esta figura sería el esquema dentro de tu LAN:

![](/assets/2019-12-26 08_39_47-Window.png)
*Fuente elaboración propia con imágenes CC de Wikipedia*

También ocurre esto entre tu router y el servidor de tu proveedor de telefónia de Internet, luego en el router tenemos dos IPs la que muestra a nuestra LAN que la podemos definir nosotros, es fija y es una de las IPs reservadas y la que navega el router por el mundo. Al ser una IP temporal se dice que es una **IP dinámica**

![](/assets/2019-12-26 08_54_36-Window.png)
*Fuente elaboración propia con imágenes CC de Wikipedia*

Todos los ordenadores de tu LAN navegan con esa **IP pública** que está asignada temporalmente a tu router, y esta geolocalizada. ¿Cual es? Pues por ejemplo lo puedes averiguar en [https://ipleak.net](https://ipleak.net/), prueba dentro de unas horas y verás que ha cambiado. Toda esa información es pública de tu navegación en Internet, y es lo que permite localizar a los cyberdelincuentes. También puedes ver que no coincide exáctamente donde estás especialmente en el mundo rural pues está geolocalizada en el servidor de Internet. 


