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
1. Abrir WOKWI en el navegar y escogemos el simulador ESP32
![](https://github.com/vicentealexhm-VAHM/Practica-DHT11/blob/main/1.png?raw=true)
2. Bajar hasta ``Starter Templates`` y elegir la ``ESP32``
![](https://github.com/vicentealexhm-VAHM/Practica-DHT11/blob/main/2.png?raw=true)
3. Una vez adentro nos vamos a la pesta que dice ``Library Manager`` y hay buscamos la libreria antes mencionada presionando en el circulo con el simbolo de mas
![](https://github.com/vicentealexhm-VAHM/Practica-DHT11/blob/main/3.png?raw=true)
4. Una vez agregada regresamos a la pestaña de sketch donde agregaremos y conectaremos el sensor a la tarjeta y para agregarlo hacemos click en el circulo azul con el simbolo de mas y lo buscamos como ``DHT22``
![](https://github.com/vicentealexhm-VAHM/Practica-DHT11/blob/main/4.png?raw=true)
5. Una vez que lo agregamo realizamos la coneccion haciendo click sobre los pines o sobre los puntos amarrillos y lo llebamos a donde lo deceamos conectar
![](https://github.com/vicentealexhm-VAHM/Practica-DHT11/blob/main/5.png?raw=true)
6. En el sketch colocamos el siguiente codigo:
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
![](https://github.com/vicentealexhm-VAHM/Practica-DHT11/blob/main/6.png?raw=true)
# Resultados 
logramos aprender como agregar librerias, agregar al simulador y como realizar conecciones entre si, tambien a modificar y enteder un poco sobre el codigo
# Creditos
Vicente Alexander Hernandez Maldonado 
   
