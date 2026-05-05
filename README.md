# Adaptive_Cruise_control_With_QNX
Driver Assisted Adaptive Cruise Control using Arduino, Python, and QNX RTOS for real-time obstacle detection, adaptive speed regulation, and emergency braking. Uses ultrasonic sensing, deterministic control, and multi-layer communication for intelligent, safety-focused vehicle automation.

## Project Overview

Traditional cruise control systems maintain a fixed speed without considering surrounding traffic or obstacles, which limits their safety in dynamic driving environments.

This project presents a Driver Assisted Adaptive Cruise Control (DACC) system designed to improve vehicle safety by continuously monitoring obstacle distance and automatically adjusting speed based on real-time conditions.

The system combines:

- Arduino Uno for hardware interfacing  
- Python for communication between hardware and control system  
- QNX RTOS for real-time decision-making and adaptive control  

---

## Objectives

### Primary Goal
To design and implement a real-time adaptive cruise control system capable of monitoring obstacles and dynamically controlling vehicle speed.

### Key Objectives
- Real-time speed regulation  
- Continuous obstacle detection  
- Automatic braking in critical situations  
- Reliable communication across multiple platforms  
- Improved safety and system responsiveness  

---

## Hardware Components

- Arduino Uno  
- HC-SR04 Ultrasonic Sensor  
- L298N Motor Driver  
- 4 BO Motors  
- Buzzer  
- Power Supply  

---

## Software Components

### Arduino IDE
Used for:
- Sensor data collection  
- Motor speed control  
- Buzzer activation  

### Python
Used for:
- Serial communication with Arduino  
- Socket communication with QNX  
- Real-time data transfer  

### QNX RTOS
Used for:
- Sensor data processing  
- Adaptive speed control decisions  
- Emergency braking logic  

---

## System Architecture

```text id="0fr9zc"
Ultrasonic Sensor
       ↓
   Arduino Uno
       ↓ Serial
   Python Bridge
       ↓ Socket
    QNX RTOS
       ↓ Command
   Python Bridge
       ↓ Serial
   Arduino Uno
       ↓
Motor Driver + Motors
