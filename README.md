# Abdelrahman (PanCakeeYT)

> Precision over hype

---

## Overview
Hands-on with embedded firmware, control systems, and real-time audio for small-scale vehicles. Single-file, dense, no fluff — everything important first.

---

## Current Focus
- 1:10 Scale RC Car — custom chassis, drivetrain tuning, and firmware stack  
- Real-time stabilization using MPU6050 on ESP32 (interrupt-driven, low-latency)  
- Multi-ESP architecture: TX / RX / EES (Engine Exhaust Sound) via ESP-NOW  
- ESP32-based engine audio: pitch / load mapping, amp control, and PWM sync  
- Robust failsafe and modular subsystem design for easy debugging  

---

## Key Projects
- **RC Car Firmware** — TX/RX comms, servo/motor control, lighting, failsafe  
- **EES (Engine Sound System)** — real-time sound mapping + amp driver (TDA2030A)  
- *rest are private*

---

## Tech Stack
**Firmware / Embedded:** ESP32 • Arduino • C++ • FreeRTOS • I2C • SPI • UART • PWM • LEDC  
**Backend / Tools:** Python • Flask • FastAPI • Firebase • REST • WebSocket • GitHub Actions  
**Frontend / UI:** React • HTML • CSS • JS (ES6) • TFT_eSPI (ESP32)  
**Audio / Media:** TDA2030A • PCM / WAV playback • real-time pitch shift • sample streaming  
**Hardware / Tools:** MPU6050 • L298N • Servos • Voltmeter dividers • Oscilloscope (when needed)  
**Design / Workflow:** VS Code • Git • Docker (local testing) • Figma • Illustrator • Photoshop  

---

## Hardware Inventory
- ESP32 (x3) — TX, RX, EES  
- MPU6050 (gyro/accel)  
- L298N motor driver (brushed)  
- TDA2030A amplifier + speaker  
- 9–12V battery packs, voltage dividers, MOSFET switching  
- Joystick, TFT display, push buttons, rotary pots  
- Air humidifier module for visual exhaust effect  

---

## Architecture Snapshot
[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> hardware: motor driver, servos, lights

`--> [EES ESP32] --> amplifier + speaker
TFT (TX) -- UI/Control Joystick -> TX

yaml
Copy code

---

## Features & Capabilities
- Dual-stage lighting with staged button logic (press1 → stage1, press2 → stage2+stage1, press3 → off)  
- Gyro-based steering correction with sub-5ms response target  
- Engine sound mapped to RPM + throttle, with gear-shift emulation  
- Modular firmware: OTA-friendly, subsystem separation, clear IPC channels  
- Connection failsafe, battery voltage monitoring, logging via serial + WebSocket  
- High-speed I2C (400kHz+) and prioritized hardware timers for control loops  

---

## Workflow & Dev Notes
- Use hardware timers for control loops; avoid blocking `delay()` in main loops  
- I2C: keep transactions small, use DMP when possible for MPU6050 to reduce jitter  
- Use `ledcWrite()` for servo-like PWM on ESP32 for stable timing under load  
- Separate power domains for motors and logic — noise kills sensors and ADC readings  
- If you see jitter: check wiring, ground plane, and decoupling caps first — then code  

---

## Active Repo Status
| Repo | Role | State |
|:----|:----:|:----:|
| rc-firmware | TX/RX/EES firmware | In development |
| ees-audio | Sound engine + samples | Prototype |
| easysetup | Admin-free installer scripts | Functional |
| fileflow-client | Background file sync | Alpha |
| localhost-v2 | Local scanner & tools | Stable |

---
# build & flash RX firmware
make rx-build && esptool.py --port /dev/ttyUSB0 write_flash 0x10000 build/rx.bin

# tail serial (windows)
python -m serial.tools.miniterm COM4 115200

# run local telemetry dashboard (dev)
cd dashboard && python -m flask run --host=0.0.0.0
Metrics


Contact
Name: Abdelrahman
GitHub: github.com/PanCakeeYT
Email: diamondmachine2022@gmail.com

Philosophy
Modular systems. Predictable behavior.
If its fragile, iterate until its solid
No hype, just reliable builds
