# Como conectar a GitHub con SSH

Para conectarme remotamente, primero el git bash tiene que estar conectado a en la carpeta del repositorio. Me fijo que con **pwd** que me da el Path y entre paréntesis **(master)**.

![alt text](<Images/Untitled 79.png>)

Voy a mi repositorio y copio su URL en donde dice HTTPS

![alt text](<Images/Untitled 80.png>)

y en git bash escribimos **git remote add orgin [*https://github.com/CanarioEchazu/hyperblog.git*](https://github.com/CanarioEchazu/hyperblog.git)**

![alt text](<Images/Untitled 81.png>)

![alt text](<Images/Untitled 82.png>)

Le doy enter y si bien hay respuesta alguna, sin embargo al escribirle

**git remote**

y su respuesta es

**origin**

![alt text](<Images/Untitled 83.png>)

y cuando escribimos

**git remote -v**     *(la “v” significa que sea verbal)*

Nos dice que hay dos ramas , 

***origin (fetch)*** Fetch es traernos cosas.

***origin (push)*** Push es enviar cosas.

Entonces ahora vemos una lista con los archivos y atributos que tiene esa carpeta.

**ls -al**

Y ahora hacemos la Magia de enviar nuestro archivo local al repositorio.

**git push origin master**