##Router

Conecta dos redes diferentes, nuestra LAN con la WAN (Wide Area Network) o sea, con Internet. 

Puede ser con una línea telefónica ADSL o con fibra óptica y puede tener también ser punto de acceso Wifi como el router doméstico de la figura

![](/assets/2019-12-23 10_04_07-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

Detrás del router tenemos que saber que tenemos:
* La conexión de la línea ADSL o de fibra óptica
* Un botón de **Reset** sólo accesible con la ayuda de por ejemplo un clip, para resetearlo mantenemos pulsado con el clip el botón reset durante unos segundos hasta que veamos que el router se apaga sólo y se vuelve a encender.
* Las diferentes conexiones **Eth**ernet para el cableado a los diferentes switchs. (en amarillo)
* Un puerto USB
* Botón de encendido y apagado y la conexión a la alimentación

![](/assets/2019-12-23 09_34_05-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

Es importante saber estos elementos y localizarlos para cualquier problema.

>PROBLEMA : Internet no va en mi centro.

El principal sospechoso sería el router, hay que comprobar si están encendidos todos los leds del router.

![](/assets/2019-12-23 09_32_22-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

 * si alguno está en **rojo** ya nos informa donde está el problema, por ejemplo si el led ADSL/Internet  está en rojo, el problema está en nuestro proveedor (Movistar, Vodafone ... ). Podemos resetear el router a ver si vuelve la conexión.
 * Si están encendidos todos en **verde**, podemos conectar por ejemplo un portátil en uno de las conexiones Eth y comprobar si hay Internet.
 
 ![](/assets/2019-12-23 09_30_42-Adobe Flash Player 11.png)
 *Fuente Movistar manual usuario*
 
   * Si no hay Internet, el problema no es el router sino el siguiente elemento de abajo de la cascada de nuestra red: El switch o el cableado entre el switch y el router.
   * Si hay Internet, el fallo es el router. Podemos resetear el router a ver si vuelve la conexión.
   
   En el caso de que haciendo estas simples comprobaciones sigue sin funcionar, [llamamos al servicio CAU](/problemas-que-hago.md).
   
##El router es un mini-ordenador

Con un sistema operativo llamado **firmware** (software almacenado en los chips de un dispositivo) funcionando y accesible mediante una aplicación web. 

**El acceso a la aplicación del router de tu centro educativo SOLO ES ACCESIBLE POR EL SERVICIO CAU** no obstante consideramos que en tu formación COFOTAP conozcas de la existencia de esta aplicación por la importancia en la configuración de tu red.

Para acceder a la aplicación hay que teclear [la IP puerta de enlace](/redes/ips.md) en un navegador:

![](/assets/2019-12-23 09_36_17-Nueva pestaña.png)

y **CADA MODELO DE ROUTER TIENE UNA APLICACION WEB DISTINTA** aquí por ejemplo vamos a enseñar capturas del modelo de router Movistar:

![](/assets/2019-12-23 09_41_42-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

Para acceder se pide un usuario y contraseña

![](/assets/2019-12-23 09_45_14-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

>Es curioso saber que el router es siempre ignorado como elemento crítico de seguridad, esto ha provocado muchos problemas. Una vez en una PYME de un amigo mio, se le infectaba cualquier PC que se conectaba en la red LAN de su pequeña oficina. Al final descubrí que el virus estaba en su router pues tenía una contraseña de acceso un poco débil: 1234 ¿no crees que algún hacker la conoce? fue cambiarla y actualizar el firmware y problema resuelto. ¿Y tú? ¿has cambiado la contraseña de tu router y tienes actualizado su firmware o llevas la misma de fábrica?

Entrar en la aplicación Web nos permite por ejemplo [cambiar la puerta de enlace, las DNS](/redes/ips.md) de tu red

![](/assets/2019-12-23 10_05_48-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

O cambiar el nombre de la red wifi y su contraseña si es un router con wifi.

![](/assets/2019-12-23 10_00_31-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

Es importante cambiar la **SSID** o nombre de red y su **contraseña**, y la encriptación que sea **WPA-PSK (TKIP)** de los que viene por defecto, para evitar accesos no deseados. 

>Existen muchas aplicaciones incluso APs que tienen los valores por defecto de los routers inalámbricos y así conectarse de forma pirata. El servicio CAU de tu centro ya ha tenido esta precaución ¿y tú en tu casa? ¿tienes el mismo nombre de red y contraseña Wifi en tu router que cuando lo comprastes?

Para actualizar el Firmware hay que descargarlo de la web del fabricante y luego en la aplicación web del router entrar en opciones avanzadas:

![](/assets/2019-12-23 10_19_19-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

Y seleccionar el fichero, teniendo en cuenta que mientras estamos actualizando el Firmware **no se puede desconectar el router** pues si se apaga, se inutiliza de forma permanente el router.

![](/assets/2019-12-23 10_19_30-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*

En esta aplicación web también se pueden **abrir puertos** PERO ESTO ES UNA PUERTA ABIERTA AL EXTERIOR con el consecuente peligro de seguridad. En la figura se puede ver que se ha abierto al equipo con la IP 192.168.1.33 diferentes puertos seguramente para descargas punto a punto P2P tipo Torrent y similares.

![](/assets/2019-12-23 10_26_23-Adobe Flash Player 11.png)
*Fuente Movistar manual usuario*


















   
   
   
   

