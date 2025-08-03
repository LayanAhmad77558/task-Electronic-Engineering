# task-Electronic-Engineering
task1 Electronic Engineering
# Servo Motor Control - Humanoid Robot Project

## Overview

This project demonstrates how to control six servo motors using Arduino. The servos initially perform a sweep motion for 2 seconds, and then all motors hold at a 90-degree position. Additionally, a walking algorithm for a humanoid robot using six servos is described.

---

## Code Description

- The Arduino code uses the Servo library.
- Six servo motors are attached to digital pins 2 to 7.
- For the first 2 seconds, all servos perform a sweep motion from 0° to 180° and back.
- After 2 seconds, all servos are set to a fixed position at 90°, simulating a neutral pose.

---

## Hardware Requirements

- Arduino Uno (or compatible)
- 6 Servo motors (e.g., SG90)
- External power supply for servos (recommended)
- Jumper wires
- Breadboard (optional)

---

## Circuit Connections

| Servo | Arduino Pin |
|-------|--------------|
| 1     | 2            |
| 2     | 3            |
| 3     | 4            |
| 4     | 5            |
| 5     | 6            |
| 6     | 7            |

Each servo should be connected with 3 wires: signal (to the pin above), VCC (to 5V), and GND.

---

## Walking Algorithm for a Humanoid Robot (6 Servos)

Assumption:
- 2 Servos for legs (hip movement)
- 2 Servos for knees
- 2 Servos for arms (balance or swing)

Algorithm Steps:

1. Initialize robot in standing position (all servos at 90°).
2. Lift left leg by moving left knee servo to 60°, and tilt body slightly right using right arm for balance.
3. Swing left leg forward (left hip servo to ~120°).
4. Place left leg down and return knee to 90°.
5. Shift weight to the left leg.
6. Lift right leg (right knee to 60°), tilt left arm for balance.
7. Swing right leg forward (right hip to ~120°).
8. Place right leg down and return knee to 90°.
9. Repeat steps 2–8 for continuous walking.
