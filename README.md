# System-for-Monitoring-the-Healthiness-of-Electrical-Earthing
This system integrates a variety of sensors with a microcontroller, such as a ESP32, to monitor key parameters, including earth resistance, soil moisture, connection continuity, and current and voltage levels. By employing soil moisture sensors, the system evaluates soil conductivity, a critical factor for effective earthing. 

4.1	Hardware Requirements


S. No.	Hardware components
1.	ESP32 Microcontroller
2.	ZMPT101B Voltage Sensor
3.	ACS712 Current Sensor
4.	Soil Moisture Sensor
5.	16x2 Liquid Crystal I2C LCD Display
6.	5V Buzzer
7.	Power supply of 5V
8.	5mm LED’s
9.	Zero PCB
10.	Connecting wires
11.	Square Plywood Surface

Table 4.1 Hardware Requirements

4.1.1	ESP32 Microcontroller

The ESP32 is the central microcontroller used in the system. It is a powerful, dual-core processor with integrated Wi-Fi and Bluetooth capabilities. The ESP32 enables real-time processing of sensor data and ensures seamless communication between the system components and the monitoring platform. It plays a key role in collecting data from sensors such as the earth leakage current sensor and transmitting it over the internet for remote monitoring.
 
 
Fig. 4.1 ESP32 GPIO pinout

4.1.2	ZMPT101B Voltage Sensor

The ZMPT101B is a voltage sensor module designed for measuring AC voltage. It detects variations in the electrical system, such as voltage spikes or drops, and helps assess the health of the earthing system. By integrating this sensor, the system can monitor fluctuations in the electrical network and ensure the earthing system remains within safe operational parameters.


Fig.4.2 ZMPT101B Voltage Sensor



4.1.3	ACS712 Current Sensor

The ACS712 is a current sensor used to measure the leakage current in the system. It is based on the Hall Effect and provides precise current readings in both AC and DC circuits. In your earthing monitoring system, the ACS712 detects earth leakage current, ensuring the earthing system is functioning correctly and alerting the maintenance team in deviations
 
 

     Fig. 4.3-ACS712 current Sensor

4.1.4	Soil Moisture Sensor

The Soil Moisture Sensor is used to monitor the soil's moisture content, which can impact the effectiveness of the earthing system. A dry environment can reduce the efficiency of earthing, so this sensor helps maintain the health of the system by providing feedback on the surrounding moisture conditions, aiding in predictive maintenance




                                                      




                         Fig. 4.4 Soil Moisture Sensor


4.1.5	16x2 Liquid Crystal I2C LCD Display

The 16x2 LCD display with I2C communication is used to provide a user interface for the earthing system. It displays real-time data such as earth resistance, leakage current, and the system’s health status.
 





     Fig. 4.5 LCD Display

4.1.6	5V Buzzer

The 5V Buzzer serves as an audible alert mechanism. It signals when there are abnormal readings, such as excessive earth leakage current or high resistance in the earthing system, indicating a potential fault. This ensures immediate awareness of the issue, enabling prompt action.

4.1.7	Power Supply of 5V

A stable 5V power supply is essential for the continuous operation of the system. It powers the Raspberry Pi, sensors, and other components, ensuring that the security system remains active and responsive.

4.1.8	5mm LED’s

The 5mm LEDs are used to visually indicate the status of the system. For example, green could represent normal operation, while red could indicate a fault, such as an earth leakage current beyond acceptable limits. These LEDs provide an additional layer of notification to the maintenance personnel.

4.1.9	Zero PCB

The Zero PCB is used for assembling the circuit components in a compact and organized manner. It is used for creating a custom circuit layout, connecting all the sensors and modules in the system 
4.1.10 Connecting Wires

Connecting wires establish the necessary electrical connections between various components, ensuring a well-organized and functional circuit layout.

4.1.10	A Floor Tile or Rectangular Cardboard Surface of 15 X 15 cm

The floor tile or rectangular cardboard surface serves as the demonstration platform for the system. It mimics the conditions of a real-world environment, allowing for practical testing.

4.2	Software Requirements

•	4.2.1 IDE: Arduino IDE or PlatformIO
•	Programming Language: C/C++
•	Libraries:
•	WiFi.h (for Wi-Fi communication)
•	ACS712.h (for current sensor data)
•	ZMPT101B.h (for voltage sensor data)
•	LiquidCrystal_I2C.h (for LCD display)
•	DHT.h (if using temperature/humidity sensors)
•	Functionality:
•	Collect data from sensors (current, voltage, soil moisture)
•	Send sensor data to the cloud platform (e.g., ThingSpeak, Blynk)
•	Trigger alerts when abnormal conditions are detected (via buzzer, LEDs, or display)


