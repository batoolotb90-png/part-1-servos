# Part 1 – Four Servo Motor Sweep

## Overview
Controls 4 servo motors simultaneously. They sweep from 0° to 180° and back
for exactly 2 seconds, then stop and hold at 90°.

## Components
| Component | Quantity |
|---|---|
| Arduino Uno | 1 |
| Servo Motor (SG90) | 4 |
| Breadboard | 1 |
| Jumper Wires | ~20 |

## Wiring
| Servo | Signal → Arduino Pin | Power | Ground |
|---|---|---|---|
| Servo 1 | Pin 3 | 5V | GND |
| Servo 2 | Pin 5 | 5V | GND |
| Servo 3 | Pin 6 | 5V | GND |
| Servo 4 | Pin 9 | 5V | GND |

## Key Code Concepts
- `#include <Servo.h>` — loads the servo library
- `servo.attach(pin)` — links servo object to a physical pin
- `servo.write(angle)` — moves servo to specified angle (0–180)
- `millis()` — reads elapsed time in milliseconds for accurate 2-second sweep

## How to Run
1. Open `Part1_4_Servos.ino` in Arduino IDE or Tinkercad.
2. Upload to Arduino Uno (or run simulation in Tinkercad).
3. All 4 servos sweep for 2 seconds, then hold at 90°.

## Expected Behavior
- 0–2 seconds: all servos sweep back and forth between 0° and 180°
- After 2 seconds: all servos stop and hold at 90°
- Behavior does not repeat unless Arduino is reset