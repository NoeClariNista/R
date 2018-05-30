___

# **Gráficos Y Matrices.**

---

## **Gráficos.**

El comando `curve(x^2, from=-3, to=3)` permite hacer gráficos de funciones.

![graficos_y_matrices01](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_01.png)

![graficos_y_matrices02](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_02.png)

También podemos hacer `curve(sin, from=-2*pi, to=2*pi)`.

![graficos_y_matrices03](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_03.png)

![graficos_y_matrices04](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_04.png)

En R constantes están grabadas, por ejemplo, `pi`.

![graficos_y_matrices05](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_05.png)

En el `curve()` también podemos poner la tangente que es `tan`.

![graficos_y_matrices06](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_06.png)

![graficos_y_matrices07](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_07.png)

Podemos asignar valores a la secuencia y a la operación que queremos realizar y luego hacemos el gráfico pero en este caso sería `plot(y~x)`, pero en este caso con puntos.

![graficos_y_matrices08](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_08.png)

![graficos_y_matrices09](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_09.png)

Si ponemos `plot(y~x, type="l")` y nos pone una línea.

![graficos_y_matrices10](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_10.png)

![graficos_y_matrices11](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_11.png)

En los gráficos `p` equivale a puntos y `l` equivale a líneas, aunque por defecto nos coge `p`.

Para hacer que la fórmula aparezca en la gráfica ponemos `text(0.5,6,expression(formulamatematica))`.

![graficos_y_matrices12](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_12.png)

También podemos poner letras griegas si dentro de la expresión ponemos su nombre, por ejemplo, `alpha`, `beta`,...

![graficos_y_matrices13](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_13.png)

En el modelo de la reducción logística podemos ver algo como lo siguiente `curve(plogis, from=-3, to=3)`.

![graficos_y_matrices14](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_14.png)

![graficos_y_matrices15](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_15.png)

Si ponemos `?plotmath` podemos ver todas las funciones que pueden ponerse en un `plot`.

![graficos_y_matrices16](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_16.png)

![graficos_y_matrices17](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_17.png)

---

## **Matrices.**

Entre el data frame y las matrices hay una diferencia, el data frame se graba como una lista, no es atómico pero sus datos dentro del data frame pueden ser atómicos. Dentro de sus variables pueden meterse caracteres como números. Las matrices son atómicas.

Para hacer matrices utilizamos el comando `matrix(c(1,2,3),c(4,5,6),c(7,8,9))` o `matrix(1:9)`, en el segundo caso queda como una columna de nueve filas, para conseguir tres columnas ponemos `matrix(1:9, ncol=3)` y ya es una matriz de 3x3.

![graficos_y_matrices18](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_18.png)

![graficos_y_matrices19](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_19.png)

Todos los elementos de una matriz tiene que ser del mismo tipo, todos numéricos o todos caracteres.

![graficos_y_matrices20](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_20.png)

La matriz es un vector con ciertas características especiales, para verlo como filas y columnas.

Para ver la segunda fila se pone `matriz[2,]` y para ver la tercera columna se pone `matriz[,3]`.

![graficos_y_matrices21](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_21.png)

También podemos ver un elemento en concreto con `matriz[2,3]` y iría al elemento de la fila 2 y columna 3.

![graficos_y_matrices22](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_22.png)

También podemos poner una matriz sin una fila poniendo `matriz[-1,]` y nos quita la fila 1.

![graficos_y_matrices23](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_23.png)

Podemos hacer lo siguiente `apply(matriz,1,mean)` y esto nos hace a la matriz a por filas la media.

![graficos_y_matrices24](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_24.png)

A parte de las matrices también podemos hablar de arreglos, las matrices son vectores almacenados por columnas, para saber la estructura de una matriz ponemos `str(matriz)` y nos sale.

![graficos_y_matrices25](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_25.png)

Para saber los atributos de una matriz ponemos `attributes(matriz)` y nos sale un atributo dim con la dimensión.

![graficos_y_matrices26](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_26.png)

También poniendo `dim(matriz)` nos sale la dimensión de la matriz.

![graficos_y_matrices27](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_27.png)

---

## **Otros Gráficos.**

Cuando tenemos variables categóricas tenemos que hacer gráfico de barras y hay que utilizar el comando `barplot(table(datos$ojos))`.

Cuando tenemos variables numéricas tenemos que hacer un histograma y hay que utilizar el comando `hist(x)`.

Hemos visto el comando `plot()`, `text()`, `legend()`, `barplot()`, `boxplot()`.

El `plot()`, el `barplot()` y el `boxplot()` son ejemplos de lo que se conoce como comandos de gráficos de alto nivel, porque estos comandos crean gráficos.

El `text()` y el `legend()` modifican el gráfico actual para añadir una legenda, para añadir un texto o para una cosa similar.

