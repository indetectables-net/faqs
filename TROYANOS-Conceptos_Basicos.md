**FAQ:**    **TROYANOS I: Conceptos básicos**
**Realizado gracias a la colaboración de todos los miembros de Indetectables.net**
Pendientes: TOR, SSH, HTTP Tunneling. Ilustraciones para explicar conexiones inversa/directa/web, enlaces importantes... y lo que se les ocurra

**CONCEPTOS BASICOS**

**Partes de un Troyano**
 El troyano consta de:
 Cliente: Es el programa que manda las ordenes a ejecutar
 Servidor: Es el programa que tiene el infectado, este deja un puerto a la escucha
 Editor: Este nos permite editar las caracteristicas de nuestro server; puerto, ip, inyeccion,etc.
 Otros: Estos pueden ser plugins tales como \*.dll para incorporarle algunas funciones al troyano.

**¿Que hace un Troyano o Caballo de Troya?**
 Las funciones que puede tener este son muy diversas, como ya he dicho anteriormente, todo depende del nivel de programacion del programador, las intenciones de este (troyano profesional o troyano de lammers...) y un poco menos influyente, el lenguage de programacion y componentes empleados.
 Los Troyanos pueden tener funciones como; Keylogger(programa/aplicacion que registra las teclas pulsadas),capturador de webcam(este capta imagenes de forma rapida, pareciendo asi como si de un video se tratase. Esto depende de nuestra velocidad de conexion a Internet), ftp de archivos(nos permiten ver los archivos que contienen los distintos discos duros, pudiendo bajar y subir archivos), opciones en pantalla(tales como cambio de Escritorio, cambio de protector la pantalla, esconder iconos, etc.), informacion del pc(Esto nos permite conocer las caracteristicas de un Pc;  tanto en el ambito de hardware &quot;perifericos&quot;, tambien su Sistema Operativo por ejemplo), Obtener shell(Esto nos permite obtener la shell del equipo remoto). Tambien podemos encontrar otro tipo de cosas como abrir/cerrar bandeja de cd, encender/apagar leds del teclado,etc,etc. Estos son ejemplos simples de lo que normalmente tiene un Troyano, las funciones de este refleja la imaginacion del programador.

**¿Cuantos tipos de Troyanos hay segun el modo de conexion?**
 Podemos clasificarlos en 3 tipos: Conexion Directa, Conexion Inversa y Conexio via web
**Regla prima:**  Si tienes algun problema de conexión, comienza ensayando tus herramientas en 127.0.0.1 (IP Local) como DNS, de esa forma descartaras posibles problemas de configuración en la creación de tu server, puertos abiertos y demas variables.

| **[+]** **Conexion Directa:
 Hablamos de conexion directa cuando nosotros (Cliente) nos conectamos al usuario infectado (Server). Es lo conexion mas habitual de los troyanos antiguos o backdoors, lo que hace es que el server deja escuchando un puerto y el cliente se conecta a través de ese puerto.**

**¿Como puedo saber el puerto del remoto? ¿Y la ip?**
 El puerto hoy en dia, en los nuevos Troyanos, es 100% editable. Gracias a esto podemos dejar nuestro Server mas seguro y sigiloso pues no habran conexiones salientes del remoto hacia nuestra maquina. Para saber la ip de nuestro infectado, existen muchisimos metodos de notificacion

 **¿Como funcionan?** Su funcionamiento es simple; nosotros al enviar el server dejamos un puerto abierto en la maquina infectada.
 Luego nosotros desde el cliente, debemos conectarnos a la ip del infectado por el puerto abierto por el server. |
 **![](RackMultipart20200708-4-1a3rmwv_html_d2a12252ed28e8ee.png)**  **fig. 1** |
 |
| --- | --- | --- |
| **Notificaciones**
 Esto es un metodo que suelen traer Troyanos para mandarnos la ip de la maquina en la cual ha sido ejecutado el server. ¿Y como nos llega?
 Nos puede llegar por diversas formas, aunque no suelen ser muy eficaces. Puede llegarnos por email; este metodo cada dia falla mas, ya que los servidores de correo lo toman como mensajes no deseados  &quot;spam&quot; y lo suelen autoeliminar. Esa es la forma mas conocida, aunque existen otras como por ejemplo por irc, el cual nos conectamos a un canal y nos da por ahi la ip. A veces tambien ftp,etc.

**Los inconvenientes de la Conexion Directa**
 Yo creo que ya nadie usa conexion directa, o solo muy pocos. Este tipo de conexion tiene muchas contras, como por ejemplo:
