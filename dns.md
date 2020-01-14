#DNS Domain Name Server

El DNS es la IP del servidor que nos proporciona los nombres de dominio, es decir, yo cuando pongo www.google.es en el navegador, mi ordenador va a pedir la página web al servidor de google ¿pero dónde está? ¿cual es su dirección IP? Para ello está el servidor DNS:

![](/assets/2020-01-14 10_46_33.jpg)

*Fuente elaboración propia con imágenes CC de Wikipedia*

#¿Vale pues cualquier dirección DNS ?

Sí teóricamente, puedes poner **cualquier dirección DNS** para que te puedas navegar en Internet, por ejemplo Google tiene un servidor DNS que es 8.8.8.8 pero **en tu centro recomendamos que pongas las de la DGA por cuestiones de seguridad**

* DNS DE LA DGA **188.244.82.1** Y **188.244.82.17** luego tiene que quedar así

![](/assets/2020-01-14 10_59_50.jpg)

##Para que experimentes
**¿Cómo puedo saber la IP de una página?** muy fácil, con el comando ping (entra en la ventana de comandos buscando cmd), por ejemplo para la página www.google.es vemos este resultado:

![](/assets/2020-01-14 11_04_22.jpg)

Sale [172.217.17.3](/172.217.17.3) si lo pones en el navegador ¡¡te sale la página de Google!!

No siempre funciona pues muchas no todos los servidores y navegadores aceptan que entres de forma directa.

¿Google tiene esa dirección siempre? si, la tiene fija la habrá contratado y no sólo esas, sino que tiene varios servidores replicados con diferentes ip, teclea en la ventana de comandos **nslookup www.google.es** y te saldrán varios que puedes tener acceso (no a todos).


