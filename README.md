**Name:**THALAKOKULA SHIVA KUMAR
**Company:**CODTECH IT SOLUTIONS PVT.LTD 
**Intern ID:**CT12DYQ 
**Domain:**Embedded systems
**Duration:**December 17 to February 17 2025

Overview of the project

## Project : USE A TEMPERATURE SENSOR TO READ AND DISPLAY TEMPERATURE DATA ON AN LCD OR SERIAL MONITOR
## Components Required
Arduino Uno/Nano
Temperature Sensor (LM35, DHT11, or DHT22)
16x2 LCD with or without I2C module
Breadboard and jumper wires
## Connections
For LM35 Sensor:
VCC → 5V (Arduino)
GND → GND (Arduino)
OUT → A0 (Arduino)
For DHT11/DHT22 Sensor:
VCC → 5V (Arduino)
GND → GND (Arduino)
DATA → Digital pin (e.g., D2)
For LCD (With I2C Module):
SDA → A4 (Arduino Uno)
SCL → A5 (Arduino Uno)
VCC → 5V
GND → GND

## How It Works
LM35: Converts temperature into a voltage (10mV/°C). The Arduino reads this voltage via an analog pin and converts it to Celsius.
DHT11/DHT22: Measures temperature digitally and sends the data via a digital pin using the DHT library
Working Principle

## Temperature Sensor:![Screenshot 2025-01-05 123954](https://github.com/user-attachments/assets/39beec40-935e-4966-ae33-f86775f86a35)

LM35: The LM35 sensor outputs a voltage proportional to the temperature. Each 10mV corresponds to 1°C. For example:
At 25°C, the output voltage = 250mV (0.25V).
DHT11/DHT22: These sensors use digital communication to send temperature data directly to the Arduino. The DHT library decodes this data.
Arduino Processing:

For LM35: Arduino reads the analog voltage signal using the analogRead() function, converts it to a temperature in Celsius using a formula, and then displays it.
For DHT11/DHT22: The library handles data decoding. Arduino uses the readTemperature() method to fetch the temperature value directly.
Display:

LCD: The temperature data is formatted and displayed on a 16x2 LCD screen.
Serial Monitor: The data is also sent via USB to the Serial Monitor for debugging or monitoring without the LCD.
