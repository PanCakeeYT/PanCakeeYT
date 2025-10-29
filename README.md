<h1 align="center">Abdelrahman (PanCakeeYT)</h1>
<h3 align="center">Precision Over Hype</h3>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=700&size=20&duration=3500&pause=600&color=00FFD1&center=true&vCenter=true&width=600&lines=Embedded+Engineer+%7C+ESP32+Firmware+%26+Control+Systems;Real-Time+Audio+Processing+%7C+Microcontrollers;Multi-ESP+Architecture+%7C+Low-Latency+Design;No+Fluff.+Just+Reliable+Builds.">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/abhisheknaiidu/abhisheknaiidu/master/code.gif" width="450">
</p>

---

## Overview
Hands-on with **embedded firmware**, **control systems**, and **real-time audio** for small-scale vehicles.  
Every file is written for clarity, speed, and reliability — no boilerplate, no noise.

---

## Current Focus
- 1:10 **Custom RC Car Platform** — full firmware stack + drivetrain tuning  
- **MPU6050 stabilization** using interrupts (<5ms latency target)  
- **Multi-ESP32** setup via ESP-NOW (TX / RX / EES architecture)  
- **Engine Sound System (EES)** — pitch/load mapped audio w/ TDA2030A amp  
- Modular firmware w/ failsafe layers and OTA-ready subsystems  

---

## Key Projects
| Project | Description | State |
|----------|--------------|--------|
| **rc-firmware** | TX/RX/EES firmware – comms, servo, motor, lighting | 🔧 In Dev |
| **ees-audio** | Real-time engine sound simulation (PWM sync) | 🧪 Prototype |
| **easysetup** | Admin-free installer + auto-start system | ✅ Functional |
| **fileflow-client** | Local background file sync | ⚙️ Alpha |
| **localhost-v2** | File scanner + dev utilities | 🧩 Stable |

---

## Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=c,cpp,py,arduino,raspberrypi,react,html,css,js,docker,git,vscode,figma&theme=dark" />
</p>

**Firmware / Embedded:** ESP32 • Arduino • FreeRTOS • I2C • SPI • UART • PWM • LEDC  
**Backend / Tools:** Python • Flask • FastAPI • Firebase • REST • WebSocket  
**Frontend / UI:** React • HTML • CSS • JS (ES6) • TFT_eSPI (ESP32)  
**Audio / Media:** TDA2030A • PCM/WAV • Real-Time Pitch Shift • Sample Streaming  
**Hardware:** MPU6050 • L298N • Servos • Voltage Dividers • MOSFET Switching  

---

## Hardware Inventory
- 3× ESP32 — TX, RX, and EES nodes  
- MPU6050 (gyro/accel)  
- L298N motor driver (brushed)  
- TDA2030A amplifier + speaker  
- 9–12V packs, voltage dividers, MOSFET switching  
- Joystick, TFT display, push buttons, rotary pots  
- Air humidifier module for exhaust simulation  

---

## System Architecture
```yaml
[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> motor driver, servos, lights
                                |
                                +--> [EES ESP32] --> amplifier + speaker

[TFT (TX)] -> UI/Control Interface -> Joystick Inputs
<p align="center"> <img src="https://raw.githubusercontent.com/rajput2107/rajput2107/master/Assets/PC.gif" width="500"> </p><h1 align="center">Abdelrahman (PanCakeeYT)</h1>
<h3 align="center">Precision Over Hype</h3>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=700&size=20&duration=3500&pause=600&color=00FFD1&center=true&vCenter=true&width=600&lines=Embedded+Engineer+%7C+ESP32+Firmware+%26+Control+Systems;Real-Time+Audio+Processing+%7C+Microcontrollers;Multi-ESP+Architecture+%7C+Low-Latency+Design;No+Fluff.+Just+Reliable+Builds.">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/abhisheknaiidu/abhisheknaiidu/master/code.gif" width="450">
</p>

---

## Overview
Hands-on with **embedded firmware**, **control systems**, and **real-time audio** for small-scale vehicles.  
Every file is written for clarity, speed, and reliability — no boilerplate, no noise.

---

## Current Focus
- 1:10 **Custom RC Car Platform** — full firmware stack + drivetrain tuning  
- **MPU6050 stabilization** using interrupts (<5ms latency target)  
- **Multi-ESP32** setup via ESP-NOW (TX / RX / EES architecture)  
- **Engine Sound System (EES)** — pitch/load mapped audio w/ TDA2030A amp  
- Modular firmware w/ failsafe layers and OTA-ready subsystems  

---

## Key Projects
| Project | Description | State |
|----------|--------------|--------|
| **rc-firmware** | TX/RX/EES firmware – comms, servo, motor, lighting | 🔧 In Dev |
| **ees-audio** | Real-time engine sound simulation (PWM sync) | 🧪 Prototype |
| **easysetup** | Admin-free installer + auto-start system | ✅ Functional |
| **fileflow-client** | Local background file sync | ⚙️ Alpha |
| **localhost-v2** | File scanner + dev utilities | 🧩 Stable |

---

## Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=c,cpp,py,arduino,raspberrypi,react,html,css,js,docker,git,vscode,figma&theme=dark" />
</p>

**Firmware / Embedded:** ESP32 • Arduino • FreeRTOS • I2C • SPI • UART • PWM • LEDC  
**Backend / Tools:** Python • Flask • FastAPI • Firebase • REST • WebSocket  
**Frontend / UI:** React • HTML • CSS • JS (ES6) • TFT_eSPI (ESP32)  
**Audio / Media:** TDA2030A • PCM/WAV • Real-Time Pitch Shift • Sample Streaming  
**Hardware:** MPU6050 • L298N • Servos • Voltage Dividers • MOSFET Switching  

---

## Hardware Inventory
- 3× ESP32 — TX, RX, and EES nodes  
- MPU6050 (gyro/accel)  
- L298N motor driver (brushed)  
- TDA2030A amplifier + speaker  
- 9–12V packs, voltage dividers, MOSFET switching  
- Joystick, TFT display, push buttons, rotary pots  
- Air humidifier module for exhaust simulation  

---

## System Architecture
```yaml
[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> motor driver, servos, lights
                                |
                                +--> [EES ESP32] --> amplifier + speaker

[TFT (TX)] -> UI/Control Interface -> Joystick Inputs
<p align="center"> <img src="https://raw.githubusercontent.com/rajput2107/rajput2107/master/Assets/PC.gif" width="500"> </p>
