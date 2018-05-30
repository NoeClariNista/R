___

# **Vectores, Listas Y Data Frame.**

---

## **Vectores Y Listas.**

La variable que graba varios números es un vector.

Para grabar varios números utilizamos el comando `c` (combine) y los separamos por comas, por ejemplo, `a=c(5,4,3)`.

![vectores_listas_y_data.frame_01](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_01.png)

Para la zona decimal se separa con el punto.

![vectores_listas_y_data.frame_02](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_02.png)

Podemos hacer combinaciones de los dos anteriores.

![vectores_listas_y_data.frame_03](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_03.png)

`c` siempre es para combinar varios datos y no sirve para uno solo.

Si miramos el modo de cualquiera de estas tres variables tiene que darnos numérico.

![vectores_listas_y_data.frame_04](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_04.png)

Para ver la longitud de los vectores utilizamos el comando `length(nombredevariable)`.

![vectores_listas_y_data.frame_05](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_05.png)

Un vector puede ser creado con datos de carácter y como son caracteres tienen que ir entre comillas dobles.

![vectores_listas_y_data.frame_06](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_06.png)

Si vemos el modo de esta variable nos tiene que darnos carácter.

![vectores_listas_y_data.frame_07](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_07.png)

Estos vectores son vectores de tipo atómico, esto quiere decir que si los vectores tienen el mismo tipo de datos en su interior, esto es que en su interior o todos son numéricos o todos son caracteres.

Para comprobar si es atómico un vector utilizamos `is.atomic(nombredevariable)` y nos devuelve TRUE o FALSE.

![vectores_listas_y_data.frame_08](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_08.png)

Podemos probar a hacer todo lo anterior mezclando caracteres y números.

![vectores_listas_y_data.frame_09](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_09.png)

Como vemos si en un vector se mezclan números con caracteres se convierten todos en caracteres.

![vectores_listas_y_data.frame_10](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_10.png)

Y esto sigue siendo atómico.

![vectores_listas_y_data.frame_11](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_11.png)

Si queremos mezclar números con caracteres debemos utilizar la lista, por ejemplo, `x=list("hola",9,"mundo")`, entonces esto nos hará una lista de tres elementos, manteniendo su tipo.

![vectores_listas_y_data.frame_12](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_12.png)

Podemos ver que este vector ya no es atómico.

![vectores_listas_y_data.frame_13](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_13.png)

Se puede crear una variable `y=list(c(3,4,5),c("hola","mundo","adios"),c(7,8,9))` la cual es una lista con tres vectores.

![vectores_listas_y_data.frame_14](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_14.png)

Podemos estudiar también cada elemento de la lista, los cuales son atómicos aunque en si la lista no es atómica, para ello ponemos, por ejemplo, `is.atomic(y[[1]])`.

![vectores_listas_y_data.frame_15](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_15.png)

Si ponemos `a[1]` o `a[2]` o `a[3]` nos nombrara el dato del vector a en la posición 1 o en la posición o en la posición 3, ya que el corchete accede a elementos del vector.

![vectores_listas_y_data.frame_16](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_16.png)

El doble corchete accede a elementos de la lista.

![vectores_listas_y_data.frame_17](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_17.png)

Si queremos ver varios elementos del vector utilizamos `a[c(1,3)]` y nos devuelve los datos de las posiciones 1 y 3, el vector dentro de la lista indica posiciones dentro del vector.

![vectores_listas_y_data.frame_18](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_18.png)

Si queremos todos los elementos menos uno utilizamos `a[-2]`, nos devuelve todos menos el valor de esa posición.

![vectores_listas_y_data.frame_19](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_19.png)

También puede ser `a[-c(1,3)]` y nos devuelve la posición 2.

![vectores_listas_y_data.frame_20](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_20.png)

Si ponemos `a[1,3]` nos dar aun error porque esto es para matrices.

![vectores_listas_y_data.frame_21](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_21.png)

También podemos hacer condiciones como, por ejemplo, `a[a>3]`, es decir, poner una condición para hacer la búsqueda.

![vectores_listas_y_data.frame_22](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_22.png)

Podemos hacer que los nombres de una variable se le asignen otra variable como, por ejemplo, `names(a)=e`, esto le da un nombre a cada posición, donde `a` es un vector numérico y `e` es un vector de caracteres.

![vectores_listas_y_data.frame_23](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_23.png)

La función `names` solo se utiliza con vectores de misma longitud. Pero en caso de que no sean iguales se pone NA en el lugar del dato vacío.

Si volvemos a poner la condición `a[a>3]` nos saldrán con sus respectivos nombres.

![vectores_listas_y_data.frame_24](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_24.png)

