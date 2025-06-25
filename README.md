# ARDUINO

Tinkercad:
https://www.tinkercad.com/things/1pzeWYt4E1A-tp-arduino-falta-pantalla

Mateo Navarro 
Jonathan Ramirez
Axel Cavero
Brandon Moreyra

Juego de Reflejos con LEDs y Puntaje
Descripción:
Juego donde competiran dos jugadores presionando un boton en el instante que se prenda el LED correcto, entre 3 que se encienden aleatoriamente, 
el jugador que presione primero el boton sumara puntos unicamente. El primero en llegar a 2 gana el juego.
Entradas: dos botones.
Salidas: LEDs de colores, pantalla LCD I2C.
Contador de flancos: presiones correctas.
Tiempo: millis() para mostrar luces aleatoriamente.
Estados: ESPERA, MOSTRAR LUZ, EVALUAR, PUNTAJE.
