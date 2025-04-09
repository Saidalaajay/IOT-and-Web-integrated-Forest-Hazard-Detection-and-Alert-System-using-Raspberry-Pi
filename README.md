# IOT-and-Web-integrated-Forest-Hazard-Detection-and-Alert-System-using-Raspberry-Pi
This project implements a real-time forest hazard detection system using a Raspberry Pi. It monitors for potential disasters such as gas leaks, fire, and abnormal motion (tilt)
It Performs following activity:
Captures sensor data.
Sends the data to ThingSpeak for cloud visualization.
Captures an image when an abnormal condition is detected.
Sends an email alert with the captured image to predefined recipients.
Displays live sensor data and system status on an I2C LCD.
COMPONENTS USED ARE:
- Raspberry Pi (any model with GPIO)
- Pi Camera Module
- Tilt Sensor (connected to GPIO 14)
- Gas Sensor (connected to GPIO 18)
- Fire Sensor (connected to GPIO 15)
- I2C LCD Display
- Internet Connection (WiFi or Ethernet)
 Cloud Integration
Data is uploaded to [ThingSpeak](https://thingspeak.com/channels/2846009), an IoT analytics platform. You can monitor real-time tilt, gas, and fire data using your browser
Email Alerts
Upon detection of any anomaly, the system:
1. Captures an image using the Pi Camera.
2. Sends an email with the image as an attachment using Gmail SMTP.
 How it Works
### Main Script Flow:
1. GPIO Initialization
2. LCD Intro Messages
3. Continuous Loop:
   - Read sensor values.
   - Display data on LCD.
   - Upload to ThingSpeak.
   - If any sensor is triggered:
     - Capture image.
     - Send email alert.
     - Display alert on LCD.
