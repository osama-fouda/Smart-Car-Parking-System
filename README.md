# Smart-Car-Parking-System

## 🚗 Smart Parking System with Arduino

This is a smart parking system built using an **Arduino Uno**, **IR sensors**, **servo motor**, and a **16x2 LCD (I2C)**. It automatically detects car entry and exit, manages a servo-controlled gate, and displays the available parking slots on the LCD in real time.

---

### 📦 Features

* 🔌 IR sensors to detect car presence at entrance and exit.
* 🎮 Servo motor to open and close the parking gate.
* 📟 LCD display to show available slots.
* 🧠 Arduino Uno for control logic.
* ⚠️ LCD warning message when parking is full.

---

### 🧰 Components Used

| Component             | Quantity  |
| --------------------- | --------- |
| Arduino Uno           | 1         |
| IR Sensors            | 2         |
| Servo Motor           | 1         |
| LCD 16x2 (I2C)        | 1         |
| Jumper Wires          | As needed |
| Breadboard (optional) | 1         |

---

### 🔌 Circuit Overview

* **IR1 Sensor**: Detects cars entering (connected to digital pin 2)
* **IR2 Sensor**: Detects cars exiting (connected to digital pin 3)
* **Servo Motor**: Connected to digital pin 4
* **LCD I2C**:

  * SDA → A4
  * SCL → A5

---

### 💻 Code Logic

1. LCD welcomes the user and displays available slots.
2. When a car is detected by IR1 and slots are available:

   * Gate opens (servo rotates)
   * Slot count decreases
3. If parking is full, LCD displays a "No Space" message.
4. When a car exits via IR2:

   * Gate opens
   * Slot count increases
5. LCD constantly updates to show remaining slots.

---

### 🎮 Simulation

You can simulate this project on [Tinkercad](https://www.tinkercad.com/), adding:

* IR sensors
* LCD with I2C module
* Arduino Uno
* Servo motor

---
