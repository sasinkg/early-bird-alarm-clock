# Early Bird Alarm Clock ⏰🚗

An interactive, mobile alarm clock designed to **force users out of bed** by combining physical movement, obstacle avoidance, and cognitive engagement. When the alarm triggers, the clock **drives away from the user** and can only be silenced by solving a math problem.

This project was completed as part of **ECE 445 – Senior Design** (Fall 2022).

---

## 🧠 Motivation

Many people rely on repeated alarms and snoozing, which disrupts sleep cycles and reduces morning alertness. The Early Bird Alarm Clock addresses this by:
- Physically forcing the user to get out of bed
- Preventing passive alarm dismissal
- Engaging the user cognitively before silencing the alarm

---

## ✨ Features

- ⏱️ **Fully functional alarm clock**
  - Set current time and alarm time
  - Visual alarm status indicator
- 🚗 **Autonomous movement**
  - Dual DC motors with H-bridge control
  - Obstacle detection via ultrasonic sensors
- 🧮 **Math-based alarm shutdown**
  - Randomly generated arithmetic problem
  - Alarm silences only after correct solution
- 📟 **LCD-based user interface**
  - Clock display
  - Alarm configuration
  - Math problem interaction
- 🔊 **Audible alarm via piezo buzzer**

---

## 🏗️ System Architecture

The system is organized into four primary subsystems:

### 1. UI Module
- 16x2 LCD display
- 8 push buttons (clock control + math input)
- Shift register (74HC165) to reduce I/O pin usage

### 2. Movement Module
- Two 12V DC motors
- L298N dual H-bridge motor driver
- Three HC-SR04 ultrasonic sensors for obstacle avoidance

### 3. Math Module
- Random arithmetic problem generation
- Button-driven numerical input (hundreds / tens / ones)
- Answer verification logic

### 4. Power Module
- Multiple NiMH batteries
- Voltage regulation for logic (5V) and motors (12V)

---

## 🧩 Software Overview

The firmware is written in **C/C++ (Arduino)** and organized modularly:

