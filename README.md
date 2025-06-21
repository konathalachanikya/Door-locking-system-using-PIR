# Door-locking-system-using-PIR
This is a basic motion-activated automatic door system using Arduino, designed for scenarios like smart entrances or contactless access control. Here's a quick breakdown of how it works and what it demonstrates:
**🔍 Project Overview**
The setup consists of:
- A PIR (Passive Infrared) sensor that detects motion—like a person approaching.
- An LCD display (16x2) to provide user feedback (e.g., "Sensor detected", "Door Opened").
- A DC motor (controlled via pins in1 and in2) that simulates opening and closing a door.
- A motor driver circuit (commonly an H-bridge or L298N) to control motor direction.
  _____________________________________________________________________________________________________________________________________________________________________________________________________
**🧠 Code Logic**
- Initialization: LCD is started; sensor and motor pins are set up.
- Main Loop:
- Reads the PIR sensor.
- Displays sensor state on LCD ("PIR:1" or "PIR:0").
- If motion is detected (pir_data == HIGH):
- LCD prints "Sensor detected".
- Door opens for 2 seconds.
- LCD prints "Door Opened", waits 2 seconds.
- Waits until the sensor no longer detects motion.
- Door closes for 2 seconds.
- LCD prints "Door Closed".
- If no motion is detected, it prints "Sensor not detect"
___________________________________________________________________________________________________________________________________________________________________________________________________
**🔧 Key Concepts Demonstrated**
- Digital input/output pin handling in Arduino.
- Condition-based motor control using GPIO pins.
- User feedback integration through LCD.
- Debouncing/waiting using while() to ensure proper door closure timing.
This kind of project is a great entry point into home automation or IoT systems.
___________________________________________________________________________________________________________________________________________________________________________________________________
**Applications**
 Home Automation
- Touchless main door systems for improved hygiene and ease of access.
- Smart bathrooms or kitchen entries, especially for accessibility.
🏢 Office and Commercial Spaces
- Secure entryways where doors open only when motion is detected, ideal for restricted zones.
- Energy-saving systems where lights and doors are triggered only when necessary.
🚪 Public Infrastructure
- Automatic doors in malls, airports, and hospitals where high foot traffic demands efficiency and hygiene.
- Contactless washroom doors in public facilities to reduce germ spread.
🤖 Robotics and IoT Integration
- Used in robotic arms or automated gates, reacting to human presence.
- As a foundation for IoT projects, combining with GSM modules, cloud logging, or RFID for smarter access.
🚗 Automotive
- Could be adapted for garage doors or car trunks that open when someone approaches.