**1º** Tienes que saber la direccion ip de tu infectado. Si los notificadores te fallan, tienes que averiguartela de otro modo.
**2º** No puede transpasar routers, por lo tanto tampoco a una Lan (cibers). | **3º** Puedes tener problemas al saltar el firewall (cortafuegos) del infectado. (ver **fig. 2** ) ![](RackMultipart20200708-4-1a3rmwv_html_5655c0472f6b1423.png) **fig. 2**

 **4º** Si la IP del server es dinamica y los metodos de notificación fallan, se habra perdido una conexión. |
 |
| **[+]** **Conexion Inversa**
 Esta vez es al reves, el infectado (Server) se conecta al nosotros (Cliente) Los troyanos de conexión inversa son los que hacen que el servidor sea el que se conecte al cliente; las ventajas de éste son que traspasan muchos firewalls y pueden ser usados en redes situadas detrás de un router sin problemas.

 El motivo de por qué éste obtiene esas ventajas es que muchos firewalls no analizan los paquetes que salen de la computadora infectada (pero sí analizan los que entran) y se dice que traspasan redes porque no es necesario que se dirija la conexión hacia una computadora que se encuentre en la red. (ver fig. 3)**
 | ![](RackMultipart20200708-4-1a3rmwv_html_bb7a9790850d3697.png)
**fig. 3** |

**[+]**  **Conexion via web**
**Este tipo de troyanos no utiliza un cliente para recibir la conexión, sino que emplea un sitio web para recibir conexiones y enviar ordenes a las maquinas. Tenemos entonces como intermediario entre los remotos y el administrador de la red una interfaz web que facilita el manejo de las maquinas. Como ejemplo de este tipo de troyanos tenemos el Apofis. Son muy similares a los ircbots, solo que en vez de tener un canal IRC se tiene una web como plataforma.
 Conexion Servidor ------\&gt; Interfaz WEB \&lt;------- Administrador Red**

**Los mejores troyanos
 No hay mejor troyano, solo que les hay mas completos y menos, pero lo mas importante es k se adapten a las necesidades de uno. Las funciones mas comunes son keylogger, screenshot, cam recorder, filemanager ...
 Los más usados y &quot;mejores&quot; para mí de conexión inversa son el **_** PoisonIvy 2 **_** , el  **_** Bifrost **_** y el **_** Bandook1.3 **_**  **

**TIPOS DE IP Y CONEXION INVERSA**

**Es habitual que un usuario que se conecta desde su hogar a Internet utilice una dirección IP que puede cambiar al reconectar; a esta forma de asignación de dirección IP se la denomina IP dinámica. Los sitios de Internet, servidores de correo, FTP, etc. que por su naturaleza necesitan estar permanentemente conectados generalmente tienen una dirección IP fija; a esta forma de asignación de dirección IP se la denomina IP estática.**

**Si configuramos un server para que se conecte a una determinada IP, y esa no es estatica sino dinamica, la conexion se perdera cuando esta cambie.**

**Una solucion para esta situacion es el uso de DNS, una DNS es una direccion virtual que nos sirve para redirigir el trafico que conecte a ella a cualquier IP que deseemos, dandonos asi la posibilidad de usar una DNS para cubrir los cambios de una IP Dinamica.**

**IP Dinamica \&lt;------\&gt; DNS \&lt;----- Server**

**IP Estatica \&lt;--------- Server**

**PREGUNTAS FRECUENTES SOBRE TROYANOS**

**¿Es cierto que si en el equipo remoto existen dos servers del mismo troyano nunca conectara? ¿Por que?**

**Depende de como esté programado.
 En muchos troyanos verás la opción de establecer un Mutex, esto lo que hace es que solo haya un server ejecutándose en la maquina, no abriéndose los otros al detectar el Mutex. En otros troyanos que usan inyección y cosas raras es posible que una segunda ejecución de un server haga que el equipo explote.
 ¿Si uno mismo esta infectado, bien sea haciendo pruebas o por alguien &quot;externo&quot;, no nos funcionaran los troyanos? ¿Por que?
 No por estar infectado te deja de funcionar los clientes de otros troyanos... Como todo en la vida podría suceder pero no es normal que suceda algo asi. Pueden ocurrir excepciones como que el mutex o puerto coincidan y no se logre una conexion.
 ¿Por que al autoinfectarnos ciertos servers solo conectan cuando activamos la casilla del &quot;override&quot; en el DUC? ¿Para que &quot;demonios&quot; sirve esta casilla?**

