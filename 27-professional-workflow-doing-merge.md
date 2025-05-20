# Flujo de trabajo profesional Haciendo merge

Para poder desarrollar software de manera óptima y ordenada, necesitamos tener un flujo de trabajo profesional, que nos permita trabajar en conjunto sin interrumpir el trabajo de otros desarrolladores. Una buena práctica de flujo de trabajo sería la siguiente:

- Crear ramas
- Asignar una rama a cada programador
- El programador baja el repositorio con git pull origin main
- El programador cambia de rama
- El programador trabaja en esa rama y hace *commits*
- El programador sube su trabajo con git push origin #nombre_rama
- El encargado de organizar el proyecto baja, revisa y unifica todos los cambios

Ahora vamos con el video de ejercicio.

# Trabajando un usuario con una rama header

Para mejorar mi header voy agregar un logo binario (.png)

![alt text](<Images/Untitled 158.png>)

Este icono lo voy a dejar en una carpeta de mi proyecto de nombre images

![alt text](<Images/Untitled 159.png>)

Las mejores practicas dicen que los archivos binarios, no deberían estar en los repositorios, sino que ignorados por el tamaño que tiene. Pero a modo de ejercicio voy a dejarlo aquí.

![alt text](<Images/Untitled 160.png>)

Para subir al repositorio, primero tengo que hacerle ADD y COMMIT pero antes que nada ir a mi espacio local de la rama Header.

También voy a usar un **alias** para trabajar mejor de nombre **tree**

**alias tree="git log --all --graph --decorate --oneline”**

![alt text](<Images/Untitled 161.png>)

de aquí ejecuto los comandos

**git status**

y veo que tengo en rojo la carpeta images

**git add images/dragon.png**

nuevamente **git status** y me dice en rojo que tengo un nuevo archivo de dragon.png

ejecuto

**git commit -am “logo del header”**

Me fijo de nuevo en **git status** y localmente en la rama **header** está todo correcto.

![alt text](<Images/Untitled 162.png>)

## Subir la rama del proyecto al servidor

para subir las nuevas modificaciones, tengo que hacer GIT PULL y luego GIT PUSH

**git pull origin header**

![alt text](<Images/Untitled 163.png>)

ahora para subir al servidor

**git push origin header**

![alt text](<Images/Untitled 164.png>)

Ahora en el servidor puedo observar dentro de la rama header, que hay una carpeta nueva con su archivo png.

![alt text](<Images/Untitled 165.png>)

y dentro de la rama

![alt text](<Images/Untitled 166.png>)

y de ahi se puede observar el archivo grafico

![alt text](<Images/Untitled 167.png>)

## Modificación de archivos en local y subir al servidor

Voy a modificar el archivo grafico que son datos binarios y tiene mucho peso ese archivo.

![alt text](<Images/Untitled 168.png>)

Ahora lo preparo para subirlo con GIT PULL y GIT PUSH

Pero antes tengo que crearle su commit con

**git commit -am “Logo mejorado”**

![alt text](<Images/Untitled 169.png>)

y ahora escribo

git pull origin header

git push origin header

![alt text](<Images/Untitled 170.png>)

y puedo observar que en el respositorio del servidor, esta subido todos los cambios con su commit de logo mejorado

![alt text](<Images/Untitled 171.png>)

![alt text](<Images/Untitled 172.png>)

Efectúo unas modificaciones en el archivo html y css para la cabecera.
Luego, grabo con **git commit -am**

![alt text](<Images/Untitled 173.png>)

No lo tengo todavía en el servidor de repositorio pero al haber hecho git commit, ya lo tengo guardado localmente.

## IMPORTANTE RAMAS

Cada Rama, guarda los realizado.
Si veo el explorador con la rama **header**, están todos los cambios perfectamente.

![alt text](<Images/Untitled 174.png>)

Sin embargo si me fijo en la rama local **main**, todavía esta lo antigüo.

![alt text](<Images/Untitled 175.png>)

Por eso ahora vamos a Daniela

## Daniela hace rama footer

Ahora Daniela va hacer la rama footer para avanzar con el proyecto.

Antes vamos preparar el espacio para trabajar la rama.

Vemos con git branch en cual rama estamos situados. O con pwd me siento ubicado en el espacio local para comenzar el trabajo.

Bajamps del repositorio del servidor la rama footer con

**git pull origin footer**

es probable que la rama footer no esté iniciado. Por eso creamos la rama con
**git checkout footer**

y ahora si quedamos situados en la rama footer. Podemos verlo al perguntar git branch estan las ramas y obviamente el footer en color verde.

![alt text](<Images/Untitled 176.png>)

Si pregunto con el comando **ls** vemos también que en la rama footer están los otros archivos.

![alt text](<Images/Untitled 177.png>)

Efectúo modificaciones en archivos de hml y css, en lo que se ve reflejada con

git status

A lo que le hago el doble git add y commit con **git commit -am** *“descripción”.*

![alt text](<Images/Untitled 178.png>)

me fijo de estar bien posicionado con **pwd** y ver que el estado esta todo correcto con **git status**

![alt text](<Images/Untitled 179.png>)

ahora previo a subir al servidor, siempre tengo que ver si hay cambios desde el servidor, por si en equipo alguien efectúo algún cambio. 

**git pull origin footer**

y luego si esta todo correcto, efectúo

**git push origin footer**

![alt text](<Images/Untitled 180.png>)

y si me fijo en el servidor, en mi repositorio, seleccionando la rama footer, veo los cambios que me hizo Daniela.

![alt text](<Images/Untitled 181.png>)

## Unificar los trabajos con Merge

Ahora tomo como usuario responsable del proyecto, Darío.

Primero antes de unir, me fijo que todos las ramas están perfectas y con sus tareas terminadas.

Después de observar la distintas ramas, voy al **main** para actualizarme localmente

**git checkout main**

y tengo esta ventana sin cambios

![alt text](<Images/Untitled 182.png>)

**git checkout header**

y tengo esta que habia arreglado

![alt text](<Images/Untitled 183.png>)

y si cambio a footer, todavia en mi sitio local no actualicé lo que hico Daniela, asi que tengo que hacer **git pull origin footer**

![alt text](<Images/Untitled 184.png>)

y ahora si obtengo la siguiente vista de mi navegador.

![alt text](<Images/Untitled 185.png>)

Perfecto !!! Ahora ya tengo todo listo para comenzar a unir todas las tareas realizadas en cada ramas.

## Tareas del jefe del proyecto

Primero es ir a la rama principal en el local y de ahí comenzar con Merge. Desde la rama maestra voy a fusionar la rama del header.

**git merge header**

![alt text](<Images/Untitled 186.png>)

Ahora tengo que subirlo a internet. Asi que lo primero en hacer es un **git pull** y luego **git push** del main.

![alt text](<Images/Untitled 187.png>)

Y ahora la rama main está actualizada de las tareas realizadas en header.

![alt text](<Images/Untitled 188.png>)

Ahora tengo que fusionar en el main, la rama footer y subirla al repositorio del servidor.

![alt text](<Images/Untitled 189.png>)

## solucion al error del merging

Para solucionar este error efectuo git add y git commit, o el clasico git commit -am “descripcion”

![alt text](<Images/Untitled 190.png>)

Y ahora si subo a la nube con git push previamente siempre un git pull para actualizar al local todo lo del servidor.

**git push origin main**

![alt text](<Images/Untitled 191.png>)


Y ahora, en nuestro navegador está completo.

![alt text](<Images/Untitled 192.png>)