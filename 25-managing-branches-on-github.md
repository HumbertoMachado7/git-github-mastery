# Manejo de ramas en GitHub

Voy a empezar a trabajar dividiendo tareas. El Header y el Footer, por lo que voy a crearle las dos ramas para trabajarlas.

## Recordatorio:

Cambio a la rama cabecera

**git checkout cabecera**

y me cambia todos mi archivos a mi disco duro. Y si coloco

**git checkout main**

retorno a mi main.

Y para ver las ramas que tengo

**git branch**

y me muestra todas las ramas que tengo.

![alt text](<Images/Untitled 124.png>)

también tengo que recordarme del **alias** que puse para ver en modo grafico de las ramas.

**git log —all —graph —decorate —oneline**

a la que en el alias hago
**alias tree=git log —all —graph —decorate —oneline”**

y tengo todos los commit que fui haciendo en el proyecto.

![alt text](<Images/Untitled 125.png>)

Y veo como cada rama tiene su propia historia.

## Otros comandos

Este nos muestra cuales son las ramas que existen y cuales fueron sus historias.

**git show-branch**

Tambien tenemos otro mas completo que nos va ser de mucha utilidad.

**git show-branch —all**

![alt text](<Images/Untitled 126.png>)

Y también tenemos otro comando que abre una aplicación más gráfica.

**gitk**

![alt text](<Images/Untitled 127.png>)

y lo que hace es mostrar mas visual la historia de las ramas.

![alt text](<Images/Untitled 128.png>)

## Preparando las ramas

Siempre antes de hacer algo, tengo que actualizar lo que esté en el servidor.

**git pull origin main**

![alt text](<Images/Untitled 129.png>)

ahora me cambio a la rama cabecera con

**git checkout cabecera**

![alt text](<Images/Untitled 130.png>)

y voy a empujar la rama cabecera a mi servidor.

**git push origin cabecera**

![alt text](<Images/Untitled 131.png>)

Y en mi repositorio del servidor al actualizar ya puedo ver las dos ramas.

![alt text](<Images/Untitled 132.png>)

## Creando otras ramas más

Entonces ahora voy a crear dos cabeceras más, header y footer.

Lo primero que voy hacer es ir a la rama más reciente, en este caso main.

**git checkout main**

Desde ahí creo la ramas con

**git branch header**

**git branch footer**

Y para ver las ramas que tengo, escribo

**git branch**

![alt text](<Images/Untitled 133.png>)

Entonces ahora lo subo a internet, por si alguien está trabajando y ya tiene actualizada desde el servidor. Entonces tengo que empujar las dos nuevas ramas

**git push origin header**

**git push origin footer**

![alt text](<Images/Untitled 134.png>)

Y podemos ver desde el repositorio del servidor ya están las dos nuevas ramas creadas. (son 4 ramas ahora)

![alt text](<Images/Untitled 135.png>)

Esto va servir para dividir tareas de trabajo. Un usuario poddria estar trabajando en footer y por mi lado estaría trabajando en header.
Después fusionamos las cabeceras en el main para ir armando el proyecto más rápidamente.