**El override sirve para actualizar los datos de tu cuenta NO-IP automaticamente, pero esto no quiere decir que sea una ley para que una prueba local funcione. Si se quiere hacer una prueba en local sin inconvenientes usa como DNS tu IP interna (127.0.0.1) y no habra ningun problema de ese tipo. También nos ofrece unas pocas opciones. Override automatic connection detection nos permite seleccionar que adaptador de red es del cual tomara la conexión y la IP, Overrride automatic IP detection nos permite especificar la IP (dentro de las disponibles en nuestro sistema) que usará para la actualización, y el último de abajo nos permite especificar el tiempo mínimo de comprobación de IP. Por defecto está en media hora, y en principio no es aconsejable modificarlo, ya que poner menos tiempo puede saturar nuestro sistema con peticiones inútiles, y ponerlo en más tiempo puede suponer que un número importante de peticiones a alguno de nuestros servicios se quede sin respuesta
 ¿Se pueden tener instalados en el equipo remoto tantos servers de rats diferentes como se quieran, siempre y cuando conecten por puertos diferentes y esten correctamente abiertos?
 En principio si, aunque puede dar problemas si por ejemplo 2 se inyectan en el internet explorer y uno cierra el internet explorer apra inyectarse o cosas así... Igual con los mutex, si coinciden no podras recibir la conexion de los repetidos, o si el puerto esta en uso por otra aplicacion o restringido tampoco podras.
 ¿Si un server conecta en mi equipo, es 100% viable que conecte en un equipo remoto sin antivirus?
 El que funcione en tu equipo no asegura que valla a funcionar en un equipo remoto, aparte del antivirus está el cortafuegos, tu router o el suyo...
 ¿Por que algunas veces al autoinfectarme, la conexion muestra mi IP privada y otras la de 127.0.0.1? ¿que diferencia hay entre ambas y que relacion tienen con la configuracion del rat o del DUC?
 Depende de lo que pongas en el campo IP/DNS al crear el troyano. Si pones 127.0.0.1 o localhost no te extrañe que salga eso al conectarse al cliente.  Si pones un dns, por ejemplo de no-ip, agustino.no-ip.com pues ya depende de a que ip resuelva este dominio. Lo puedes saber haciendo:
 ping agustino.no-ip.com**

**¿Tengo router y no puedo conectarme?
 bueno si tienes router y quieres usar conexion inversa lo que tienes que hacer es cojer y abrir el puerto que use el troyano en cuestión y luego crearse un no-ip.**

**Problemas con troyanos
 A la hora de usar un troyano de conexión inversa se nos dan muchas ventajas pero también tiene algún inconveniente.
 Si tienes una IP dinámica (que cambia) necesitas crearte un DNS con no-ip por ejemplo para k tu ip siempre este actualizada.
 Si el Server no se conecta a ti puede ser pro varias cosas, la mas común es k no tengas abiertos los puestos de tu router, tendrás k abrirlos, también puede ser k la victima tenga un firewall y no deje conectarse a Internet o simplemente k tu troyano sea detectado y su antivirus lo borre.**

**¿Como puedo saber si anda bien el server?**

**La forma más segura para hacerlo es en un entorno virtual (VMWARE, VIRTUALPC) o en un entorno controlado o freezeado (DEEP FREEZE, SANDBOX), conectando a 127.0.0.1 como DNS y asegurandose que toda la configuración este correcta, tanto interna del server, como del cliente y sus necesidades para recibir la conexion (puertos, firewall, etc). Si todo esta aparentemente bien configurado, puedes pensar en que una de estas cosas este fallando:**

- **Algun dato mal tipeado (Chequea que el DNS es realmente .org, y no .biz).**
- **No tenes abierto el DUC (Parece medio obvio pero hay que resaltarlo, fijate que el DUC de no-ip tenga cargado el host correctamente, al tildarlo aparece una carita sonriente).**
- **Usas antivirus, cual?. Hay antivirus que aunque los cierres el kernell te puede estar jodiendo.**
- **Usas router y tenes el puerto que usa cerrado.**

**Ensayando troyanos en VMWARE**

Primero debes de configurar la salidad de red de tu maquina virtual, Revisa las interfaces de red que crea la VM y como dijo alguien deberias tener el Duc corriendo en la VM.. Te digo que revises las interfaces de red porque a mi al menos..(normalmente suelo usar el modo bridge en vmware) si hago un netstat me salen varias ip´s,por ejemplo:

