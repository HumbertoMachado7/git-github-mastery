# Continuo conectar a GitHub…

Entonces una vez corregida la rama principal de Master a Main, aparece este error que necesito corregir.

![alt text](<Images/Untitled 85.png>)

Para solucionarlo, tengo que traerlo asi que escribo:

**git pull origin main**

![alt text](<Images/Untitled 86.png>)

Y ahora si bien tengo un error que dice “*fatal: refusing to merge unrelated histories*” porque, las dos ramas tienen distintas historias de commit. Entonces es una simple solución escribiendo lo siguiente:

**git pull orgin main —allow-unrelated-histories**

![alt text](<Images/Untitled 87.png>)

de ahi me fijo que esten los archivos con

**ls -al**

y tambien me aseguro que este todo listo en el lugar local de mi pc con git status que este todo en orden con 

**git status**

![alt text](<Images/Untitled 88.png>)

Entonces ahora si, puedo subir al repositorio de GIT HUB

**git push origin main**

![alt text](<Images/Untitled 89.png>)

Actualizo mi git hub y observo que esta todo subido en mi repositorio.

![alt text](<Images/Untitled 90.png>)