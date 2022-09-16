# Conceptos Fundamentales

> Estos son los conceptos y términos fundamentales que se suelen utilizar.
> Arrancamos con cuestiones elementales y vamos avanzando, así que si le parecen muy fáciles las primeras preguntas por favor siga leyendo para asegurarse de que entiende también las que le siguen.

## Temario

1. [Redes](#redes)
1. [Malware](#malware)
1. [Antivirus y Firewalls](#antivirus-y-firewalls)
1. [Glosario](#glosario)



## Redes

#### ¿Qué es una Dirección IP?
Es un número que identifica a un dispositivo (habitualmente una computadora) dentro de una red que utilice el protocolo IP (protocolo usado en Internet), de modo que las direcciones IP son para los dispositivos lo que la dirección postal es para una casa. Actualmente las direcciones IP están formadas por 4 números separados por un punto y que pueden ir del 0 al 255 (Ej. 164.12.123.65).

#### ¿Que son las IP Estáticas e IP Dinámicas?
Es habitual que un usuario que se conecta desde su hogar a Internet utilice una dirección IP que puede cambiar al reconectar; a esta forma de asignación de dirección IP se la denomina IP dinámica.
Los sitios de Internet, servidores de correo, FTP, etc. que por su naturaleza necesitan estar permanentemente conectados generalmente tienen una dirección IP fija; a esta forma de asignación de dirección IP se la denomina IP estática.

#### ¿Qué es una LAN (red privada local)?
Local Area Network. Red de área local. Red de computadoras ubicadas dentro de un espacio limitado y que tiene un enlace encargado de distribuir las comunicaciones. Por ejemplo, computadoras conectadas en una oficina, en un edificio o en hogares.

#### ¿Qué son las IP Públicas e IP Privadas?
Dentro del rango de números IP se ha convenido reservar algunos para ser utilizados dentro de redes LAN, a estas IPs se las llama IP Privadas. Las IP privadas no son &quot;alcanzables&quot; desde Internet sino solo dentro de la propia LAN, pudiendo repetirse los números IP en distintas redes LAN. La IP pública es una IP de Internet y solo puede asignársela a un dispositivo por vez, ya que Internet hay una sola. Usualmente las redes LAN tienen un router que les da salida a Internet al resto de las computadoras y que cuenta con una IP pública mientras que los demás dispositivos dentro de la red tienen IP privadas.

#### ¿Qué es un Puerto?
Es un número que va del 1 al 65536 y que designa un canal para el envío/recepción de datos desde una computadora u otro dispositivo conectado a Internet.
Si la IP es para la computadora lo que la dirección postal es para la &quot;casa&quot;, el puerto sería la &quot;puerta&quot; de la casa y la casa tendría 65536 puertas. En la práctica lo que hacemos es asignarle un puerto distinto a cada programa (Ej. troyano) que tenemos en la computadora.

#### ¿Qué es un Nombre de Dominio?
Es un nombre que permite identificar a un dispositivo (generalmente una computadora) en Internet y que se asocia a un número IP siendo más fácil de recordar. Los Nombres de Dominios van separados por un punto y jerárquicamente están organizados de derecha a izquierda. (Ej. google.com, no-ip.com).
Un Subdominio es un dominio que está dentro de otro dominio principal (Ej. atacante.no-ip.com).

#### ¿Qué es un DNS?
El Domain Name System (DNS) es una base de datos distribuida y jerárquica que almacena la asignación de Nombres de Dominio a direcciones IP. Cuando ponemos un nombre de dominio en nuestro navegador este consulta a un servidor DNS para que le diga la IP y poder mostrarnos la página.

#### ¿Qué es un DNS Dinámico?
Es un sistema que permite la actualización en tiempo real de la IP asignada a un nombre de dominio. El uso más común que se le da es permitir la asignación de un nombre de dominio de Internet a un ordenador con dirección IP variable (dinámica). Esto permite conectarse con la máquina en cuestión sin necesidad de tener que rastrear las direcciones IP. Hay varios proveedores gratuitos de este servicio, entre ellos no-ip.com, dyndns.com y freedns.afraid.org.

#### ¿Para que sirve la IP 127.0.0.1 y el dominio localhost?
127.0.0.1 es la IP de loopback, IP con la que todas las computadoras y routers usan para referirse a sí mismo. El nombre localhost es traducido como la dirección IP 127.0.0.1. En la práctica se puede utilizar para probar el cliente y el servidor de un troyano en la misma máquina.

#### Smtp
El Protocolo Simple de Transferencia de Correo (o Simple Mail Transfer Protocol del inglés) es un protocolo de red utilizado para el intercambio de mensajes de correo electrónico.  
Este protocolo, aunque es el más comúnmente utilizado, posee algunas limitaciones en cuanto a la recepción de mensajes en el servidor de destino (cola de mensajes recibidos). 
Como alternativa a esta limitación crearon los protocolos POP o IMAP, otorgando a SMTP la tarea específica de enviar correo, y recibirlos empleando los otros protocolos antes mencionados (POP O IMAP

## Malware

Es un tipo de software que tiene como objetivo dañar o infiltrarse sin el consentimiento de su propietario en un sistema de información. Palabra que nace de la unión de los términos en inglés de software malintencionado: malicious software. 
Dentro de esta definición tiene cabida un amplio elenco de programas maliciosos: virus, gusanos, troyanos, backdoors, spyware, etc. La nota común a todos estos programas es su carácter dañino o lesivo.

#### Virus

Programa diseñado para que al ejecutarse, se copie a sí mismo adjuntándose en aplicaciones existentes en el equipo. De esta manera, cuando se ejecuta una aplicación infectada, puede infectar otros archivos.
A diferencia de otro tipo de malware, como los gusanos, se necesita acción humana para que un virus se propague entre máquinas y sistemas.
Los efectos que pueden provocar varían dependiendo de cada tipo de virus: mostrar un mensaje, sobrescribir archivos, borrar archivos, enviar información confidencial mediante correos electrónicos a terceros, etc. Los más comunes son los que infectan a ficheros ejecutables.

#### ¿Cuál es la diferencia troyano con un RAT?
Un RAT (Remote Administration Tool) realiza las mismas funciones que un troyano con la diferencia de que el RAT no está oculto en la computadora controlada. La diferencia es sutil pudiéndose transformar fácilmente un RAT en un troyano. Además algunos programadores prefieren llamar RATs a sus creaciones para evitar problemas legales y para persuadir a las compañías antivirus de que sus programas no son maliciosos y por lo tanto no deben ser detectados.

#### ¿Qué significa Troyanos de conexión Directa e Inversa?
Los troyanos de conexión directa son aquellos que hacen que el cliente se conecte al servidor; a diferencia de éstos, los troyanos de conexión inversa son los que hacen que el servidor sea el que se conecte al cliente; las ventajas de éste son que traspasan muchos firewalls y pueden ser usados en redes situadas detrás de un router sin problemas.

El motivo de por qué éste obtiene esas ventajas es que muchos firewalls no analizan los paquetes que salen de la computadora infectada (pero sí analizan los que entran) y se dice que traspasan redes porque no es necesario que se dirija la conexión hacia una computadora que se encuentre en la red.

#### ¿Qué significa Troyanos con Inyección o sin Inyección?
Sin inyección: Se ejecutan como un programa común y corriente, siendo visibles como un proceso más.
Con inyección: Se infiltran en otro proceso para intentar camuflarse de los firewall por software.

#### Puerta trasera
Se denomina backdoor o puerta trasera a cualquier punto débil de un programa o sistema mediante el cual una persona no autorizada puede acceder a un sistema.  Las puertas traseras pueden ser errores o fallos, o pueden haber sido creadas a propósito, por los propios autores pero al ser descubiertas por terceros, pueden ser utilizadas con fines ilícitos.
Por otro lado, también se consideran puertas traseras a los programas que, una vez instalados en el ordenador de la víctima, dan el control de éste de forma remota al ordenador del atacante.
Por lo tanto aunque no son específicamente virus, pueden llegar a ser un tipo de malware que funcionan como herramientas de control remoto. Cuentan con una codificación propia y usan cualquier servicio de Internet: correo, mensajería instantánea, http, ftp, telnet o chat. Chat.

#### Gusano

Es un programa malicioso (o malware) que tiene como característica principal su alto grado
de «dispersabilidad», es decir, lo rápidamente que se propaga.
Mientras que los troyanos dependen de que un usuario acceda a una web maliciosa o ejecu-
te un fichero infectado, los gusanos realizan copias de sí mismos, infectan a otros ordenado-
res y se propagan automáticamente en una red independientemente de la acción humana.
Su fin es replicarse a nuevos sistemas para infectarlos y seguir replicándose a otros equipos
informáticos, aprovechándose de todo tipo de medios como el correo electrónico, IRC, FTP,
correo electrónico, P2P y otros protocolos específicos o ampliamente utilizados.

#### ¿Qué significa inyección o FWB, FWB+, FWB++ y FWB#?
La inyección del server en un proceso sirve para que evitar que el firewall filtre (prohíba) las conexiones salientes. La idea es inyectarse de un proceso que tenga salida a internet para poder conectarse.

En cuanto a FWB, FWB+, etc son términos que hacen referencia a la tecnología utilizada para traspasar los firewalls.

#### Spyware

Es un malware que recopila información de un ordenador y después la envía a una entidad remota sin el conocimiento o el consentimiento del propietario del ordenador.  
El término spyware también se utiliza más ampliamente para referirse a otros productos como adware, falsos antivirus o troyanos.

#### Adware
Es cualquier programa que automáticamente va mostrando publicidad al usuario durante su instalación o durante su uso y con ello genera beneficios a sus creadores.

#### Bomba Lógica

Trozo de código insertado intencionalmente en un programa informático que permanece oculto hasta cumplirse una o más condiciones
preprogramadas, momento en el que se ejecuta una acción maliciosa.
La característica general de una bomba lógica y que lo diferencia de un virus es que este código insertado se ejecuta cuando una determinada
condición se produce, por ejemplo, tras encender el ordenador una serie de veces, o pasados una serie de días desde el momento en que la bomba lógica se instaló en nuestro ordenador.

#### ¿Qué es un Crypter?
Software que encapsula un archivo ejecutable (ej. un troyano) dentro de otro archivo ejecutable ocultando su código y tornándolo irreconocible para los antivirus. Al momento de la ejecución el troyano es desencriptado en algún sector del disco rígido o de la memoria RAM y ejecutado.

##### Crypters Scan Time
El contenido del archivo, o sea el archivo original, es desencriptado y liberado en el disco cuando se ejecuta. Por lo tanto el archivo solo es indetectable a un scan con Anti-virus antes de ser ejecutado, perdiendo luego su indetectabilidad.

##### Crypters Run Time
El archivo original no es desencriptado en el disco, por lo tanto permanece indetectable a los Anti-Virus antes y luego de ser ejecutado.

#### ¿Qué es un PE Packer?
También conocido como Compresor PE. Las siglas PE significan Portable Executable. No es un malware propiamente dicho aunque muchas veces se usa para alivianar y camuflar troyanos. 

Es un software que encapsula un archivo ejecutable (ej. un troyano) dentro de otro archivo ejecutable teniendo como resultado un exe de menor tamaño. Como efecto secundario si el antivirus no posee la información para poder ver dentro del archivo empacado éste será indetectable. 

Al momento de la ejecución, el archivo externo descomprime el archivo interno en la memoria RAM y lo ejecuta. El funcionamiento es similar al de un Crypter Run Time con la diferencia de que en el Packer se prioriza la reducción de peso. El PE Packer mas conocido es UPX.

#### ¿Qué es un Binder?
Es un software que puede encapsular varios archivos dentro de uno, de modo que, por ej. al ejecutar el archivo resultante se instale un troyano, un keylogger y se abra una imagen para disimular. Es común que los Binders encripten los archivos que encapsulan teniendo también las cualidades de un Crypter Scan Time.

#### Bug
Es un error o fallo en un programa de dispositivo o sistema de software que desencadena un resultado indeseado.

## Antivirus y Firewalls

#### ¿Como los antivirus detectan los troyanos?

##### Método de Firmas
El antivirus tiene una o varias muestras (firmas) del código del troyano guarda en una base de datos, luego busca estas muestras en el archivo a analizar, éste método requiere que previamente la compañía antivirus haya ingresado la firma a su base de datos.

##### Método Heurístico
Se trata de buscar características comunes halladas en el código, nombre o ubicación de los troyanos para detectarlos aunque el antivirus no tenga una firma del mismo. Su importancia radica en que es la única defensa posible frente a la aparición de nuevos códigos maliciosos.

##### Modo Residente
Cuando el antivirus permanece alerta analizando cada archivos que se lee o escribe en nuestro disco. Tiene la desventaja de consumir recursos del sistema.

##### Modo A Pedido (on demand)
Cuando el antivirus realiza el análisis solo cuando se lo solicitamos.

##### Defensas Pro-Activas
Son una especie de Método Heurístico que opera en modo Residente detectando, por ejemplo, cambios en sectores críticos del sistema y que programa lo realiza.

#### ¿Qué es un Firewall?
Es un elemento de hardware o software utilizado en una red o computadora para controlar las comunicaciones, permitiéndoles o prohibiéndolas según las reglas establecidas por el administrador.

#### ¿Qué es un Firewall Personal?
Es un caso particular de firewall que se instala como software en una computadora, filtrando las comunicaciones entre dicha computadora y el resto de la red. Tiene la ventaja de que además del control de paquetes y puertos puede controlar que un malware no esté intentando hacerse pasar por una aplicación legítima. Estos firewalls suelen ser estar integrados con el antivirus.


## Glosario

#### Hacker
Es un término discutido ya que mientras los medios de comunicación como la TV y los diarios llaman hacker a cualquier persona que haya cometido un delito utilizando medios electrónicos, otros, los expertos, sostienen que para ser hacker hay que cumplir bastantes requisitos. En general hay consenso en que un hacker es un experto en varias o alguna rama técnica relacionada con la informática. Lo importante es que sepa que si ustedes sólo sabe manejar un par de troyanos, binders y crypters no debe creerse un hacker, el camino para serlo es largo y aunque pueda alardear delante de la mayoría de la gente, si lo hace en otros ámbitos podrá ser considerado un lammer.

#### Lammer
Persona sin conocimientos avanzados de computación que se cree o hace pasar por hacker. Originalmente era usada en la cultura cracker y phreaker para referirse a alguien que realmente no entendía lo que estaba haciendo.

#### Script kiddies
Término en forma de burla referido a alguien que tiene un poco de conocimiento de computadoras y solo sabe usar software estándar para hacer cosas como "tirar" sitios web o rastrear contraseñas sobre un WiFi protegido. Es básicamente un término para desacreditar a alguien que dice ser un hacker experto.

#### Troll
Usuario de las redes sociales/foros que escribe mensajes sin el objeto de contribuir, sino para crear polémica, provocar al resto y perturbar el funcionamiento armónico de la comunidad. Se recomienda a los usuarios no contestar este tipo de mensajes ya que es la mejor manera de desalentar a un troll.

#### Dark web
"Dark web" o "darknet" a veces se usan indistintamente, aunque no debería hacerse. La web oscura (darknet) está formada por sitios que no están indexados por los motores de búsqueda (como Google) y solo son accesibles a través de redes especializadas como Tor (ver Tor). A menudo, la web oscura es utilizada por operadores de sitios web que desean permanecer en el anonimato. Todo en la web oscura está en la web profunda (ver Deep Web), pero no todo en la web profunda está en la web oscura.

#### Deep web
Este término y "dark web" o "darknet" a veces se usan indistintamente, aunque no deberían serlo. La web profunda (deep web) es la parte de Internet que los motores de búsqueda no indexan. Eso incluye páginas protegidas con contraseña, sitios con paredes de pago, redes encriptadas y bases de datos.

####  Spoofing

Es una técnica de suplantación de identidad en la Red, llevada a cabo por un ciberdelincuente generalmente gracias a un proceso de investigación o con el uso de malware. Los ataques de seguridad en las redes usando técnicas de spoofing ponen en riesgo la privacidad de los
usuarios, así como la integridad de sus datos.
De acuerdo a la tecnología utilizada se pueden diferenciar varios tipos de spoofing:
• IP spoofing: consiste en la suplantación de la dirección IP de origen de un paquete TCP/
IP por otra dirección IP a la cual se desea suplantar.
• ARP spoofing: es la suplantación de identidad por falsificación de tabla ARP. ARP (Address Resolution Protocol) es un protocolo de nivel de red que relaciona una dirección MAC con la dirección IP del ordenador. Por lo tanto, al falsear la tabla ARP de la víctima,
todo lo que se envíe a un usuario, será direccionado al atacante.
• DNS spoofing: es una suplantación de identidad por nombre de dominio, la cual consiste en una relación falsa entre IP y nombre de dominio.
• Web spoofing: con esta técnica el atacante crea una falsa página web, muy similar a la que suele utilizar el afectado con el objetivo de obtener información de dicha víctima como contraseñas, información personal, datos facilitados, páginas que visita con frecuencia, perfil del usuario, etc. Los ataques de phishing son un tipo de Web spoofing.
• Mail spoofing: suplantación de correo electrónico bien sea de personas o de entidades con el objetivo de llevar a cabo envío masivo de spam.

#### Exploit

Secuencia de comandos utilizados para, aprovechándose de un fallo o vulnerabilidad en un sistema, provocar un comportamiento no deseado o imprevisto. Mediante la ejecución de exploit se suele perseguir:
• el acceso a un sistema de forma ilegítima.
• obtención de permisos de administración en un sistema ya accedido.
• un ataque de denegación de servicio a un sistema.

#### Zero-day

Son aquellas vulnerabilidades en sistemas o programas informáticos que son únicamente conocidas por determinados atacantes y son desconocidas por los fabricantes y usuarios. Al ser desconocidas por los fabricantes, no existe un parche de seguridad para solucionarlas.
Por esta razón son muy peligrosas ya que el atacante puede explotarlas sin que el usuario sea consciente de que es vulnerable.

#### Zombie

Es el nombre que se da a los ordenadores controlados de manera remota por un ciberdelincuente al haber sido infectados por un malware.
El atacante remoto generalmente utiliza el ordenador zombie para realizar actividades ilícitas a través de la Red, como el envío de comunicaciones electrónicas no deseadas, o la propagación de otro malware.
Son sistemas zombie los ordenadores que forman parte de una botnet, a los que el bot master utiliza para realizar acciones coordinadas como ataques de denegación de servicio.

#### Ransomware

El ciberdelincuente, toma control del equipo infectado y «secuestra» la información del usuario cifrándola, de tal forma que permanece ilegible si no se cuenta con la contraseña de descifrado. De esta manera extorsiona al usuario pidiendo un rescate económico a cambio de esta contraseña para que, supuestamente, pueda recuperar sus datos.
La seguridad del sistema está basada en la dificultad de factorización de grandes números. Su funcionamiento se basa en el envío de un mensaje cifrado mediante la clave pública del destinatario, y una vez que el mensaje cifrado llega, éste se encarga de descifrarlo con su clave privada.

#### Phishing

Phishing es la denominación que recibe la estafa cometida a través de medios telemáticos mediante la cual el estafador intenta conseguir,
de usuarios legítimos, información confidencial (contraseñas, datos bancarios, etc.) de forma fraudulenta.
El estafador o phisher suplanta la personalidad de una persona o empresa de confianza para que el receptor de una comunicación electró-
nica aparentemente oficial (vía e-mail, fax, SMS o telefónicamente) crea en su veracidad y facilite, de este modo, los datos privados que
resultan de interés para el estafador.
Existen diferentes modalidades de phishing. Cuando éste se realiza vía SMS el nombre técnico es Smishing y cuando se realiza utilizando Voz
sobre IP, se denomina vishing. Otra variedad es el spear phishing, en la que los atacantes intentan mediante un correo electrónico, que apa-
renta ser de un amigo o de empresa conocida, conseguir que les facilitemos: información financiera, números de tarjeta de crédito, cuentas
bancarias o contraseñas.

#### Pharming

Ataque informático que aprovecha una vulnerabilidad del software de los servidores DNS y que consiste en modificar o sustituir el archivo del servidor de nombres de dominio cambiando la dirección IP legítima de una entidad (comúnmente una entidad bancaria) de manera que en el momento en el que el usuario escribe el nombre de dominio de la entidad en la barra de direcciones, el navegador redirigirá automáticamente al usuario a una dirección
IP donde se aloja una web falsa que suplantará la identidad legítima de la entidad, obteniéndose de forma ilícita las claves de acceso de los clientes la entidad.

#### Sniffer

Un sniffer es un programa que monitoriza la información que circula por la red con el objeto de capturar información.
Las tarjetas de red pueden verificar si la información recibida está dirigida o no a su sistema.
Si no es así, la rechaza. Un sniffer lo que hace es colocar a la placa de red en un modo el cual desactiva el filtro de verificación de direcciones (promiscuo) y por lo tanto acepta todos los paquetes que llegan a la tarjeta de red del ordenador donde está instalado estén dirigidos o no
a ese dispositivo.
El tráfico que no viaje cifrado podrá por tanto ser «escuchado» por el usuario del sniffer.
El análisis de tráfico puede ser utilizado también para determinar relaciones entre varios usuarios (conocer con qué usuarios o sistemas se relaciona alguien en concreto).
No es fácil detectar si nuestro tráfico de red está siendo «escuchado» mediante un sniffer,por lo que siempre es recomendable utilizar tráfico cifrado en todas las comunicaciones.

#### Denegación de servicio (DDOoS)

Se entiende como denegación de servicio, en términos de seguridad informática, a un conjunto de técnicas que tienen por objetivo dejar un servidor inoperativo. Mediante este tipo de ataques se busca sobrecargar un servidor y de esta forma impedir que los usuarios legítimos puedan utilizar los servicios por prestados por él. 
El ataque consiste en saturar con peticiones de servicio al servidor, hasta que éste no puede 
atenderlas, provocando su colapso.
Un método más sofisticado es el ataque de Denegación de Servicio Distribuido (DDoS), mediante el cual las peticiones son enviadas, de forma coordinada entre varios equipos, que pueden estar siendo utilizados para este fin sin el conocimiento de sus legítimos dueños (por ejemplo a través de una botnet).
Esto puede ser así mediante el uso de programas malware que permitan la toma de control del
equipo de forma remota, como puede ser en los casos de ciertos tipos de gusanos.

#### Red privada virtual

Una red privada virtual, también conocida por sus siglas VPN (Virtual Private Network) es una tecnología de red que permite una extensión segura de una red local (LAN) sobre una red pública o no controlada como Internet.
Al establecerlas, la integridad de los datos y la confidencialidad se protegen mediante la autentificación y el cifrado.
Se trata realmente de una conexión virtual punto a punto entre dos redes LAN usando para la conexión una red pública como es Internet y consiguiendo que esta conexión sea segura gracias al cifrado de la comunicación.

#### Botnet

Una botnet es un conjunto de ordenadores (denominados bots) controlados remotamente por un atacante que pueden ser utilizados en conjunto para realizar actividades maliciosas como envío de spam, ataques de DDoS, etc.
Las botnets se caracterizan por tener un servidor central (C&C, de sus siglas en inglés Command & Control) al que se conectan los bots para enviar información y recibir comandos.
Existen también las llamadas botnets P2P que se caracterizan por carecer de un servidor C&C
único.


