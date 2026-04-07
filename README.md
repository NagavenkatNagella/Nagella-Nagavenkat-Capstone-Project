🌿 GreenFlow – VAWT Smart Monitoring System
📌 Overview

GreenFlow is an IoT-based smart monitoring system designed for Vertical Axis Wind Turbines (VAWT).
It provides real-time monitoring, threat detection, cloud logging, and alert notifications using the ESP8266 microcontroller.

The system integrates sensors, web dashboard, Google Sheets logging, and email alerts to ensure efficient and safe turbine operation.

🚀 Features
📡 Real-time temperature & humidity monitoring (DHT11)
🌐 Live web dashboard hosted on ESP8266
📊 Google Sheets data logging
⚠️ Threat detection using touch sensors
📧 Email alerts for abnormal conditions
📍 GPS-based turbine location tracking
🖥️ LCD display for local monitoring
📈 Live charts using web interface
🧠 System Architecture
Sensors (DHT11, Touch Sensors)
        ↓
     ESP8266
        ↓
 ┌───────────────┬───────────────┬───────────────┐
 │ Web Dashboard │ Google Sheets │ Email Alerts  │
 └───────────────┴───────────────┴───────────────┘
🛠️ Hardware Components
ESP8266 (NodeMCU)
DHT11 Temperature & Humidity Sensor
Touch Sensors (3 units for threat detection)
16x2 LCD with I2C module
Power supply (Battery/Adapter)
💻 Software & Libraries
Arduino IDE
Libraries used:
ESP8266WiFi
ESP8266WebServer
ESP8266HTTPClient
ESP_Mail_Client
DHT
LiquidCrystal_I2C
🔌 Pin Configuration
Component	Pin
DHT11	D4
Touch Sensor 1	D5
Touch Sensor 2	D6
Touch Sensor 3	D7
LCD (I2C)	0x27
⚙️ Configuration

Update the following in the code:

const char* ssid = "YOUR_WIFI_NAME";
const char* password = "YOUR_WIFI_PASSWORD";

#define AUTHOR_EMAIL     "your_email@gmail.com"
#define AUTHOR_PASSWORD  "your_app_password"
#define RECIPIENT_EMAIL  "receiver_email@gmail.com"

Also update your Google Sheets Web App URL:

const char* SHEETS_URL = "YOUR_GOOGLE_SCRIPT_URL";
📊 Working Principle
ESP8266 reads temperature and humidity from DHT11.
Touch sensors detect tampering or threats.
Data is:
Displayed on LCD
Sent to web dashboard
Logged into Google Sheets
If a threat is detected:
Email alert is sent
Alert is shown on dashboard
Event is logged
🌐 Web Dashboard
Real-time sensor data
Live charts (Temperature & Humidity)
Threat alerts popup
System status monitoring
Event logs
📧 Email Alert System
Sends alert when:
Threat detected
Abnormal condition occurs
Uses Gmail SMTP server
📍 Location Tracking

Predefined turbine coordinates:

const float TURBINE_LAT[] = {9.575062, 9.575180, 9.575310};
const float TURBINE_LON[] = {77.675734, 77.675890, 77.676050};
📈 Data Logging
Data is sent to Google Sheets every 15 seconds
Includes:
Temperature
Humidity
Status
Timestamp
⚠️ Security Note
Do NOT share your email password publicly
Use App Passwords for Gmail
Secure your WiFi credentials
📷 Project Output
LCD shows live readings
Web dashboard displays analytics
Google Sheets logs all data
Email alerts for threats
🎯 Applications
Smart Wind Energy Systems
Highway Energy Monitoring
Industrial IoT Monitoring
Smart Grid Integration
👨‍💻 Team
Nagella Nagavenkat
Kommineni Kavya Sree
Maruprolu Jyothsna
Munugu Tejasree
Kumaran Gobika
📄 License

This project is for academic and research purposes.
