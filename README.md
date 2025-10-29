# Abdelrahman (PanCakeeYT)
### Precision Over Hype

![Header](https://i.imgur.com/zl0vL3l.gif) <!-- clean tech gif, can swap later -->

---

## Overview
Hands-on with embedded firmware, control systems, and real-time audio for small-scale vehicles.  
Single-file, dense, no filler — everything that matters first.

---

## Current Focus
- 1:10 Scale RC Car — custom chassis, drivetrain tuning, and firmware stack  
- Real-time stabilization using MPU6050 on ESP32 (interrupt-driven, low-latency)  
- Multi-ESP architecture: TX / RX / EES (Engine Exhaust Sound) via ESP-NOW  
- ESP32-based engine audio: pitch/load mapping, amp control, and PWM sync  
- Robust failsafe + modular subsystem design for quick debugging  

![RC](https://i.imgur.com/m5kzKjR.gif)

---

## Key Projects
| Repo | Role | State |
|------|------|-------|
| **rc-firmware** | TX/RX/EES firmware – comms, servo, motor, lighting | In Development |
| **ees-audio** | Real-time sound engine (pitch mapping + amp driver) | Prototype |
| **easysetup** | Admin-free installer scripts | Functional |
| **fileflow-client** | Background file sync app | Alpha |
| **localhost-v2** | Local scanning toolkit | Stable |

---

## Tech Stack
**Firmware / Embedded:** ESP32 • Arduino • C++ • FreeRTOS • I2C • SPI • UART • PWM • LEDC  
**Backend / Tools:** Python • Flask • FastAPI • Firebase • REST • WebSocket • GitHub Actions  
**Frontend / UI:** React • HTML • CSS • JS (ES6) • TFT_eSPI (ESP32)  
**Audio / Media:** TDA2030A • PCM / WAV • Real-time pitch shift • Sample streaming  
**Hardware / Tools:** MPU6050 • L298N • Servos • Voltage dividers • Oscilloscope  
**Design / Workflow:** VS Code • Git • Docker (local) • Figma • Illustrator • Photoshop  

---

## Hardware Inventory
- ESP32 (x3): TX / RX / EES  
- MPU6050 (gyro/accel)  
- L298N motor driver (brushed)  
- TDA2030A amplifier + speaker  
- 9–12V packs, dividers, MOSFET switching  
- Joystick, TFT display, push buttons, rotary pots  
- Air humidifier module for exhaust effect  

---

## Architecture Snapshot
```text
[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> motor driver, servos, lights
                               |
                               +--> [EES ESP32] --> amplifier + speaker

[TFT (TX)] --> UI / Control Input
