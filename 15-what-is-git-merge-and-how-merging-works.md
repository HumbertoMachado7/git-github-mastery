# Qué es Git merge y cómo funciona la fusión de ramas

1. Con el ejemplo de archivo, vamos a trabajar en la **rama cabecera**, con los dos archivos html y css. Pero también vamos hacer un nuevo commit al **master**, para que tome unos cambios en contenido y como unimos las ramas con el master. 
    
![alt text](<Images/Untitled 29.png>)
    
2. Esa fusión la realizamos con el comando MERGE
3. Lo que sucede cuando usamos el comando merge, la rama cabecera desaparece y sigue unida como master. Tambien puedes suceder que no se muera, porque le sigo haciendo más cosas y que se una en un futuro con otro merge.
    
![alt text](<Images/Untitled 30.png>)
    
4. efectue cambios en la cabecera de los archivos html y css, asi que tengo que escribir el comando **git add .**   y ejecutar  **git commit -m *“Finalizada la cabecera de color azul”***
5. Ahora voy a corregir en la rama MASTER un par de modificiaciones. Por lo que tengo que ir con **git checkout master** 

![alt text](<Images/Untitled 31.png>)
    
6. Realizo unas modificaciones en los archivos html y css de la rama master. Le pongo **git commit -am *“Agregado el contenido adicional del blog y una mejor tipografia”*** 
    
![alt text](<Images/Untitled 32.png>)
    
7. Si necesito saber en cual rama estoy ubicado, ejecuto el comando git branch