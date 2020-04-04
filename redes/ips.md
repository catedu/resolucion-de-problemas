# IPv4

Está formado por 4 números cada uno de ellos puede ser desde 0 hasta 255 y el ordenador lo traduce en una secuencia de 8bits

Por ejemplo la IP `192.168.1.55` es realmente `1100000 10101000 00000001 00110111`

**NO PUEDE HABER EN EL MUNDO DOS EQUIPOS QUE NAVEGUEN CON LA MISMA IP**. Esto provoca que ya quedan pocos IP4 disponibles, por eso se creó el [IPv6](https://es.wikipedia.org/wiki/IPv6).

La afirmación anterior no entra en contradicción con lo explicado de las IP Públicas en [Protocolos](/protocolos.md), pues dos equipos de tu LAN pueden navegar con la misma IP Pública pues quien navega realmente es el servidor que te proporciona Internet, luego él distribuye esos paquetes de información a quienes se lo han solicitado gracias a las IP reservadas.

##IPv4 reservadas

Dentro de la LAN de tu centro se asignan IPs a cada equipo, son IP reservadas, cada una es única **dentro de tu LAN** pero esta información llega al router y al servidor de Internet y cambia esa IP por la suya **la IP pública** que es única en la WAN de Internet, o sea que la IP del ordenador del centro que es IP reservada *no viaja como cabecera por Internet*. 

Luego el router ya se encarga de distribuir los paquetes a cada equipo de la LAN pues realmente la IP del equipo se sigue conservando dentro del paquete de información.
 
En resumen que un ordenador del centro puede tener la 192.168.1.55 y en *otro centro educativo* puede tener la 192.168.1.55 en otro equipo. Pero no puede haber dos ordenadores de tu centro con la IP 192.168.1.55.
  
>**info**
>**Conclusión:** Las 192.168.x.x donde x son números entre 0 y 255 están reservadas para uso privado interno dentro de las LAN. También las 172.16.x.x hasta la 172.31.x.x, y [otras más...](https://es.wikipedia.org/wiki/Red_privada)
  
La 127.0.0.1 es una dirección especial que se usa para referirse a uno mismo y las que tienen todos unos: 255 también es especial que es para referirse a todos (Broadcast).
  
![](/assets/2020-01-20 13_34_28.jpg)
  
#CONFIGURAR LA IPv4
   
Nos vamos a **Inicio - Panel de control - Conexiones de red e Internet - Conexiones de red** y aparecen nuestras conexiones, fija, inalámbrica. Nos vamos a la que queremos configurar con el **botón derecho - Propiedades - Protocolo TPCP/IPv4** 

![Captura de pantalla](/assets/2019-12-24 10_17_13-Window.png)
  
Aquí tenemos varias opciones que tienes que ver detenidamente:
 
###IP AUTOMÁTICA

Podemos hacer que el router, switchs , o  los AP asignen automáticamente una IP al equipo. Esto es posible si en la configuración del AP, switch o router se ha activado la **DHCP** ya lo hemos visto en el [anterior capítulo](/protocolos.md)
 
###IP ESTÁTICA - DIRECCIÓN IP
 
En muchos centros interesa que los equipos estén localizados, esto suele pasar en equipos fijos e impresoras. 
 
* Hay que tener cuidado con no poner una IP de otro equipo.
* Las IPs tienen que ser de las reservadas pues estamos hablando de tu LAN local no de la WAN (o sea la externa, Internet).

>**info**
>Si por error hemos configurado manualmente una IP estática al rango DHCP de un router, AP... puede ocurrir que dicha dirección sea asignada dinámicamente a otro PC, provocándose un **conflicto de IP**.

####IP ESTÁTICA - MÁSCARA DE RED

La máscara de red es un número de unos y ceros y en la frontera es lo que corta en la dirección IP que parte es lo común en toda la LAN de tu centro y qué parte es exclusiva a cada equipo.

#### IP estática - Máscara de red - Tipo C (la más común)

Esto se ve mejor en un ejemplo, supongamos que tenemos una IP en el **ordenador ALUMNO 172.168.1.23** y una MÁSCARA DE RED: **255.255.255.0** o sea en binario 11111111 . 11111111 . 11111111 . 00000000 eso quiere decir que la parte común de toda la LAN de tu centro es 172.168.1 y el número 23 es propio de ese equipo. 

O sea que las IPs de esa subred de ese centro van desde la 172.168.1.0 hasta la 172.168.1.254 en total puedes tener 255 equipos.

>**success**
>Nota: no se puede utilizar la 172.168.1.255 pues es la dirección especial *Broadcast*.

Si a otro equipo, por ejemplo **ordenador PROFESOR IP 172.168.2.15 ** entonces pertenece a otra LAN es decir **no se pueden ver entre ellos PROFESOR-ALUMNO**. Y a otro equipo **JEFATURA IP 172.168.3.6** tampoco se verán entre ellos ALUMNO-PROFESOR-JEFATURA. Es lo que se llama crear subredes **VLAN**.

Un ejemplo de arquitectura de red sería la siguiente

![Elaboración propia con imágenes CC de Wikipedia](/assets/2020-01-14 18_57_48.jpg)

>**info**
>Podrías pensar que algún alumno *listo* 👿 simplemente cambiando la IP a por ejemplo 172.168.3.24 podría acceder a jefatura 172.168.3.6, pero si el switch que le tiene que dar acceso (los Ubiquitis en el caso de la figura anterior) pertenecen a la red 172.168.1.x no puede, ese ordenador hacker se queda aislado, ni siquiera podría navegar. 

>Pero si es *muy listo* 😈😈 puede coger un cable de red RJ45 y conectarse a la red cableada, luego **SI QUE PUEDE**. Luego: los ordenadores de profesores y administración que no compartan nada sin contraseña (eso lo permite Windows, si tuvieran Linux 🐧no habría ese problema).

#### IP estática - Máscara de red - Tipo B

Pero si en tu centro quieres una VLAN más amplia puedes utilizar la máscara 255.255.0.0 por lo tanto el rango de IPs de esa red para los ordenadores sería desde la 172.168.1.1 hasta 172.168.255.254 (la 172.168.255.255 sería la de *Broadcast*) o sea que pueden haber hasta 2 elevado a 16 o sea 65.536 dispositivos en esa VLAN.

#### IP estática - Máscara de red - Otros tipos

Como te puedes imaginar existe la Tipo A con máscara 255.0.0.0 para un número de dispositivos de 2 elevado a 24.

>**info**
>Las máscaras de red no tienen por que ser de las descritas por ejemplo una máscara 255.255.248.0 sería en binario 11111111 . 11111111 . 1111000 . 00000000 lo que permite 2 elevado a 11 equipos en la VLAN (tantos como 0) o sea 2.048 equipos.

##IP ESTÁTICA - PUERTA DE ENLACE o GATEWAY

Es la IP del router, es decir, el equipo tiene que saber qué equipo de su LAN es el que le da acceso a la WAN exterior, o sea Internet. Normalmente suele ser 172.168.1.1 ver [Router](/redes/router.md)

#Registra tus IPs
Como responsable de los medios informáticos es **importante** que registres qué IP tiene cada equipo de tu centro (o rangos, por ejemplo de las 172.30.7.1 a 50 es la aula de informática) no lo hagas en papel pues suele ser información muy "viva". 

>**info**
*Pfff eso es mucho curro...* bueno pues asegúrate que **TODOS** los chismes de tu centro están encendidos y ejecuta [Wireless Network Watcher](https://www.nirsoft.net/utils/wireless_network_watcher.html) y en View-Htlm Report el resultado de la tabla la seleccionas y la copias y pegas en una hoja de cálculo. Faena hecha !!

