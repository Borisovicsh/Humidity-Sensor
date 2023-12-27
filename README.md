# Humidity-Sensor
Temperature and Humidity Sensor (DHT11) with Arduino
#include <dht.h>

dht DHT;

#define DHTPIN 2

void setup() {
  Serial.begin(9600);
}

void loop() {
  int chk = DHT.read11(DHTPIN);

  Serial.print("Temperature: ");
  Serial.println(DHT.temperature);
  Serial.print("Humidity: ");
  Serial.println(DHT.humidity);

  delay(2000);
}
