#DNS Domain Name Server

El DNS es la IP del servidor que nos proporciona los nombres de dominio, es decir, yo cuando pongo www.google.es en el navegador, mi ordenador va a pedir la página web al servidor de google ¿pero dónde está? ¿cual es su dirección IP? Para ello está el servidor DNS, se lo pregunta antes a él:

![](/assets/2020-01-14 10_46_33.jpg)

*Fuente elaboración propia con imágenes CC de Wikipedia*

#¿Vale pues cualquier dirección DNS ?

Sí, teóricamente, puedes poner **cualquier dirección DNS válida** para que te puedas navegar en Internet, por ejemplo Google tiene un servidor DNS que es 8.8.8.8 pero **en tu centro educativo público es obligatorio que pongas las de la DGA por cuestiones de seguridad y control de navegación**

* DNS DE LA DGA **188.244.82.1** Y **188.244.82.17** luego tiene que quedar así

![](/assets/2020-01-14 10_59_50.jpg)

Si tecleas en la [ventana de comandos](/redes/a-experimentar.md) **nslookup** puedes ver el nombre de su servidor, te tiene que salir el servidor del gobierno de aragón (en el caso de centros públicos):

![](/assets/2020-01-14 20_45_04.jpg)

>EXPERIMENTA ¿qué dirección me proporciona mi servidor DNS para una página concreta? por ejemplo www.catedu.es
>Respuesta: Teclea **nslookup www.catedu.es** y te saldrá una cosa así:

![](/assets/2020-01-15 07_39_38-Window.png)

>Donde las primeras dos direcciones son las de tu servidor DNS (en el caso de la figura es un servidor de Jazztel con IP 87.216.1.65 pues lo he hecho en casa) y las otras dos son las de CATEDU, o sea que su IP es 217.76.130.174.



