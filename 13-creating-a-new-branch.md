# Creando una nueva rama

Voy a crear una nueva rama de nombre Cabecera.

**git branch** *cabecera*

al escribir git show, nos muesta que HEAD apunta las dos branches, master y cabecera.

![alt text](<Images/Untitled 19.png>)

Entonces como hago para ir a la otra rama Cabecera?

escribo **git ckeckout *cabecera***

y ahora si escribo **git status**, me va decir que el HEAD apunta a Cabecera.

![alt text](<Images/Untitled 20.png>)

Ahora mi git bash apunta a la cabecera. Si escribo git status apunta a cabecera.

Ahora al archivo de ejemplo blogpost.html le creo un div nuevo de cabecera, y al escribir git status, tenemos un archivo modificado.

![alt text](<Images/Untitled 21.png>)

Escribo git add blogpost.html y tambien le hago un git commit.

Al escribir git status, nos da la siguiente respuesta.

![alt text](<Images/Untitled 22.png>)

luego tambien si le pido git show me da la siguiente respuesta.

![alt text](<Images/Untitled 23.png>)

y si le escribo git log tambien me da ésta otra respuesta.

![alt text](<Images/Untitled 24.png>)

Como puedo observar, ya el HEAD apunta a la rama cabecera. Y en log, todos los commit a cual cabeza apuntaba en su momento.