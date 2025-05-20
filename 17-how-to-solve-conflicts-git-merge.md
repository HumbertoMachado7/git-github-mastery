# Como solucionar conflictos al hacer Git merge.

Si efectuo ahora el git checkout cabecera, retorno a la rama cabecera. Y mi web esta ausente de un parrafo. Para practicar en caso de conflicto en el merge, voy a unir en la rama cabecera el ultimo commit de master.

![alt text](<Images/Untitled 38.png>)


Al efectuar el **git merge *master***, no genero conflictos, y por eso mi HEAD apunta a cabecera y master.

![alt text](<Images/Untitled 39.png>)

## Creo un conflicto

Voy hacer ahora modificaciones en las ramas cabecera en sus archivos html y css, para aprender a resolver el MERGE en caso de conflictos.

![alt text](<Images/Untitled 40.png>)

![alt text](<Images/Untitled 41.png>)

Estoy en master y al hacer git merge, tengo varios conflictos para solucionarlos.

![alt text](<Images/Untitled 42.png>)

Si me fijo en Visual Studio, tengo conflicto.

![alt text](<Images/Untitled 43.png>)

![alt text](<Images/Untitled 44.png>)

Entonces ahora me fijo en visual studio code para corregir y evaluar con cual me quedo en el master. Seleccionando cual acepto.

Guardo los cambios en los archivos y efectuo el git commit de nuevo.

![alt text](<Images/Untitled 45.png>)