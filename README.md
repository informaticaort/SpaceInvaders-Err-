# SpaceIvaders-Err-



****** Movimiento del jugador

Cuando empezamos el juego vemos que nuestra nave no se mueve.
Esto pasa porque el código que se encarga de mover la nave está comentado.
Para modificar este estado, vamos a sacar los comentarios de las líneas 383 y 389


Una vez que se mueve nuestra nave esta lo hace de izquierda a derecha y viceversa.
Pero para la izquierda se mueve más rápido que para la derecha. Esto es porque en el código
los valores absolutos de los movimientos son diferentes.
Vamos a cambiar el valor -9 por el valor -3, para que se mueva más lento a la izquierda.
Y también vamos a modificar el valor de movimiento hacia la derecha, modificando el número
6 por 3.


**** Disparos del jugador

Cuando empezamos el juego vemos que nuestra nave no dispara.
Esto pasa porque el código que se encarga de disparar está comentado.
Para modificar este estado, vamos a sacar los comentarios de las líneas 390, 391 y 392


***** Acumular puntos

Se supone que al disparar y eliminar aliens, tenemos que acumular puntos.
De hecho, al inicio del juego vemos en la pantalla cuántos puntos deberíamos recibir por cada
tipo de alien que hay en el juego.
Si revisamos nuetro código, veremos que tenemos una función que se encarga de acumular puntos.
Esta se encuentra aproximadamente en la línea 943 de nuestro código. 
Tiene el siguiente encabezado: Ship.prototype.killScore = function() 
El alien llamado "Grunt" debería devolver (return) 10 puntos.
El alien llamado "Soldier" debería devolver (return) 20 puntos.
El alien llamado "Invader" debería devolver (return) 40 puntos.


**** Perdida de VIDAS

Cuando iniciamos el juego, observamos que tenemos 3 vidas disponibles.
Pero ni bien recibimos el primer impacto por parte del enemigo, notamos que de las 3 vidas
que teníamos disponibles, bajamos a cero.
Esto sucede porque en el código, la función que se encarga de restar vidas tiene mal el 
proceso matemático de la resta.
Si vemos en la línea 841,

	  this.game.defenderLives -= 3;

ahí tenemos la resta de las vidas disponibles, modifiquemos ese número 3 para
reemplazarlo por el número 1.



----- Volumen del juego

El juego tiene efectos de sonidos, pero podemos observar que por más que presionemos el botón
de muteo nunca tenemos sonido.
Esto es algo que vamos a tener que modificar en el código del juego.
Si hacemos Control+F, y buscamos la palabra volume en el archivo bundle.js,
observamos que en la línea 896, el volumen del juego está el cero.
Modifiquemos este valor con valores entre 0.1 y 1 para darle volumen al sonido.