Ahora vamos a hacer un gráfico de tres dimensiones.

Para esto utilizaremos la base de datos `mtcars`.

Lo primero que hacemos es el siguiente gráfico, `plot(mpg~wt, data=mtcars)`, con esto podemos ver la relación que hay entre las variables.

![graficos_y_matrices28](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_28.png)

![graficos_y_matrices29](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_29.png)

Ahora si hacemos `plot(mpg~hp, data=mtcars)` y veremos denuevo la relación que tienen las variables.

![graficos_y_matrices30](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_30.png)

![graficos_y_matrices31](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_31.png)

También podemos hacer lo siguiente `plot(mpg~cyl, data=mtcars)` y seguiriamos viendo una gráfico con la relación de variables.

![graficos_y_matrices32](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_32.png)

![graficos_y_matrices33](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_33.png)

Y también con la siguiente `plot(wt~cyl, data=mtcars)` se vería como en las otras la relación entre las variables.

![graficos_y_matrices34](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_34.png)

![graficos_y_matrices35](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_35.png)

Y con la siguiente `plot(wt~hp, data=mtcars)` se ve la relación entre variables.

![graficos_y_matrices36](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_36.png)

![graficos_y_matrices37](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_37.png)

Y con la siguiente `plot(hp~wt, data=mtcars)` se ve la relación entre variables.

![graficos_y_matrices38](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_38.png)

![graficos_y_matrices39](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_39.png)

Ahora vamos a hacer un gráfico de tres dimensiones utilizando `plot3d(mtcars$wt,mtcars$hp,mtcars$mpg)`.

![graficos_y_matrices40](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_40.png)

![graficos_y_matrices41](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_41.png)

Ahora crearemos la función f como `f=function(x,y) exp(-(x^2+y^2))`.

![graficos_y_matrices42](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_42.png)

Luego creamos x e y como se ve a continuación.

![graficos_y_matrices43](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_43.png)

![graficos_y_matrices44](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_44.png)

![graficos_y_matrices45](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_45.png)

Luego creamos z con respecto de los valores x e y, y también respecto la función f.

![graficos_y_matrices46](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_46.png)

El valor de z sería el siguiente.

![graficos_y_matrices47](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_47.png)

![graficos_y_matrices48](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_48.png)

Luego realizamos un gráfico en tres dimensiones con los datos anteriormente calculados y con el comando `persp3d(x,y,z, front="line", back="line")`.

![graficos_y_matrices49](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_49.png)

![graficos_y_matrices50](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_50.png)

Ahora hacemos otra gráfica para ver el contorno de la gráfica anterior para ello utilizamos `contour(x,y,z)`

![graficos_y_matrices51](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_51.png)

![graficos_y_matrices52](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_52.png)

También podemos utilizar el comando `image(x,y,z)` y se vería como a continuación.

![graficos_y_matrices53](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_53.png)

![graficos_y_matrices54](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_54.png)

También podemos hacer lo anterior pero cambiandole el color utilizando `image(x,y,z,col=terrain.colors(20))`.

![graficos_y_matrices55](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_55.png)

![graficos_y_matrices56](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_56.png)

También poniendo otro nombre de la asignacción nos coge otro tipo de colores `image(x,y,z,col=topo.colors(20))`.

![graficos_y_matrices57](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_57.png)

![graficos_y_matrices58](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_58.png)

También podemos hacer gráficos con elipses como se ve `ploted(ellipse3d(diag(3)))`.

![graficos_y_matrices59](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_59.png)

![graficos_y_matrices60](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_60.png)

Ahora volveremos a hacer un gráfico con elipses con el comando `ploted(ellipse3d(diag(3)),front="line",back="line")`.

![graficos_y_matrices61](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_61.png)

![graficos_y_matrices62](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_62.png)

Ahora haremos otra gráfico diferente con el comando `ts.plot(BJsales)`.

![graficos_y_matrices63](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_63.png)

![graficos_y_matrices64](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_64.png)

Lo volvemos a hacer pero con otra variable.

![graficos_y_matrices65](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_65.png)

![graficos_y_matrices66](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_66.png)

Esta variable anteriormente utilizada `AirPassengers` son los pasajeros que se han tenido cada mes de los distintos años que salen en la tabla.

![graficos_y_matrices67](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_67.png)

Creamos una variable respecto la variable anteriormente nombrada.

![graficos_y_matrices68](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_68.png)

Hacemos una predicción en los próximos 12 meses con respecto al modelo que se creo.

![graficos_y_matrices69](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_69.png)

Hacemos un gráfico con la predicción de esos 12 meses.

![graficos_y_matrices70](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_70.png)

![graficos_y_matrices71](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_71.png)

A continuación se puede ver los parametros para poder hacer la predicción.

![graficos_y_matrices72](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_72.png)