Para sacar la suma de un vector tenemos que poner `sum(nombredevariable)`. Este comando funciona igual que el sumatorio.

![vectores_listas_y_data.frame_25](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_25.png)

Para calcular el promedio o media utilizamos `mean(nombredevariable)` y esto se hace sobre un vector.

![vectores_listas_y_data.frame_26](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_26.png)

La formula de la media es la siguiente.

![vectores_listas_y_data.frame_27](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_27.png)

Para calcular la varianza de un vector utilizamos `var(nombredevariable)`.

![vectores_listas_y_data.frame_28](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_28.png)

La formula de la varianza es la siguiente.

![vectores_listas_y_data.frame_29](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_29.png)

Las siguientes son la misma, es decir, son la varianza, `var(nombredevariable)` y `sum((nombredevariable-mean(nombredevariable))^2)/(length(nombredevariable)-1)`.

![vectores_listas_y_data.frame_30](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_30.png)

Para calcular la desviación típica de un vector utilizamos `sd(nombredevariable)`.

![vectores_listas_y_data.frame_31](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_31.png)

La formula de la desviación típica es la siguiente.

![vectores_listas_y_data.frame_32](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_32.png)

Para calcular la raíz cuadrada utilizamos `sqrt(nombredevariable)`.

![vectores_listas_y_data.frame_33](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_33.png)

Para calcular la desviación típica también podemos hacerlo de otra forma con `sqrt(var(nombredevariable))`.

![vectores_listas_y_data.frame_34](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_34.png)

Para calcular la mediana de un vector utilizamos `median(nombredevariable)`.

![vectores_listas_y_data.frame_35](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_35.png)

Para cualquier es el valor máximo o el valor mínimo de un vector utilizamos `max(nombredevariable)` o `min(nombredevariable)`.

![vectores_listas_y_data.frame_36](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_36.png)

Para calcular el producto de un vector utilizamos `prod(nombredevariable)`.

![vectores_listas_y_data.frame_37](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_37.png)

Para calcular la suma acumulada utilizamos `cumsum(nombredevariable)`, es decir, acumulando los valores anteriores.

![vectores_listas_y_data.frame_38](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_38.png)

También podemos calcular el producto acumulado para ello utilizamos `cumprod(nombredevariable)`.

![vectores_listas_y_data.frame_39](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_39.png)

Para hacer operaciones con vectores podemos hacer lo siguiente `y=z*a` y nos devuelve otro vector con el producto entre cada elemento.

![vectores_listas_y_data.frame_40](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_40.png)

Lo anterior también ocurre con la suma, la resta, la división, la división entera y el módulo.

![vectores_listas_y_data.frame_41](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_41.png)

Si hacemos una suma de un vector y una constante, sumará dicho valor a todos los elementos del vector.

![vectores_listas_y_data.frame_42](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_42.png)

Si ponemos un vector de un tamaño distinto y hacemos una operación entre este y otro vector lo que ocurre es que el vector de tamaño distinto se repite, el vector se recicla, el de menor tamaño. Pero este vector, el de menor tamaño, tiene que ser múltiplo del vector grande, hará el cálculo pero nos da un aviso de error.

![vectores_listas_y_data.frame_43](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_43.png)

Se pueden compilar las operaciones, por ejemplo, `y=z*a+z-c(10,20)`.

![vectores_listas_y_data.frame_44](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_44.png)

Para ordenar el vector de menor a mayor lo podemos hacer con el comando `sort(nombredevariable)`.

![vectores_listas_y_data.frame_45](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_45.png)

Si queremos ordenar el vector de mayor a menor utilizamos decreasing de la siguiente forma `sort(nombredevariable, decreasing=TRUE)` ya que por defecto es FALSE.

![vectores_listas_y_data.frame_46](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_46.png)

Si queremos ordenar un vector con respecto a otro vector utilizamos `order(nombredevariable)`.

![vectores_listas_y_data.frame_47](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_47.png)

Si grabamos lo anterior en una variable y hacemos `a[j]` nos sale ordenado. También podemos utilizarlo para ordenar otra variable, como por ejemplo, `e[j]` o `e[order(a)]` y esto nos daría lo mismo, con esto podemos ver como podemos meter en una variable una orden que utilicemos mucho.

![vectores_listas_y_data.frame_48](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_48.png)

También podemos hacer `order(nombredevariable, decreasing=TRUE)`.

![vectores_listas_y_data.frame_49](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_49.png)

Para hacer un vector con varios números consecutivos podemos utilizar `z=1:3` y nos de la secuencia del número 1 al número 3.

![vectores_listas_y_data.frame_50](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_50.png)