**Proto Dirección local Dirección remota Estado**
 TCP 0.0.0.0:135 0.0.0.0:0 LISTENING
 TCP 0.0.0.0:445 0.0.0.0:0 LISTENING
 TCP 0.0.0.0:6346 0.0.0.0:0 LISTENING
 TCP 10.0.2.15:139 0.0.0.0:0 LISTENING
 TCP 127.0.0.1:1028 0.0.0.0:0 LISTENING
 TCP 127.0.0.1:30606 0.0.0.0:0 LISTENING

 **Ahi se ve la loopback ip que es 127.0.0.1 se suele usar para hacer pruebas localmente y la ip 10.0.2.15...esto es en VirtualBox... En VMWare en vez de 10.0.2.15 suelen ser del tipo 168.x.x.x debe haber algun conflicto en las ip´s pues en tu server pones tu no-ip para que conecte al router (en caso de usar) y este debe redireccionar a la ip en la cual tienes el cliente escuchando...mira a ver como lo tienes...
 Si usas router y tienes el dhcp activado cada vez que reinicies el pc le asignará una ip diferente y si tu duc lo tienes corriendo en la VM en el router igual tu ip ha cambiado dentro de la lan y no conecta por eso..**

**Comprobar si un troyano es detectado**

**Para comprobar si un troyano es detectado lo mas fácil es usar nuestro antivirus, pero cada antivirus es distinto por lo tanto si la victima tiene un antivirus distinto alo mejor se lo detecta. Hay varios escaners de varios antivirus a la vez:
 Online : Son antivirus en paginas Web como VirusTotal, no enviéis nunca vuestros troyanos a analizar ya k mandan muestras a las compañías antivirus y si no es detectado lo será en pocos días
 Offline: Hay herramientas llamadas Multi AV (Varios AV a la vez) como la de Thor (KISM) k hace lo mismo solo k no manda muestras a ningún antivirus.**

**Pasos comunes para todos los troyanos
 1: **_** primero se crea el server**_
**Eso es correcto  ..lo tenes que crear con las opciones correctas, pero segùn lei en otros post tuyos, ya lo hiciste asi que ..bien
 2: **_** se usa un crypter de los muchos que los users publican aqui y se crypta el programa**_
**Esto tambièn es correcto, el crypter lo que hace, es en forma automatica hacer indetectable a determinados AV, el server, modificando ciertas partes del mismo...sobre el funcionamiento hay bastante info..
 3: **_** la parte del stub no la entiendo &#39;tengo que crear mi propio stub o agarro el que sea de los muchos que hay aqui? o que vienen con los cripters ?**_
 **El stub viene a ser el corazòn del crypter..de echo lo que generalmente detectan los AV, es el stub, con modificarlo, se logra su indetectabilidad temporal.. Pero el tema no es sencillo, lo mejor seria que domines el uso de los crypter , para mas adelante adentrarte en la modificacion de ellos
 4: **_** despues uso un binder para juntarlo con una foto**_
 **Exacto, aca unis el server con una foto, o un programa cualquiera..las razones son obvias
 5: **_** le hago un scaneo para los virus**_
 **mmmm?? se supone que si vas a hacer todo lo de arriba...el server tiene que ser indetectable..por lo menos para el Av del amigo que lo va a recibir..
 6: **_** finalmente lo pruebo en mi pc y si me conecta listo lo puedo mandar y seguro tengo varias
 conecciones &quot;bueno seguro nada&quot; pero si intentara  **_** y...eso seria lo mas prudencial..**

**SOBRE VOLVER INDETECTABLE UN TROYANO**
**Por desgracia las compañías antivirus no son tontas y actualizan sus bases de datos a diario con los nuevos virus y troyanos k aparecen, por eso no nos servirá de nada usar un troyano si es detectado porque si la victima tiene un antivirus será eliminado.
 Para hacerlo indetectable hay varias maneras:**

- **Cambiar offsets detectados con editor hex.**
- **Cambiar el código fuente detectado en ASM**
- **Usar encriptadores y compresores (no es lo mismo)**
- **Empleando metodos como XOR, RIT, MEEPA**

