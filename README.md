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

2do juego: Los jugadores deberan pasar por la mano por su sensor correspondiente antes que el otro, el primero que la pase suma un punto.

Ambos juegos suman puntos en simultaneo, el ganador sigue siendo el que sume 7 puntos.


(Codigo para los sensores y el juego EJEMPLOOO no trabajo hecho)

const int sensor1Pin = 2;
const int sensor2Pin = 3;
const int led1Pin = 8;
const int led2Pin = 9;

bool jugadorDetectado = false;

void setup() {
  pinMode(sensor1Pin, INPUT);
  pinMode(sensor2Pin, INPUT);
  pinMode(led1Pin, OUTPUT);
  pinMode(led2Pin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  if (!jugadorDetectado) {
    int sensor1 = digitalRead(sensor1Pin);
    int sensor2 = digitalRead(sensor2Pin);

    if (sensor1 == LOW) { // Dependiendo del sensor, puede ser HIGH
      digitalWrite(led1Pin, HIGH);
      Serial.println("Jugador 1 ganó");
      jugadorDetectado = true;
    } else if (sensor2 == LOW) {
      digitalWrite(led2Pin, HIGH);
      Serial.println("Jugador 2 ganó");
      jugadorDetectado = true;
    }
  }
}

