# Como usar GIT reset y checkout

1. Escribo **git log** nombre archivo para ver todos los commit.
2. Para retornar un commit anterior usamos **git reset** y el numero del commit. 
3. Existen dos tipos de pedidos. 
**git reset *numerocommit* —hard** vuelve al estado anterior y es el más peligroso.
 **—soft** vuelve lo que queda en staging (hasta donde hicimos el git add). 

Aqui le hice reset hard y desaparecio el 4 commit.
![alt text](<Images/Untitled 4.png>)

1. Creando otro archivo HTML con su estilos en CSS
2. Ahora si escribo **git log —stat** me da informacion de todas las modificaciones realizadas.
3. Ahora voy a practicar con git checkout. Voy a tomar el primer commit y escribir **git checkout** *numerocommit nombrearchivo*
4. El archivo retorna a su primer commit.
5. Ahora si quiero recuperar todo de nuevo, tengo que escribir **git checkout master**, y retorna  todo al estado ultimo.

![git log -stat](<Images/Untitled 5.png>)

1. Creando otro archivo HTML con su estilos en CSS
2. Ahora si escribo **git log —stat** me da informacion de todas las modificaciones realizadas.
3. Ahora voy a practicar con git checkout. Voy a tomar el primer commit y escribir **git checkout** *numerocommit nombrearchivo*
4. El archivo retorna a su primer commit.
5. Ahora si quiero recuperar todo de nuevo, tengo que escribir **git checkout master**, y retorna  todo al estado ultimo.

![git checkout](<Images/Untitled 6.png>)