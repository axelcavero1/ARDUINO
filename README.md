# ARDUINO

Tinkercad:
https://www.tinkercad.com/things/07CY5AX1Ngz-proyecto-arduino?sharecode=TpGmJWSHoRdmQQ2pgBoHO29OGomGjqp_Y6MmpIXI8Fw

Mateo Navarro 
Jonathan Ramirez
Axel Cavero
Brandon Moreyra

https://docs.google.com/document/d/1ndyrVWjGHlbHIExOg-Xm_yNVXN0F79GH_tmiTj2Szf4/edit?usp=sharing

Juego de Reflejos con Semáforo y Puntaje
Descripción:
Juego donde el jugador debe presionar un botón cuando un LED verde se enciende. Se usa temporizador para encendido aleatorio y cuenta aciertos.
Entradas: botón
Salidas: LEDs de colores, buzzer
Contador de flancos: presiones correctas
Tiempo: millis() para mostrar luces aleatoriamente
Estados: ESPERA, MOSTRAR LUZ, EVALUAR, PUNTAJE

Se puede utilizar esta idea jugando de a 2 jugadores, agregamos mas LEDs y un boton mas, dividimos las lineas del buzzer entre los aciertos del Jugador 1 y el Jugador 2
El que llega a 5 ciertos ganaria y se imprime el ganador.
Para iniciar el juego el loop al inicio solicita que ambos jugadores presionen el boton asi no se repite infinitamente el juego. Al finalizar podemos hacer un delay grande
que evite el reinicio instantaneo del juego.

Agregando un juego mas segun profes: Los jugadores, por turnos, deben ingresar un codigo en el pinpad donde tienen un tiempo regresivo para ingresarlo en caso de no ingresarlo se le suma punto al jugador contrario. 

Ambos juegos suman puntos en simultaneo, el ganador sigue siendo el que sume 7 puntos.
