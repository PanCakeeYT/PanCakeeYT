<p align="center">
  <img src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI5MDAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgOTAwIDEyMCIgcHJlc2VydmVBc3BlY3RSYXRpbz0ibm9uZSI+CiAgPGRlZnM+CiAgICA8bGluZWFyR3JhZGllbnQgaWQ9ImciIHgxPSIwIiB4Mj0iMSI+CiAgICAgIDxzdG9wIG9mZnNldD0iMCIgc3RvcC1jb2xvcj0iIzAwZmZkMSIgc3RvcC1vcGFjaXR5PSIwLjk1Ii8+CiAgICAgIDxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iIzAwYjNmZiIgc3RvcC1vcGFjaXR5PSIwLjk1Ii8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogIDwvZGVmcz4KICA8cmVjdCB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiBmaWxsPSJub25lIi8+CiAgPHBhdGggaWQ9InAiIGQ9Ik0wIDYwIEMxNTAgMTAgMzAwIDExMCA0NTAgNjAgQzYwMCAxMCA3NTAgMTEwIDkwMCA2MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ1cmwoI2cpIiBzdHJva2Utd2lkdGg9IjQiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgogIDxjaXJjbGUgcj0iNSIgZmlsbD0iIzAwZmZkMSI+CiAgICA8YW5pbWF0ZU1vdGlvbiBkdXI9IjNzIiByZXBlYXRDb3VudD0iaW5kZWZpbml0ZSI+CiAgICAgIDxtcGF0aCB4bGluazpocmVmPSIjcCIvPgogICAgPC9hbmltYXRlTW90aW9uPgogIDwvY2lyY2xlPgogIDxnIG9wYWNpdHk9IjAuMTgiPgogICAgPHVzZSByZWY9IiBwIiBzdHJva2U9IiMwMGZmZDEiIHN0cm9rZS13aWR0aD0iOCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CiAgPC9nPgo8L3N2Zz4=" alt="waveform" width="900" style="max-width:100%; display:block; margin: 0 auto 10px auto;" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&size=22&duration=4000&pause=700&color=00FFD1&center=true&vCenter=true&width=900&lines=Embedded+Firmware+Engineer+%7C+ESP32+%7C+Real-Time+Control;1:10+RC+Platform+%7C+MPU6050+Stabilization+%7C+ESP-NOW;EES+Engine+Audio+%7C+Pitch+%26+Load+Mapping+%7C+TDA2030A;OTA-Ready+Modular+Firmware+%7C+Low-Latency+%7C+No+Fluff" alt="typing" />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=PanCakeeYT&label=Profile+Views&color=00ffd1&style=flat-square" alt="profile views" />
</p>

---

# Abdelrahman (PanCakeeYT)
## Precision Over Hype

**Overview**  
Firmware-first engineer focused on embedded control systems, low-latency signal processing, and real-time audio for small-scale vehicles. Predictable behavior, modular subsystems, hardware-aware software: tight loops, hardware timers, prioritized I/O, and noise-hardened power design.

---

## Current Focus
- 1:10 RC Platform — custom chassis, drivetrain tuning, and firmware stack  
- MPU6050 stabilization on ESP32 (ISR-driven, target <5ms reaction)  
- Multi-ESP architecture: TX / RX / EES via ESP-NOW  
- EES (Engine Exhaust Sound): pitch/load mapping, sample streaming, TDA2030A amp sync  
- Modular firmware with OTA, telemetry (serial + WebSocket), and robust failsafes

---

## Key Projects
| Repo | Focus | Status |
|---|---:|:---|
| **rc-firmware** | TX / RX / EES — comms, servo/motor control, lighting, failsafe | In development |
| **ees-audio** | Dedicated EES node — real-time pitch/load mapping, PWM sync to amp | Prototype |
| **rc-ui** | TFT_eSPI UI — drive info, input debug, steering angle graphic, voltage readout | Design |

---

## Tech Stack
**Firmware / Embedded:** ESP32 · Arduino · C++ · FreeRTOS · I2C (400kHz+) · SPI · UART · PWM (LEDC)  
**Backend / Tools:** Python · Flask · FastAPI · WebSocket · GitHub Actions  
**UI / Display:** React · HTML · CSS · JS (ES6) · TFT_eSPI  
**Audio:** PCM/WAV playback · real-time pitch shift · TDA2030A amp control

<p align="center">
  <img src="https://skillicons.dev/icons?i=arduino,cpp,py,react,git,vscode&theme=dark" alt="stack" />
</p>

---

## Hardware Inventory (core)
- ESP32 ×3 — TX, RX, EES  
- MPU6050 (gyro + accel)  
- L298N motor driver (brushed)  
- TDA2030A amplifier + speaker  
- Joystick, TFT display, push buttons, rotary pots  
- 9–12V battery packs, voltage dividers, MOSFET switching  
- Servos (steering + spoiler)  
- Air humidifier module for visual exhaust effect

---

## Architecture
```text
[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> L298N, servos, lights
                                  |
                                  +--> [EES ESP32] --> TDA2030A amp + speaker

[TFT (TX)] -> UI/Control -> Joystick / Pots / Buttons
Features & Goals
Dual-stage lighting logic (press1 → stage1, press2 → stage2+1, press3 → off)

Gyro-based steering correction with target <5ms latency

Engine sound mapped to RPM + throttle with gear-shift emulation

OTA-ready modular firmware with subsystem separation

Failsafe reconnection, battery voltage monitoring, serial + WebSocket telemetry

High-speed I2C (400kHz+), hardware timers for stable PID & control loops

Dev Rules & Notes
Hardware timers for control loops; avoid delay() and blocking calls.

Keep I2C transactions short; use DMP to reduce MPU6050 jitter where helpful.

Use ledcWrite() for precise PWM on ESP32 under load.

Always separate power domains: motors vs logic vs audio.

Debug jitter by checking wiring, grounding, and decoupling caps before changing algorithms.

Build & Flash
bash
Copy code
make rx-build && esptool.py --port /dev/ttyUSB0 write_flash 0x10000 build/rx.bin

python -m serial.tools.miniterm COM4 115200

cd dashboard && python -m flask run --host=0.0.0.0
Live Stats
<p align="center"> <img src="https://github-readme-stats.vercel.app/api?username=PanCakeeYT&show_icons=true&theme=tokyonight" alt="github stats" height="160" /> <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=PanCakeeYT&layout=compact&theme=tokyonight" alt="top languages" height="160" /> </p>
Public Handle
<p align="center"> <a href="https://github.com/PanCakeeYT">github.com/PanCakeeYT</a> </p> ```





