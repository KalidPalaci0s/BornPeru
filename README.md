<div align="center">

![NutriPet Banner](https://capsule-render.vercel.app/api?type=waving&color=0:B91C1C,100:111111&height=260&section=header&text=NutriPet%20F1&fontSize=75&fontColor=FFFFFF&animation=fadeIn&fontAlignY=38&desc=SMART%20IoT%20FEEDING%20SYSTEM&descAlignY=60&descSize=19)

# 🐾 NUTRIPET
### Smart FeedStation Node F1

**An intelligent IoT-powered pet feeding experience.**

![ESP32](https://img.shields.io/badge/ESP32-DC2626?style=for-the-badge&logo=espressif&logoColor=white)
![C++](https://img.shields.io/badge/C++-111111?style=for-the-badge&logo=cplusplus&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-DC2626?style=for-the-badge&logo=arduino&logoColor=white)
![Wokwi](https://img.shields.io/badge/WOKWI-111111?style=for-the-badge)
![IoT](https://img.shields.io/badge/IoT-DC2626?style=for-the-badge&logo=iot&logoColor=white)

---

### AUTOMATE. MONITOR. PROTECT.

An embedded IoT system designed to automate pet feeding through intelligent sensing, real-time monitoring, and event-driven control.

</div>

## 🔴 Overview

**NutriPet FeedStation Node F1** is a smart feeding station prototype powered by an **ESP32 microcontroller**.

The system integrates sensors, actuators, and embedded software to manage food dispensing while monitoring water availability, food weight, and pet proximity.

Built with **Arduino C++**, object-oriented programming principles, and the **Modest IoT Nano Framework**.

## ⚡ Key Features

- 🐾 **Smart Pet Detection** — Detects nearby pets using an ultrasonic proximity sensor.
- 🍖 **Automatic Food Dispensing** — Controls a servo-based feeding mechanism.
- 💧 **Water Level Monitoring** — Tracks water availability and detects empty conditions.
- ⚖️ **Food Weight Tracking** — Uses an HX711 load-cell interface.
- 📟 **LCD Status Display** — Displays water levels, food weight, and system status.
- 📊 **Telemetry & Events** — Records operational states and feeding events.
- 🛑 **Safety Controls** — Prevents dispensing when the water tank is empty.

## 🧠 System Architecture

```text
               NUTRIPET F1
                    |
             ESP32 CONTROLLER
                    |
       +------------+------------+
       |            |            |
    SENSORS       LOGIC       ACTUATORS
       |            |            |
   HC-SR04      FeedStation     Servo
   HC-SR04      Controller      LCD
   HX711            |
                    |
              TELEMETRY
                    |
              SERIAL LOGS
```

## 🔧 Tech Stack

| Technology | Purpose |
|:---|:---|
| ESP32 | Main IoT controller |
| Arduino C++ | Embedded programming |
| Wokwi | Hardware simulation |
| Modest IoT Nano Framework | Device architecture |
| HC-SR04 | Water and proximity detection |
| HX711 | Food weight measurement |
| Servo Motor | Feeding mechanism |
| LCD 16×2 I2C | Local monitoring |
| ArduinoJson | Telemetry serialization |

## 🚦 Operating Modes

| Mode | Description |
|:---|:---|
| `MONITORING` | Normal sensor monitoring |
| `DISPENSING` | Automatic food dispensing |
| `EMPTY` | Water unavailable; dispensing disabled |
| `SENSOR_FAULT` | Invalid sensor measurement |

## 📂 Project Structure

```text
NutriPet/
├── sketch.ino
├── NutriPetDevice.h
├── diagram.json
├── libraries.txt
└── README.md
```

## 🎯 Feeding Rules

```cpp
constexpr float MIN_FOOD_WEIGHT = 200.0f;
constexpr float TARGET_FOOD_WEIGHT = 800.0f;
constexpr float PET_DISTANCE_CM = 20.0f;
```

The feeding mechanism activates when:

1. The food weight is below **200 g**.
2. A pet is detected within **20 cm**.
3. The water tank is not empty.

Dispensing stops when the food reaches **800 g** or a safety condition requires interruption.

## 🧪 Simulation

The project is designed for simulation in **Wokwi**.

[![Wokwi](https://img.shields.io/badge/OPEN_WOKWI_SIMULATOR-DC2626?style=for-the-badge)](https://wokwi.com/projects/new/esp32)

> **Note:** This repository contains a practice implementation. Full end-to-end simulation validation is pending.

---

<div align="center">

### BUILT FOR THE FUTURE OF PET CARE

**Smart sensing. Intelligent feeding. Better care.**

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:111111,100:B91C1C&height=130&section=footer)

</div>
