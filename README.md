# Project-Smart-Water-Level-Indicator
# 💧 Smart Water Level Indicator using Ultrasonic Sensor and LEDs

## 📌 Project Overview

The **Smart Water Level Indicator** is a simple and efficient system designed to monitor the water level in a tank using an ultrasonic sensor. It displays the water level percentage on the serial monitor and uses a set of three LEDs (Red, Yellow, Green) to indicate whether the water level is low, medium, or high.

---

## ⚙️ Components Used

- Arduino Uno / Mega
- Ultrasonic Sensor (HC-SR04)
- Red, Yellow, and Green LEDs
- 220Ω Resistors (x3)
- Jumper Wires
- Breadboard
- Water Tank / Simulated Tank Setup

---

## 🧠 Working Principle

- The HC-SR04 ultrasonic sensor measures the distance from the top of the tank to the water surface.
- This distance is converted to a percentage of tank fill based on the total tank height.
- Depending on the water level:
  - Green LED turns ON for >75%
  - Yellow LED turns ON for 41%–75%
  - Red LED turns ON for ≤40%
- The percentage is displayed on the Serial Monitor every second.

---

## 🔌 Circuit Connections

| Arduino Pin | Connected To        |
|-------------|---------------------|
| 9           | HC-SR04 Trigger Pin |
| 10          | HC-SR04 Echo Pin    |
| 2           | Red LED             |
| 3           | Yellow LED          |
| 4           | Green LED           |

*Each LED is connected via a 220Ω resistor.*

---

## 🔁 Code Behavior

- Uses `pulseIn()` to get echo time.
- Converts time to distance using sound speed formula.
- Calculates percentage fill:  
  `levelPercent = ((tankHeight - distance) * 100) / tankHeight;`
- Uses `constrain()` to ensure values are between 0 and 100.
- LEDs update based on the calculated percentage.

---

## 🚦 LED Indication Logic

| Water Level (%) | LED Status |
|------------------|-------------|
| 76–100%          | Green ON    |
| 41–75%           | Yellow ON   |
| 0–40%            | Red ON      |

---

## 📟 Serial Monitor Output Example


---

## 📌 Applications

- Household tank monitoring
- Water overflow prevention
- Agriculture and irrigation systems
- School/college embedded systems projects

---

## 🔧 Optional Improvements

- Add a buzzer or SMS alert for low level
- Display level on an LCD or OLED
- Use Wi-Fi (ESP8266/ESP32) for IoT-based monitoring

---

## 🧑‍💻 Developed By

**Shashank**
