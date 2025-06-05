# ARDUINO

Tinkercad:
https://www.tinkercad.com/things/07CY5AX1Ngz-proyecto-arduino?sharecode=TpGmJWSHoRdmQQ2pgBoHO29OGomGjqp_Y6MmpIXI8Fw

Mateo Navarro 
Jonathan Ramirez
Axel Cavero
Brandon Moreyra

https://docs.google.com/document/d/1ndyrVWjGHlbHIExOg-Xm_yNVXN0F79GH_tmiTj2Szf4/edit?usp=sharing

Juego de Reflejos con LEDs y Puntaje
Descripción:
Juego donde el jugador debe activar un sensor cuando un LED verde se enciende para acumular más puntos que el otro jugador. Se usa temporizador para encendido aleatorios. Contará con un potenciometro que será usado para variar la frecuencia en la que los LEDs se encenderán. Al terminar, deberá anunciar al ganador del juego y preguntar si se desea jugar otra vez, para reiniciar el juego ambos sensores deben ser activados en simultaneo.
Entradas: dos sensores.
Salidas: LEDs de colores, buzzer.
Contador de flancos: presiones correctas.
Tiempo: millis() para mostrar luces aleatoriamente.
Estados: ESPERA, MOSTRAR LUZ, EVALUAR, PUNTAJE.

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

