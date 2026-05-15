# IoT-Based-Automatic-Smart-Water-Level-Management-Bottle

An IoT-inspired smart hydration monitoring system designed to track water levels in a bottle or container using an ultrasonic sensor and microcontroller-based alert mechanism. The system detects minimum, normal, and maximum water levels and provides real-time indication using a buzzer and LED.

This project demonstrates embedded systems, sensor interfacing, hardware prototyping, and IoT-oriented system design. It can be extended further with cloud integration, dashboards, and personalized hydration analytics.

---

## Project Overview

The system uses an ultrasonic sensor to measure the water level inside a container. Based on the measured level, the system triggers visual and audio alerts.

### Water Level Behavior

- **Minimum water level:** LED ON and buzzer ON at high frequency
- **Normal water level:** LED OFF and buzzer OFF
- **Maximum water level:** LED ON and buzzer ON at low frequency

The project is useful for understanding real-time sensing, microcontroller programming, and alert-based automation systems.

---

## Hardware and Software Components

The project uses basic embedded hardware components along with Arduino IDE for programming and testing.

![Hardware and Software Components](assets/components-table.png)

### Hardware Requirements

- Arduino board
- Ultrasonic sensor
- Buzzer
- LED
- Breadboard
- Connecting wires
- Battery pack or USB power source

### Software Requirements

- Arduino IDE
- Embedded C / Arduino C++

---

## Experimental Setup

The prototype was built using an Arduino board, ultrasonic sensor, buzzer, LED, breadboard, and connecting wires. The ultrasonic sensor was mounted near the container opening to measure the distance between the sensor and the water surface.

![Experimental Setup](assets/experimental-setup.png)

---

## System Architecture

The system follows a simple sensor-to-actuator workflow:

1. The ultrasonic sensor measures the distance from the sensor to the water surface.
2. The Arduino processes the distance value.
3. Based on predefined threshold values, the system classifies the water level.
4. The buzzer and LED are activated according to the detected level.

![System Flow](assets/system-flow.png)

### Architecture Flow

    Battery Pack / USB Power
            ↓
    Arduino Board
            ↓
    Ultrasonic Sensor
            ↓
    Water Level Detection
            ↓
    Buzzer and LED Indication

---

## Water Level Indication Logic

The system classifies the water level into three states: minimum, normal, and maximum.

![Water Level Indication Table](assets/water-level-table.png)

| Water Level Condition | Buzzer Status | LED Status |
|---|---|---|
| Minimum Level | ON - High Frequency | ON |
| Normal Level | OFF | OFF |
| Maximum Level | ON - Low Frequency | ON |

---

## Buzzer and LED Response

The LED and buzzer provide immediate feedback based on the water level condition. The alert mechanism helps identify whether the water level is too low, within the normal range, or too high.

![Buzzer and LED Graph](assets/buzzer-led-graph.png)

---

## Key Features

- Real-time water level detection using ultrasonic sensing
- Arduino-based embedded system implementation
- LED indication for minimum and maximum water levels
- Buzzer alert with different frequency behavior
- Simple and low-cost hardware prototype
- Easy to modify threshold values for different containers
- Suitable for IoT and smart monitoring applications

---

## Working Principle

The ultrasonic sensor sends sound waves toward the water surface and receives the reflected signal. The Arduino calculates the distance using the time taken by the signal to return.

Based on the calculated distance:

- If the water level is below the minimum threshold, the system activates a high-frequency buzzer alert.
- If the water level is within the desired range, both buzzer and LED remain OFF.
- If the water level reaches the maximum threshold, the system activates a low-frequency buzzer alert.

---

## Technologies Used

### Hardware

- Arduino
- Ultrasonic Sensor
- Buzzer
- LED
- Breadboard
- Connecting Wires

### Software

- Arduino IDE
- Arduino C/C++

---

## Possible IoT Extension

This project can be extended into a complete IoT-based hydration tracking system by adding:

- ESP8266 or ESP32 Wi-Fi module
- Firebase Realtime Database
- Web dashboard for live monitoring
- User-wise hydration history
- Time-series analysis of water consumption
- Personalized hydration reminders
- Mobile notification system

---

## Future Enhancements

- Add ESP8266/ESP32 for wireless data transmission
- Store water level readings in Firebase or cloud database
- Build a web dashboard for real-time visualization
- Add user authentication for multi-user tracking
- Implement daily water intake goal tracking
- Add machine learning-based hydration recommendations
- Improve enclosure design for practical bottle mounting
- Add battery optimization for portable usage

---

## Skills Demonstrated

- Embedded systems development
- Arduino programming
- Ultrasonic sensor interfacing
- Circuit design and prototyping
- Real-time condition monitoring
- Buzzer and LED control logic
- Hardware-software integration
- IoT system design fundamentals
- Technical documentation

---

## Project Structure

    IoT-Smart-Hydration-Tracking-System/
    │
    ├── README.md
    ├── code/
    │   └── hydration_level_monitor.ino
    │
    ├── assets/
    │   ├── components-table.png
    │   ├── experimental-setup.png
    │   ├── water-level-table.png
    │   ├── system-flow.png
    │   └── buzzer-led-graph.png
    │
    └── docs/
        └── project-report.pdf

---

## How to Run

### 1. Hardware Setup

Connect the ultrasonic sensor, buzzer, and LED to the Arduino board using a breadboard and jumper wires.

Example connection:

    Ultrasonic Sensor VCC  → Arduino 5V
    Ultrasonic Sensor GND  → Arduino GND
    Ultrasonic Sensor TRIG → Digital Pin
    Ultrasonic Sensor ECHO → Digital Pin

    Buzzer Positive → Digital Pin
    Buzzer Negative → GND

    LED Positive → Digital Pin through resistor
    LED Negative → GND

### 2. Software Setup

1. Open Arduino IDE.
2. Connect the Arduino board to the system.
3. Select the correct board and port.
4. Upload the Arduino code.
5. Open Serial Monitor to observe sensor readings.

---

## Applications

- Smart water bottle monitoring
- Hydration reminder systems
- Water level alert systems
- Basic IoT-based health monitoring projects
- Embedded systems learning project
- Sensor-based automation prototype

---

## Conclusion

The IoT-Based Smart Hydration Tracking System demonstrates how ultrasonic sensing and microcontroller-based control can be used to monitor water levels and generate real-time alerts. The project provides a strong foundation for building more advanced IoT-enabled hydration monitoring systems with cloud storage, dashboards, and personalized recommendations.
