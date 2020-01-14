#A EXPERIMENTAR
#¿Cómo puedo saber la IP de una página WEB?

Muy fácil, con el comando ping a esa página (entra en la ventana de comandos buscando **cmd** en linux tiene su propia ventana de comandos en **terminal**)

Por ejemplo para la página www.google.es vemos este resultado:

![](/assets/2020-01-14 11_04_22.jpg)

Sale [172.217.17.3](/172.217.17.3) si lo pones en el navegador ¡¡te sale la página de Google!!

No siempre funciona pues muchas no todos los servidores y navegadores aceptan que entres de forma directa.

¿Google tiene esa dirección siempre? si, la tiene fija la habrá contratado y no sólo esas, sino que tiene varios servidores replicados con diferentes ip, teclea en la ventana de comandos **nslookup www.google.es** y te saldrán varios que puedes tener acceso (no a todos).

#¿Cuantos switchs y servidores hay entre mi ordenador y una página Web?

Pues ya que sabes entrar a la ventana de comandos, teclea **tracert y la página que quieras** por ejemplo tracert google.es y te sorprenderás. La primera IP que verás es la de tu router (ver [IP puerta de enlace](/protocolos.md))

Este es el resultado desde el ordenador donde estoy escribiendo (para que veas que no siempre las IP reservadas de un centro son 172.168.1.x en este caso es 4.6.1.x)

![](/assets/2020-01-14 20_16_38.jpg)

o sea

![](/assets/2020-01-14 20_17_09.jpg)

*Fuente imágenes libres y elaboración propia*

Nos da una idea de la calidad de nuestra conexión a esa web.

##¿Qué dirección IP tengo rápidamente?

En Windows teclea en comandos **ipconfig** o si quieres saber también las dns **ipconfig/all** 
En Linux teclea **ifconfig**

Por ejemplo se puede ver que mi IP es 4.6.1.30, que la puerta de enlace es 4.6.1.251 que la máscara de red es de tipo C y que mis DNS son las del Gobierno de Aragón:

![](/assets/2020-01-14 20_25_04.jpg)

Si por ejemplo el ordenador está conectado a Internet desde dos sitios, sale toda la información:

![](/assets/2020-01-14 20_28_56-Window.png)

En este caso puedes ver que la tarjeta de red está conectado con la IP 4.6.1.33 al router 4.6.1.251 y la tarjeta inalámbrica Wifi está con la ip 192.168.1.33 al router 192.168.1.1

##¿Cómo puedo saber si un ordenador está bien conectado a la LAN?

Haz ping desde ese ordenador al router, por ejemplo si la puerta de enlace es 192.168.1.1 el comando es **ping 192.168.1.1**

![](/assets/2020-01-14 20_23_31-Window.png)

##¿Cómo puedo saber si dos dispositivos están conectados?

Esto es muy útil por ejemplo hacer una IP a la impresora para comprobar que la conexión es correcta y las configuraciones de IPs son correctas. Es simplemente hacer un ping a ese dispositivo, por ejemplo si la impresora la tengo en la 4.6.1.148 hago :

![](/assets/2020-01-14 20_33_36.jpg)






