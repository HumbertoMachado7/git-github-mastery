# **Retorno al MASTER desde cabecera**

Para retornar a la cabecera escribo git checkout master, y va pasar algo sorprendente.

Al colocar git status, el HEAD apunta a Master. 

Y el git log, hizo desaparecer los cambios que hice en cabecera.

![alt text](<Images/Untitled 25.png>)


![alt text](<Images/Untitled 26.png>)

Pero si quiero seguir con lo agregado anterior, cambio el HEAD para que retorne a apuntar a la rama cabecera con **git checkout *cabecera***.

![alt text](<Images/Untitled 27.png>)

![alt text](<Images/Untitled 28.png>)