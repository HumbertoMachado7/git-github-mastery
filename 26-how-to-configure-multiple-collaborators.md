# Cómo configurar múltiples colaboradores en un repositorio

Acaba de sumarse una nueva colaboradora en el Proyecto.

Es Daniela, y tengo que configurar todo de nuevo para que ella tenga su nombre usuaria y nomber del mail, como así también configurarle y autorizarle en el servidor  su SSH.

Lo primero que tengo que hacer es 

**git config —list**

![alt text](<Images/Untitled 136.png>)

Ahora tengo que poner los datos de Daniela con los siguientes comandos.

**git config —global [user.email](http://user.email) “danielafabbroni7@gmail.com”**

**git config —global [user.name](http://user.name) “Daniela Fabbroni”**

Y chequeo que esta bien los datos reiterando

**git config —list**

![alt text](<Images/Untitled 137.png>)

de ahi, Daniela va tener una carpeta 01Curso donde va estar trabajando ella. Voy usar los siguientes comandos basicos de Git Bash.

**pwd**

**ls**

**cd ..**

**ls**

**mkdir 01Curso**

**ls**

**cd 01Curso/**

**pwd**

![alt text](<Images/Untitled 138.png>)

Me fijo que no hay nada en esa carpeta

**ls -al**

![alt text](<Images/Untitled 139.png>)

y de ahi voy a crear una carpeta de nombre proyecto1

**mkdir** *proyecto1*

**cd** *proyecto1*

![alt text](<Images/Untitled 140.png>)

Ahora Daniela va visitar desde su github el hyperblog del repositorio de CanarioEchazu, y desde ahí va CLONAR el repositorio para su espacio local.k

![alt text](<Images/Untitled 141.png>)

Y para bajar el repositorio al espacio local escribo
**git clone** [*https://github.com/CanarioEchazu/hyperblog.git*](https://github.com/CanarioEchazu/hyperblog.git)

![alt text](<Images/Untitled 142.png>)

y me bajo el repositorio en una carpeta del hyperblog con todos sus archivos.

![alt text](<Images/Untitled 143.png>)

Ahora voy a corregir algo desde el editor de consola al archivo historia.txt con el comando **VIM** y agrego un texto de Daniela

**vim** *historia.txt*

![alt text](<Images/Untitled 144.png>)

Termino guardando con ESC, Shift + Z (dos veces) y tengo modificado el archivo.

Luego realizo el git add y git commit para  terminar en modo local.

![alt text](<Images/Untitled 145.png>)

Entonces SIEMPRE traemos lo ultimo desde internet con

**git pull origin main**

![alt text](<Images/Untitled 146.png>)

Y puedo ver que tiene la rama que uso

**git branch**

tambien que este toda la historia con

**git log**

![alt text](<Images/Untitled 147.png>)

## IMPORTANTE: Daniela puede clonar pero no puede enviar.

Entonces Darío tiene que dar permisos para que Daniela puede enviar también,

Y el propietario tiene que agregar los datos del colaborador.

![alt text](<Images/Untitled 148.png>)

![alt text](<Images/Untitled 149.png>)

Y a Daniela le llega una invitacion a ser colaboradora.

![alt text](<Images/Untitled 150.png>)

Entonces Daniela ve su opcion de aceptarme para trabajar en este proyecto.

![alt text](<Images/Untitled 151.png>)

y ejecuto 

**git push origin main**

![alt text](<Images/Untitled 152.png>)

Y en el github de Daniela ya está subida al servidor todos los cambios realizados.

![alt text](<Images/Untitled 153.png>)

## Bajar los cambios como Dario Echazu y reiterar la subida del local al repositorio.

**git pull origin main**

**git push origin main**

![alt text](<Images/Untitled 154.png>)