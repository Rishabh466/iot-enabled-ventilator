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
| **Internet of Things (ESP8266)** | For sending data to a locally hosted wbesite |
| **Microcontroller (Arduino Nano)** | Main controller/CPU |
| **LCD Display (20X4)** | Shows vitals locally |
| **Potentiometer (10Kohm)** | For selecting the age group |
| **Servo Motor (MG995)** | For driving the robotic arm |
| **Vital Sensor (MAX30100)** | Measures vitals |
| **Flow Sensor (HX710B)** | Measures airflow rate |
| **Ventilator Bag** | For pumping air into lungs |
| **Metal Rod and Plate** | Acts as robotic arm |
| **12V 2A Power Supply** | For powering everything |


---


## Applications
**Emergency Healthcare - Can be deployed in emergency situations like pandemics or natural disasters, where traditional ventilators may be unavailable.**
Home Healthcare - Ideal for patients requiring long-term respiratory support, allowing them to be monitored remotely by healthcare professionals while staying at home.
Medical Research and Education - Useful in research and educational institutions for studying respiratory therapy, ventilator technologies, and IoT integration in medical devices.
Military and Remote Operations - Useful for military medical teams operating in remote or conflict zones where conventional ventilators are unavailable or impractical to transport.
Veterinary Care - Could be adapted for use in veterinary hospitals, providing respiratory support for animals during surgery or in emergency cases.


---


## Advantages
Cost Effective - Built using affordable and easily available components like Arduino, ESP8266, and a silicone ventilator bag, significantly reducing the overall cost compared to commercial ventilators.
Portable and Lightweight - Due to its compact design, the ventilator is easily portable and can be used in mobile healthcare units, field hospitals, or remote settings.
Energy Efficient - The ventilator can be powered by a standard 5V DC power supply, and with a battery backup, it can continue functioning in the event of a power outage, ideal for use in disaster-prone areas.
Easy to Build and Maintain - The system uses off-the-shelf parts that are widely available, making it accessible for technicians or makers to assemble and maintain, even in resource-limited areas.
User-Friendly - Simple to operate with a push-button start/stop mechanism and intuitive controls, allowing quick deployment in emergency situations.


---


## Summary
This project presents the design and working of a low-cost, IoT-enabled ventilator using Arduino technology. The ventilator provides a safe, reliable, and portable solution for patients with respiratory difficulties. Key components include an Arduino microcontroller, pressure sensors, SpO2 sensor, servo motor, and ESP8266 Wi-Fi module for IoT connectivity.
The system controls the flow of air or oxygen into the patient's lungs by simulating natural breathing cycles. Real-time monitoring, remote data transmission, and alerts are enabled through an IoT platform, allowing healthcare providers to monitor the patient from a distance.
This ventilator is ideal for use in emergency healthcare, low-resource settings, home healthcare, and portable medical applications, offering a highly accessible and scalable solution for life-saving respiratory support.





