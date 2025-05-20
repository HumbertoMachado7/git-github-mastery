# Como usar Tags y versiones

Para aprender a conocer la historia de nuestro proyecto, en sus distintas versiones a medida que se estaban actualizando. Como primer inicio usamos en Git Bash el comando:

**git log**

y veremos lo que más o menos pasó.

Si escribo con más parámetros, voy a ver literalmente todo lo realizado.

**git log —all**

![alt text](<Images/Untitled 104.png>)

## Hay una opcion especial

Para ver como han funcionado las distintas ramas, nos muestra con unas rayitas para ser más visuales

**git log —all —graph**

![alt text](<Images/Untitled 105.png>)

Y si quiero tener un grafico más resumido.

**git log —all —graph —decorate —oneline**

![alt text](<Images/Untitled 106.png>)

## Alias

## Método 1 como el video

Si escribo el comando

**git log —all —graph —decorate —oneline** 

funciona correctamente y a este texto lo agrego la opcion de:

alias *nombrealias* = “*todo el comando del alias*”

**alias tree=”git log —all —graph —decorate —online”**

Luego llamo con *nombrealias* y funciona correctamente

**tree**

![alt text](<Images/Untitled 107.png>)

## Método 2 (más complicado)

Para generar un comando complejo con varios comandos de una forma optimizada, utilizamos conjuntos de sentencias conocidas como *alias*.

Cómo aregar un alias solo para git

- Para un proyecto:

**git config alias.arbolito "log --all --graph --decorate --oneline"**

- Global:

**git config --global alias.arbolito "log --all --graph --decorate --oneline"**

![alt text](<Images/Untitled 108.png>)

- Para correrlo:

**git arbolito**

### Diferencias:

Las diferencias es que con Método 1 solo llamo al alias

**tree**

Y con el Método 2 llamo con git

**git arbolito**

## Tags o etiquetas

Los tags o etiquetas nos permiten asignar versiones a los commits con cambios más importantes o significativos de nuestro proyecto.

Ahora despues de llamar a mi alias **tree** o tambien **git arbolito**, selecciono mi primera version:

![alt text](<Images/Untitled 109.png>)

copio el hash (numeros amarillos) para crear la versión, en este caso es **32d0f06**

y le escribo git tag -a *nombreversion* -m *“mensaje descriptivo”* NumeroHash

**git tag -a v0.1 -m “Resultado de las primeras clases” 32d0f06**

![alt text](<Images/Untitled 110.png>)

Si quiero ver la lista de tags que tengo escribo

**git tag**

![alt text](<Images/Untitled 111.png>)

Para ver a qué tag estoy trabajando, lo consigo escribiendo

**git show-ref —tags**

![alt text](<Images/Untitled 112.png>)

Importante, si hago git status, la respuesta me va decir que no hay nada que enviar al servidor, pero si tengo que enviarlo.

Entonces antes de enviar los cambios, como siempre tengo que hacer 

**git pull origin main**

![alt text](<Images/Untitled 113.png>)

Ahora tengo que enviar los datos del tags al repositorio en el servidor. Le escribo:

**git push origin —tags**

![alt text](<Images/Untitled 114.png>)

Ahora me fijo en el repositorio del servidor y actualizando, puedo observar que en el nombre del repositorio, al ver en main, en su lengüeta Tags, se ve el nuevo Tags de v0.01

![alt text](<Images/Untitled 115.png>)

y al hacer click ahi, tengo mi proyecto hasta ese instante.

![alt text](<Images/Untitled 116.png>)

## Borrando Tags

Voy hacer un simple ejercicio para borrar un tags temporario. Por ejemplo llegar a una instancia de trabajo y antes de dormir, creo todos los resguardos y tambien sus Tags.

Creo un punto de Tags

**git tag -a dormido -m “tengo sueklnbo sdfas” e22b1d3**

Luego bajo con PULL

**git pull origin main**

y de ahi, hago PUSH pero de los Tags.

**git push orgin —tags**

![alt text](<Images/Untitled 117.png>)

Me fijo en el repositorio del servidor y veo que ahora tengo dos Tags.

![alt text](<Images/Untitled 118.png>)

Y tengo mi tags *dormido*

![alt text](<Images/Untitled 119.png>)

Ahora voy a borrar el tag temporario del *dormido*, desde el Git Bash.

![alt text](<Images/Untitled 120.png>)

Y ahora ejecuto el clasico  

**git pull orign main**

Y luego 

git push origin —tags

### Importante: Falta borrar en repositorio

Si me fijo en el repositorio en el servidor, siguen presente los dos tags

![alt text](<Images/Untitled 121.png>)

Entonces escribo el siguiente comando:

**git push origin :refs/tags/dormido**

![alt text](<Images/Untitled 122.png>)

y automáticamente me borra el tags en el repositorio.

![alt text](<Images/Untitled 123.png>)

Otros resumen para tener presente.

**Comandos para trabajar con etiquetas:**

- Crear un nuevo tag y asignarlo a un commit: **git tag -a *nombre-del-tag* *id-del-commit***.
- Borrar un tag en el repositorio local: **git tag -d *nombre-del-tag***.
- Listar los tags de nuestro repositorio local: **git tag** o **git show-ref --tags**.
- Publicar un tag en el repositorio remoto: **git push origin --tags**.
- Borrar un tag del repositorio remoto: git tag -d nombre-del-tag y **git push origin :refs/tags/nombre-del-tag**.