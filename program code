#include <OneWire.h>
#include <DallasTemperature.h>

// === PIN SENSOR ===
#define ONE_WIRE_BUS 10  // GPIO10 pada ESP32-C3

// === OBJEK SENSOR ===
OneWire oneWire(ONE_WIRE_BUS);
DallasTemperature sensors(&oneWire);

void setup() {
  Serial.begin(115200);

  // Inisialisasi sensor suhu
  sensors.begin();
  Serial.println("Sensor suhu DS18B20 siap.");
}

void loop() {
  sensors.requestTemperatures();  // Minta pembacaan suhu
  float suhu = sensors.getTempCByIndex(0);  // Ambil suhu dalam Celcius

  Serial.print("Suhu: ");
  Serial.print(suhu);
  Serial.println(" °C");

  delay(2000);  // Baca setiap 2 detik
}