Se crea un vector si ponemos `1:5` pero también poniendo 5:1, la diferencia que uno es creciente y el otro es decreciente.

![vectores_listas_y_data.frame_51](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_51.png)

Para hacer secuencias más elaboradas como, por ejemplo, `seq(1,5,by=0.2)` y va de 1 a 5 de 0.2 en 0.2.

![vectores_listas_y_data.frame_52](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_52.png)

También se puede hacer para que tenga una longitud para ello ponemos `seq(1, 5, length=20)`.

![vectores_listas_y_data.frame_53](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_53.png)

Esto sirve para gráficos de funciones, es una secuencia regular y tiene espacio igual.

---

## **Data Frame.**

El data frame es una tabla de datos en la cual se permite incluir diferentes variables con los mismos individuos. En el data frame se exige que los vectores sean del mismo tamaño. El data frame es una tabla de datos, base de datos de memoria.

Creamos un data frame de la siguiente forma `datos=data.frame(estatura=c(1.78,1.70,1.72,1.76), peso=c(70,64,80,78), row.names=c("tierra","fuego","aire","agua")` donde `row.names` son los nombres de las filas.

![vectores_listas_y_data.frame_54](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_54.png)

Si el vector no es de la misma longitud que los demás vectores este se recicla hasta que sea de la misma longitud. Los elementos de dentro de la variable no son variables y si queremos verlas podemos afirmar que no existen.

![vectores_listas_y_data.frame_55](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_55.png)

Se puede hacer suma, es decir, `sum(datos)` con la variable data frame.

![vectores_listas_y_data.frame_56](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_56.png)

También podemos hacer `summary(datos)` y nos salen varias operaciones, el mínimo, el primer cuartil, la mediana, la media, el tercer cuartil y el máximo, pero de los elementos de la variable por separado.

![vectores_listas_y_data.frame_57](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_57.png)

Si alguno de los datos introducidos anteriormente no existe tendríamos que poner NA, no disponible, sin comillas. Al hacer operaciones es como si no hubiera este dato.

![vectores_listas_y_data.frame_58](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_58.png)

Lo anterior es como una matriz, si queremos cambiar un dato podemos hacerlo poniendo `datos$peso[3]=80` esto es porque `datos$peso` es un vector de todos esos datos.

![vectores_listas_y_data.frame_59](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_59.png)

También podemos poner `datos[3,2]=80`, con esto quiere decir fila tres columna dos.

![vectores_listas_y_data.frame_60](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_60.png)

Lo anterior no es atómico y se guarda en una lista, pero dentro de la lista son elementos atómicos.

![vectores_listas_y_data.frame_61](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_61.png)

Si hacemos `mean(datos)` nos hace la media de cada columna por separado.

![vectores_listas_y_data.frame_62](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_62.png)

Lo anterior también pasa por la varianza pero algo distinto, nos hace la varianza de cada columna pero también nos hace la covarianza.

![vectores_listas_y_data.frame_63](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_63.png)

La covarianza es un número y es la relación entre los elementos de cada columna. La covarianza depende de la varianza.

![vectores_listas_y_data.frame_64](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_64.png)

También podemos hacer la correlación con el comando `cor(datos)` y el resultado es la matriz de correlación.

![vectores_listas_y_data.frame_65](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_65.png)

La correlación es un número entre -1 y +1. Si la correlación es cero es que no hay una relación lineal entre las variables. Puede haber una relación cuadrática si la correlación es cero. Cuanto más cerca de uno hay una relación más fuerte entre las variables. La correlación con la misma variable es siempre uno.

La suma, el mínimo, el máximo y el producto nos lo hace de todos los elementos del data frame y solo nos saldrá un resultado.

![vectores_listas_y_data.frame_66](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_66.png)

Para que nos haga las operaciones por columnas podemos utilizar el comando `apply(datos, 2, sum)`, esto quiere decir aplicar a datos por columnas la función suma. El 1 es para filas y el 2 para columnas. Y al final nos saldría por columnas. También podemos hacerlo con el mínimo, el máximo y el producto.

![vectores_listas_y_data.frame_67](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_67.png)

El comando apply se utiliza para cualquier matricial.

Para listas, para cualquier tipo de lista, se puede utilizar el comando `sapply(datos, min)` y nos daría el mismo resultado pero para hacerlo con listas.

![vectores_listas_y_data.frame_68](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_68.png)

Data frame luce como una matriz por eso se pueden utilizar ambos comandos.

Hay otro tipo de variables, variable categórica. Las variables categóricas pueden representarse como variables numéricas pero se identifican como categóricas. Este tipo de variable se les llamas factores.

