# pull request en GitHub

Tenemos errores en archivos y para corregirlo, vamos hacer una nueva rama fix-typo, donde vamos a corregir los errores antes de unirlos.

Primero voy a llamar localmente como siempre desde la rama main con

**git pull origin main**

Creo la rama 

**git branch fix-typo**

y apunto ahora localmente a esa rama

**git checkout fix-typo**

![alt text](<Images/Untitled 155.png>)

Una vez ubicado ahí, realizo la correcciones y con git status veo que el archivo está modificado, y con git diff veo los cambios, siendo verde el último y rojo el anterior.

![alt text](<Images/Untitled 156.png>)

Escribo los arreglos con

**git commit -am “*acentos arreglados”***

Ahora para subir al servidor el repositorio, si hago **git pull** a la rama nueva, me va dar error, porque esa rama no estaba creada. Así que escribo:
**git push origin fix-typo**

![alt text](<Images/Untitled 157.png>)

Sigue en 
D:\Platzy 3B\Curso Profesional de Git y GitHub
Video 28