# Object Detection Radar System  

This project is an object detection radar system using an **Arduino**, **Ultrasonic Sensor**, **Servo Motor**, and **Buzzer**. The system detects objects within a specified range and displays the distance and angle on a radar-like graphical interface using **Processing**. It also triggers a buzzer when an object is detected within the specified range.  

## Table of Contents  
- [Components Used](#components-used)  
- [Circuit Diagram](#circuit-diagram)  
- [Working Principle](#working-principle)  
- [Software Requirements](#software-requirements)  
- [Installation and Setup](#installation-and-setup)  

---

## Components Used  
- Arduino Uno  
- Ultrasonic Sensor  
- Servo Motor  
- Buzzer  
- Jumper Wires  
- Breadboard  

---

## Circuit Diagram  
Connect the components as follows:  
- **Ultrasonic Sensor**:  
  - VCC → 5V on Arduino  
  - GND → GND on Arduino  
  - Trig → Digital Pin 10  
  - Echo → Digital Pin 11  
- **Servo Motor**:  
  - Signal → Digital Pin 12  
  - VCC → 5V on Arduino  
  - GND → GND on Arduino  
- **Buzzer (Optional)**:  
  - Signal → Digital Pin 9  
  - VCC → 5V  
  - GND → GND  

---

## Working Principle  
The Ultrasonic Sensor measures the distance to an object by emitting ultrasonic waves and measuring the time taken for the echo to return. The servo motor rotates the sensor, allowing the system to scan a specified area. The distance and angle are sent to the **Processing** sketch, which visualizes the data as a radar.  

---

## Software Requirements  
1. [Arduino IDE](https://www.arduino.cc/en/software)  
2. [Processing IDE](https://processing.org/download/)  

---

## Installation and Setup  
### 1. Arduino Code  
- Open the `ObjectDetection.ino` file in the Arduino IDE.  
- Select the correct board and COM port.  
- Upload the code to your Arduino.  

### 2. Processing Code  
- Open the `RadarVisualization.pde` file in the Processing IDE.  
- Change the line:  
  ```java
  myPort = new Serial(this,"COM5", 9600);
