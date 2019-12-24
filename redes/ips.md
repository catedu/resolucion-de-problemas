#Protocolos
Digamos que son las reglas del lenguaje de los paquetes de información, hay muchos protocolos, los comunes son:

* **HTTP** es el protocolo de las páginas Web
* **HTTPS** es el mismo que en anterior pero añadiendo una seguridad de su origen. **Nunca tenemos que navegar en una página web importante por ejemplo un banco o tienda virtual que no sea en su inicio HTTPS** (o el símbolo del candado en el navegador) de lo contrario es una página web falsa o fishing que nos quiere robar las contraseñas.
* **FTP** es el protocolo para la transferencia de ficheros.
* **SMTP POP3** el de los correos electrónicos.

Todos estos protocolos utilizan paquetes de información, pero estos a su vez utilizan el protocolo **TCP/IP** 

* **TCP**  (transmision control protocol) se encarga de asegurar que el paquete tenga su contenido correcto.
* **IP** (Internet protocol) es la dirección del equipo destino. **Todos** los equipos conectados a Internet tienen un número.
 
# IP4

Está formado por 4 números cada uno de ellos puede ser desde 0 hasta 255 y el ordenador lo traduce en una secuencia de 8bits

Por ejemplo la IP 192.168.1.55 es realmente 1100000 10101000 00000001 00110111

**NO PUEDE HABER DOS EQUIPOS CON LA MISMA IP** pero hay trampas para saltarse esta regla:

##IP4 reservadas
Dentro de la LAN de tu centro se asignan IPs a cada equipo, cada una es única **dentro de la LAN** pero esta información llega al router y el router cambia esa IP por la suya que es única en la WAN de Internet, o sea que la IP del ordenador del centro *no viaja como cabecera por Internet* sino la del router.

 Luego el router ya se encarga de distribuir los paquetes a cada equipo de la LAN pues realmente la IP del equipo se sigue conservando dentro del paquete de información.
 
  En resumen que un ordenador del centro puede tener la 192.168.1.55 y en *otro centro educativo* puede tener la 192.168.1.55 en otro equipo. Pero no puede haber dos ordenadores de tu centro con la IP 192.168.1.55.
  
  Conclusión: Las 192.168.x.x donde x son números entre 0 y 255 están [reservadas para uso privado](https://es.wikipedia.org/wiki/Red_privada) interno dentro de las LAN.
  
  La 127.0.0.1 es una dirección especial que se usa para referirse a uno mismo y la 255.255.255.255 es para referirse a todos.
  
 #CONFIGURAR LA IP
   
Nos vamos a **Inicio - Panel de control - Conexiones de red e Internet - Conexiones de red** y aparecen nuestras conexiones, fija, inalámbrica. Nos vamos a la que queremos configurar con el **botón derecho - Propiedades - Protocolo TPCP/IPv4** 

  ![](/assets/2019-12-24 10_17_13-Window.png)
  
 Aquí tenemos varias opciones que tienes que ver detenidamente:
 
 #####IP AUTOMÁTICA
 Podemos hacer que el router, switchs , o  los AP asignen automáticamente una IP al equipo. Esto es posible si en su configuración se ha activado la **DHCP** 
  
  
  
  
    

 