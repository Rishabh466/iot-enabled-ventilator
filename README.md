# IoT-Enabled Smart Ventilator

## Introduction
In recent years, the need for affordable, portable, and easily accessible medical devices has surged, particularly in response to global health crises such as the COVID-19 pandemic. Among these critical devices, ventilators have played a key role in saving lives by supporting patients with respiratory difficulties. This project presents a low-cost, Arduino-based ventilator, aimed at providing essential life support for patients with compromised respiratory systems.


---

## Principle of Operation
This IOT based ventilator operates on the principle of Positive Pressure Ventilation (PPV). In PPV, air is forced into the lungs, helping patients breathe by inflating the lungs and ensuring proper gas exchange using ventilator bag and servo motor.


---


## Working
The IoT-based ventilator operates by controlling air or oxygen flow into the patient’s lungs using an Arduino microcontroller. The process begins with system initialization, where sensors are calibrated, the motor setup is defined, and an IoT connection is established.
When the ventilation cycle starts, the servo motor compresses a silicone bag to push air into the patient's lungs, simulating natural breathing. Pressure sensors monitor airflow, and an SpO2 sensor tracks oxygen saturation. These sensors provide real-time feedback to ensure safe and consistent operation.
The system allows manual adjustments via a potentiometer for air pressure and volume, while automatic safety measures stop the motor if unsafe pressure is detected. Through IoT connectivity, real-time patient data is transmitted to a cloud platform for remote monitoring and alerts.
Finally, pressing the stop button halts the ventilation cycle, saving the patient’s vitals to the cloud for record-keeping.


---


## Hardware Components
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

