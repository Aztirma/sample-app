**Alumna: Zuñiga Chicaña, Alejandra Aztirma Código: 20202142E**

**PREGUNTA 2**

Para la pregunta 2, se procedió a reutilizar el código del TicTacToe.

Requisito1: colocación de piezas

Requisito2: agregar soporte para dos jugadores

Requisito3: agregar condiciones ganadores

Requisito4: condiciones de empate

**Requisito 1: colocación de piezas**

**Prueba: límites del tablero I**

Todo lo que tenemos que hacer es crear el método jugar y asegurarnos de que arroja RuntimeException
cuando el argumento x es menor que 1 o mayor que 3 (el tablero es 3x3).

*Debes ejecutar esta prueba tres veces. La primera vez, debería fallar porque el método jugar no existe.*
![1](https://github.com/Aztirma/sample-app/assets/89436252/6955d6b3-8419-4323-90e0-f5d7f14b3971)

<a name="br2"></a>*Una vez que se agrega, debería fallar porque no se lanza RuntimeException.*

*La tercera vez, debería tener éxito porque el código que corresponde a esta prueba está completamente
implementado.*

**Prueba: límite de tablero II**




<a name="br3"></a>Realiza la implementación de esta especificación es casi la misma que la anterior.

**Prueba: lugar ocupado**

Una vez establecidos los límites del tablero, ahora solo falta asegurar de que se pongan en lugares
desocupados, se creó la prueba para esto y se complementó el método Jugar.

Se tiene esta salida debido a que aún no se complementó el método jugar, se procede a
complementar y ahora si la prueba pasa.



<a name="br4"></a>Prueba pasada una vez se implementa el código

Ahora nos pide Refactorizar el método Jugar, esto para que se tenga un mejor entendimiento del
código

**Requisito 2: agregar soporte para dos jugadores**

El siguiente requisito se dividió en estas 3 pruebas:

\- El primer turno lo debe jugar el jugador X.

\- Si el último turno fue jugado por X, entonces el próximo turno debe ser jugado por O



<a name="br5"></a>- Si el último turno fue jugado por O, entonces el próximo turno debe ser jugado por X

Procederemos a escribir las pruebas, antes que la implementación del método, en este caso el
método getTurn();

**Prueba – X juega primero**

Se creó la prueba para que el método proximoJugador devuelva X. Pero al pasar ejecutarlo se ve
que no se compila puesto que aún no se creó dicho método.

Se implementó el método ProximoJugador, el cual devuelve el turno inicial, en este caso X. Esta
implementación inicial solo cumple con la primera prueba. En las pruebas posteriores, refinaremos
este código para determinar correctamente qué jugador debe jugar a continuación.

Ahora si una vez creado nuestro método nuestra prueba pasa.

**Prueba: O juego justo después de X**

Como hemos estado haciendo, primero se implemento la prueba, por ende, la prueba falló ya que
no se implemento el método jugar




<a name="br6"></a>El método jugar ya existe, pero falta las condiciones necesarias para que pueda pasar la prueba

**Prueba: X juega justo después de O**

No se implementó nada al método ProximoJugador y aun así la prueba ha pasado, como se sugirió
se desechará esta prueba, pero de todos modos aquí se deja una captura de la prueba.

**Requisito 3: agregar condiciones ganadoras
Prueba: por defecto no hay ganador**

En esta prueba, se crea una instancia de TicTacToe y se llama al método jugar() con una posición
válida en el tablero (en este caso, la posición (1, 1)). Luego se verifica que el resultado del método
jugar() sea false, lo cual indica que no hay ganador.




<a name="br7"></a>**Prueba – condición ganadora I**

Se realizó la implementación del método jugar y de esta manera se procedió a hacer la prueba
respectiva para verificar esta condición.

Nuevamente se procedió a refactorizar el método Jugar, para poder realizar los siguientes casos
sobre las condiciones ganadoras.




<a name="br8"></a>En esta refactorización, se creó un método separado llamado hayGanador() que se encarga de
verificar si hay un ganador en las líneas horizontales. El método jugar() ahora simplemente llama a
hayGanador() y retorna el resultado.

**Prueba – condición ganadora II**

Esta implementación es similar a la anterior

También se implementó el método hayGanador() para verificar la ganancia vertical:




<a name="br9"></a>**Prueba – condición ganador** III

La prueba "ganarDiagonalSuperiorIzquierdaInferiorDerecha" verifica si el juego detecta
correctamente una ganancia en la línea diagonal superior izquierda a inferior derecha.

Por otro lado se tuvo que implementar nuevamente el método hayGanador(), se verifica tanto la
ganancia en líneas horizontales, verticales y diagonales, asegurando que todas las condiciones
ganadoras estén cubiertas.

**Prueba – condición ganadora IV**



<a name="br10"></a> Finalmente, existe la última condición ganadora posible para abordar: El jugador gana cuando se
forma la diagonal desde la parte inferior izquierda hasta la parte superior derecha

Con esta implementación, se verifican todas las condiciones ganadoras posibles, incluyendo las
líneas diagonales desde la parte inferior izquierda hasta la parte superior derecha.

**Refactorización**




<a name="br11"></a>En esta refactorización, el bucle existente condiciones adicionales para verificar las dos diagonales.
Esto reutiliza el bucle existente y evita la duplicación de código.

**Requisito 4: condiciones de empate**

Se creó por ultima la prueba para el caso de empate, en este caso la prueba no funciona debido a
que no se implementó aún el método hayEmpate()




<a name="br12"></a>Se implementó el método hayEmpate para que así la prueba anteriormente mencionada pueda
pasar.

Una vez implementado, la prueba paso.

Por último, nos piden nuevamente un refactorización usando un método llamado esGanador() a
pesar de que no esté al alcance la última prueba.




<a name="br13"></a>Con esta refactorización, se mejora la claridad y legibilidad del código al separar las
responsabilidades de verificación de empate y ganador en métodos individuales. Esto facilita el
mantenimiento y comprensión del código,

