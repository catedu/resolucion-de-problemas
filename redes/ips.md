# IP4

Está formado por 4 números cada uno de ellos puede ser desde 0 hasta 255 y el ordenador lo traduce en una secuencia de 8bits

Por ejemplo la IP 192.168.1.55 es realmente 1100000 10101000 00000001 00110111

**NO PUEDE HABER EN EL MUNDO DOS EQUIPOS CON LA MISMA IP** excepto las IP reservadas. Esto provoca que ya quedan pocos IP4 disponibles, por eso se creó el IPv6.

##IP4 reservadas
Dentro de la LAN de tu centro se asignan IPs a cada equipo, cada una es única **dentro de la LAN** pero esta información llega al router y el router cambia esa IP por la suya que es única en la WAN de Internet, o sea que la IP del ordenador del centro *no viaja como cabecera por Internet* sino la del router.

 Luego el router ya se encarga de distribuir los paquetes a cada equipo de la LAN pues realmente la IP del equipo se sigue conservando dentro del paquete de información.
 
  En resumen que un ordenador del centro puede tener la 192.168.1.55 y en *otro centro educativo* puede tener la 192.168.1.55 en otro equipo. Pero no puede haber dos ordenadores de tu centro con la IP 192.168.1.55.
  
  **Conclusión:** Las 192.168.x.x donde x son números entre 0 y 255 están [reservadas para uso privado](https://es.wikipedia.org/wiki/Red_privada) interno dentro de las LAN. También las 172.16.x.x hasta la 172.31.x.x.
  
  La 127.0.0.1 es una dirección especial que se usa para referirse a uno mismo y la 255.255.255.255 es para referirse a todos.
  
 #CONFIGURAR LA IP
   
Nos vamos a **Inicio - Panel de control - Conexiones de red e Internet - Conexiones de red** y aparecen nuestras conexiones, fija, inalámbrica. Nos vamos a la que queremos configurar con el **botón derecho - Propiedades - Protocolo TPCP/IPv4** 

  ![](/assets/2019-12-24 10_17_13-Window.png)
  
 Aquí tenemos varias opciones que tienes que ver detenidamente:
 
 #####IP AUTOMÁTICA
 Podemos hacer que el router, switchs , o  los AP asignen automáticamente una IP al equipo. Esto es posible si en su configuración se ha activado la **DHCP** 
 
 
 >Si por error hemos configurado manualmente una IP estática al rango DHCP, puede ocurrir que dicha dirección sea asignada dinámicamente a otro PC, provocándose un **conflicto de IP**.


  
  
  
  
    

 