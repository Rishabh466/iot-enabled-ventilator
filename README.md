# IoT-Enabled Smart Ventilator

## Introduction
In recent years, the need for affordable, portable, and easily accessible medical devices has surged, particularly in response to global health crises such as the COVID-19 pandemic. Among these critical devices, ventilators have played a key role in saving lives by supporting patients with respiratory difficulties. This project presents a low-cost, Arduino-based ventilator, aimed at providing essential life support for patients with compromised respiratory systems.
<img width="8010" height="88" alt="image" src="https://github.com/user-attachments/assets/514322ba-357e-4e7a-ba74-ce85ddef0138" />


---

## System Architecture

### 🧩 Hardware Components
| Component | Function |
|------------|-----------|
| **ESP32 / Arduino** | Main controller handling all I/O operations |
| **Pressure Sensor (MPX5010)** | Measures airway pressure |
| **Flow Sensor (FS300A)** | Measures airflow rate |
| **Pulse Oximeter (MAX30100)** | Measures SpO₂ and BPM |
| **Motor Driver (L298N)** | Controls blower or motorized valve |
| **Display (OLED 0.96”)** | Shows vitals locally |
| **Wi-Fi Module (ESP32 built-in)** | Sends data to IoT dashboard via MQTT |

---

## 📡 Working Principle
The ventilator maintains a **target pressure** within the patient airway.  
It continuously samples sensor readings, calculates error against the setpoint, and drives the blower motor using a PID algorithm.  
All vital parameters are sent to an IoT dashboard for monitoring and logging.

### 🔁 Control Flow