**¿Para que sirve la inyeccion en un proceso?
 la inyeccion del server en un proceso sirve para que evitar que el firewall filtre (prohiba) las conexiones salientes. Como el explorer.exe y el msnmsgr.exe son programas &#39;confiables&#39; que utilizan conexiones saliente a menudo, los firewalls los dejan actuar por defecto. Pero no tiene que ver con el **_** timing **_** de la conexion o su indetectabilidad, es más, podria ser detectada por la defensa proactiva de algun antivirus si no se le usa adecuadamente. Los procesos más usuales para ser inyectados son iexplore.exe (navegador) y svhost.exe. Cada que el proceso inyectado se inicie, tambien se iniciara el malware inyectado, pero de igual forma si el proceso es finalizado o tiene un error, el malware tambien finalizara. En la inyeccion a otros procesos, el server se ejecuta UNA VEZ al inicio del sistema operativo, busca el proceso victima y se inyecta ahi. A partir de ese momento, las secciones del proceso victima estan compartidas con las del server. Cuantas instancias tenemos del server? una. Si cierro el proceso victima, procedimiento en el que el nucleo de windows cierra los threads, mata el proceso y LIBERA LA IMAGEN DEL PROCESO EN MEMORIA (compuesta por las secciones compartidas con el server) ¿se cierra el server? claro. Y cuantas instancias teniamos? Una. Entonces? chau server.
 Cambiar offsets detectados con editor hex.
 Es una de las técnicas mas antiguas de todas consistes en ir buscando los offsets detectados y cuando encontramos el que caza el antivirus cambiamos su numero por un numero mas alto y generalmente conseguimos hacerlo indetectable, pero muchas veces se jode la aplicación.
 Cambiar el código fuente detectado en ASM
 A mi es la técnica k mas me gusta, es como la anterior solo k en vez de sumar un numero abres el programa con un debuger como ollydbg y te diriges al offset detectado y cambias el código fuente en ASM, así consigues k sea indetectable y no estropeas el ejecutable.
 Si abres un programa con un editor hexadecimal solo ves numeritos, pero si usas un debuger esos números se traducen a código en ASM.
 Y por ejemplo si el offset detectado es &quot;74&quot; (&quot;je&quot; en ASM, significa si es igual salta) y si cambias el 74 por &quot;75&quot; (&quot;jne&quot; en ASM, significa salta si no es igual) Por lo tanto lo k tas haciendo es invertir un salto, aparentemente se queda indetectable ya k es lo contrario, pero si por ejemplo tienes este código tan simple: **** Si cam ESTA apagada entonces enciéndela**
 **Si cambias ese 74 por 75 quedaría así:**  **Si cam NO ESTA apagada entonces enciéndela**
 **Por eso al cambiar usando el editor hex algunas funciones quedan inutilizadas o incluso te puedes cargar el programa.
 Si lo modificas el código fuente en ASM como por ejemplo poniendo un salto a la función o algo k haga lo mismo de manera diferente pues te queda indetectable y funcional. **** EXTENSIONES DE UN TROYANO**
 **Los troyanos siempre tiene tener la extensión &quot;exe&quot; para que sean ejecutados como una aplicación.
 Hablando claro, no se puede mandar un troyano como si fuera una foto (con extensión jpg) , la explicación es muy sencilla. Windows ejecuta cada extensión con un programa predeterminado, y si tiene extensión jpg lo abrirá con el visor de imágenes, por lo tanto el troyano no se ejecuta.
 También es sabido que hay varios trucos para engañar a la victima asíéndola creer que es una foto...
 Por ejemplo:
 Doble extensión
 Consiste simplemente en renombrar un archivo de troyano.exe a troyano.jpg.exe
 Así Windows ocultara la extensión exe y el usuario vera k tiene extensión de foto.
 Cambiar el icono
 Con herramientas como el ResHacker puedes cambiar los iconos de una aplicación y poner por ejemplo el icono k usa Windows para las fotos y así lo abrirá creyendo k es una foto...
 Contaminar el registro
 En el registro esta guardado con que programa se abre cada extensión.
 Pues el truco esta en cambiar el programa k abre los archivos jpg por ejemplo para k los abra como programas y después de haber hecho ese cambio cualquier archivo jpg que le mandemos lo abrirá como una aplicación.
 Ejemplo:**[**http://cyruxnet.org/extensiones.htm**](http://cyruxnet.org/extensiones.htm)
 **Extensiones engañosas
 Se pueden usar extensiones poco comunes como .scr (screensaver), o si se quiere hospedar un troyano en una web se podria usar la extension .com (ejemplo.**[**http://sitioweb.com/server.com**](http://sitioweb.com/server.com)**)**

**ENVIO DE TROYANOS**
**Lo mas frecuente para enviar un troyano suele ser enviarlo por email o por mensajería instantánea, pero estos bloquean los ejecutables y avisan de que son archivos peligrosos para el equipo. Para evitar eso se pueden hacer 2 cosas:**

- **Comprimir archivos: Si el archivo exe lo comprimes en zip por ejemplo te dejaran enviarlo por todos los lados y la victima lo podrá abrir ya que viene por defecto con Windows.**
- **Tres puntitos: En Hotmail si después de el exe pones 3 puntitos no te dice nada de el archivo y te lo ejecuta normal.
 Por ejemplo &quot;troy.exe&quot; =\&gt; &quot;troy.exe...&quot; **
- **Hospedar .exe: Se puede recurrir a un freehost, o montar un host en local para dicho fin. Cambiar el .exe por .com ayudaria en esto
 Por ejemplo. &quot;troy.exe&quot; =\&gt; &quot;**[**youtube.com**](http://www.youtube.com/)**&quot;**

**DNS GRATUITAS PARA CONEXION INVERSA**

Existen muchos sitios que nos permiten crear una direccion DNS para redirigir el trafico a nuestra IP, los mas usados son NO-IP y dyndns, pero ademas de esos existen muchos otros más:

| [**http://www.ddns.nu/register.php**](http://www.ddns.nu/register.php)
[**https://members.dhs.org/signup**](https://members.dhs.org/signup)
[**http://www.dnip.net/register.cgi**](http://www.dnip.net/register.cgi)
[**http://domain-dns.com/**](http://domain-dns.com/)
[**https://www.dtdns.com/**](https://www.dtdns.com/)
[**http://dns.blueline.be/**](http://dns.blueline.be/)
[**http://dyndns.dk/ny.php**](http://dyndns.dk/ny.php)
[**http://www.dyndsl.com/**](http://www.dyndsl.com/)
[**http://dynserv.com/**](http://dynserv.com/)
[**http://www.dynu.com/basic.asp?type=signup**](http://www.dynu.com/basic.asp?type=signup)
[**http://www.dynup.net/signup/signup.php3**](http://www.dynup.net/signup/signup.php3)
[**http://www.eurodns.com/register.php**](http://www.eurodns.com/register.php)
[**http://www.everydns.net**](http://www.everydns.net/)
[**http://fdns.net/**](http://fdns.net/)
[**http://freedns.afraid.org/signup**](http://freedns.afraid.org/signup)
[**http://hn.org/signup/vanity.shtml**](http://hn.org/signup/vanity.shtml)
[**http://www.ipupdater.com/signup.php**](http://www.ipupdater.com/signup.php)
[**http://www.mtgsy.net/new\_user.php?action=add**](http://www.mtgsy.net/new_user.php?action=add)
[**http://www.minidns.net**](http://www.minidns.net/)
[**http://www.dyn.ee**](http://www.dyn.ee/) | [**http://www.mydynip.org/metadot/**](http://www.mydynip.org/metadot/)
[**http://myip.org/signup/index.htm?loc=signupPickDomain**](http://myip.org/signup/index.htm?loc=signupPickDomain)
[**https://ssl.myserver.org/registerbeta/Free.asp**](https://ssl.myserver.org/registerbeta/Free.asp)
[**http://www.nerdie.net/index.php?site=register**](http://www.nerdie.net/index.php?site=register)
[**http://www.opendns.be/Content/newuser.asp**](http://www.opendns.be/Content/newuser.asp)
[**http://www.prout.be/dns/?p=user\_new**](http://www.prout.be/dns/?p=user_new)
[**http://www.selfhost.com/register.asp**](http://www.selfhost.com/register.asp)
[**http://www.sitelutions.com/signup**](http://www.sitelutions.com/signup)
[**http://www.yi.org/new.pl**](http://www.yi.org/new.pl)
[**http://www.dyns.cx/signup**](http://www.dyns.cx/signup)
[**https://www.2mydns.com/signup.asp**](https://www.2mydns.com/signup.asp)
[**http://www.dhis.org/register.html**](http://www.dhis.org/register.html)
[**http://www.ddo.jp**](http://www.ddo.jp/)
[**http://www.editdns.com**](http://www.editdns.com/)
[**https://www.xname.org**](https://www.xname.org/)
[**http://www.dynddns.us**](http://www.dynddns.us/)
[**http://www.serverthuis.nl**](http://www.serverthuis.nl/)
[**http://www.dnsexit.com**](http://www.dnsexit.com/)
[**http://www.zonedit.co**](http://www.zonedit.com/) |
| --- | --- |