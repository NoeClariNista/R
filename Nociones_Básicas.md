___

# **Nociones Básicas De R.**

---

Para editar el tamaño de la consola vamos al Menú -> Editar -> Preferencias de la interface gráfica.

![nociones_basicas_01](./img/2-Nociones_Básicas/nociones_basicas_01.png)

![nociones_basicas_02](./img/2-Nociones_Básicas/nociones_basicas_02.png)

Para ver los manuales de R solo tenemos que ir al Menú -> Ayuda -> Manuales (En PDF).

![nociones_basicas_03](./img/2-Nociones_Básicas/nociones_basicas_03.png)

Si pinchamos Control + L se limpia la consola.

![nociones_basicas_04](./img/2-Nociones_Básicas/nociones_basicas_04.png)

Lo primero que vamos a hacer es crear las variables. Las variables pueden llevar letras, números, puntos y barras bajas.

![nociones_basicas_05](./img/2-Nociones_Básicas/nociones_basicas_05.png)

Las minúsculas y las mayúsculas son diferentes, a eso se le llama case sensitivity.

![nociones_basicas_06](./img/2-Nociones_Básicas/nociones_basicas_06.png)

Estas variables no tienen límite de tamaño o bytes los nombres de las variables, en versiones anteriores de R si tenían un límite.

Las variables pueden empezar con punto pero las variables que empiezan con punto son las variables del sistema.

![nociones_basicas_07](./img/2-Nociones_Básicas/nociones_basicas_07.png)

Las variables no pueden empezar con números.

![nociones_basicas_08](./img/2-Nociones_Básicas/nociones_basicas_08.png)

Si utilizamos `mode(nombredevariable)` nos dice que tipo de variable es.

![nociones_basicas_09](./img/2-Nociones_Básicas/nociones_basicas_09.png)

Los `mode(nombredevariable)` pueden ser numéricos, caracteres, logical, lista.

![nociones_basicas_10](./img/2-Nociones_Básicas/nociones_basicas_10.png)

Las variables numéricas pueden ser enteros o númericas reales como precisión sencilla o como precisión doble, para comprobar esto utilizamos el comando `storage.mode(nombredevariable)`.

![nociones_basicas_11](./img/2-Nociones_Básicas/nociones_basicas_11.png)

El storage mode de una variable carácter es carácter.

![nociones_basicas_12](./img/2-Nociones_Básicas/nociones_basicas_12.png)

Los `storage.mode(nombredevariable)` pueden ser logical, doble, simple, entero, cáracter, lista,...

![nociones_basicas_13](./img/2-Nociones_Básicas/nociones_basicas_13.png)

Todas las variables tiene que estar definidas con algún valor. El tipo de la variable se define automáticamente.

Para saber las variables que he creado se utiliza `ls()`.

![nociones_basicas_14](./img/2-Nociones_Básicas/nociones_basicas_14.png)

Para ver la historia de los comandos que se han utilizado, se utiliza el comando `history()`.

![nociones_basicas_15](./img/2-Nociones_Básicas/nociones_basicas_15.png)

![nociones_basicas_16](./img/2-Nociones_Básicas/nociones_basicas_16.png)

Para obtener ayuda sobre un comando utilizo el comando `?nombredecomando`, se abre una ventana de un navegador y no es necesario tener Internet porque es una página web local.

![nociones_basicas_17](./img/2-Nociones_Básicas/nociones_basicas_17.png)

![nociones_basicas_18](./img/2-Nociones_Básicas/nociones_basicas_18.png)

En la ayuda nos pueden salir funciones relacionadas.

Para poner comentarios utilizamos el símbolo `#`.

![nociones_basicas_19](./img/2-Nociones_Básicas/nociones_basicas_19.png)

Para salir de R simplemente ponemos q() y salimos.

![nociones_basicas_20](./img/2-Nociones_Básicas/nociones_basicas_20.png)

---
