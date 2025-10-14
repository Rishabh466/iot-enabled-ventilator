# IoT-Enabled Smart Ventilator

## 🧭 Project Overview
During the COVID-19 pandemic, ventilator shortages highlighted the need for **low-cost, reliable, and remotely monitorable systems**.  
This project presents an **IoT-enabled ventilator prototype** that can automatically regulate airflow pressure using sensor feedback and send real-time patient data (SpO₂, BPM, air pressure) to a cloud dashboard.

The ventilator uses an **ESP32 microcontroller** for data acquisition and control, a **PID-based closed-loop algorithm** for pressure regulation, and **MQTT communication** for IoT connectivity.

---

## ⚙️ System Architecture

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

