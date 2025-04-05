## iot-bedside-control-panel
An initiative for patients
🛏️ IoT-Based Bedside Control Panel (Arduino-Based)
A smart bedside control panel built using Arduino for health monitoring, comfort control, and emergency alerting. This system integrates sensors, actuators, and GSM communication to support patients, the elderly, or individuals in smart homes.

# 📌 Project Overview
This project is my final-year engineering project that utilizes an Arduino microcontroller to manage sensors and actuators. 
It provides:
Real-time health and environmental monitoring
Mechanized bed movement
SMS alerts on abnormal heart rate
Remote data access via IoT/cloud platforms

# ⚙️ Features
🌡️ Temperature Monitoring
Using DHT11/DHT22, displays real-time room temperature.

🛏️ Movable Bed Headboard
Controlled via a servo or linear actuator to adjust the head position for user comfort.

📐 Gyroscope Feedback
The MPU6050 sensor detects the tilt angle and motion of the bed headboard.

❤️ Heart Rate Monitoring with Alerts
Uses MAX30100 / Pulse Sensor to detect heart rate. If it goes out of a safe range, an SMS alert is sent via SIM800L GSM module to a caregiver.

# 🔧 Components Used
Component	Description
Arduino Uno / Mega	Main microcontroller board
DHT11/DHT22	Temperature and humidity sensor
MPU6050	Accelerometer + Gyroscope sensor
MAX30100 / Pulse Sensor	Heart rate monitoring
SIM800L / SIM900	GSM module for SMS alerts
Servo / Linear Actuator	Bed movement mechanism
OLED / LCD Display	For showing sensor readings
Push Buttons	Manual input for adjusting bed
Relay Module (optional)	For controlling fans/lights
Power Supply	5V regulated + GSM-capable source
🛠️ How It Works
Sensors continuously read temperature, tilt angle, and heart rate.

The Arduino processes the data and displays it on an LCD/OLED screen.

The servo/actuator moves the bed when buttons or app commands are received.

If the heart rate crosses critical limits, Arduino triggers an SMS alert via GSM module.

Optional: Data is sent to ThingSpeak or Blynk for remote monitoring.

🔋 System Architecture

[ Temp Sensor ]       [ Gyro Sensor ]
       ↓                     ↓
 [ Heart Rate Sensor ]    [ Push Buttons ]
            ↓                     ↓
           →→ [ Arduino UNO  ] ←←
               ↓      ↑      ↓
          [ LCD/OLED ]  [ Actuator ]
               ↓
         [ GSM Module (SIM800L) ]
               ↓
        [ Sends SMS Alerts ]

# ✅ Requirements
Arduino IDE

Libraries: DHT, Wire, Adafruit_GFX, Adafruit_SSD1306, MPU6050, SoftwareSerial, PulseSensorPlayground

SIM card (with balance/SMS plan)


📚 Documentation
Circuit Diagram

Arduino Code Folder

📈 Future Improvements
Voice control via Google Assistant / Alexa

Fall detection via MPU6050

Battery backup and solar support

Touch screen UI panel

👨‍🎓 Author
Abirami Ravindran, Ashmitha Dhamodharan, Jeevitha Arivazhagan.
Final Year B.E. in Electronics and Communication Engineering
📧 abiramiravi320@gmail.com

📜 License
This project is a part of academic research and intended for educational use only.
Open for collaboration and improvements.