4.2.1	ZMPT101B Voltage Sensor

The ZMPT101B voltage sensor measures the AC voltage of the earthing system. It provides an analog voltage signal that the ESP32 processes to monitor the earthing system’s voltage level. The voltage is critical for determining if the system is grounded properly and if there are any voltage fluctuations that could indicate faults.
 

 
       4.6 Evolution of the Solution


4.2.2	Microsoft Visual Code

Microsoft Visual Code serves as the integrated development environment (IDE) for writing and managing the system's codebase. Its user-friendly interface and robust features support efficient coding, debugging, and deployment of the security algorithm on the Raspberry Pi.

4.3	Workflow

The workflow of the Earthing Monitoring System unfolds through a series of interconnected
 
processes, ensuring the seamless integration of hardware and software components. This section provides a comprehensive overview of how each step contributes to the system's functionality, security, and user interface.

The evolution of the IoT-based earthing monitoring system reflects a thoughtful and deliberate process of integrating modern technology to address critical challenges in electrical safety. From the initial concept to deployment, the solution has continuously improved in terms of accuracy, reliability, and user experience. As the system matures, it aligns with broader trends in smart infrastructure, contributing to safer, more efficient, and sustainable electrical system.


Fig.4.7 Circuit Diagram used in the project



4.3.1	Trigger Mechanism and Data Processing

The trigger mechanism of the IoT-based earthing monitoring system detects anomalies in earth leakage current, voltage, and soil moisture using sensors like the ZMPT101B and ACS712. When values exceed thresholds, the system triggers alarms through a 5V Buzzer and 5mm LED indicators. The ESP32 microcontroller processes the data from sensors, converting analog signals with the ADC0809. If faults are detected, the system displays the information on the 16x2 I2C LCD and sends it to a cloud platform for remote monitoring. This ensures real-time monitoring and quick response to maintain system safety and efficiency.

4.3.2	Audible Alert and User Interface

The Audible Alert and User Interface of the IoT-based earthing monitoring system are crucial
 
for providing real-time feedback and ensuring user awareness of potential issues with the earthing system. The system is equipped with a 5V buzzer that generates an audible alert whenever any of the monitored parameters, such as earth leakage current or voltage, exceed the set threshold. This immediate feedback helps users take timely action to prevent potential safety hazards or system malfunctions.

The User Interface consists of a 16x2 LCD screen, which displays critical information such as earth leakage current, voltage levels, soil moisture, and system status. The data on the LCD screen is updated in real-time, providing users with clear, easy-to-read insights into the health of the earthing system.

This combination of an audible alert and a visual display ensures that users are promptly informed about the system's status, allowing them to respond quickly to potential issues. Whether on-site or remotely through the cloud-based platform, the intuitive interface ensures that the system remains user-friendly and effective in monitoring earthing health.

4.3.3	Continuous Operation and Standalone Capability

The Continuous Operation and Standalone Capability of the IoT-based earthing monitoring system ensures that it operates autonomously without requiring frequent manual intervention. Powered by a stable 5V power supply, the system runs continuously, monitoring critical parameters such as earth leakage current, voltage levels, and soil moisture through sensors like ZMPT101B, ACS712, and soil moisture sensors.
Its ESP32 microcontroller processes the collected data and triggers alerts based on predefined thresholds, which are displayed on the 16x2 LCD screen. The system operates independently, ensuring reliable functionality even without direct interaction with external devices.

This standalone capability is particularly valuable in remote or off-grid locations, as the system can function autonomously while continuously transmitting data to a cloud platform for remote monitoring. The integration of a 5V buzzer and LED indicators allows immediate local notifications, further enhancing the system’s reliability in any environment.
The combination of real-time data processing, continuous operation, and autonomous functioning makes this system an ideal solution for effective earthing system monitoring, minimizing the risk of electrical faults or failures without requiring constant attention.
 
4.3.4	Privacy and Downloadable Snapshot

The privacy of captured snapshots is maintained through restricted access. Only users with the IP address of the Raspberry Pi can access the designated webpage. This privacy measure ensures that sensitive information remains within the hands of authorized users.

Additionally, the system allows users to download the captured snapshots. This feature enhances user control and provides a means for preserving evidence or sharing information with law enforcement if necessary.

4.3.5	Live Feed Functionality

The Live Feed Functionality in the IoT-based earthing monitoring system provides real-time updates on the system's status and performance. Using the ESP32 microcontroller, the system continuously collects data from the ZMPT101B voltage sensor, ACS712 current sensor, and soil moisture sensor, and processes it for immediate analysis.
