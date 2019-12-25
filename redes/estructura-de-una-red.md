#Estructura de una red

La red local de tu centro (**LAN** Local Area Network) seguramente tiene esta estructura en estrella o árbol:

![](/assets/2019-12-21 09_16_52-Window.png)
*Fuente elaboración propia con imágenes CC de Wikipedia*

* Los portátiles tienen una conexión inalámbrica con un **Punto de acceso AP Access Point** actualmente de la marca *Ubiquiti*.
* Los PCs y los AP están conectados a un **switch** por medio de cableado:
 * Los **switch** o conmutadores (en azul) es un dispositivo hardware que permite la transmisión de información entre varios equipos. Antiguamente se utilizaban concentradores **Hub** o concentradores que transmitían la información a todos indistintamente, los switch almacena la dirección MAC de cada dispositivo conectado de manera que envía el paquete de información al equipo al que va dirigido.
 * Es importante tener unos buenos switch que permita velocidades de Gps y no sean un cuello de botella en la red del centro.
 * Las conexiones se realizan por medio de un cableado que dentro son 4 pares de hilos trenzados y en sus extremos conectores RJ25 que lo veremos [más adelante](/redes/cableado.md).
* En **router** (en la figura en negro) une nuestra red LAN con Internet, lo veremos [más adelante](/redes/router.md)
* Seguramente no sólo existe un switch en tu centro sino varios que en forma de pirámide o cascada van conectando todos los equipos de tu LAN. Cada Switch agrupa a varios equipos de un edificio o de una planta, por lo tanto los switch no separan redes, sino se distribuyen según el espacio físico. En la figura siguiente puedes ver que hay tres switch para tres plantas pero no tiene nada que ver con las tres redes que se han definido en esta estructura : contabilidad, mercadeo e ingeniería. Técnicamente tres redes virtuales **VLAN**.

 Ya de paso puedes ver los símbolos comunes del Router (círculo con cuatro flechas que apuntan al centro) y el de Switch (cuadrado con cuatro flechas paralelas).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/VLAN.svg/615px-VLAN.svg.png)
*Fuente [Wikipedia](https://es.m.wikipedia.org/wiki/Archivo:VLAN.svg)*


 
