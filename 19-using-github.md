El Git Hub es muy util porque paso a ser la red social de los programadores.

Una vez ingresado en la web de git hub, veamos las alternativas de trabajo para hacer en la nube.

Una vez ingresado, creo un nuevo repositorio presionando el boton NEW

![alt text](<Images/Untitled 64.png>)

De ahi efectuo estos ingresos

![alt text](<Images/Untitled 65.png>)

Creando un archivo de README y por ahora no le sumo ninguna licencia.

Presiono el boton Create Repository

![alt text](<Images/Untitled 66.png>)

presiono en el nombre del archivo en este caso en [README.md](http://README.md) que esta abajo de CanarioEchazu Initial comment y se abre la siguiente ventana.

![alt text](<Images/Untitled 67.png>)

ahora tengo cuatro opciones.

1. Raw
2. Code
3. Blame
4. History

Con **Raw**, me abre una ventana nueva, visualizando texto plano del commit que se ha creado.

En **Code**, tengo la posibilidad de editar al presionar el boton del lapiz

![alt text](<Images/Untitled 68.png>)

Y con **Blame** puedo observar quien fue el responsable de este commit.

![alt text](<Images/Untitled 69.png>)

y con **History**, es como cuando ejecuto un git log, que me muestra toda la vida de los commit que tuvo ese archivo.

![alt text](<Images/Untitled 70.png>)

## Como traer lo realizado en la PC al repositorio

Tengo las llaves creadas tanto publica como privada. Entonces vamos a trabajar con **SSH**.
Estas llaves están ubicadas en el home de mi PC y no del repositorio

### **Importante**:

Cada Usuario, cada computadora, cada lugar de trabajo, tiene **UNA LLAVE UNICA** !!!

Entonces si tienes tres laptops, tiene que tener 3 llaves conectadas a tu repositorio. Sino nunca podria trabajar en ese lugar.

Mis llaves estan aqui:
C:\Users\dario\.ssh

Y la que tengo que abrir, es solamente la publica
id_rsa (tiene una P).

![alt text](<Images/Untitled 71.png>)

Y abrimos con Visual Studio Code.

![alt text](<Images/Untitled 72.png>)

En Visual Estudio Code, seleccionamos todo el archivo y lo copiamos.

![alt text](<Images/Untitled 73.png>)

De ahi vamos a nuestro perfil del Git Hub, y selecciono la opcion settings

![alt text](<Images/Untitled 74.png>)

de ahi busco en mi columna de la izquierda la opcion que dice **SSH and GPG kyes** y pego mi llave

![alt text](<Images/Untitled 75.png>)

Ahi presiono la tecla **New SSH key**

![alt text](<Images/Untitled 76.png>)

y creo la nueva llave, colocando arriba la descripcion y abajo el codigo de la llave.

![alt text](<Images/Untitled 77.png>)

y al presionar **Add SSH key** me creo la llave dándome la siguiente ventana.

![alt text](<Images/Untitled 78.png>)

Y acabo de crear mi llave publica para trabajar.

Ya tenemos viculados nuestro repositorios con SSH.