Por ejemplo, `x=factor(c(1,3,2,4,1,2,4,3), labels=c("verde","azul","rojo","amarillo"))` este factor se guarda como numérico pero al salir por pantalla sin comillas y son valores de las variables, les da un nivel a las variables. El labels es para asignar a las variables los valores, también se dice etiqueta.

![vectores_listas_y_data.frame_69](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_69.png)

El factor se guarda como numérico pero le agrega ciertos tributos a la variable y sale por pantalla el nombre de sus etiquetas.

![vectores_listas_y_data.frame_70](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_70.png)

Mejor es crearlo como numérico y decir que significa cada número después. Si intentamos hacer operaciones nos saldrá un error, ya que es un factor.

![vectores_listas_y_data.frame_71](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_71.png)

Sí podríamos hacer `summary(x)` y nos cuenta cuántos son de cada nivel.

![vectores_listas_y_data.frame_72](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_72.png)

`table(x)=summary(x)` esto es la tabla de frecuencias absolutas.

![vectores_listas_y_data.frame_73](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_73.png)

Para hacer un gráfico utilizamos `plot(x)` y nos hace un gráfico de barras.

![vectores_listas_y_data.frame_74](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_74.png)

![vectores_listas_y_data.frame_75](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_75.png)

También podemos hacer `plot(datos$peso)` y como es una variable numérica la gráfica que nos da es en una gráfica numérica.

![vectores_listas_y_data.frame_76](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_76.png)

![vectores_listas_y_data.frame_77](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_77.png)

Si hacemos `plot(peso~estatura, data=datos)` esto nos sale un gráfico enfrentando dos variables (~ es versus) de la variable datos.

![vectores_listas_y_data.frame_78](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_78.png)

![vectores_listas_y_data.frame_79](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_79.png)

Para agregar un factor al data frame, otra columna, para ello ponemos `datos$provincia=factor(c(1,2,2,3), labels=c("Isla","Península","Continente"))` y nos crea una nueva variable que es un factor.

![vectores_listas_y_data.frame_80](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_80.png)

Si hacemos un `plot(peso~provincia, data=datos)` nos hace un diagrama de cajas.

![vectores_listas_y_data.frame_81](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_81.png)

![vectores_listas_y_data.frame_82](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_82.png)

Cuando ponemos una variable numérica versus una variable categórica es un diagrama de cajas por cada nivel de la variable categórica.

El `summary(datos)` nos da las operaciones del mínimo, el primer cuartil, la mediana, el tercer cuartil y el máximo y esta formado por los datos que nos da `summary(datos)`.

![vectores_listas_y_data.frame_83](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_83.png)

Para poner nuevos datos podemos hacer `datos[5,]=c(1.85, 80, "todo")`.

![vectores_listas_y_data.frame_84](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_84.png)

Por defecto pone el nombre 5 para cambiarlo ponemos `row.names(datos)[5]="otro"` y ya tendríamos una nueva fila.

![vectores_listas_y_data.frame_85](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_85.png)

Se cambio a carácter porque al añadir un nuevo valor carácter se pusieron los valores numéricos como caracteres, entonces hacemos lo siguiente y lo solucionaremos.

![vectores_listas_y_data.frame_86](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_86.png)

Para cambiar el modo de un vector o de lo que sea podemos utilizar `mode(datos$estatura)="numeric"` y `mode(datos$peso)="numeric"`.

![vectores_listas_y_data.frame_87](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_87.png)

El comando `str(datos)` permite ver la estructura de esa variable, es decir, un resumen.

![vectores_listas_y_data.frame_88](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_88.png)

Para quitar una fila podemos poner `datos=datos[-5,]`.

![vectores_listas_y_data.frame_89](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_89.png)

En el caso de que una nueva fila tenga números y caracteres en vez de `c()` es mejor poner `list()`. En vez de `datos[5,]` podemos poner un nombre entre comillas dobles.

![vectores_listas_y_data.frame_90](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_90.png)

Para un diagrama de cajas solo con una variable utilizamos el comando `boxplot(datos$peso)`.

![vectores_listas_y_data.frame_91](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_91.png)

![vectores_listas_y_data.frame_92](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_92.png)

Si solo quiero ver los nombres de las columnas ponemos `names(datos)`, esto solo funciona en los data frame.

![vectores_listas_y_data.frame_93](./img/4-Vectores_Listas_Y_Data.Frame/vectores_listas_y_data.frame_93.png)

Esto es así porque el data frame es una lista.

En las matrices si queremos ver el nombre de las columnas ponemos `conex(nombredematriz)` para ver los nombres de las columnas.

---
