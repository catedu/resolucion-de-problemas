# A EXPERIMENTAR

## Entrar en la ventana de comandos

Entra en la ventana de comandos buscando **cmd** en Windows. En Linux tiene su propia ventana de comandos (busca **terminal** o pulsa Ctrl+Alt+t)

>**tip**
>Nota: si tu versión de Windows es XP entra en Inicio-Ejecutar (o las teclas Windows+R) y teclea cmd para entrar en la ventana de comandos:

>![Captura de pantalla](/assets/2020-01-14 20_48_06.jpg)

## ¿Cómo puedo saber la IP de una página WEB?

Muy fácil, con el comando **ping** a esa página. Por ejemplo para la página www.google.es teclea **ping google.es** y vemos este resultado:

![Captura de pantalla](/assets/2020-01-14 11_04_22.jpg)

Sale [172.217.17.3](http://172.217.17.3) (a ti te puede salir otra IP pues tiene varios IPs contratados y varios servidores replicados) si lo pones en el navegador ¡¡te sale la página de Google!! No siempre funciona para todas las páginas web, en Google si, pero en otras páginas, los servidores y navegadores no aceptan que entres de forma directa.

Otra manera rápida de averiguarlo es con el comando nslookup que ya vimos en [DNS](/dns.md).

## ¿Cuantos switchs y servidores hay entre mi ordenador y una página Web?

Pues ya que sabes entrar a la ventana de comandos, teclea **tracert y la página que quieras** por ejemplo tracert google.es y te sorprenderás. La primera IP que verás es la de tu router (ver [IP puerta de enlace](/protocolos.md))

Éste es el resultado desde el ordenador del centro donde estoy escribiendo (para que veas que no siempre las IPs reservadas de un centro son 192.168.x.x, en este caso es 4.6.1.x)

![Captura de pantalla](/assets/2020-01-14 20_16_38.jpg)

o sea

![Imágenes libres y elaboración propia](/assets/2020-01-14 20_17_09.jpg)

Nos da una idea de la calidad de nuestra conexión a esa web.

## ¿Qué dirección IP tengo rápidamente?

En Windows teclea en comandos **ipconfig** o si quieres saber también las dns **ipconfig/all**. En Linux teclea **ifconfig**.

Por ejemplo se puede ver que mi IP es 4.6.1.30, que la puerta de enlace es 4.6.1.251 que la máscara de red es de tipo C y que mis DNS son las del Gobierno de Aragón:

![](/assets/2020-01-14 20_25_04.jpg)

>**info**
>Verás unos números largos que en la figura los he ocultado por seguridad, son **las direcciones físicas MAC** de la tarjeta de red y del router. Son direcciones físicas que vienen de fábrica y son únicas y no se pueden cambiar. Ahora puedes entender ciertos chistes informáticos 🤣.

>![](/assets/meme-ip.jpg)

Si por ejemplo el ordenador está conectado a Internet desde dos sitios, sale toda la información:

![](/assets/2020-01-14 20_28_56-Window.png)

En este caso puedes ver que la tarjeta de red está conectado con la IP 4.6.1.33 al router 4.6.1.251 y la tarjeta inalámbrica Wifi está con la ip 192.168.1.33 al router 192.168.1.1

## ¿Cómo puedo saber si un ordenador está bien conectado a la LAN?

Haz ping desde ese ordenador al router, por ejemplo si la puerta de enlace es 192.168.1.1 el comando es **ping 192.168.1.1**.

![](/assets/2020-01-14 20_23_31-Window.png)

## ¿Cómo puedo saber si mi ordenador está bien conectado a Internet?

Haz ping a google por ejemplo **ping 8.8.8.8**.

![](/assets/2020-01-14 20_35_14.jpg)

## Estoy bien conectado a Internet (tengo ping 8.8.8.8) pero no me resuelve los nombres (o sea hago ping google.es y no contesta), ¿cómo es posible?

Muy fácil, si con IPs navegas pero con URLs no, es que **tienes mal las DNS** haz ipconfig/all y comprueba que tienes las DNS del Gobierno de Aragón 188.244.82.1 y 188.244.82.17, teclea nslookup a ver si te salen bien las DNS.

Luego comprueba que las DNS del Gobierno de Aragón funcionan (puede ser que hayan caído), luego haz ping a esas direcciones, en la imagen puedes ver que funcionan :

![](/assets/pingdnsaragon.png)

## Tengo ping google.es pero no navego
En ese caso tu ordenador está bien conectado y bien configurado pero algo en el software impide la navegación ¿virus? ¿lo formateo? ¡¡¡ espera  !!! consulta [el protocolo](/problemas-que-hago.md).

## ¿Cómo puedo saber si dos dispositivos están conectados?

Esto es muy útil por ejemplo hacer una IP a la impresora para comprobar que la conexión es correcta y las configuraciones de IPs son correctas. Es simplemente hacer un ping a ese dispositivo, por ejemplo si la impresora la tengo en la 4.6.1.148 hago :

![](/assets/2020-01-14 20_33_36.jpg)

##¿Cómo sé si alguien está "pirateando" la wifi?

Hay programas como [Wireless Network Watcher](https://www.nirsoft.net/utils/wireless_network_watcher.html) (es portable) que te enseña qué equipos tienes en tu red, y como seguramente nos has hecho caso en [Retistra tus IPs](/redes/ips.md) entonces puedes detectar al intruso, y es totalmente denunciable.

![](https://www.nirsoft.net/utils/wnetwatcher.gif)

![](/assets/2020-03-24 10_44_58.jpg)

*fuente: elaboración propia*
