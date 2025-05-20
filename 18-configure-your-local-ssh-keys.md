# Configura tus llaves SSH en local

Cuando configuras para GIT HUB colocas usuario y contraseña, estas configurando para tu acción local. Pero si pierdes la computadora, cualquiera puede entrar a tu repositorio.

![alt text](<Images/Untitled 46.png>)


Estas expuesto a tu Password cracking, donde te pueden robar todos tus trabajos y proyectos.

Para solucionarlo, en tu entorno local, en tu computadora tienes dos tipos de llaves. Crea una **llave privada** y una **llave publica**.

![alt text](<Images/Untitled 47.png>)

Envio la llave publica a mi git hub 

![alt text](<Images/Untitled 48.png>)

Y le digo a mi git hub, aqui tiene ésta llave publica de mi llave privada que tengo en mi computadora.

Y eso lo conecto con otro protocolo distinto al HTTPS, sino por SSH (secure shell).

![alt text](<Images/Untitled 49.png>)

En la **primera conexión GIT HUB** es muy inteligente. Se va dar cuenta que le enviaste una **llave publica**, que está correlacionada con la **llave privada**. Entonces te va enviar **su propia llave publica cifrada de GIT HUB**.

![alt text](<Images/Untitled 50.png>)

Automaticamente, GIT HUB te va enviar esa llave publica y tengo que conectarla con mi computadora.

![alt text](<Images/Untitled 51.png>)

Voy a configurar la llave de mi usuario. Entonces en mi git bash me voy a posicionar en la raiz de todos los proyectos y no en cada uno, sino en la raiz de los directorios.

con el comando **pwd** se donde estoy ubicado. 

y para saber como esta configurado mi **git bash** local escribo

**git config -l**

![alt text](<Images/Untitled 52.png>)

al ejecutar el comando mencionado puedo ver dos cosas

mi [user.email](http://user.email) y tambien mi [user.name](http://user.name) 

Entonces tengo que hacer coi unncidir los mismos datos con mi repositorio de la web de GIT HUB.

Si tuviera que corregirlo, debo escribir el siguiente comando.

**git config —global [user.email](http://user.email) *“darioechazu@hotmail.com”***

Si el cambio es correcto, entonces al escribo 

**git config -l**, que sean los datos correctos.

Lo que sigue es hacer la llave SSH

## Crear llave SSH

Nos posicionamos  en el home de la instalacion de los proyectos y escribo.

**ssh-keygen -t rsa -b 4096 -C “darioechazu@hotmail.com”**

y se crea esta llave, donde en cada opcion las vamos a dejar libre presionando enter, por esta sola vez.

![alt text](<Images/Untitled 53.png>)

y aqui he creado dos llaves publicas, donde me dice que esta llave, solo se puede usar con el correo mio.

Y en el explorador de archivos, me ha creado una carpeta .ssh, donde estan las dos archivos, publico y privado.

![alt text](<Images/Untitled 54.png>)

El primer archivo es la llave privada.

El segundo archivo es la llave publica (la que tiene el logo P en verde) y ese archivo, lo abro con visual studio code, y lo copio para llevarla a GIT HUB.

![alt text](<Images/Untitled 55.png>)

Ahora, es importante saber que en mi laptop este el servidor de SSH encendido.

En windows se hace del siguiente modo:

**eval $(ssh-agent -s)**

Nuestro siguiente paso es agregar la llave a nuestro sistema.

Ahora voy dejar un par de comandos de cd, cd / o tambien cd ~ .

![alt text](<Images/Untitled 56.png>)

Ahora escribo **ssh-add ~/.ssh/id_rsa** y listo, mi identidad ha sido añadida.

![alt text](<Images/Untitled 57.png>)

Esto es para instalar con sistema operativo WINDOWS.

## Configuracion de llave para MAC

Para la Mac, es totalmente distinto.

![alt text](<Images/Untitled 58.png>)

Y desde la terminal para evaluar si esta corriendp el SSH Agent se escribe lo siguiente:

![alt text](<Images/Untitled 59.png>)

Puede suceder que otro modelos de MAC con la Manzanita, no tengan el archivo config. Por lo que hay que crearla con el editor de la terminal.
Lo que se ve es lo siguiente.

![alt text](<Images/Untitled 60.png>)

Y como el archivo config no existe, escribo:

**vim config**

y se abre un editor de texto y escribo.

Host * (enter)
(tab) Add…… (enter)
(tab) Use….    (enter)
(tab) Iden….   (enter)
Y salgo con (ESC) (Shift) (z) (z)

![alt text](<Images/Untitled 61.png>)

Ahi esta creado el archivo config, y entonces ahora si ejecuto lo siguiente:

**cat config**

![alt text](<Images/Untitled 62.png>)

y le escribo el comando que esta en la imagen

![alt text](<Images/Untitled 63.png>)

Y Listo, ya esta terminada para la MAC.

Le proximo paso es conectarnos con GIT HUB pero no conexion de HTTPS sino SSH