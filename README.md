# Practica-DHT22
Se realizo la primera practica con el simulador wokwi, de como podemos programar una ``ESP32`` 

# Introduccion
### Descripcion
Se realizo la simulacion y programacion utilizando un sensor ``DHT22`` que nos muestra la temperatura y humedad del entorno.

# Materiales
- WOKWI
- Tarjeta ``ESP32``
- Sensor ``DHT22``
- Librerias dentro del simulador que son: ``DHT sensor library for ESPx``

# Instrucciones
1. Abrir WOKWI en el navegar
2. Escoger el simulador ESP32
3. Bajar hasta ``Starter Templates`` y elegir la ``ESP32``
4. Una vez adentro nos vamos a la pesta que dice ``Library Manager`` y hay buscamos la libreria antes mencionada presionando en el circulo con el simbolo de mas
5. Una vez agregada regresamos a la pestaña de sketch donde agregaremos y conectaremos el sensor a la tarjeta y para agregarlo hacemos click en el circulo azul con el simbolo de mas y lo buscamos como ``DHT22``
6. Una vez que lo agregamo realizamos la coneccion haciendo click sobre los pines o sobre los puntos amarrillos y lo llebamos a donde lo deceamos conectar
7. En el sketch colocamos el siguiente codigo:
```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}
```
8. Ya que lo tengamos damos click al boton de play para que nos muestre la lectura del sensor en la parte inferior
# Resultados 
logramos aprender como agregar librerias, agregar al simulador y como realizar conecciones entre si, tambien a modificar y enteder un poco sobre el codigo
# Creditos
Vicente Alexander Hernandez Maldonado 
   
