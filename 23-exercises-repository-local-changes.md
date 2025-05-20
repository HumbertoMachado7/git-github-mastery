# Ejercicios de cambios en repositorio y cambios local

Ahora voy a practicar, cuando efectuo cambios en mi repositorio y despues cambios en mi local.

Desde el repositorio selecciono el archivo html y lo edito modificando el titulo a hyperblog.
Guardo los cambios y le agrego su commit, pero en internet.

![alt text](<Images/Untitled 91.png>)

ahora esta modificación, no esta en mi PC, 

![alt text](<Images/Untitled 92.png>)

así que para actualizar esa modificación, tengo que hacer los siguiente para que me traiga al proyecto local.

**git pull origin main**

![alt text](<Images/Untitled 93.png>)

Y ahora en mi archivo local, ya esta modificado.

![alt text](<Images/Untitled 94.png>)

y si me fijo con **git log**, estan todos los commit.

![alt text](<Images/Untitled 95.png>)

## Cambios en el local

Ahora voy a efectuar cambios desde mi Virtual Studio de modo local. A mi hyperblog le agrego 2.0

![alt text](<Images/Untitled 96.png>)

y en mi repositorio, no esta modificada.

![alt text](<Images/Untitled 97.png>)

IMPORTANTE: Antes de hacer un commit, tengo que traer la ultima version del servidor Escribo:

git pull 

![alt text](<Images/Untitled 98.png>)

PEEEEEEERO me da error todavia. Entonces tengo que hacer lo mismo que lo que hice anteriormente.

Traer del origin a mi rama actual

**git pull origin main**

![alt text](<Images/Untitled 99.png>)

Para ver el estado obviamente lo puedo observar con **git status**, y para ver que cambios tuve, lo realizo con **git diff**

![alt text](<Images/Untitled 100.png>)

Y ahora antes de subir, para evitar conflictos reitero

**git pull origin main**

![alt text](<Images/Untitled 101.png>)

Y ahora si, efectuo todo para subir mis cambios para que lo tenga el servidor.

git push origin main

![alt text](<Images/Untitled 102.png>)

Actualizo en el servidor, y ya esta tambien cargada.

![alt text](<Images/Untitled 103.png>)

## Cambios desde el local hacia el repositorio

Una vez que hayas retrocedido al commit anterior, podemos usar **`git push --force`** para actualizar el repositorio remoto en GitHub.

Recordemos que si estás trabajando en un proyecto compartido, es importante coordinar los cambios y tomar precauciones para evitar conflictos.