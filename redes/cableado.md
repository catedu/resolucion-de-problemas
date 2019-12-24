#Cableado

##Cable de par entrelazado

Este cable está formado por 4 pares de hilos entrelazados, según su calidad (sobre todo por la cantidad de vueltas para evitar interferencias) se divide en diferentes categorías:

* **Cat 5** es muy vieja, hasta 100 Mbps.
* **Cat 5e** es la más común, soporta 1000 Mbps.
* **Cat 6** trabajan bien los 1000 Mbps.
* **Cat 6a** pueden aguantar 10000 Mbps = 10Gbps. 
* **Cat 7** son los que se utilizan 10 gigabit ethernet.
* **Cat 7A** igual pero con una frecuencia de 1000MHz
* ** Cat 8** compatible con frecuencias 2000 MHz y 40 Gbps.

>PROBLEMA : En mi centro Internet va lento y tengo un cableado Cat5 ¿tengo que hacer una inversión de cambiar todo el cableado?

La respuesta es que seguramente NO ES NECESARIO pues de nada sirve cambiar a una categoría superior si la conexión de Internet es lenta, los switch no soportan esas velocidades y lo más comúm: Las tarjetas de red no aguantan velocidades por encima de los 100Mps. Además van a salir nuevos protocolos que permitirán velocidades de Gbps con cableado Cat5.
Hemos visto centros educativos que han hecho un importante esfuerzo económico de cambiar todo el cableado y la velocidad seguía siendo pésima. Al final era porque tenían una [Botnet](/seguridad.md). 
Para estas cuestiones es mejor contar con el asesoramiento del servicio de informática del [Departamento](/problemas-que-hago.md).

No se tienen que hacer cableados muy largos pues la señal se atenúa, aún así el máximo es 100m.

##RJ45
Es la interfaz que conecta nuestro cableado.

![](/assets/2019-12-24 09_31_50-Window.png)
*Fuente [Wikipedia](https://es.wikipedia.org/wiki/RJ-45)*

**No podemos conectar** dos ordenadores con un cable normal o directo, sino es a través de un Switch o Hub, la razón es que los cables se tienen que *cruzar* es decir el cable de transmisión tiene que ir al de recepción del otro y viceversa. Esto lo hace el Switch o Hub. Hay cables especiales llamados *cruzados* que ya están conectados el RJ45 de forma cruzada y sólo sirven para este propósito.

Suele ser un elemento muy castigado si el PC donde está conectado no está fijo o está en una mesa con ruedas luego suele ser un punto crítico ante problemas de conexión:

>PROBLEMA: NO VA INTERNET en un equipo concreto conectado por cable.

Primero valoraremos si hay o no conexión entrando en Panel de control - Redes e Internet - Conexiones de red:

![](/assets/2019-12-22 08_50_50-Window.png)

Si encontramos que no hay conexión o no hay tráfico, el problema puede ser que el cable con RJ25 está estropeado. Una comprobación simple de cambiar el cable puede ahorrarnos tiempo.

Si quieres, son útiles los *comprobadores de cable* que por menos de 10€ se pueden comprar en proveedores online Aliexpress o Amazon.

![](/assets/2019-12-22 09_54_21-Window.png)

Metes los dos extremos y tienen que encenderse las luces en su mismo órden tanto en un extremo como en el otro 1-1 2-2 3-3 ... 8-8 si hay algún fallo ya podemos desechar ese cable.

>PREGUNTA: ¿Qué conexión es mejor la conexión por cable o la conexión por Wifi?

La conexión cableada **siempre** nos va a dar más velocidad, fiabilidad y conexión segura frente a la wifi. La wifi la tenemos que dejar cuando no hay otro remedio (aula con tablets, carro de portátiles, etc...)

##Fibra óptica
Es un cableado formado por filamentos transparentes donde viaja la luz por medio de rebotes entre las paredes, no hay casi pérdida