![graficos_y_matrices73](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_73.png)

Volvemos a hacer un `plot(mtcars$wt)`.

![graficos_y_matrices74](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_74.png)

![graficos_y_matrices75](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_75.png)

Ahora hacemos `ts.plot(mtcars$wt)`.

![graficos_y_matrices76](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_76.png)

![graficos_y_matrices77](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_77.png)

Ahora cogemos una variable con una secuencia `x=seq(0,2,length=21)`.

![graficos_y_matrices78](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_78.png)

Ahora creamos otra variables `y1`,`y2` e `y3`, y luego hacemos una combinación de todas ellas en la variable y.

![graficos_y_matrices79](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_79.png)

Con todo esto utilizamos el comando `matplot(x,y,type="l")`, y nos crea una gráfica con las tres variables creada anteriormente que se combinaron en y.

![graficos_y_matrices80](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_80.png)

![graficos_y_matrices81](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_81.png)

Ahora le ponemos una leyenda y nos aparecera en la gráfica.

![graficos_y_matrices82](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_82.png)

![graficos_y_matrices83](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_83.png)

A continuación se puede ver un ejemplo más completo de las gráficas en tres dimensiones.

![graficos_y_matrices84](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_84.png)

![graficos_y_matrices85](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_85.png)

![graficos_y_matrices86](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_86.png)

![graficos_y_matrices87](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_87.png)

![graficos_y_matrices88](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_88.png)

![graficos_y_matrices89](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_89.png)

![graficos_y_matrices90](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_90.png)

![graficos_y_matrices91](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_91.png)

![graficos_y_matrices92](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_92.png)

![graficos_y_matrices93](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_93.png)

![graficos_y_matrices94](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_94.png)

![graficos_y_matrices95](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_95.png)

![graficos_y_matrices96](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_96.png)

![graficos_y_matrices97](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_97.png)

![graficos_y_matrices98](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_98.png)

![graficos_y_matrices99](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_99.png)

## **Detalles De Los Gráficos.**

Ahora vamos a ver como hacer pequeños cambios a los gráficos.

Lo que hacemos es lo siguiente `plot(mpg~wt, data=mtcars)`. En este gráfico podemos ver la relación que existen entre las dos variables.

![graficos_y_matrices100](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_100.png)

![graficos_y_matrices101](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_101.png)

Ahora haremos lo siguiente `plot(mpg~wt, data=mtcars, xlab="Peso", ylab="Millas Por Galon", main="Eficiencia", sub="Datos")`, y esto serían las etiquetas para cada eje, un título y un subtitulo.

![graficos_y_matrices102](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_102.png)

![graficos_y_matrices103](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_103.png)

Otro data frame que hay en R es `names(iris)` o `View(iris)` para ver el contenido.

![graficos_y_matrices104](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_104.png)

![graficos_y_matrices105](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_105.png)

![graficos_y_matrices106](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_106.png)

Creamos otro gráfico como el siguiente `plot(Sepal.Length~Sepal.Width, data=iris)` aqui se ve la relación entre las dos variables.

![graficos_y_matrices107](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_107.png)

![graficos_y_matrices108](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_108.png)

`plot(Sepal.Length~Sepal.Width, data=iris, col=Species)` esto pone un color distinto para cada especie.

![graficos_y_matrices109](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_109.png)

![graficos_y_matrices110](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_110.png)

`plot(Sepal.Length~Sepal.Width, data=iris, col=Species, pch=as.numeric(Species))` también ponemos ponerle el segun la diferencia de caracteres una forma distinta con el que trabajamos en el gráfico, `pch` no acepta factores y entonces hacemos lo anterior. Al ponerle `as.numeric` cambia el nombre de la especie por un número.

![graficos_y_matrices111](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_111.png)

![graficos_y_matrices112](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_112.png)

Ponemos `?points` y nos saldrá la ayuda para saber los puntos distintos que hay para poner en los `plots` y sobre el `pch`.

![graficos_y_matrices113](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_113.png)

![graficos_y_matrices114](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_114.png)

Si ponemos `legend` despues del `plot` como `legend("topleft", levels(iris$Species), col=1:3, pch=1:3)` nos pone como legenda.

![graficos_y_matrices115](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_115.png)

![graficos_y_matrices116](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_116.png)

Para resumir el nombre de las especies en la legenda ponemos
`plot(Sepal.Length~Sepal.Width, data=iris, col=Species, pch=c("s","v","i")[as.numeric(Species)])
legend("topleft", levels(iris$Species), col=1:3, pch=c("s","v","i"))` y nos cambia la simbologia por lo que pusimos, es decir, s,v e y.

![graficos_y_matrices117](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_117.png)

![graficos_y_matrices118](./img/5-Gráficos_Y_Matrices/graficos_y_matrices_118.png)

---
